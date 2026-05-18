---
artifact: 7 — AI Pilot Plan core
bai-tap: Pilot Plan — cam kết hai chiều: xin – hứa – đo – dừng
phase: Double Diamond vòng 2 · ◇ giãn → ◆ siết (liệt kê hết rồi chốt gọn)
time: ~10 phút (xem deck để biết khung giờ chính xác trong buổi)
input: 02-solution/2-FINAL-solution.md · 00-context.md · prompts/06-pilot-plan-challenge.md
nop-cuoi: Không — file trung gian (bản nộp ở 2-FINAL-pitch.md)
---

# 1 — AI Pilot Plan core

Mục tiêu: viết phần kế hoạch xin pilot — scope, người, data, budget, timeline, metric, exit criteria, adoption, lời hứa, lời xin. Bước này giãn ra (liệt kê hết những thứ cần) rồi siết lại (chốt bản gọn đủ để stakeholder quyết).

Lý do làm bước này: đây là thứ stakeholder dùng để **quyết approve hay dừng**. AI Pilot Plan **không phải proposal xin tiền** — là *cam kết hai chiều*: nhóm xin nguồn lực, đổi lại hứa giao evidence + chấp nhận dừng nếu metric fail. Demo đẹp mà không nói được "xin gì, hứa gì, đo gì, dừng khi nào" → trượt Gate 5.

Quy tắc: **budget tách từng hạng mục, không gộp 1 cục; không có mục "miscellaneous".** Exit criteria phải có người có quyền thực thi, không chỉ trên giấy.

## Quy trình 10 phút

```text
6 phút  — Điền 10 mục core (kéo nguyên liệu từ 00 + 01-frame + 02-solution)
3 phút  — Phần exit criteria + adoption (chỗ nhóm hay bỏ quên)
1 phút  — Tự phản biện
```

---

## 10 mục core

Câu hỏi phụ (tự trả lời):

- Nếu tóm vấn đề không gọn trong 1 câu → nhóm chưa hiểu vấn đề.
- Exit criteria của nhóm có ai DÁM thực thi khi sếp vẫn thích pilot không?
- Adoption: ai dùng đầu tiên — không phải "cả khóa ~500 người"?

### Trả lời

1. **Tóm vấn đề** (1 câu, từ Problem Framing): Sau Day 28, học viên chuẩn bị vào 6 tuần thực chiến nhưng chưa biết rõ 3 skill gap quan trọng nhất của mình, còn coach nếu cá nhân hóa feedback thủ công cho từng học viên sẽ tốn nhiều thời gian và khó đo hiệu quả.
2. **Cách làm + lý do** (từ 02-solution, 1 câu): Chọn **Boost**: dùng LLM API/tool có sẵn + prompt riêng + rubric Day 28 + coach review, vì bài toán cần một productivity layer có kiểm soát chứ chưa cần build model/platform riêng.
3. **Scope pilot**: phục vụ ai · bao nhiêu người · bao lâu · mấy phase: Pilot phục vụ trước cho học viên track Product vừa nộp bài Day 28; chạy nhỏ trên 10-15 học viên hoặc 5 nhóm đầu tiên có đủ bài nộp + self-assessment; thời lượng 3 tuần; gồm 2 phase: calibration trên bài mẫu và pilot có coach review trước khi gửi feedback.
4. **Người**: nhóm làm · ai review output rủi ro cao · ai có quyền quyết approve/dừng: Nhóm 3 thiết kế prompt, workflow và bảng đo; coach review 100% output rủi ro cao trước khi gửi học viên; lead coach/instructor có quyền approve, yêu cầu sửa, mở rộng hoặc dừng pilot.
5. **Data**: dùng data gì (mẫu/giả định) · cơ chế privacy/citation: Dùng bài nộp Day 28, rubric Day 28, self-assessment ngắn của học viên và tài liệu/slide/LMS liên quan. Trong lab dùng dữ liệu mẫu/giả định; nếu pilot thật phải có consent, ẩn tên/thông tin cá nhân khi dùng bài cũ, chỉ dùng trong phạm vi feedback formative. Mỗi skill gap bắt buộc có citation: trích dẫn nguyên văn từ bài nộp/rubric/tài liệu; nếu thiếu evidence thì AI phải ghi "không tìm thấy dữ liệu để đánh giá", không được suy diễn.
6. **Budget** (tách hạng mục): API/tool: dùng Dify/Coze hoặc web form nhỏ gọi OpenAI/Claude API, ước tính 0.01-0.05 USD/bài, tổng pilot 10-15 học viên dưới 5 USD và nếu mở rộng 80 học viên vẫn khoảng 5-10 USD. Thời gian người: nhóm 3 cần khoảng 4-6 giờ dựng prompt/flow/bảng đo; 1 coach cần 2 giờ calibration tuần 1 và 2-3 giờ/tuần để review output trong tuần 2-3; lead coach/instructor cần 30 phút duyệt đầu và 30 phút quyết định cuối. Hạng mục ẩn: 30-45 phút train coach cách đọc output và đánh dấu approve/edit/reject; 1 giờ bảo trì prompt sau phase 1; 30 phút tổng hợp báo cáo cuối pilot.
7. **Timeline + cổng giữa phase**: Phase 1 (1 tuần) chạy trên 3-5 bài mẫu/ẩn danh để calibrate prompt với coach → cổng: ≥70% skill gap được coach đánh giá đúng trọng tâm và 100% citation tồn tại trong nguồn. Phase 2 (2 tuần) chạy với 10-15 học viên/5 nhóm có consent, coach review trước khi gửi → cổng cuối: đạt ngưỡng metrics, không chạm exit criteria nghiêm trọng, lead coach quyết định mở rộng/đổi hướng/dừng.
8. **Metrics** (SMART + baseline + ngưỡng + ai đo):

| Metric | Đo bằng gì · ai đo | Baseline | Ngưỡng đạt |
|---|---|---|---|
| Độ đúng của 3 skill gap | Coach đánh dấu từng gap: approve / edit nhẹ / reject; nhóm tổng hợp tỷ lệ approve + edit nhẹ | Chưa có AI; coach phải tự đọc bài và tự viết gap thủ công | ≥70% gap được approve hoặc chỉ cần edit nhẹ; không quá 1 gap/học viên bị reject |
| Citation chính xác | Coach kiểm tra quote có tồn tại đúng trong bài nộp/rubric/tài liệu không | Feedback thủ công hiện chưa bắt buộc quote nguyên văn | 100% citation tồn tại trong nguồn; 0 trường hợp bịa quote |
| Thời gian coach review mỗi học viên | Coach ghi thời gian review output AI và so với ước tính làm thủ công | Giả định hiện tại 10-15 phút/học viên để đọc và viết 3 skill gap | Giảm ít nhất 30% thời gian so với thủ công mà vẫn đạt ngưỡng chất lượng |
| Adoption của học viên | Form ngắn sau khi nhận feedback: đã đọc, có hiểu gap không, có biết bước học bù tiếp theo không | Chưa có bước chuẩn để học viên nhận 3 skill gap cá nhân sau Day 28 | ≥70% học viên pilot xác nhận feedback giúp họ biết nên học lại phần nào |

   Leading indicator (biết kết quả sớm trong 1–2 tuần): Sau 5 bài đầu ở Phase 1, nếu coach approve/edit nhẹ ≥70% gap và không có citation bịa thì tiếp tục Phase 2; nếu thấp hơn thì sửa prompt/rubric mapping trước khi cho học viên xem.

9. **Exit criteria** (định trước, ≥2 mức):

| Mức | Điều kiện | Hành động | Ai có quyền dừng |
|---|---|---|---|
| Cảnh báo | Độ đúng skill gap chỉ đạt 60-70%, hoặc coach phải edit nhiều hơn dự kiến, hoặc học viên phản hồi "chung chung" ở >30% mẫu | Tạm chưa mở rộng; sửa prompt, bổ sung ví dụ calibration, làm rõ rubric mapping rồi chạy lại 3-5 bài | Coach phụ trách pilot đề xuất; lead coach duyệt tiếp hay sửa |
| Nghiêm trọng | Có bất kỳ citation bịa/không tồn tại; hoặc độ đúng skill gap <60%; hoặc feedback khiến học viên hiểu sai nghiêm trọng dù đã có coach review | Dừng pilot, không gửi thêm output cho học viên; phân tích lỗi và chỉ khởi động lại khi có cơ chế chặn lỗi rõ ràng | Lead coach/instructor |
| Không đáng mở rộng | Sau 3 tuần không giảm được ≥30% thời gian coach hoặc adoption <50% học viên pilot | Kết thúc pilot ở phạm vi nhỏ; chuyển sang use case khác như checklist học bù hoặc đo trước-sau | Lead coach/instructor |

   *Liên hệ 2 Red Flag ở `00-context.md`:* Red flag "cá nhân hóa giả" được chặn bằng metric độ đúng skill gap, yêu cầu evidence/citation và phản hồi học viên về mức hữu ích. Red flag "không đo được học viên có tốt lên không" được chặn bằng baseline, ngưỡng adoption và báo cáo cuối; nếu muốn mở rộng phase sau phải bổ sung mini quiz hoặc bài sửa lại để đo trước-sau.

10. **Adoption** (tool không ai dùng = $0): Người dùng đầu tiên là 10-15 học viên/5 nhóm Product có bài Day 28 và consent; coach là người dùng vận hành đầu tiên vì coach phải review output trước khi gửi. Workflow đổi ở bước sau nộp bài: thay vì coach tự viết feedback từ đầu, AI tạo draft 3 skill gap có quote, coach approve/edit/reject, rồi mới gửi cho học viên. Nhóm 3 train coach bằng 1 buổi 30-45 phút và hỗ trợ sửa prompt trong 1 tuần đầu. Nếu học viên không đọc hoặc thấy feedback chung chung, không mở rộng; nhóm phỏng vấn nhanh 3-5 học viên để biết lỗi nằm ở output, kênh gửi hay timing.

11. **Lời hứa giao gì**: Sau 3 tuần, nhóm giao báo cáo pilot gồm tỷ lệ skill gap được coach approve, tỷ lệ citation đúng, thời gian coach tiết kiệm được, phản hồi học viên, lỗi thường gặp, quyết định đề xuất: mở rộng / đổi hướng / dừng. Nhóm chấp nhận báo cáo cả kết quả fail nếu metric không đạt.

12. **Lời xin**: Xin quyền chạy pilot 3 tuần với 10-15 học viên/5 nhóm Product có consent; xin 1 coach review 2-3 giờ/tuần, 30 phút lead coach duyệt đầu/cuối, quyền dùng bài nộp Day 28 đã ẩn thông tin cá nhân, rubric, self-assessment và ngân sách API tối đa 10 USD. Đổi lại, nhóm hứa giao evidence đủ để quyết định có mở rộng Personalized Learning Path hay không. Mức rủi ro thấp vì output chỉ là feedback formative, có coach review 100%, không dùng để chấm điểm chính thức và không gửi tự động khi chưa duyệt.

---

## Tự phản biện

- Budget đã tách API/tool, thời gian coach/lead coach, training, bảo trì prompt và báo cáo cuối. Hạng mục dễ thiếu nhất là thời gian coach review 100% output, nên đã tính riêng 2-3 giờ/tuần.
- Exit criteria đủ mạnh vì lead coach/instructor có quyền dừng nếu citation bịa, độ đúng <60%, hoặc adoption quá thấp. Đây không chỉ là cảnh báo kỹ thuật mà là điều kiện không được gửi tiếp cho học viên.
- Giả định quan trọng nhất là AI có thể tạo 3 skill gap dựa trên evidence trong bài nộp/rubric. Nếu giả định này sai, nhóm không mở rộng Personalized Learning Path; chuyển sang use case ít rủi ro hơn như checklist học bù dựa trên rubric chung hoặc đo trước-sau bằng mini quiz.

---

## Tổng kiểm tra trước khi sang `2-FINAL-pitch.md`

| Hạng mục | Xong? |
|---|---|
| Tóm vấn đề trong 1 câu | x |
| Budget tách hạng mục, không "miscellaneous" | x |
| Metric có baseline + ngưỡng + ai đo | x |
| Exit criteria có người có quyền thực thi (≥2 mức) | x |
| Adoption: chỉ rõ ai dùng đầu tiên (không "cả khóa") | x |

⚑ Coach kiểm tra ở Mốc 4: *"Xin gì? Hứa gì? Đo gì? Dừng khi nào?"*

Sau bước này, mở `2-FINAL-pitch.md` — dồn tất cả thành 5-slide pitch + AI Support Log.

*Liên quan: handbook §A7+§A8 · `templates/ai-pilot-plan-core.md` · `prompts/06-pilot-plan-challenge.md`*
