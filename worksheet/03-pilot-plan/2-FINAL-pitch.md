---
artifact: 8 — 5-slide Pitch + AI Support Log (bản nộp cuối lab)
bai-tap: Pilot Plan — dồn thành pitch, sẵn sàng phản biện
phase: Double Diamond vòng 2 · ◆ output (bản nộp cuối + present)
time: ~5 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 1-pilot-plan.md + toàn bộ 01-frame + 02-solution · templates/5-slide-pitch.md
nop-cuoi: Có — bản nộp cuối lab (Part E · 5-slide Pitch + AI Support Log)
---

# 2 — FINAL: 5-slide Pitch + AI Support Log

Mục tiêu: dồn cả A3 Working Canvas thành 5 slide pitch (5 phút), chuẩn bị trả lời 3 câu phản biện, và ghi AI Support Log. Đây là bản nộp cuối cùng của lab.

Lý do làm bước này: nguyên tắc *demo đơn giản + lập luận chặt > demo đẹp + lập luận yếu*. Slide đẹp mà không trả lời được "số này lấy ở đâu" thì hỏng. Pitch không phải kể chuyện — là đưa evidence để stakeholder ra được một quyết định.

Quy tắc: **slide cuối phải là một lời xin rõ ràng** (xin gì · đổi lại hứa gì). Không có lời xin = stakeholder không biết approve cái gì.

## Quy trình 5 phút

```text
3 phút  — Dồn 5 slide (mỗi slide 1 thông điệp)
1 phút  — Chuẩn bị 3 câu phản biện
1 phút  — AI Support Log
```

---

## Phần A — 5 slide (mỗi slide 1 thông điệp)

Kéo nguyên liệu từ các file đã làm, đừng viết mới. Khung đầy đủ: `templates/5-slide-pitch.md`.

| # | Slide | Lấy từ | Nội dung 1–2 gạch đầu dòng | Ai nói |
|---|---|---|---|---|
| 1 | Problem & user | 01-frame/3-FINAL | Học viên Product sau Day 28 chuẩn bị vào 6 tuần thực chiến nhưng chưa biết 3 skill gap ưu tiên của mình. Coach có thể feedback thủ công, nhưng ở quy mô ~80 học viên Product việc cá nhân hóa sâu dễ tốn 13-20 giờ và khó đo hiệu quả. | Lê Đức Thanh |
| 2 | Breakdown & Quick Win | 01-frame/1,2 | Big Ask "Personalized Learning Path" được tách nhỏ, nhóm không làm full adaptive engine. Quick Win chọn UC1: AI phân tích bài nộp Day 28 + rubric + self-assessment để chỉ ra 3 skill gap quan trọng nhất, vì có data sẵn, impact trực tiếp và có thể kiểm chứng nhanh bằng coach review. | Lê Đức Thanh |
| 3 | Solution + bản vẽ trực quan | 02-solution/2-FINAL | Chọn **Boost**: LLM API/tool có sẵn + prompt riêng + rubric + form UI đơn giản, không build model từ số 0. Flow: upload bài nộp/rubric → AI tạo draft 3 skill gap kèm exact quote → coach approve/edit/reject từng gap → chỉ gửi feedback đã duyệt cho học viên. | Chu Minh Quân |
| 4 | AI Pilot Plan | 03-pilot-plan/1 | Pilot 3 tuần với 10-15 học viên hoặc 5 nhóm Product có consent; 2 phase: calibration trên 3-5 bài mẫu, sau đó chạy pilot nhỏ. Data gồm bài nộp Day 28, rubric, self-assessment, tài liệu khóa; budget tối đa 10 USD API + 2-3 giờ/tuần của 1 coach + thời gian nhóm dựng prompt/đo. | Đặng Quang Minh |
| 5 | Metric · exit criteria · **lời xin** | 03-pilot-plan/1 | Đo bằng tỷ lệ skill gap được coach approve/edit nhẹ ≥70%, citation đúng 100%, thời gian coach giảm ≥30%, adoption học viên ≥70%. **Lời xin:** cho phép chạy pilot 3 tuần với 10-15 học viên/5 nhóm, 1 coach review 2-3 giờ/tuần, quyền dùng dữ liệu đã ẩn danh và ngân sách API tối đa 10 USD; đổi lại nhóm giao báo cáo evidence để quyết định mở rộng/đổi hướng/dừng. | Đặng Quang Minh |

## Phần B — Chuẩn bị 3 câu phản biện

Business owner/instructor sẽ hỏi mỗi nhóm 1–2 câu. Viết sẵn câu trả lời:

1. *"Số liệu / giả định này lấy ở đâu?"* → Số ~500 học viên và ~80 học viên Product lấy từ context lab. Các số 10-15 phút/học viên, 13-20 giờ coach, 0.01-0.05 USD/bài và tỷ lệ adoption là giả định pilot để chốt plan; trước khi chạy thật nhóm sẽ xác nhận bằng 3-5 bài mẫu, log thời gian coach và chi phí token thực tế.
2. *"Nếu giả định quan trọng nhất của bạn sai thì sao?"* → Giả định quan trọng nhất là AI có thể tạo skill gap dựa trên evidence thật trong bài nộp/rubric. Nếu sai, nhóm không mở rộng Personalized Learning Path; dừng pilot ở phase calibration hoặc chuyển sang use case ít rủi ro hơn như checklist học bù dựa trên rubric chung/mini quiz đo trước-sau.
3. *"Tình huống nào sẽ khiến bạn dừng pilot?"* → Dừng ngay nếu có citation bịa/không tồn tại, độ đúng skill gap dưới 60%, hoặc feedback khiến học viên hiểu sai nghiêm trọng dù đã có coach review. Không mở rộng nếu sau 3 tuần không giảm được ≥30% thời gian coach hoặc adoption dưới 50%.

## Phần C — AI Support Log

| Câu hỏi | Trả lời |
|---|---|
| AI giúp được gì trong lab này? | AI giúp nhóm tách Big Ask thành các use case nhỏ, so sánh Build/Buy/Boost/Partner, gợi ý cấu trúc pilot plan và nhắc các tiêu chí dễ quên như baseline, exit criteria, adoption, citation và human review. |
| AI đưa output nào nghe hợp lý nhưng nhóm phải sửa? | AI dễ đề xuất cá nhân hóa rộng cho toàn bộ 6 tuần hoặc gửi feedback tự động cho học viên. Nhóm sửa lại thành pilot nhỏ sau Day 28, chỉ tạo draft 3 skill gap, bắt buộc coach review 100% và không dùng làm điểm chính thức. |
| Phần nào nhóm tự lập luận, KHÔNG copy AI? | Nhóm tự chốt Quick Win UC1 thay vì làm full Personalized Learning Path, tự chọn Boost vì phù hợp budget nhỏ, tự đặt ngưỡng dừng theo 2 red flag của track và tự xác định lời xin nguồn lực cụ thể cho pilot 3 tuần. |

---

## Tổng kiểm tra trước khi nộp

| Hạng mục | Xong? |
|---|---|
| 5 slide, mỗi slide 1 thông điệp, đã phân ai nói slide nào | x |
| Slide 5 có lời xin rõ ràng (xin gì · hứa gì) | x |
| Có câu trả lời sẵn cho cả 3 câu phản biện | x |
| AI Support Log điền đủ 3 dòng | x |
| Tất cả file worksheet/ đã commit + push, link dán vào Discord | / |

Đây là file cuối. Pitch 5 phút + nhận phản biện theo bảng 5 Gate (`templates/rubric-gate-sheet.md`).

*Liên quan: handbook §A9 · `templates/5-slide-pitch.md` · `templates/ai-support-log.md`*
