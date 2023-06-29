Web project using ASP.NET and SQL Server to manage items

Tài liệu hướng dẫn triển khai web thời trang online
- Sau khi tải về file dưới dạng rar, giải nén 

- Vào trong thư mục “WebBanHangOnline”, mở file ‘WebBanHangOnline.sln’ bằng Visual Studio Code

- Dự án web sử dụng Migration tạo database, các bước sau sẽ hướng dẫn cách tạo migration cho dự án:

Bước 1: Xoá folder Migration có sẵn trong dự án
Bước 2: Vào web.config cấu hình lại kết nối

Sửa kết nối ở DataSource, thay bằng kết nối của máy tính admin

Bước 3: Vào Package Manager Console

Nhập ‘Enable-Migrations’  Migration sẽ tự tạo folder và configuration

Tiếp theo nhập ‘Add-migration (tên tuỳ chọn)’. Ví dụ: Add-database CreateDatabase

Cuối cùng là ‘Update-database’ hoặc ‘Update-database -verbose’ tuỳ máy nhận

Bắt đầu chạy dự án lên

Thanh menu của dự án được nạp vào từ dữ liệu database quản lý bằng trang Admin

Vì vậy, admin cần vào localhost:xxxx/Admin/Home để quản lý thanh menu trước tiên

Thứ tự mặc định của thanh menu nhóm đang thực hiện cần được thêm vào lần lượt là: Trang chủ  Sản phẩm  Giới thiệu

Sau đó Admin vào mục Cấp quyền  Thêm mới để cấu hình phân quyền

Sau khi cấu hình xong, đã có tài khoản admin, quay lại code. Vào ~/Area/Controller, 

có 3 controller sau cần thay đổi để bắt đầu sử dụng.

Ở mỗi controller đều có một [Authorize] đang được comment, bỏ comment các dòng này để bắt đầu phân quyền

Vậy là đã xong tất cả bước để triển khai dự án, sau khi hoàn thành, admin có thể tạo tài khoản cho nhân viên,
dùng các chức năng như thêm thanh menu, thêm danh mục sản phẩm, sản phẩm,…