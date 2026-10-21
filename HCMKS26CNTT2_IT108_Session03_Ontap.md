# (Bài Tập Tổng Hợp) Kiến Trúc Hệ Điều Hành & Tư Duy Quản Lý File
## Phần 1 — Kiến trúc Hệ điều hành :
1. ***Theo mục 3a, Máy của bạn đang cùng lúc chạy Word, Chrome, VS Code và phần mềm nộp bài. Hãy cho biết: đây là hoạt động của chức năng nào trong **4 chức năng cốt lõi** của HDH? Vì sao 4 phần mềm này chạy được cùng lúc mà không conflic nhau?***
---> Đây là chức năng quản lý tiến trình và tài nguyên. Hệ điều hành phân chia CPU, RAM và các tài nguyên khác cho Word, Chrome, VS Code và Portal, giúp các phần mềm hoạt động đồng thời mà hạn chế xung đột.
2. ***Khi bạn double-click vào file báo cáo để mở, hành động đó thực chất được xử lý qua lớp nào trước — **Shell** hay **Kernel**? Nêu vai trò của lớp đó và vì sao người dùng thường không tương tác trực tiếp với lớp còn lại.***
---> Khi đúp chuột  vào file báo cáo, thao tác đầu tiên đi qua Shell . Shell tiếp nhận thao tác và yêu cầu hệ điều hành mở file; Kernel quản lý tài nguyên và thực hiện các hoạt động cần thiết. Người dùng sẽ tương tác qua Shell vì Kernel hoạt động ở mức hệ thống, không phải giao diện trực tiếp dành cho người dùng.
## Phần 2 — Cây thư mục & Ổ đĩa :
1.  ***Dựa vào cây thư mục ở mục 3b, hãy xác định:***
-   **Root Directory**:  `D:\`
-  **Parent Directory** trực tiếp của file `anh 1.jpg` :`D:\Nam1\HocKy1\MonHoc\CongNgheThongTin\BaiTapLon\Session02\BaoCaoCuoiKy\Chuong1\Hinh anh`
-   File `anh 1.jpg` đóng vai trò là "cành" hay "lá" trong mô hình cây thư mục : là lá trong cây thư mục vì đây là file
   
2. ***Giả sử toàn bộ dự án đang nằm ở `Desktop` hoặc `Downloads` (thuộc User Profile trên ổ `C:\`). Nêu **2 lý do kỹ thuật** đây là lựa chọn nguy hiểm và đề xuất nơi lưu đúng.***
Trả lời: 
-   Các thư mục này nằm trong User Profile trên ổ `C:\`, có thể bị ảnh hưởng khi dọn dẹp, cài lại Windows.
-   File dự án dễ bị lẫn với file tải về và tài liệu cá nhân, gây khó khăn khi quản lý hoặc sao lưu.
- Đề xuất : Lưu dự án tại `D:\02_Projects\BaiTapLonIT101\`

## Phần 3 — Đường dẫn Path :
1.  ***Viết **Absolute Path** đầy đủ, chính xác của file `anh 1.jpg` trong cây thư mục ở mục 3b.***     
`D:\Nam1\HocKy1\MonHoc\CongNgheThongTin\BaiTapLon\Session02\BaoCaoCuoiKy\Chuong1\Hinh anh\anh 1.jpg`
3.  ***Dựa vào cấu trúc dự án ở mục 3e, hãy viết **Relative Path** để chèn file `logo.png` vào trong file `report.html` (sử dụng đúng ký hiệu `.` hoặc `..` nếu cần). Giải thích ngắn gọn vì sao dùng **Relative Path** ở đây sẽ giúp dự án không bị lỗi khi bạn nén thư mục `BaiTapLonIT101` gửi cho giảng viên qua máy khác.***
`assets/logo.png`
Giải thích : `report.html` nằm ở thư mục gốc `BaiTapLonIT101`, còn `logo.png` nằm trong thư mục con `assets`. Relative Path xác định vị trí file dựa trên thư mục hiện tại nên khi nén và chuyển toàn bộ dự án sang máy khác, đường dẫn vẫn hoạt động nếu giữ nguyên cấu trúc thư mục.
## Phần 4 — Quy tắc Đặt tên chuẩn :
1. Đổi tên file ở mục 3c theo `kebab-case`
Trả lời: `bao-cao-bai-tap-lon-it101-ban-cuoi-v2.docx`
## Phần 5 — Tổ chức & Dọn dẹp Ổ đĩa
1.  Đường dẫn ở mục 3b đang lồng 9 cấp thư mục
2. Vi phạm quy tắc `3 cấp thư mục`  đã được học
3. Hãy thiết kế lại đường dẫn thư mục chứa file `anh 1.jpg` sao cho tuân thủ **Quy tắc 3 Cấp Thư Mục** và mô hình **4 Trụ Cột** (`01_HocTap`, `02_Projects`, `03_Personal`, `04_Media`) trên ổ `D:\`.
Trả lời: `D:\01_HocTap\IT101\HinhAnh\anh-1.jpg`
## Phần 6 — Đuôi file & File ẩn
1.  File ở mục 3d hiển thị là `de-thi-dap-an.pdf` nhưng máy đang ẩn đuôi mở rộng. Hãy giải thích: đây có thể là cạm bẫy gì, tên file thật có khả năng là gì, và thao tác cụ thể nào trong Windows File Explorer giúp bạn phát hiện ra sự thật này **trước khi** nhấp đôi chuột mở file?
Trả lời: 
-Đây có thể là thủ thuật giả mạo phần mở rộng để khiến người dùng tưởng file là PDF an toàn, trong khi thực chất có thể là file thực thi.
Cách kiểm tra:
+ Mở File Explorer.
+  Chọn View → Show → File name extensions.
+  Quan sát lại tên file trong thư mục Downloads trước khi mở.
Nếu phát hiện file có đuôi đáng ngờ như `.exe`, `.bat` hoặc `.scr`, không mở file và nên xóa hoặc quét bằng Windows Security.
