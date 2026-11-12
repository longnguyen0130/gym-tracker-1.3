# Gym Tracker PWA

Ứng dụng theo dõi tập luyện chạy trên trình duyệt, tối ưu cho iPhone. Có thể thêm vào màn hình chính như một app.

## Chạy thử trên Windows
1. Giải nén thư mục.
2. Mở PowerShell tại thư mục này.
3. Chạy `py -m http.server 8000`.
4. Trên máy tính mở `http://localhost:8000`.
5. Để mở trên iPhone cùng Wi-Fi: tìm IPv4 của máy Windows bằng `ipconfig`, sau đó mở `http://IP-MAY-TINH:8000` trên Safari.

## Cài lên màn hình chính iPhone
Để PWA cài đặt ổn định và Service Worker hoạt động, website cần được host bằng HTTPS (ví dụ GitHub Pages hoặc Netlify).
1. Đưa các file trong thư mục lên một repository GitHub.
2. Bật GitHub Pages trong Settings > Pages.
3. Mở URL HTTPS trên Safari iPhone.
4. Chọn Share > Add to Home Screen > Add.

## Tính năng
- Tạo buổi tập, thêm bài tập và ghi set/kg/rep/RIR.
- Lưu lịch sử trong localStorage của trình duyệt.
- Tính volume (kg × reps), thống kê tuần, PR và Estimated 1RM theo công thức Epley.
- Thư viện mở rộng 317 bài tập thuộc 10 vùng cơ thể, phân loại thành các nhóm cơ nhỏ hơn; có tìm kiếm theo tên, cơ mục tiêu và thiết bị.
- Trang chi tiết có ảnh minh họa, video MP4 phát trực tiếp, hướng dẫn từng bước, gợi ý kỹ thuật và lỗi thường gặp khi nguồn dữ liệu cung cấp.
- Thư viện bài tập được lưu cache trên thiết bị sau lần tải đầu để hạn chế gọi API lặp lại.
- Đồng hồ nghỉ giữa set: chọn 30–300 giây, bắt đầu/tạm dừng/đặt lại; tự chạy khi đánh dấu set hoàn thành.
- Biểu đồ volume tuần và tiến bộ theo bài.
- Light/Dark mode, xuất/nhập JSON để sao lưu.

## Lưu ý
- Dữ liệu lưu trên chính trình duyệt/thiết bị, không tự đồng bộ giữa máy tính và iPhone.
- Xuất file JSON định kỳ để sao lưu.
- Đây là bản MVP; không thay thế ứng dụng native và chưa có tài khoản/cloud sync.


## Nguồn ảnh và video
- Danh mục mở rộng và metadata/video lấy từ [Free Exercise DB with Videos](https://github.com/harshvishu/free-exercise-db-with-videos), công bố theo giấy phép MIT. Dữ liệu nguồn mô tả 317 bài tập và 593 video demo MP4.
- Ứng dụng tải danh mục từ API công khai ở lần đầu và lưu cache trên thiết bị. Vì vậy, cần kết nối Internet trong lần tải đầu; video/ảnh cũng cần Internet để phát/tải. API demo có thể thay đổi hoặc giới hạn truy cập; nếu không truy cập được, ứng dụng vẫn hiển thị danh sách bài tập dự phòng.
- Không thể liệt kê mọi biến thể bài tập tồn tại trên thế giới; đây là thư viện lớn theo bộ dữ liệu được nêu, bao phủ nhiều vùng cơ và loại thiết bị.
