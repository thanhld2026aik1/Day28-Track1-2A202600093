---
title: 00 — Context (bối cảnh nhóm + track)
section: Day 28 — điền 1 lần đầu buổi, dùng lại cho mọi lần hỏi AI
format: Nhóm 3
time: Điền ~5 phút đầu buổi
---

# 00-context.md — Context nhóm + track

Điền file này một lần ở đầu buổi. Mỗi lần dùng AI ở các bước sau, paste nguyên nội dung file này vào đầu cuộc trò chuyện. AI không tự nhớ context giữa các lần — context khác nhau thì câu trả lời cũng lệch.

---

## 1. Bối cảnh AI20k (đọc, không sửa)

Khóa **AI Thực Chiến** có ~500 học viên (sinh viên năm cuối + người đi làm), đang chuẩn bị cho giai đoạn 6 tuần thực chiến sau Day 28. Lab này do track Product (~80 học viên, nhóm 3) làm. Hoạt động cả khóa nằm trên Discord, LMS, lớp live, lab, nộp bài, coaching — ở quy mô ~500 người.

Lãnh đạo chương trình muốn xây **AI20k Learning OS** — một hệ công cụ AI hỗ trợ học và vận hành khóa. Chính quy mô ~500 người là lý do **không build hết cùng lúc** được: mỗi nhóm nhận 1 track (1 công cụ lớn), tách nhỏ, chọn Quick Win, viết AI Pilot Plan để xin pilot.

Việc của nhóm hôm nay đúng là việc một PM/PO AI làm ngoài doanh nghiệp thật: stakeholder giao một "công cụ AI" quá lớn — bạn phải tách nhỏ, chọn đúng phần làm trước, và bảo vệ lựa chọn bằng lập luận chứ không bằng slide đẹp.

---

## 2. Track của nhóm (điền sau khi nhận track card)

- **Track số / tên**: Track 1 — Lộ trình học cá nhân hóa / Personalized Learning Path
- **Big Ask — chép nguyên văn câu yêu cầu trong track card**:

```text
Hệ thống cá nhân hóa lộ trình học cho từng học viên dựa trên mục tiêu, level, tiến độ, điểm yếu, hành vi học.
```

- **Công cụ lớn này phục vụ ai** (học viên / coach / instructor / admin): Học viên, coach.

Trong phạm vi Day 28, nhóm ưu tiên hai nhóm người dùng này vì:

- Học viên là người trực tiếp cần biết mình đang yếu ở đâu và nên học lại nội dung nào.
- Coach là người cần kiểm tra, hỗ trợ và xác nhận chất lượng khuyến nghị của AI trước khi gửi cho học viên.

- **2 Red Flag đáng lo nhất (chép từ track card)**:

1. **Cá nhân hóa giả**: AI có thể chỉ đổi tên học viên nhưng nội dung khuyến nghị gần như giống nhau giữa các học viên. Điều này làm hệ thống trông có vẻ "personalized", nhưng thực chất không dựa trên dữ liệu học tập, điểm yếu, mục tiêu hoặc tiến độ thật của từng học viên.
2. **Không đo được học viên có tốt lên không**: Hệ thống có thể tạo ra lộ trình học cá nhân hóa, nhưng không có cách đo rõ ràng rằng học viên có thật sự tiến bộ sau khi nhận lộ trình đó hay không. Nếu không có metric trước và sau, team sẽ không biết AI đang tạo giá trị thật hay chỉ tạo thêm một lớp khuyến nghị nghe có vẻ thông minh.

---

## 3. Ràng buộc mọi track phải tôn trọng (đọc, không sửa)

- **Privacy** — data học viên/submission/Discord nhạy cảm; trong lab dùng data mẫu/giả định, nói rõ dùng cái gì.
- **Human review** — output rủi ro cao phải có người review, AI không tự quyết việc quan trọng.
- **Citation** — trả lời dựa trên tài liệu khóa thì phải có nguồn; thiếu nguồn thì nói "không biết", không bịa.
- **Budget nhỏ** — ưu tiên tool/API có sẵn, prototype nhanh, không xây platform lớn.
- **Formative ≠ summative** — feedback/chấm bằng AI là formative, chưa phải điểm chính thức nếu chưa có người calibrate.
- **Adoption** — tool không ai dùng = $0 dù accuracy 99%.
- **Pilot đủ nhỏ** — chạy được trong bối cảnh khóa hiện tại.

---

## 4. Ghi chú thêm (tùy nhóm)

Nhóm chọn hướng ưu tiên là tạo Quick Win cho học viên sau Day 28:

> AI phân tích bài nộp, rubric và self-assessment để chỉ ra 3 điểm yếu chính, sau đó gợi ý tài liệu hoặc bước học lại trước giai đoạn 6 tuần thực chiến.

### Data giả định dùng trong pilot

- Bài nộp Day 28 của học viên
- Rubric Day 28
- Self-assessment ngắn của học viên
- Tài liệu khóa học / slide / LMS liên quan

### Output mong muốn

- 3 skill gap quan trọng nhất
- Lý do vì sao mỗi điểm được xem là gap
- 3 tài liệu hoặc phần học cần xem lại
- 1 checklist học bù ngắn trong 3-5 ngày
- Coach có quyền review trước khi gửi cho học viên

### Phạm vi ưu tiên trong Day 28

Trong Day 28, nhóm không xây toàn bộ hệ thống Personalized Learning Path hoàn chỉnh. Nhóm chỉ tập trung vào một lát cắt nhỏ có thể pilot nhanh:

> Sau khi học viên hoàn thành bài Day 28, AI tạo một bản lộ trình học bù cá nhân hóa dựa trên bài nộp, rubric và self-assessment, sau đó coach review trước khi gửi cho học viên.

### Những việc chưa làm trong phạm vi pilot

Các phần sau **không nằm trong phạm vi Day 28 pilot**:

- Không xây full adaptive learning engine.
- Không xây dashboard toàn khóa cho instructor.
- Không tự động chấm điểm chính thức.
- Không dùng dữ liệu nhạy cảm nếu chưa có consent.
- Không cá nhân hóa toàn bộ 6 tuần thực chiến ngay từ bản pilot đầu tiên.
- Không để AI gửi khuyến nghị trực tiếp cho học viên mà chưa qua coach review.

### Định hướng cho các bước tiếp theo

File này sẽ được dùng làm context đầu vào cho các bước sau:

1. `01-frame/1-intake-breakdown.md`: Tách Big Ask thành các use case nhỏ.
2. `01-frame/2-quick-win.md`: Chọn Quick Win đầu tiên có impact, khả thi và đo được.
3. `01-frame/3-FINAL-problem-framing.md`: Chốt vấn đề, workflow, pain evidence, constraint và validation.
4. `02-solution/2-FINAL-solution.md`: Chọn hướng triển khai Build / Buy / Boost / Partner.
5. `03-pilot-plan/1-pilot-plan.md`: Thiết kế pilot plan có metric, budget, timeline, người tham gia và điều kiện dừng.
6. `03-pilot-plan/2-FINAL-pitch.md`: Đóng gói thành 5-slide pitch để xin phê duyệt pilot.

---

## Cách dùng

```text
1. Đầu buổi: điền mục 2 (+ mục 4 nếu cần). Mục 1 và 3 chỉ để đọc.
2. Mỗi lần mở AI ở một bước: paste nguyên file này vào đầu chat trước.
3. Chọn prompt trong ../prompts/ hợp bước đang làm, chỉnh lại theo track.
4. Đọc kỹ bản nháp AI ra → sửa cho đúng context nhóm → lưu vào đúng file worksheet/.
```

Chỗ `[...]` là chỗ cần điền; điền xong xóa ngoặc nếu muốn.
