# HW03 — Kết quả chạy checklist GUI trên Chrome (Run 01)

## Thông tin lượt chạy

- **Run ID:** `HW03-CHROME-20261105-01`
- **Thời gian:** 20:25–20:38, 05/11/2026 (UTC+07:00)
- **SUT:** EShop SUT trong bản làm việc cô lập `HW03_EShop_Isolated`
- **URL:** `http://127.0.0.1:5173/`
- **Nền tảng:** Windows, Chrome trong Codex in-app browser. Phiên bản build Chrome không được giao diện hiện tại cung cấp.
- **Commit nguồn cô lập:** `85af3ba875c88283615e22cb108f13e2fccaf0e9`
- **Dữ liệu:** dữ liệu seed của môi trường cô lập; đã kiểm tra luồng iPhone 15 Pro Max. Không dùng cơ sở dữ liệu trong checkout gốc `eshop-sut`.
- **Tài khoản:** chưa xác thực thành công; mật khẩu thử không ghi vào hồ sơ.
- **Checklist:** 50 mục, giữ nguyên 7 cột. Bản nền không bị thay đổi trong lượt này; kết quả ghi trong `HW03_GUI_Checklist_Chrome_Run01.xlsx`.

## Tổng hợp

| Trạng thái | Số mục |
|---|---:|
| Passed (Yes) | 16 |
| Failed (No) | 21 |
| Chưa chạy (trạng thái để trống) | 13 |
| **Tổng** | **50** |

Ô trạng thái để trống nghĩa là chưa chạy/không đủ điều kiện kết luận; lý do cụ thể nằm trong Note của từng mục. Không xem đây là Pass.

## Các sai lệch nổi bật đã quan sát

- **Trang chủ:** hai thẻ `h1`; cả 5 ảnh danh sách có `alt` rỗng; giá dùng `VND` trong khi trang chi tiết dùng `₫`; giá màu đỏ có tương phản đo được khoảng **3,76:1**, thấp hơn ngưỡng 4,5:1 của checklist; tìm kiếm không có kết quả không nêu thông báo trống rõ.
- **Chi tiết sản phẩm:** nhãn “Số lượng” không liên kết với trường số; số 0 được giữ lại mà không có thông báo; không có breadcrumb/danh mục; ký hiệu tiền khác trang danh sách.
- **Giỏ hàng:** tổng dùng nhãn “Tổng tạm tính” thay vì “Tổng cộng”; trạng thái trống không có icon; không có nút chỉnh số lượng; xóa hàng không hỏi xác nhận; thêm lại cùng sản phẩm không làm tăng số lượng; không thấy badge giỏ.
- **Thanh toán:** người dùng chưa đăng nhập có thể mở trực tiếp `/checkout`; tổng tiền hiển thị như một spinbutton; mã không hợp lệ không hiện thông báo lỗi quan sát được. Khi bấm nút checkout từ giỏ lúc chưa đăng nhập, SUT hiện alert “Bạn cần đăng nhập để thanh toán!”.

## Mục chưa chạy

- **Viewport:** `HOME-02`, `HOME-08`, `DETAIL-02`, `DETAIL-03`, `CART-03` cần 375×812 và/hoặc 1440×900; tab kiểm thử không cung cấp chức năng đặt viewport.
- **Mạng chậm:** `HOME-17`, `CHECKOUT-12` chưa chạy vì không có công cụ điều tiết mạng trong tab.
- **Giỏ nhiều hàng / cập nhật:** `CART-12` chưa chạy; `CART-13` chưa chạy phần sau khi sửa số lượng do UI không có nút `+`/`−`.
- **Đơn hàng:** `CHECKOUT-01`, `CHECKOUT-03`, `CHECKOUT-13`, `CHECKOUT-16` cần giỏ hàng/đơn hàng hợp lệ; `CHECKOUT-14` mới thử mã giả `BADCODE`, chưa chạy mã `EXPIRED` hoặc trường hợp dưới ngưỡng.
- **Nhánh đăng nhập:** chưa xác minh thành công nên nhánh đã đăng nhập của `CART-10` chưa chạy.

## Bằng chứng

Trong lượt này đã quan sát ảnh chụp trang chủ, chi tiết sản phẩm và checkout qua giao diện trình duyệt. Các ảnh đang nằm trong kết quả thao tác giao diện của phiên làm việc, **chưa được xuất thành tệp riêng trong thư mục evidence**. Cần lưu ảnh chụp thật cho các mục Failed trước khi xem hồ sơ là hoàn chỉnh/nộp được.

## Giới hạn kết luận

Đây mới là một lượt trên Chrome ở viewport đang dùng, chưa phải hoàn tất Giai đoạn B. Chưa chạy đa nền tảng, chưa tạo GitHub Issues và chưa có ảnh lỗi dạng tệp. Kết quả No là quan sát của SUT tại lượt chạy này, không tự suy rộng thành kết luận về các phiên bản khác.
