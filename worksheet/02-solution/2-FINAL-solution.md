---
artifact: 5 — Solution Approach + 6 — Demo/Mockup/Flow (bản nộp phase Solution)
bai-tap: Solution — chốt cách làm + cho stakeholder nhìn thấy
phase: Double Diamond vòng 2 · ◆ siết (chốt 1 cách làm + 1 artifact trực quan)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-find-existing-solutions.md · 00-context.md · templates/demo-examples.md · prompts/05-demo-challenge.md
nop-cuoi: Có — bản nộp của phase Solution (Part B + C · A3 mục Solution Approach + Demo/Mockup/Flow)
---

# 2 — FINAL: Solution Approach + Demo/Mockup/Flow

Mục tiêu: chốt cách làm cho Quick Win (Build / Buy / Boost / Partner), nói rõ data & ai review cần có, và tạo 1 bản vẽ trực quan để stakeholder *nhìn* được. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 và là bản nộp của phase Solution.

Lý do làm bước này: hai cái bẫy. Một, "tự build" cho oai — trong khi 80–90% nhu cầu nội bộ chỉ cần Boost/Buy; tự build là quyết định khó rút lại nhất. Hai, chỉ nói bằng chữ — stakeholder không duyệt một đoạn văn, họ duyệt khi *nhìn thấy* flow. Không có bản vẽ → trượt Gate 4 dù lập luận tốt.

Quy tắc: **bản vẽ trực quan là BẮT BUỘC; demo chạy được chỉ là điểm cộng.** *Demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu.*

## Quy trình 12 phút

```text
4 phút  — Phần A: chốt Build/Buy/Boost/Partner (decision tree + ego check)
3 phút  — Phần B: data & ai review cần có
5 phút  — Phần C: vẽ 1 artifact trực quan + đánh dấu chỗ người review
```

---

## Phần A — Chốt cách làm

Đi decision tree, đừng chọn theo cảm giác:

```text
Bài này có phải LỢI THẾ CẠNH TRANH CỐT LÕI không?
 ├─ CÓ  → đội có AI engineer mạnh? CÓ → Build · KHÔNG → Boost
 └─ KHÔNG (chỉ là productivity layer) → có tool sẵn?
          CÓ → Buy · KHÔNG → Boost (model sẵn + data riêng)
```

Câu hỏi phụ:

- Nhóm chọn cách này vì *cần* hay vì *thích tự build*? Một câu thành thật.
- Hướng nào ở file `1` (đã tìm được người làm rồi) khớp với cách này — "đi từ 5 lên"?

### Trả lời

- **Cách làm chốt**: Boost (dùng LLM API có sẵn + Prompt riêng + form UI đơn giản)
- **Lý do CẦN (không phải thích), 2–3 câu**: Chúng ta chỉ cần một productivity layer giúp Coach nhặt ra các điểm yếu (gap) từ bài nộp dựa trên rubric. Bài toán này không phải lợi thế cạnh tranh cốt lõi để phải tự Build model riêng, và chưa có tool Buy nào đáp ứng được chính xác format rubric của khóa học AI20k.
- **Vì sao KHÔNG "Build từ số 0"**: Nhóm không có AI Engineer mạnh để train model từ đầu. Các model lớn hiện nay (GPT-4o, Claude 3.5 Sonnet) qua API đã quá đủ thông minh để làm nhiệm vụ đọc hiểu và trích xuất (extraction) theo tiêu chí, việc tự train model là lãng phí thời gian và ngân sách.
- **Tool / API / vendor cần + ước lượng chi phí thô** (budget nhỏ, ưu tiên sẵn có): Dùng nền tảng có sẵn (như Dify, Coze) hoặc một web app nhỏ gọi API Claude 3.5 Sonnet / OpenAI. Chi phí token ước tính: ~0.01$ - 0.05$/bài nộp. Tổng cộng chưa tới 5-10$ cho đợt pilot với 80 bài nộp của track Product.

## Phần B — Data & ai review (cách làm này cần gì để chạy được)

| Cần gì | Có sẵn trong AI20k? | Trong lab dùng (mẫu/giả định) | Privacy? |
|---|---|---|---|
| Data: Bài nộp Day 28 của học viên | Có (trên Notion/LMS/Drive) | Dùng 3-5 bài nộp mẫu giả định của các nhóm trước | Cần che tên/thông tin cá nhân nếu lấy bài của nhóm khác |
| Data: Rubric chấm điểm Day 28 | Có | Dùng trực tiếp từ context | Không nhạy cảm |
| Data: Form tự đánh giá (nếu có) | Có (dữ liệu thô trên form) | Dùng mẫu giả định | Cần che tên |

- **Output nào rủi ro cao** (sai gây hậu quả): AI "ảo giác" tự bịa ra điểm yếu không hề có trong bài nộp, hoặc trích xuất sai đoạn văn. Nếu gửi trực tiếp cho học viên, họ sẽ bức xúc và mất niềm tin vào feedback.
- **Ai review + bao nhiêu mẫu + pass/fail theo gì**: Coach là người review. Trong pilot, review 100% output AI tạo ra. Pass/Fail theo tiêu chí: 3 skill gap có đúng trọng tâm Rubric không và phần "Trích dẫn nguyên văn" có chính xác 100% từ bài nộp không.
- **Có cần citation / nói "không biết" khi thiếu nguồn không**: BẮT BUỘC có citation (trích xuất text nguyên văn). Bắt buộc phải có fallback trong prompt: "Nếu bài nộp không có thông tin để đánh giá tiêu chí này, hãy ghi: KHÔNG TÌM THẤY DỮ LIỆU ĐỂ ĐÁNH GIÁ, không được tự suy diễn".

## Phần C — Bản vẽ trực quan (BẮT BUỘC)

Chọn **1** dạng nhẹ nhất đủ rõ (xem `templates/demo-examples.md`): mockup 2–3 màn hình · user flow trước/sau · prompt flow · agent flow · 1 cặp input–output thật. Vẽ tay / ASCII / bảng đều được.

```text
[ GIAO DIỆN CỦA COACH - BẢNG ĐIỀU KHIỂN ]

1. INPUT
[ Upload Bài nộp của học viên (PDF/Notion Link) ]
[ Upload File Rubric Day 28 ]
( Nút: "TẠO DRAFT 3 SKILL GAPS" )
          |
          v
2. AI PROCESSING (Prompt Chaining)
- Phân tích Bài nộp vs Rubric
- Rút ra 3 Gap ưu tiên
- Trích xuất Exact Quote làm bằng chứng (Citation)
          |
          v
3. OUTPUT REVIEW (CHỖ CON NGƯỜI CAN THIỆP - BẮT BUỘC)
+-----------------------------------------------------------+
| Học viên: Nhóm A                                          |
|                                                           |
| ⚠️ Gap 1: Vấn đề thật chưa có số baseline                 |
| 💬 AI Trích dẫn: "Nhiều người phàn nàn về hệ thống..."     |
| [ ] APPROVE (Coach check trích dẫn đúng là chung chung)   |
| [ ] REJECT / EDIT (Coach sửa lại câu chữ cho mềm mỏng)    |
|                                                           |
| ⚠️ Gap 2: Demo chưa thể hiện chỗ con người review         |
| 💬 AI Trích dẫn: (Không có text nào nói về human review)  |
| [ ] APPROVE  [ ] REJECT / EDIT                            |
+-----------------------------------------------------------+
          |
          v
4. SEND FEEDBACK
( Bấm "Gửi" để tự động bắn feedback đã duyệt qua Email/Discord học viên )

Chỗ con người review (output rủi ro cao) nằm ở: Bước 3 (Output Review). Coach phải trực tiếp kiểm tra trích dẫn (citation) và bấm Approve/Edit từng Gap trước khi hệ thống gửi cho học viên.
```

Câu hỏi phụ — một người đóng vai stakeholder nhìn 20 giây: *hiểu user làm gì, nhận lại gì, không cần giải thích thêm không? Có chỗ nào "đẹp nhưng rỗng" không?*

---

## Tổng kiểm tra trước khi sang `../03-pilot-plan/`

| Hạng mục | Xong? |
|---|---|
| Cách làm có lý do CẦN, không phải "mặc định tự build" | x |
| Nói rõ data cần + ai review output rủi ro cao | x |
| Có ≥1 bản vẽ trực quan, người ngoài hiểu trong ~20 giây | x |
| Có đánh dấu chỗ con người review | x |

⚑ Coach kiểm tra ở Mốc 3: *"Stakeholder nhìn vào đâu để hiểu flow? Mockup/sketch/demo đâu?"* Chỉ nói bằng chữ = chưa qua.

Sau bước này, mở `../03-pilot-plan/1-pilot-plan.md`.

*Liên quan: handbook §A5+§A6 · `templates/demo-examples.md` · `prompts/05-demo-challenge.md`*
