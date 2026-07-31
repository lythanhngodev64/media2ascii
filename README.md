# ASCII Video Studio

Ứng dụng web chuyển ảnh và video sang ASCII ngay trong trình duyệt, hỗ trợ xem trước theo thời gian thực và xuất kết quả ra PNG, TXT hoặc MP4.

## Tính năng

- Chuyển ảnh hoặc video thành ASCII.
- Xem trước kết quả theo thời gian thực.
- Hỗ trợ nhiều tỷ lệ khung hình:
  - Giữ nguyên bản gốc
  - 1:1
  - 16:9
  - 9:16
- Điều chỉnh:
  - Số cột ASCII
  - Kích thước ký tự
  - Độ sáng
  - Độ tương phản
- Nhiều chế độ màu:
  - Màu sắc
  - Trắng đen
  - Matrix
  - Cyberpunk
- Nhiều bộ ký tự ASCII.
- Xuất ảnh ASCII dưới dạng PNG.
- Xuất nội dung ASCII dưới dạng TXT.
- Xuất toàn bộ video ASCII dưới dạng MP4.
- Có thể giữ âm thanh gốc khi trình duyệt hỗ trợ.
- Tối ưu màu MP4 để gần giống với phần xem trước trên web.
- Giao diện responsive, sử dụng được trên máy tính và thiết bị di động.

## Demo

Sau khi bật GitHub Pages, website sẽ có địa chỉ dạng:

[media2ascii](https://lythanhngodev64.github.io/media2ascii/)

Thay `<github-username>` bằng tên tài khoản GitHub của bạn.

## Cách sử dụng

1. Mở website.
2. Nhấn **Chọn ảnh hoặc video**.
3. Chọn tỷ lệ khung hình, kích thước ký tự và số cột ASCII.
4. Chọn chế độ màu và bộ ký tự.
5. Điều chỉnh độ sáng hoặc độ tương phản khi cần.
6. Chọn định dạng xuất:
   - **Xuất PNG** đối với ảnh ASCII.
   - **Xuất TXT** để lưu nội dung ký tự.
   - **Xuất toàn bộ video MP4** để tạo video ASCII.

Trong lúc xuất video, nên giữ tab đang mở và không để thiết bị chuyển sang chế độ ngủ.

## Chạy trên máy tính

Dự án chỉ gồm một file HTML nên có thể chạy trực tiếp:

1. Tải repository về máy.
2. Mở file `index.html` bằng trình duyệt.

Để tránh một số hạn chế bảo mật của trình duyệt, bạn cũng có thể chạy bằng web server cục bộ.

### Dùng Python

```bash
python -m http.server 8080
```

Sau đó mở:

```text
http://localhost:8080
```

## Quyền riêng tư

Ảnh và video được xử lý trực tiếp trên trình duyệt của người dùng. Ứng dụng không chủ động tải nội dung đã chọn lên máy chủ.

Khi trình duyệt không thể tạo MP4 trực tiếp, ứng dụng có thể tải FFmpeg WebAssembly từ CDN để chuyển đổi video. Thiết bị cần kết nối Internet trong lần tải thư viện này.

## Khả năng tương thích

Nên sử dụng phiên bản mới của:

- Google Chrome
- Microsoft Edge
- Mozilla Firefox
- Safari

Khả năng xuất MP4 trực tiếp, giữ âm thanh và hiệu năng có thể khác nhau tùy trình duyệt và thiết bị.

## Lưu ý về hiệu năng

Video dài, số cột ASCII cao hoặc kích thước ký tự nhỏ có thể làm tăng mức sử dụng CPU và bộ nhớ.

Để xuất video ổn định hơn:

- Đóng bớt các tab không cần thiết.
- Không đặt số cột quá cao trên thiết bị yếu.
- Giữ tab ứng dụng ở trạng thái hoạt động.
- Thử tắt âm thanh nếu quá trình xuất gặp lỗi.
- Dùng Chrome hoặc Edge mới nhất khi có thể.

## Hạn chế hiện tại

- Thời gian xuất MP4 thường gần bằng thời lượng video gốc.
- Một số trình duyệt không cho phép lấy luồng âm thanh từ video.
- Lần đầu chuyển đổi bằng FFmpeg WebAssembly có thể mất thêm thời gian tải.
- Video độ phân giải ASCII rất lớn có thể vượt giới hạn bộ nhớ của trình duyệt.

## Đóng góp

Bạn có thể tạo issue hoặc pull request để:

- Báo lỗi.
- Đề xuất chế độ màu mới.
- Thêm bộ ký tự ASCII.
- Cải thiện hiệu năng xuất MP4.
- Cải thiện giao diện và khả năng tương thích trình duyệt.
