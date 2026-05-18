---
artifact: 3 — Quick Win Selection
bai-tap: Frame — chọn lát cắt làm trước
phase: Double Diamond vòng 1 · ◆ siết (hội tụ về 1 lựa chọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-intake-breakdown.md · prompts/02-quick-win-challenge.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 2 — Quick Win: chọn lát cắt làm trước

Mục tiêu: từ 5–8 use case ở file `1`, chấm điểm nhanh và chốt **1 Quick Win** để pilot đầu tiên — kèm lý do chọn và lý do *không* chọn các phần khác. Đây là nửa "siết lại" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1.

Lý do làm bước này: đây là quyết định quan trọng nhất của phase Frame. Quick Win **không phải** phần dễ nhất hay nghe hay nhất — là phần *chứng minh được giá trị nhanh và có người ủng hộ*. Chọn sai → pilot fail → mất uy tín → khó xin pilot tiếp. Nhóm phải chọn được *và bảo vệ được bằng lý do*, không bằng cảm tính.

Quy tắc: **điểm số chỉ là gợi ý, không phải đáp án.** Đừng để con số quyết thay nhóm — nó chỉ giúp so sánh.

## Bước 0 — Lấy 4–6 use case mạnh nhất từ file `1` (1 phút)

## Quy trình 10 phút

```text
1 phút  — Bước 0: chọn 4–6 ứng viên
5 phút  — Phần A: chấm điểm 4 trục
3 phút  — Phần B: 1 lý do nên / 1 lý do không cho top 2
1 phút  — Phần C: chốt + ai ủng hộ + cái KHÔNG chọn
```

---

## Phần A — Chấm điểm 4 trục (1–5 mỗi trục)

Câu hỏi phụ (tự trả lời):

- "Risk" ở đây là *sai thì mất gì* — chọn đúng việc chính của user (task centrality) thì sai cũng đỡ đau; chọn việc lớn nhất thì sai rất đắt. Use case nào risk thấp thật?
- Use case nào có sẵn data + có người trong AI20k thật sự muốn dùng?

| Use case | Impact | Feasibility | Evidence nhanh | Risk (cao = an toàn) | Tổng |
|---|:--:|:--:|:--:|:--:|:--:|
| UC1 — Phân tích bài nộp Day 28 + rubric + self-assessment để chỉ ra 3 skill gap quan trọng nhất | 5 | 4 | 5 | 4 | 4.55 |
| UC2 — Gợi ý 3 tài liệu/phần LMS cần xem lại theo skill gap | 4 | 4 | 4 | 4 | 4.00 |
| UC3 — Tạo checklist học bù 3-5 ngày sau Day 28 | 4 | 5 | 4 | 5 | 4.45 |
| UC4 — Tạo bản tóm tắt cho coach về học viên cần can thiệp trước | 4 | 3 | 4 | 4 | 3.75 |
| UC6 — So sánh self-assessment với evidence trong bài nộp để phát hiện lệch nhận thức | 4 | 4 | 4 | 3 | 3.85 |
| UC8 — Theo dõi trước-sau bằng mini quiz hoặc bài sửa lại để kiểm tra cải thiện | 5 | 3 | 3 | 4 | 3.70 |

(Thang điểm chi tiết: `templates/quick-win-scoring.md`.)

## Phần B — 1 lý do nên / 1 lý do không, cho top 2

**Ứng viên A — UC1: Phân tích bài nộp Day 28 + rubric + self-assessment để chỉ ra 3 skill gap quan trọng nhất**

```text
Nên chọn vì: Dữ liệu đầu vào đã có hoặc có thể giả định nhanh trong lab (bài nộp, rubric, self-assessment), pain rõ với học viên trước 6 tuần thực chiến, và evidence có thể kiểm bằng coach review trong 1-2 tuần.
Không nên vì: Nếu rubric hoặc bài nộp không đủ rõ, AI có thể suy diễn gap sai; cần coach review và citation theo rubric để giảm rủi ro.
```

**Ứng viên B — UC3: Tạo checklist học bù 3-5 ngày sau Day 28**

```text
Nên chọn vì: Rất khả thi, dễ tạo output hữu ích cho học viên, rủi ro thấp vì chỉ là kế hoạch học bù ngắn.
Không nên vì: Nếu chưa có bước phát hiện skill gap đáng tin, checklist có thể trở thành khuyến nghị chung chung và rơi vào red flag "cá nhân hóa giả".
```

## Phần C — Chốt Quick Win

- **Quick Win nhóm chọn**: UC1 — AI phân tích bài nộp Day 28 + rubric + self-assessment để chỉ ra 3 skill gap quan trọng nhất của học viên trước giai đoạn 6 tuần thực chiến.
- **Vì sao chọn cái này trước** (2–4 câu, bám điểm + impact + evidence nhanh): UC1 có tổng điểm cao nhất (4.55) vì tác động trực tiếp vào pain chính: học viên không biết mình yếu ở đâu và nên học lại gì trước khi vào thực chiến. Use case này dùng được dữ liệu sẵn có trong Day 28, không cần xây platform lớn, và có thể kiểm chứng nhanh bằng việc coach review xem 3 skill gap AI nêu có khớp với rubric/bài nộp không. UC1 cũng là nền cho các bước sau như gợi ý tài liệu hoặc checklist học bù, nên chọn nó trước sẽ tránh tạo khuyến nghị chung chung.
- **Ai trong AI20k sẽ ủng hộ pilot này** (và vì sao họ care — "có người ủng hộ" thường quan trọng hơn "impact cao"): Học viên sẽ ủng hộ vì nhận được feedback cụ thể về điểm yếu thay vì lời khuyên chung. Coach sẽ ủng hộ vì có bản nháp skill gap để review nhanh hơn và ưu tiên hỗ trợ học viên/nhóm đang yếu trước giai đoạn thực chiến. Instructor/lead coach có lý do quan tâm vì pilot giúp kiểm tra liệu cá nhân hóa có tạo evidence thật hay không trước khi mở rộng.
- **Nhóm KHÔNG chọn gì + vì sao** (≥2 use case bị loại): 1. UC7 — Gợi ý peer hỗ trợ: cần dữ liệu nhiều học viên và logic ghép nhóm, dễ vượt quá phạm vi pilot Day 28.  2. UC8 — Theo dõi trước-sau bằng mini quiz hoặc bài sửa lại: quan trọng nhưng cần thêm vòng đo sau, chưa phải lát cắt nhanh nhất để bắt đầu.  3. UC3 — Tạo checklist học bù 3-5 ngày: hữu ích và rất khả thi, nhưng nên làm sau UC1 vì checklist cần dựa trên skill gap đáng tin.

---

## Phát hiện ban đầu

- UC1 và UC3 là hai ứng viên mạnh nhất. UC3 dễ làm hơn, nhưng UC1 chứng minh đúng giá trị cốt lõi của "personalized learning path": cá nhân hóa phải bắt đầu từ chẩn đoán gap thật.
- Các use case liên quan đến dashboard, peer matching hoặc đo trước-sau đều có giá trị nhưng cần thêm dữ liệu/quy trình, phù hợp làm phase sau hơn là Quick Win đầu tiên.
- Quick Win được chọn phải luôn kèm coach review để tránh biến feedback AI thành kết luận chính thức.

## Câu hỏi mở (mang sang Problem Framing)

- Tiêu chí nào để coach xác nhận 3 skill gap AI đưa ra là "đúng đủ dùng"?
- Baseline hiện tại của học viên là gì: chưa có feedback cá nhân hóa, thời gian coach review lâu, hay tỷ lệ bài nộp thiếu các mục trọng yếu?
- Pilot nên chạy ở mức cá nhân hay mức nhóm 3 người nộp chung bài Day 28?
- Output nên gửi cho học viên dưới dạng feedback ngắn, checklist, hay bảng skill gap có dẫn chứng từ rubric?

---

## Tổng kiểm tra trước khi sang `3-FINAL-problem-framing.md`

| Hạng mục | Xong? |
|---|---|
| Có bảng chấm 4 trục cho ≥4 use case | x |
| Chốt 1 Quick Win, lý do bám số/impact (không "nghe hay") | x |
| Nêu rõ ai ủng hộ pilot này | x |
| Ghi rõ ≥2 phần KHÔNG chọn + lý do | x |

⚑ Đây là phần coach kiểm tra ở Mốc 1: *"Vì sao không làm full tool? Vì sao chọn lát cắt này trước?"*

Sau bước này, mở `3-FINAL-problem-framing.md` — đóng khung vấn đề thật (bản nộp của phase Frame).

*Liên quan: handbook §A3 · `templates/quick-win-scoring.md` · `prompts/02-quick-win-challenge.md`*
