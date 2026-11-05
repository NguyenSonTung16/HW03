# Kế hoạch thực hiện HW03 GUI và đánh giá tính khả dụng

> Tài liệu làm việc dựa trên [đề HW03 bản tiếng Anh](C:/Users/tung1/Downloads/2026.HW03.GUI%20Usability_En.pdf), 9 trang. Đây là checklist để lập kế hoạch, không phải bài làm hoặc minh chứng đã hoàn thành. Mọi ô để trống cho đến khi có công việc và bằng chứng thực tế. Ký hiệu `§` chỉ mục trong đề gốc.

## 1. Thông tin quan trọng cần chốt trước

- **Hình thức:** bài tập cá nhân; thời lượng dự kiến 10 giờ; hạn nộp xem trực tiếp tại liên kết nộp bài trên Moodle (§1, tr. 1).
- **Nộp bài:** một tệp ZIP theo mẫu `<StudentID>_HW03_AI_GUIUsability_<SelfAssessedGrade>.zip`; điểm tự đánh giá gồm ba chữ số từ `000` đến `100` (§14, tr. 7–8).
- **Phạm vi:** GUI checklist, đánh giá tính khả dụng có điều phối với **7 người tham gia thật**, và thực thi checklist trên **ít nhất 3 nền tảng** (§5–6, tr. 3–6).
- **Checklist GUI:** **hơn 40 mục**, tức ít nhất **41 mục**. Phải bao phủ IA-01 (tiêu chuẩn giao diện chung), IA-02 (biểu mẫu), IA-03 (điều hướng), IA-04 (phản hồi/trạng thái) (§4, §6, tr. 3–4).
- **Chính sách AI:** được dùng AI, nhưng phải rà soát kết quả, khai báo việc dùng AI, nộp AI Audit Report; AI Critique 200–300 từ là phần riêng (§2, §9–10, tr. 1–2, 6–7).
- **Điểm:** Task 1: 30; Task 2: 40; Task 3: 20; Agent Skills: 10; tổng 100 (§15, tr. 8).
- **Rủi ro bị 0 điểm:** giả mạo người tham gia làm Task 2 bị 0; thiếu bất kỳ tài liệu bắt buộc nào bị 0; sao chép giữa sinh viên, kể cả prompt, làm cả hai bị 0; không chấp nhận nộp muộn (§6, §17, tr. 5, 9).

## 2. Những gì cần chuẩn bị trước khi bắt đầu

### 2.1. Đề, học liệu và quyền truy cập

- [ ] Đọc trọn đề gốc, nhất là §5–6 và §9–17; kiểm tra hạn nộp trên Moodle.
- [ ] Xem lại bài giảng về GUI checklist và đánh giá tính khả dụng trước khi thiết kế (§6).
- [ ] Truy cập được [kho mã EShop](https://github.com/ttbhanh/eshop-sut), chạy được SUT và xác định URL localhost (§4).
- [ ] Kiểm tra giao diện web, ứng dụng di động và dữ liệu thử cần thiết cho luồng định chọn; chuẩn bị tài khoản / vai trò phù hợp.
- [ ] Tạo nơi lưu tài liệu Markdown, ảnh, video, bảng Excel, Git commit log và liên kết GitHub Issues. Đây là cách tổ chức **đề xuất**, không phải cấu trúc thư mục bắt buộc của đề.
- [ ] Chuẩn bị công cụ AI định dùng và cách lưu nguyên văn tên công cụ, ngày giờ, prompt, output cho từng tương tác (§8–9).
- [ ] Chuẩn bị BrowserStack hoặc LambdaTest trial; nếu không dùng được, chọn công cụ đám mây khác hoặc thiết bị thật đáp ứng điều kiện ảnh (§6, tr. 6).
- [ ] Xác định ba nền tảng sẽ thực thi checklist. Giao diện web cần bao phủ Chrome, Firefox, Safari **hoặc Chrome trên Android**. Expo Go trên điện thoại thật có thể thay thế **một** trong ba nền tảng trình duyệt (§6, tr. 6).

### 2.2. Chốt phạm vi kiểm thử

- [ ] Chọn **ít nhất một màn hình** cho GUI checklist; nên chọn nhiều màn hình để có trên 40 mục có ý nghĩa, không lặp (§5, tr. 3).
- [ ] Chọn **một luồng đầu cuối** cho đánh giá tính khả dụng; đó là luồng duy nhất người tham gia sẽ thực hiện (§5, tr. 3–4).
- [ ] Phối hợp trong nhóm để không trùng **màn hình chính** của checklist hoặc **luồng tính khả dụng** với thành viên khác, dù bài nộp là cá nhân (§5, tr. 4).
- [ ] Ghi rõ màn hình/luồng đã chọn, lý do chọn, nền tảng và phiên bản SUT tại thời điểm kiểm thử. Đây là thông tin truy vết **đề xuất**.

### 2.3. Chuẩn bị người tham gia và bộ công cụ nghiên cứu

- [ ] Xác định hồ sơ người dùng mục tiêu trước khi tuyển người.
- [ ] Tuyển **7 người tham gia thật**, ở **ngoài lớp này**; sinh viên đang học HW03 không hợp lệ. Ưu tiên người không làm CNTT/kiểm thử, nhưng đó không phải điều kiện cứng (§6, tr. 5).
- [ ] Có thông tin liên hệ xác minh được: Zalo, email hoặc điện thoại; che bốn chữ số ở giữa khi trình bày theo yêu cầu đề (§6, tr. 5).
- [ ] Chuẩn bị một người cho phiên pilot để phát hiện kịch bản khó hiểu, luồng lỗi hoặc vấn đề thời lượng; chỉnh sửa trước bảy phiên chính thức (§6, tr. 5). **Đề không nói rõ có được tính người pilot vào bảy người hay không; để chắc chắn, nên xem pilot là phiên riêng.**
- [ ] Soạn kịch bản nhiệm vụ theo **mục tiêu thực tế**, không viết hướng dẫn từng cú nhấp chuột (§6, tr. 5).
- [ ] Chuẩn bị thang SUS hoặc UEQ-S cho từng phiên; nếu tự thiết kế thang đo, viết lý do rõ ràng (§6, tr. 5).
- [ ] Chuẩn bị câu hỏi mở tối thiểu về **độ rõ ràng, khắc phục lỗi, tốc độ, niềm tin** (§6, tr. 5).
- [ ] Chuẩn bị mẫu ghi chú quan sát: thời điểm, thao tác, điểm vướng, lỗi, do dự, lời nói, kết quả nhiệm vụ.
- [ ] Chuẩn bị cách xin đồng ý ghi âm/ghi hình và kiểm tra công cụ ghi màn hình; chỉ ghi âm khi có sự đồng ý (§6, tr. 5).

## 3. Checklist công việc theo trình tự

### Giai đoạn A — Thiết kế checklist GUI

- [ ] Chọn màn hình, liệt kê yêu cầu giao diện liên quan và gắn mỗi mục với IA-01/02/03/04.
- [ ] Dùng AI để tạo **bộ mục ban đầu**, lưu nguyên prompt và output để đưa vào AI Audit (§6, §9).
- [ ] Tự rà soát từng mục: cụ thể, kiểm tra được trên màn hình đã chọn, không trùng và có kết quả quan sát được.
- [ ] Tự bổ sung những mục AI bỏ sót. Với **mỗi mục tự thêm**, ghi lý do AI bỏ sót: chất lượng prompt, giới hạn mô hình hoặc đặc thù giao diện (§6, tr. 4).
- [ ] Xem xét khả năng tiếp cận, bố cục RTL, chế độ tối khi phù hợp; đây là ví dụ đề nêu, không phải danh sách đóng (§6, tr. 4).
- [ ] Bảo đảm **ít nhất 41 mục** và đủ bốn IA; xuất checklist Excel và mô tả quá trình thiết kế trong báo cáo chính.
- [ ] Tạo Git commit cho bước thiết kế checklist (§12).

### Giai đoạn B — Thực thi checklist và ghi lỗi

- [ ] Chạy từng mục checklist trên SUT; ghi **Passed** hoặc **Failed** cho mỗi mục (§6, tr. 4).
- [ ] Thêm cột **Notes**; với mỗi mục Failed, ghi lý do thất bại (§6, tr. 4).
- [ ] Chụp và đính kèm ảnh **chỉ cho mục Failed** trong checklist (§6, tr. 4).
- [ ] Kiểm tra ảnh không bị AI dựng hoặc chỉnh thành minh chứng giả; bảo toàn khả năng xác minh thực tế.
- [ ] Ghi mọi bug tìm được trong báo cáo Markdown **và** GitHub Issues; mỗi GitHub issue có ảnh lỗi (§6, tr. 4–5).
- [ ] Lập test summary: số mục thiết kế, thực thi, Passed, Failed và số bug.
- [ ] Tạo commit riêng cho thực thi checklist và bước ghi bug (§12).

### Giai đoạn C — Đánh giá tính khả dụng

**Lập kế hoạch và pilot**

- [ ] Nêu mục tiêu muốn tìm hiểu từ người dùng trên luồng đã chọn.
- [ ] Hoàn thiện kịch bản theo mục tiêu, thang đo, câu hỏi mở và mẫu ghi chú.
- [ ] Chạy pilot với một người thật; ghi điều chưa rõ và chỉnh kịch bản/công cụ trước các phiên chính thức.

**Bảy phiên thật, mỗi người một phiên**

- [ ] Lên lịch bảy phiên với bảy người hợp lệ; lưu danh sách liên hệ có thể xác minh và bản trình bày đã che bốn chữ số giữa.
- [ ] Mỗi phiên: nói rõ đang kiểm thử **sản phẩm, không phải người tham gia**; đề nghị họ suy nghĩ thành lời (§6, tr. 5).
- [ ] Quan sát trung lập; không gợi ý dẫn dắt hoặc giải thích giao diện; chỉ can thiệp khi họ hoàn toàn bế tắc (§6, tr. 5).
- [ ] Ghi màn hình; chỉ ghi âm khi đã có đồng ý; ghi có cấu trúc các điểm vướng, lỗi, do dự và bực bội được nói ra (§6, tr. 5).
- [ ] Cuối mỗi phiên, cho người tham gia tự hoàn thành SUS/UEQ-S rồi hỏi các câu thăm dò (§6, tr. 5).
- [ ] Lưu ghi chú, câu trả lời, bản ghi màn hình (khi có) và một Git commit cho **từng phiên** (§12).

**Phân tích**

- [ ] Tính điểm SUS/UEQ-S cho cả bảy người; trình bày cách tổng hợp kết quả.
- [ ] Nhóm các khó khăn tương tự; tách bug đơn lẻ khỏi vấn đề thiết kế mang tính hệ thống.
- [ ] Xếp phát hiện theo mức nghiêm trọng, ví dụ vấn đề chặn hoàn thành nhiệm vụ so với vấn đề hình thức nhỏ.
- [ ] Báo cáo bug thật trong Markdown và GitHub Issues, mỗi issue kèm ảnh (§6, tr. 5).
- [ ] Tạo Git commit cho phân tích (§12).

### Giai đoạn D — Kiểm thử đa nền tảng

- [ ] Thực hiện lại **Nhiệm vụ 1** trên **ít nhất 3 nền tảng**, ghi kết quả theo từng nền tảng (§6, tr. 5–6).
- [ ] Nếu dùng cloud trial, kiểm tra ảnh cho thấy rõ tên trình duyệt / hệ điều hành / thiết bị và URL localhost của SUT; nếu thay bằng thiết bị vật lý cũng phải đáp ứng điều kiện này (§6, tr. 6).
- [ ] Kiểm tra giao diện web trên Chrome, Firefox, Safari hoặc Chrome trên Android; nếu dùng Expo Go trên điện thoại thật thì tính là một trong ba nền tảng (§6, tr. 6).
- [ ] Phủ tên người dùng dưới dạng **email sinh viên** lên **mỗi ảnh** theo Task 3 (§6, tr. 6).
- [ ] Với ảnh thuộc ràng buộc chống gian lận ở §11, bảo đảm **mã số sinh viên và họ tên đầy đủ xuất hiện trong biểu mẫu** (§11, tr. 7). Đây là yêu cầu khác với lớp phủ email; nên kiểm tra cả hai khi ảnh được dùng làm minh chứng cho cả hai mục.
- [ ] Ghi kết quả, khác biệt giữa các nền tảng và bug trong báo cáo; lưu ảnh gốc và ảnh nộp để truy vết.

### Giai đoạn E — AI, tài liệu hóa và rà soát

- [ ] Viết báo cáo chính dạng Markdown, gồm quy trình, checklist GUI, thực thi, bug, đánh giá tính khả dụng và kết quả đa nền tảng (§6, §14).
- [ ] Xuất báo cáo chính sang PDF (§14).
- [ ] Khai báo AI theo §9. Nếu đã dùng AI: “I use AI tools for the following tasks,” và ghi **tên công cụ, ngày giờ, prompt, output cho từng tương tác**. Nếu không dùng AI: “I do not use any AI help in this exercise.” Chỉ chọn khai báo đúng sự thật.
- [ ] Đính kèm AI Audit Report như phụ lục, dạng Markdown + PDF theo danh sách tệp nộp (§9, §14).
- [ ] Viết **AI Critique 200–300 từ**: AI sai/thiên lệch/thiếu ở đâu, vì sao không phát hiện, học được nguyên tắc cộng tác nào; lưu Markdown + PDF (§10, §14).
- [ ] Nếu làm Agent Skills, nộp skill và video YouTube thể hiện từ đầu đến cuối cách dùng trên một màn hình/luồng hoàn chỉnh (§7). Mục này có 10 điểm trong bảng chấm (§15).
- [ ] Xuất Git commit log thành tệp văn bản; bảo đảm có commit cho các bước quan trọng (§12).
- [ ] Viết README.md gồm bảng tự đánh giá và test summary đúng các chỉ số yêu cầu (§14).
- [ ] Tự rà soát mọi kết quả AI; sửa và lưu bằng chứng sửa. Không nộp nguyên output AI chưa xem xét (§2).
- [ ] Chuẩn bị giải thích quy trình nếu được chọn bảo vệ vấn đáp 5–7 phút (30% sinh viên được chọn ngẫu nhiên trong tuần sau hạn nộp) (§13).

## 4. Những việc phải do con người thật thực hiện và điều AI bị cấm tạo/bịa

Đề viết nguyên văn: “**The following must not be AI-generated or fabricated**” (§11, tr. 7). Hai loại minh chứng bị cấm AI tạo hoặc bịa là:

1. **Danh sách 7 người tham gia thật**, gồm tên và Zalo / số điện thoại đã che bốn chữ số giữa. Trợ giảng có thể gọi ngẫu nhiên hai người để xác minh. Không nhờ AI tạo tên, số liên hệ, danh sách hoặc câu trả lời giả. §6 còn cho phép thông tin liên hệ xác minh bằng Zalo, email hoặc điện thoại; cần đáp ứng đồng thời cách trình bày tại §11.
2. **Ảnh chụp màn hình kiểm thử đa nền tảng thật**, trong đó mã số sinh viên và họ tên đầy đủ hiện trong biểu mẫu. Không nhờ AI sinh ảnh, ghép trình duyệt/thiết bị, hoặc tạo trạng thái kiểm thử giả. Task 3 cũng yêu cầu phủ email sinh viên trên mỗi ảnh.

Ngoài hai loại nội dung được §11 nêu rõ, các bước dưới đây cũng đòi hỏi **hành động thật của con người** theo §6: tuyển người tham gia hợp lệ, điều phối pilot và bảy phiên, quan sát, xin đồng ý trước khi ghi âm, thu câu trả lời thang đo và liên hệ xác minh được; chạy SUT trên các nền tảng thật và chụp minh chứng thật. AI có thể hỗ trợ soạn câu hỏi, phân loại ghi chú hoặc tính toán **từ dữ liệu thực**, nhưng không được đóng vai người tham gia hay bịa kết quả. Đây là cách thực hiện phù hợp với yêu cầu “real participants” và “real cross-platform runs” của đề, không phải một lệnh cấm AI bổ sung ngoài §11.

## 5. Danh sách tệp và minh chứng cần nộp

| Thành phần trong ZIP | Định dạng / nội dung tối thiểu | Nguồn |
|---|---|---|
| Báo cáo chính | **Markdown + PDF**; gồm GUI checklist report và usability evaluation report | §14, tr. 8 |
| Báo cáo bug | Trong báo cáo Markdown và trên **GitHub Issues**; ảnh lỗi đính kèm từng issue | §6, §14, tr. 4–5, 8 |
| AI Critique | **Markdown + PDF**; 200–300 từ | §10, §14, tr. 7–8 |
| AI Audit Report | **Markdown + PDF**; phụ lục có thông tin từng tương tác AI | §9, §14, tr. 6–8 |
| Git commit log | Tệp văn bản; phản ánh các bước kiểm thử | §12, §14, tr. 7–8 |
| GUI checklist Excel | **Hơn 40 mục**, trạng thái Passed/Failed, Notes cho Failed; kèm test summary | §6, §14, tr. 4, 8 |
| Minh chứng usability | Kịch bản, ghi chú quan sát, trả lời SUS/UEQ-S, phát hiện xếp độ nghiêm trọng, video màn hình khi có, bảng 7 người | §14, tr. 8 |
| Ảnh đa trình duyệt / đa nền tảng | Ảnh thật của ít nhất 3 nền tảng; đáp ứng yêu cầu nhận diện nêu ở §6 và §11 | §6, §11, §14, tr. 6–8 |
| README.md | Bảng tự đánh giá và test summary: số màn hình/luồng, số mục checklist thiết kế/thực thi/Passed/Failed, số bug, số người tham gia, video demo | §14–15, tr. 8 |
| Agent Skills và video | Skill cùng liên kết YouTube demo từ đầu đến cuối nếu thực hiện phần Agent Skills | §7, §15, tr. 6, 8 |
| Tài liệu hỗ trợ khác | Những tệp cần thiết để người chấm kiểm chứng kết quả | §14, tr. 8 |

**Checklist đóng gói cuối:**

- [ ] Tên ZIP khớp mẫu; điểm tự đánh giá có đúng ba chữ số.
- [ ] Báo cáo chính có cả `.md` và `.pdf`; AI Critique và AI Audit Report cũng có cả hai định dạng.
- [ ] Checklist Excel chứa trên 40 mục, đủ bốn IA, có kết quả thực thi và ghi chú mục Failed.
- [ ] Mọi GitHub issue báo lỗi có ảnh; các liên kết trong báo cáo mở được.
- [ ] Có đủ minh chứng **bảy** phiên thật, bảng người tham gia hợp lệ và kết quả thang đo.
- [ ] Có ảnh kiểm thử **ít nhất ba** nền tảng, đúng thông tin hiển thị và lớp phủ yêu cầu.
- [ ] README có bảng tự chấm 30/40/20/10 và tất cả chỉ số tổng kết.
- [ ] Có Git commit log dạng văn bản và các commit tương ứng các bước.
- [ ] Đã kiểm tra không thiếu tài liệu bắt buộc, không sao chép prompt/bài làm, nộp trước hạn trên Moodle.

## 6. Điều cần đối chiếu với giảng viên khi còn mơ hồ

- Đề §6 yêu cầu che bốn chữ số giữa đối với thông tin liên hệ Zalo/email/điện thoại; §11 viết danh sách gồm tên và Zalo/số điện thoại. Nếu dự định **chỉ dùng email** để xác minh, nên hỏi trợ giảng trước.
- Đề §6 nói mỗi ảnh phải phủ email sinh viên; §11 yêu cầu ảnh cho thấy MSSV và họ tên đầy đủ trong biểu mẫu. Chuẩn bị ảnh thỏa **cả hai**, nếu có thể.
- Đề yêu cầu pilot với một người và bảy phiên với bảy người thật nhưng không nói rõ pilot có được tính vào bảy phiên. Phương án an toàn là tổ chức pilot riêng.

## 7. Trích dẫn gốc để kiểm tra các ngưỡng dễ nhầm

> “Design a checklist of more than 40 items” (§6, tr. 4).

> “seven (7) real participants (seven sessions, one per participant)” (§6, tr. 4).

> “Perform Task 1 across at least three (3) platforms.” (§6, tr. 5).

> “The following must not be AI-generated or fabricated” (§11, tr. 7).
