---
artifact: 5 — Solution Approach (phần khám phá)
bai-tap: Solution — tìm lời giải đã có sẵn trước khi tự xây
phase: Double Diamond vòng 2 · ◇ giãn (mở hết lựa chọn, chưa chốt)
time: ~8 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 01-frame/3-FINAL-problem-framing.md · 00-context.md · prompts/04-find-solutions.md
nop-cuoi: Không — file trung gian (bản chốt ở 2-FINAL-solution.md)
---

# 1 — Find existing solutions (đừng xây lại từ số 0)

Mục tiêu: trước khi quyết Build / Buy / Boost / Partner, nhóm phải biết bài này đã có ai giải ở chỗ khác chưa, và họ giải bằng cách nào. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 2 — mở hết các lời giải đang tồn tại, chưa chốt cái nào.

Lý do làm bước này: đây là chỗ nhiều nhóm hỏng mà không biết. Hỏng vì nhảy thẳng vào "tự build" cho oai, trong khi 80–90% nhu cầu nội bộ chỉ cần Boost hoặc Buy. Hỏng vì không hỏi "ai làm rồi" nên đi lại từ số 0. Gần như bài nào cũng đã có người giải ở một ngành khác — không thấy thì phí cả pilot.

Quy tắc: **không có nguồn = giả định.** Mỗi cái AI/web nói ra, hỏi lại "lấy ở đâu?". Không chỉ được nguồn thì đánh dấu 🧮 (giả định để giảng), đừng xài như fact.

## Bước 0 — Bài này thực ra là dạng bài gì? (2 phút)

Bỏ context AI20k sang một bên. Mô tả Quick Win của nhóm như một bài toán chung — không có chữ "học viên / coach / Discord". Vài ví dụ cho dễ hình dung:

- "câu hỏi của user → câu trả lời kèm nguồn" → đây là bài Q&A có citation
- "một đống văn bản lộn xộn → data có cấu trúc" → bài extraction
- "bài nộp → nhận xét theo rubric" → bài rubric grading

Dạng bài (the pattern) đó gần như chắc chắn đã có người làm ở ngành khác. Tìm ra dạng bài → tìm ra người đã giải nó.

- **Quick Win của nhóm, viết lại thành 1 dạng bài chung (không có chữ domain)**: Phân tích tài liệu đầu vào từ nhiều nguồn (văn bản không cấu trúc, tiêu chí đánh giá, form tự đánh giá) để trích xuất và tổng hợp ra 3 điểm thiếu hụt (gap) cốt lõi kèm theo dẫn chứng cụ thể.
- **Input → output thực chất là gì**: [Văn bản bài làm + bộ tiêu chí (rubric) + dữ liệu tự đánh giá] → [Danh sách 3 điểm thiếu hụt ưu tiên có cấu trúc kèm trích dẫn nguyên văn (citation)].
- **Ràng buộc không bỏ được (lấy từ `00-context.md`)**: Phải có người review (chuyên gia duyệt trước khi gửi end-user), không dùng dữ liệu nhạy cảm nếu không có consent, bắt buộc có citation (không nguồn = không tin), budget nhỏ cho pilot.

## Quy trình 8 phút

```text
2 phút  — Bước 0: gọi tên dạng bài
4 phút  — Phần A: deep research 4 tầng "ai giải dạng bài này rồi"
2 phút  — Phần B: rút về 2–3 hướng khả thi, đánh dấu nguồn
```

---

## Phần A — Deep research: ai giải dạng bài này rồi, giải sao?

Không phải gõ 1 câu vào AI rồi chép. Chạy 4 tầng, **tầng sau lấy kết quả tầng trước làm input**. Khung câu lệnh ở `prompts/04-find-solutions.md`.

Câu hỏi phụ (tự trả lời — viết ra cái nhóm *tìm thấy*, không phải cái nhóm *đoán*):

- Dạng bài này giống bài nào ở một ngành hoàn toàn khác?
- Hướng nào AI gợi ý mà nhóm **không kiểm được nguồn** — vậy có nên tin không?
- Một ca thất bại của người đi trước dạy nhóm tránh đúng điều gì?
- Nhóm "đi từ mức mấy" — kế thừa được gì để khỏi bắt đầu từ 0?

### Trả lời — điền theo 4 tầng

| Tầng | Hỏi AI/web câu gì | Tìm được gì | Nguồn / 🧮 nếu là giả định |
|---|---|---|---|
| 1 · Map | "Dạng bài trích xuất điểm yếu từ văn bản dựa trên tiêu chí thường giải bằng những hướng nào? 4–6 hướng, mỗi hướng khi nào nên dùng." | 1. Prompt Chaining (LLM đọc rồi tổng hợp qua nhiều prompt). 2. RAG (tìm đoạn liên quan rồi đánh giá). 3. Rule-based extraction (dựa trên form). 4. Multi-Agent Workflow. | 🧮 Giả định kiến thức chung về AI architecture |
| 2 · Tiền lệ | "Đội nào đã làm trích xuất và đánh giá dựa trên tiêu chí ở quy mô tương tự? Họ làm cách nào?" | EdTech (Gradescope, Coursera) dùng LLM Prompting kết hợp Rubric rất chi tiết. Ngành HR dùng hệ thống ATS/AI để match CV của ứng viên với Job Description (JD) tìm ra skill gap. | 🧮 Case study HR CV Matching / EdTech Auto-grader |
| 3 · Phản chứng | "Ca nào làm trích xuất và đánh giá (grading/matching) thất bại? Nguyên nhân gốc là gì?" | Thất bại thường do LLM "ảo giác" (hallucination) tự bịa ra điểm yếu không có trong văn bản, hoặc đánh giá sai do Rubric (tiêu chí) quá mơ hồ, không rõ ràng. | 🧮 Các bài phân tích về LLM hallucination trong automated assessment |
| 4 · Thu hẹp | "Với ràng buộc [budget nhỏ · có người review · cần citation], hướng nào khả thi cho pilot 6 tuần?" | Prompt Chaining + In-context Learning (đưa vài ví dụ mẫu vào prompt). Yêu cầu LLM bắt buộc trích xuất nguyên văn (exact quote) để làm citation. Dùng API có sẵn (OpenAI/Anthropic). | 🧮 Kinh nghiệm triển khai GenAI budget nhỏ |

---

## Phần B — Rút về 2–3 hướng khả thi

Câu hỏi phụ:

- Hướng nào *kế thừa được nhiều nhất* từ người đã làm?
- Hướng nào nghe hay nhưng nhóm **không có nguồn** để tin?

### Trả lời

| Hướng giải khả thi | Ai làm rồi (gần bài mình nhất) | Nguồn / 🧮 | Hợp ràng buộc `00-context`? |
|---|---|---|---|
| 1. Prompt Chaining + LLM API (yêu cầu exact quote citation) | HR Tech (match CV vs JD), EdTech (Rubric grading) | 🧮 HR/EdTech case studies | Có vì chi phí API rẻ, kiểm soát được citation (bắt trích nguyên văn), dễ tạo UI/form cho coach review. |
| 2. RAG (Retrieval-Augmented Generation) | Chatbot nội bộ QA tìm kiếm tài liệu | 🧮 Các dự án RAG nội bộ | Không vì over-engineering. Bài nộp D28 không quá dài, context window của LLM hiện tại (128k+) đủ chứa cả bài nộp + rubric mà không cần setup Vector DB. |
| 3. Multi-Agent Workflow (các Agent đóng vai phản biện nhau) | Hệ thống research phức tạp, AutoGPT | 🧮 AI Agent frameworks | Không vì tốn thời gian setup, khó kiểm soát citation, tốn token/budget hơn mức cần thiết cho một pilot 6 tuần. |

**"Đi từ 5 lên" — nhóm kế thừa cụ thể cái gì** (1–2 câu):

```text
Nhóm kế thừa cách cấu trúc Prompt của các hệ thống HR CV Matching: "Đây là Tiêu chí (Rubric). Đây là Bài nộp (CV). Hãy đối chiếu và tìm ra 3 gap lớn nhất, bắt buộc trích xuất nguyên văn dẫn chứng từ Bài nộp để chứng minh."
```

---

## Phát hiện ban đầu

Ghi nhanh 2–3 cái đáng chú ý nhất (chưa phải quyết định — quyết định ở file FINAL):

- Không cần dùng RAG vì context window của LLM hiện đại đủ rộng để nạp toàn bộ Bài nộp + Rubric vào trong 1 prompt.
- Rủi ro lớn nhất là AI "ảo giác" ra lỗi không có, nên bắt buộc phải thiết kế prompt yêu cầu "trích nguyên văn" (exact quote citation).
- Dạng bài tìm skill gap của học viên cực kỳ giống với bài toán HR tìm skill gap của ứng viên so với Job Description.

## Câu hỏi mở (mang sang bước chốt)

- Làm sao để trình bày kết quả (UI/UX) cho Coach review một cách nhanh nhất (VD: highlight màu những chỗ cần check citation)?
- Nên chọn LLM model nào (GPT-4o, Claude 3.5 Sonnet, Gemini 1.5 Pro) để cân bằng giữa khả năng tuân thủ rubric tốt và chi phí API hợp lý cho pilot?

---

## Tổng kiểm tra trước khi sang `2-FINAL-solution.md`

| Hạng mục | Xong? |
|---|---|
| Gọi được dạng bài trong 1 câu, không còn chữ domain | x |
| Đủ 4 tầng deep research, tầng nào cũng có kết quả | x |
| Mỗi kết quả có nguồn, hoặc đánh dấu 🧮 nếu là giả định | x |
| Rút về 2–3 hướng + nói được "đi từ 5 lên" cái gì | x |

Hàng nào chưa xong → quay lại Phần A, đừng sang bước chốt vội.

Sau bước này, mở `2-FINAL-solution.md` — chốt Build/Buy/Boost/Partner + data & ai review + bản vẽ trực quan (đây là bản nộp của phase này).

*Liên quan: handbook §A5 · `prompts/04-find-solutions.md` · `00-context.md`*
