---
artifact: 1 — Track & Big Ask + 2 — Tool Breakdown
bai-tap: Frame — nghe đúng đề rồi tách nhỏ
phase: Double Diamond vòng 1 · ◇ giãn (nghe rộng, chưa chốt)
time: ~12 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 00-context.md · track card · prompts/01-breakdown.md
nop-cuoi: Không — file trung gian (bản chốt phase này ở 3-FINAL-problem-framing.md)
---

# 1 — Intake & Breakdown: nghe đúng đề, tách nhỏ

Mục tiêu: cả nhóm hiểu giống nhau "công cụ lớn stakeholder muốn", rồi tách nó thành 5–8 use case nhỏ làm được riêng. Đây là nửa "giãn ra" của [Double Diamond](https://www.thefountaininstitute.com/blog/what-is-the-double-diamond-design-process) vòng 1 — nghe rộng, tách rộng, chưa chọn.

Lý do làm bước này: hai cái bẫy chết người ở đây. Một, nhận đề literal ("làm con chatbot") rồi nhảy vào build — trong khi yêu cầu mơ hồ thường chỉ là triệu chứng. Hai, ôm cả công cụ lớn đi pitch "build cả platform" → trượt Gate 1 ngay. Tách nhỏ là động tác bắt buộc để từ "một ý tưởng to" sang "danh sách phần làm được".

Quy tắc: **nghe trước, tách trước, chưa chọn.** Bước này không được chốt Quick Win (việc đó ở file `2`).

## Bước 0 — Đọc track card + 00-context (2 phút)

Đọc track card được giao và `00-context.md` (mục 2 đã điền). Đừng lướt.

## Quy trình 12 phút

```text
2 phút  — Bước 0: đọc track card + context
4 phút  — Phần A: phát biểu lại Big Ask bằng lời nhóm
6 phút  — Phần B: tách 5–8 use case + check độc lập
```

---

## Phần A — Phát biểu lại Big Ask bằng lời nhóm

Đừng chép lại đề. Cả nhóm nói lại "công cụ lớn stakeholder muốn" bằng lời mình. Nếu 3 người nói 3 kiểu khác nhau → chưa hiểu giống nhau, bàn thêm.

Câu hỏi phụ (tự trả lời):

- Stakeholder nói họ muốn gì, và họ thực sự *cần* gì — có khác nhau không?
- "Tại sao bây giờ?" — ở quy mô ~500 người, cái gì đang đau khiến phải làm công cụ này lúc này?
- Ai là người dùng đầu tiên thật sự, không phải "cả khóa"?

### Trả lời

- **Big Ask, viết lại bằng lời nhóm (2–3 câu)**: Stakeholder muốn một hệ thống giúp mỗi học viên biết rõ mình đang yếu ở đâu, nên học lại phần nào, và nên đi tiếp như thế nào thay vì nhận cùng một lộ trình giống nhau. Với Track 1, nhóm hiểu đây không phải là xây ngay toàn bộ "adaptive learning platform", mà là tìm một lát cắt nhỏ để tạo khuyến nghị học tập cá nhân hóa dựa trên dữ liệu học thật như bài nộp, rubric và self-assessment. Output của AI cần được coach review trước khi gửi cho học viên.
- **Tại sao bây giờ**: Khóa AI20k có quy mô khoảng 500 học viên và sắp bước vào giai đoạn 6 tuần thực chiến, trong khi background, mục tiêu và điểm yếu của học viên rất khác nhau. Nếu mọi người nhận cùng một lộ trình chung, học viên yếu ở các concept quan trọng như Problem Framing, Build/Buy/Boost hoặc Pilot Plan có thể không biết mình cần học bù gì trước khi vào thực chiến.
- **Người dùng đầu tiên cụ thể**: Học viên vừa hoàn thành bài Day 28 và cần biết 3 điểm yếu quan trọng nhất trước giai đoạn 6 tuần thực chiến; coach là người review và xác nhận khuyến nghị trước khi gửi.

## Phần B — Tách công cụ lớn thành 5–8 use case

Nhìn mục **Big Vision Modules** trong track card. Mỗi dòng = 1 use case làm được riêng, viết dạng *"AI làm X cho ai để họ Y"* — không phải tính năng mơ hồ. Cần 5–8 dòng (ít hơn 5 = chưa tách đủ; nhiều hơn 8 = đang liệt kê vụn).

| # | Use case (AI làm gì · cho ai · để họ làm được gì) | Người dùng | Làm được độc lập? |
|---|---|---|---|
| 1 | AI phân tích bài nộp Day 28 + rubric + self-assessment cho học viên để chỉ ra 3 skill gap quan trọng nhất trước 6 tuần thực chiến. | Học viên, coach | Có |
| 2 | AI gợi ý 3 tài liệu/phần LMS cần xem lại cho từng học viên dựa trên skill gap đã phát hiện để học viên biết học bù ở đâu. | Học viên | Có |
| 3 | AI tạo checklist học bù 3-5 ngày cho học viên sau Day 28 để họ có kế hoạch sửa điểm yếu cụ thể. | Học viên | Có |
| 4 | AI tạo bản tóm tắt cho coach về học viên nào cần can thiệp trước dựa trên bài nộp và self-assessment để coach ưu tiên hỗ trợ. | Coach | Có |
| 5 | AI sinh câu hỏi phản tư ngắn cho học viên sau khi nhận feedback để họ tự xác nhận có hiểu đúng điểm yếu của mình không. | Học viên | Có |
| 6 | AI so sánh self-assessment của học viên với evidence trong bài nộp để phát hiện lệch nhận thức như "tự tin cao nhưng bài làm thiếu baseline". | Học viên, coach | Có |
| 7 | AI gợi ý nhóm peer hỗ trợ theo skill gap tương đồng/bổ sung để học viên có người trao đổi trong giai đoạn thực chiến. | Học viên, coach | Có, nhưng cần dữ liệu nhiều học viên |
| 8 | AI theo dõi trước-sau bằng mini quiz hoặc bài sửa lại để kiểm tra học viên có cải thiện sau lộ trình học bù không. | Học viên, coach | Có, nhưng cần thêm bước đo sau |

Cần ít nhất **4 use case thật sự độc lập** (làm được mà không cần cái khác xong trước). Nếu nhiều cái phụ thuộc nhau → gộp hoặc viết lại cho tách bạch.

---

## Phát hiện ban đầu

- Công cụ lớn có nhiều hướng hấp dẫn, nhưng lát cắt phù hợp nhất với Day 28 nên bắt đầu từ dữ liệu đã có ngay: bài nộp, rubric, self-assessment và tài liệu khóa học.
- Hai rủi ro phải chặn từ đầu là cá nhân hóa giả và không đo được tiến bộ. Vì vậy use case nào được chọn cần có evidence từ bài nộp/rubric và có cách đo trước-sau.
- Coach review là bắt buộc vì output có thể ảnh hưởng đến cách học viên nhìn nhận năng lực của mình; AI không nên gửi khuyến nghị trực tiếp.

## Câu hỏi mở (mang sang bước chọn Quick Win)

- Nên chọn Quick Win tập trung vào "phát hiện skill gap" hay "tạo checklist học bù" trước?
- Baseline để đo tiến bộ nên là điểm rubric Day 28, self-assessment trước-sau, mini quiz, hay bài sửa lại?
- Mỗi coach có thể dành bao nhiêu thời gian để review output AI cho một học viên/nhóm?
- Trong pilot, nên thử với bao nhiêu học viên hoặc bao nhiêu nhóm để đủ nhỏ nhưng vẫn có evidence?

---

## Tổng kiểm tra trước khi sang `2-quick-win.md`

| Hạng mục | Xong? |
|---|---|
| Cả nhóm phát biểu lại Big Ask giống nhau, không cần nhìn card | x |
| Có 5–8 use case dạng "AI làm X cho ai để Y" | x |
| Có ≥4 use case thật sự độc lập | x |
| Nhóm KHÔNG còn ý định pitch "build cả platform" | x |

Sau bước này, mở `2-quick-win.md` — chấm điểm chọn 1 lát cắt làm trước.

*Liên quan: handbook §A1+§A2 · `prompts/01-breakdown.md` · `00-context.md`*
