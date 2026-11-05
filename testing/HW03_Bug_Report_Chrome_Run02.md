# HW03 — Bug Report Chrome Run 02

- **Run ID:** `HW03-CHROME-20261105-02`
- **Ngày:** 05/11/2026 (UTC+07:00)
- **SUT:** EShop SUT cô lập, Chrome trên Windows
- **Nguồn:** [Kết quả thực thi checklist](HW03_Test_Execution_Chrome_Run02.md) và [checklist Run 02](../checklist/HW03_GUI_Checklist_Chrome_Run02.xlsx)
- **Kết quả:** 24 checklist mục Failed được nhóm thành 19 bug. Mỗi GitHub Issue bên dưới đã được tạo kèm ảnh chụp từ lần chạy.

| # | Bug / hiện tượng | Checklist Failed | GitHub Issue | Ảnh evidence trong repo |
|---:|---|---|---|---|
| 1 | Ký hiệu tiền tệ giữa danh sách và chi tiết không thống nhất (`VND` / `₫`) | `HOME-06`, `DETAIL-04` | [#1](https://github.com/NguyenSonTung16/HW03/issues/1) | `HOME-06_HOME-07_HOME-09_HOME-10.jpg`; `DETAIL-04_DETAIL-05_DETAIL-07_DETAIL-10_375px.jpg` |
| 2 | Tương phản màu giá thấp hơn 4,5:1 | `HOME-07` | [#2](https://github.com/NguyenSonTung16/HW03/issues/2) | `HOME-06_HOME-07_HOME-09_HOME-10.jpg` |
| 3 | Trang chủ có hai thẻ `h1` | `HOME-09` | [#3](https://github.com/NguyenSonTung16/HW03/issues/3) | `HOME-06_HOME-07_HOME-09_HOME-10.jpg` |
| 4 | Ảnh sản phẩm thiếu alternative text hữu ích | `HOME-10` | [#4](https://github.com/NguyenSonTung16/HW03/issues/4) | `HOME-06_HOME-07_HOME-09_HOME-10.jpg` |
| 5 | Tìm kiếm không có kết quả không hiện thông báo trạng thái rỗng rõ ràng | `HOME-18` | [#5](https://github.com/NguyenSonTung16/HW03/issues/5) | `HOME-18_no_search_results.jpg` |
| 6 | Nhãn “Số lượng” chưa liên kết với ô nhập | `DETAIL-05` | [#6](https://github.com/NguyenSonTung16/HW03/issues/6) | `DETAIL-04_DETAIL-05_DETAIL-07_DETAIL-10_375px.jpg` |
| 7 | Giá trị số lượng `0` không bị từ chối và không có thông báo lỗi | `DETAIL-07`, `DETAIL-10` | [#7](https://github.com/NguyenSonTung16/HW03/issues/7) | `DETAIL-04_DETAIL-05_DETAIL-07_DETAIL-10_375px.jpg` |
| 8 | Enter lần đầu ở nút “Thêm vào giỏ” không cho phản hồi quan sát được | `DETAIL-11` | [#8](https://github.com/NguyenSonTung16/HW03/issues/8) | `DETAIL-11_keyboard_activation_no_feedback.jpg` |
| 9 | Trang chi tiết thiếu breadcrumb và thông tin danh mục | `DETAIL-13`, `DETAIL-23` | [#9](https://github.com/NguyenSonTung16/HW03/issues/9) | `DETAIL-04_DETAIL-05_DETAIL-07_DETAIL-10_375px.jpg` |
| 10 | Nhãn tổng giỏ là “Tổng tạm tính”, không đúng “Tổng cộng” | `CART-02` | [#10](https://github.com/NguyenSonTung16/HW03/issues/10) | `CART-02_CART-03_CART-05_375px.jpg` |
| 11 | Trạng thái giỏ trống thiếu biểu tượng trạng thái | `CART-04` | [#11](https://github.com/NguyenSonTung16/HW03/issues/11) | `CART-04_empty_after_deletions.jpg` |
| 12 | Không thể chỉnh số lượng trong giỏ và kiểm tra cập nhật tổng sau chỉnh | `CART-05`, `CART-13` | [#12](https://github.com/NguyenSonTung16/HW03/issues/12) | `CART-13_quantity_two_calculation.jpg` |
| 13 | Xóa mặt hàng không có xác nhận | `CART-06`, `CART-12` | [#13](https://github.com/NguyenSonTung16/HW03/issues/13) | `CART-06_CART-12_after_delete_first.jpg` |
| 14 | Thêm lại sản phẩm đã có tạo thành dòng trùng | `CART-08` | [#14](https://github.com/NguyenSonTung16/HW03/issues/14) | `CART-08_duplicate_product_rows.jpg` |
| 15 | Header không hiển thị số lượng/badge của giỏ | `CART-11` | [#15](https://github.com/NguyenSonTung16/HW03/issues/15) | `CART-02_CART-03_CART-05_375px.jpg` |
| 16 | Có thể mở checkout trực tiếp khi chưa đăng nhập | `CHECKOUT-09` | [#16](https://github.com/NguyenSonTung16/HW03/issues/16) | `CHECKOUT-09_accessible_while_logged_out.jpg` |
| 17 | Tổng tiền checkout có thể sửa trực tiếp | `CHECKOUT-05` | [#17](https://github.com/NguyenSonTung16/HW03/issues/17) | `CHECKOUT-01_populated_order.jpg` |
| 18 | Mã `SAVE10` tính sai giảm giá và tổng sau giảm | `CHECKOUT-13` | [#18](https://github.com/NguyenSonTung16/HW03/issues/18) | `CHECKOUT-13_SAVE10_bad_calculation.jpg` |
| 19 | Giỏ hàng vẫn còn mặt hàng sau khi giao diện báo thanh toán thành công | `CHECKOUT-16` | [#19](https://github.com/NguyenSonTung16/HW03/issues/19) | `CHECKOUT-16_cart_not_cleared.jpg` |

## Ghi chú phạm vi

- Đây là kết quả của một lượt Chrome trên môi trường SUT cô lập, không đại diện cho các nền tảng còn lại.
- `CART-13` không thể chạy hết nhánh chỉnh số lượng bên trong giỏ vì giao diện hiện tại không có điều khiển cập nhật. Bug #12 ghi rõ giới hạn này.
- `CHECKOUT-05` ghi nhận tổng là trường có thể sửa; không sửa dữ liệu SUT trong quá trình lập báo cáo.
- Các issue là báo cáo phát hiện; việc xác minh sửa lỗi sẽ cần lượt kiểm thử lại riêng.
