# WebGIS Long Phú — 14 ấp

Website WebGIS tĩnh dùng Leaflet + OpenStreetMap + Chart.js, phù hợp triển khai bằng GitHub Pages.

## Tính năng
- Bản đồ ranh giới 14 ấp từ KMZ.
- Kết hợp dữ liệu diện tích, số hộ, dân số từ Excel.
- Tô màu chuyên đề theo dân số, số hộ, diện tích, mật độ.
- Tìm kiếm tên ấp, nhấp vùng để xem chi tiết.
- Biểu đồ so sánh, bảng thống kê, xuất CSV mở bằng Excel, tải GeoJSON.
- In trang / lưu thành PDF bằng hộp thoại in của trình duyệt.

## Cấu trúc
- `index.html`: giao diện và chức năng WebGIS.
- `data/ranh_14_ap.geojson`: ranh giới đã chuyển đổi từ KMZ và ghép số liệu thống kê.
- `data/thong_ke.json`: dữ liệu thống kê tóm tắt.

## Triển khai GitHub Pages
1. Đăng nhập GitHub và tạo repository mới, ví dụ `webgis-long-phu`. Chọn Public nếu muốn trang web công khai.
2. Giải nén gói ZIP trên máy tính. Mở repository vừa tạo, chọn **Add file → Upload files**.
3. Tải lên `index.html` và cả thư mục `data` (bao gồm hai tệp JSON). Giữ đúng cấu trúc thư mục. Có thể tải toàn bộ nội dung đã giải nén bằng cách kéo thả các tệp/thư mục vào trang upload.
4. Chọn **Commit changes**.
5. Vào **Settings → Pages**. Trong **Build and deployment**, chọn **Deploy from a branch**; branch `main`, folder `/(root)`, rồi **Save**.
6. Chờ GitHub Pages hoàn tất. Địa chỉ thường có dạng `https://TEN-TAI-KHOAN.github.io/webgis-long-phu/`. Mở link do GitHub hiển thị trong Settings → Pages.
7. Nếu cập nhật dữ liệu, thay `data/ranh_14_ap.geojson` và/hoặc `data/thong_ke.json` rồi commit lại.

## Kiểm tra trước khi công bố
- Mở website và xác nhận 14 vùng được hiển thị, tổng diện tích 76,77 km², 8.879 hộ và 39.920 người.
- Thử tìm kiếm một ấp, đổi chỉ tiêu tô màu, nhấp vùng, xuất CSV và in/lưu PDF.
- Bản đồ nền và thư viện JavaScript cần Internet. Dữ liệu ranh giới/thống kê nằm trong repository công khai nếu repository Public; không tải dữ liệu nhạy cảm lên.
- Đây là website tĩnh, chưa có đăng nhập, phân quyền hay chức năng chỉnh sửa dữ liệu trực tiếp.

## Nguồn và lưu ý dữ liệu
Ranh giới lấy từ `Cac ap sau nhap.kmz`; thống kê lấy từ `thong_ke_14_ap_long_phu.xlsx`. Mật độ = dân số / diện tích; người/hộ = dân số / số hộ. Vui lòng xác minh số liệu và ranh giới trước khi dùng trong hồ sơ chính thức.
