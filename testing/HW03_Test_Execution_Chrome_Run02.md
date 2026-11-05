# HW03 — Kết quả chạy checklist GUI trên Chrome (Run 02)

## Thông tin lượt chạy

- **Run ID:** `HW03-CHROME-20261105-02`
- **Ngày chạy:** 05/11/2026 (UTC+07:00)
- **SUT:** EShop SUT trong bản làm việc cô lập `HW03_EShop_Isolated`
- **URL:** `http://127.0.0.1:5173/`
- **Nền tảng:** Windows, Google Chrome qua extension điều khiển trình duyệt.
- **Dữ liệu:** dữ liệu seed trong môi trường cô lập; không dùng cơ sở dữ liệu của checkout gốc `eshop-sut`.
- **Tài khoản:** đăng nhập thành công bằng tài khoản Admin seed sẵn; không tạo tài khoản mới.
- **Checklist:** 48 mục, giữ nguyên 7 cột của template. Hai mục điều tiết mạng nằm ngoài phạm vi theo quyết định trước đó.
- **Workbook:** `checklist/HW03_GUI_Checklist_Chrome_Run02.xlsx`.

## Test summary

| Trạng thái | Số mục |
|---|---:|
| Passed (Yes) | 24 |
| Failed (No) | 24 |
| Chưa chạy | 0 |
| **Tổng thiết kế / thực thi** | **48 / 48** |

Có 19 bug khác nhau được nhóm từ 24 mục Failed; ánh xạ checklist ID, issue và ảnh nằm trong [`HW03_Bug_Report_Chrome_Run02.md`](HW03_Bug_Report_Chrome_Run02.md). Một bug có thể liên quan nhiều mục checklist.

## Kết quả đáng chú ý

- `DETAIL-03`: mô tả nhiều dòng nhất trong dữ liệu seed xuống hai dòng tại 375 × 812 px; nút vẫn nằm dưới mô tả, không chồng lấn. Không có sản phẩm seed với mô tả dài hơn để kiểm tra stress.
- `CART-03`: giỏ hai mặt hàng vẫn dùng được ở 375 × 812 px; một số nội dung xuống dòng nhưng không bị cắt.
- `CART-10`: khi đăng xuất, bấm thanh toán hiện cảnh báo đăng nhập. Sau khi đăng nhập, nút mở checkout và hiển thị tóm tắt đơn.
- `CART-12`: xóa hàng đầu làm hàng đó biến mất ngay, không có xác nhận; hàng còn lại vẫn là Samsung.
- `CART-13`: đặt MacBook số lượng 2 tại trang chi tiết cho thành tiền 90.000.000 ₫, tổng giỏ 148.000.000 ₫. Trong giỏ không có điều khiển để tăng/giảm sau khi thêm; mục Failed vì không thể thực hiện chỉnh số lượng trong giỏ.
- `CHECKOUT-01` và `CHECKOUT-03`: tóm tắt hai mặt hàng và tổng 58.000.000 ₫; sau xác nhận, giao diện báo thanh toán thành công và có nút quay về trang chủ.
- `CHECKOUT-13`: `SAVE10` báo giảm 10% nhưng tính giảm 522.000.000 ₫ trên tổng 58.000.000 ₫, làm tổng sau giảm thành 580.000.000 ₫.
- `CHECKOUT-14`: chạy lại `BADCODE` cho thông báo không tồn tại/vô hiệu hóa; `EXPIRED` báo hết hạn; `SAVE10` với tổng nhập 200.000 ₫ báo chưa đạt ngưỡng 300.000 ₫. Cả ba lần giữ nguyên giá trị tổng trong lúc áp mã. Nhánh dưới ngưỡng được tạo bằng cách sửa trường tổng trên checkout; danh sách mặt hàng vẫn có giá trị 58.000.000 ₫, vì dữ liệu seed không có sản phẩm dưới ngưỡng. Mục được đánh Yes cho phản hồi mã và ghi rõ hạn chế dữ liệu.
- `CHECKOUT-16`: sau thông báo thành công, mở lại giỏ vẫn thấy iPhone và Samsung với tổng 58.000.000 ₫.

## Các nhóm lỗi

- **Trang chủ:** ký hiệu tiền không đồng nhất; tương phản giá khoảng 3,76:1, thấp hơn 4,5:1; hai thẻ `h1`; ảnh danh sách thiếu `alt`; tìm kiếm rỗng không có thông báo không tìm thấy.
- **Chi tiết sản phẩm:** nhãn số lượng không liên kết với input; số 0 không bị từ chối; lần nhấn Enter vào nút thêm giỏ không có phản hồi; thiếu breadcrumb và danh mục.
- **Giỏ hàng:** nhãn tổng là “Tổng tạm tính” thay vì “Tổng cộng”; trạng thái trống thiếu icon; không có chỉnh số lượng; xóa không xác nhận; thêm lại sản phẩm tạo dòng trùng; header không có badge.
- **Thanh toán:** mở trực tiếp khi đăng xuất; tổng có thể sửa; mã `SAVE10` tính sai; giỏ không xóa sau thanh toán.

## Ảnh evidence

Ảnh chụp trực tiếp phần nội dung tab EShop, không gồm thanh tab/bookmark của trình duyệt, nằm trong `testing/evidence/Chrome_Run02/`:

- `HOME-06_HOME-07_HOME-09_HOME-10.jpg`
- `HOME-18_no_search_results.jpg`
- `DETAIL-04_DETAIL-05_DETAIL-07_DETAIL-10_375px.jpg`
- `DETAIL-11_keyboard_activation_no_feedback.jpg`
- `CART-02_CART-03_CART-05_375px.jpg`
- `CART-04_empty_after_deletions.jpg`
- `CART-06_CART-12_after_delete_first.jpg`
- `CART-08_duplicate_product_rows.jpg`
- `CART-13_quantity_two_calculation.jpg`
- `CHECKOUT-01_populated_order.jpg`
- `CHECKOUT-09_accessible_while_logged_out.jpg`
- `CHECKOUT-13_SAVE10_bad_calculation.jpg`
- `CHECKOUT-16_cart_not_cleared.jpg`

## Giới hạn

Đây là một lượt Chrome trên bản SUT cô lập, không thay thế việc chạy Task 1 trên ít nhất ba nền tảng. `DETAIL-03` chỉ dùng mô tả dài nhất có sẵn trong seed. Nhánh coupon dưới ngưỡng dùng trường tổng có thể sửa trực tiếp, không phải một giỏ hàng gồm sản phẩm thật dưới 300.000 ₫. Các phiên pilot và bảy phiên usability cần người tham gia thật, không thuộc lượt chạy này.

