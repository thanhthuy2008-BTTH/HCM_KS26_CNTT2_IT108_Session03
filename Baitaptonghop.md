# (Bài tập tổng hợp) Nhóm SmartCampus Chạy Nước Rút Trước Deadline Nộp Báo Cáo
# Phần 1 – Thiết lập Hybrid Workflow

1. Laptop hỏng ổ cứng có mất file không?

Nếu Auto Sync đã hoàn tất trước khi laptop hỏng thì file vẫn còn trên Cloud. Nếu file chưa kịp đồng bộ thì có thể bị mất bản mới nhất.

2. Ba bước thiết lập Auto Sync

1.  Cài Google Drive for Desktop hoặc OneDrive trên laptop.
    
2.  Chọn thư mục dự án `SmartCampus` để đồng bộ lên Cloud.
    
3.  Bật đồng bộ tự động, kiểm tra trạng thái đã Sync thành công.
    

3. Khôi phục 2 trang bị xóa

Mở file Word → vào File → Info → Version History → chọn phiên bản trước khi xóa → khôi phục.

4. Hai sai lầm khi đồng bộ

-   `node_modules`: Có quá nhiều file nhỏ, làm chậm quá trình đồng bộ. Nên loại trừ và cài lại bằng `npm install`.
    
-   File phim 4K: Chiếm nhiều dung lượng Cloud nhưng không phục vụ dự án. Nên để ngoài thư mục dự án.
    

# Phần 2 – Phân quyền chia sẻ an toàn

### 1. Bảng phân quyền

```
| File | Mức quyền | Phạm vi chia sẻ | Giải thích |
|---|---|---|---|
| BaoCao_CuoiKy_SmartCampus.docx | Viewer | Restricted | Giảng viên chỉ cần xem và chấm bài, tránh sửa nhầm nội dung. |
| Slide_BaoCao.pptx | Editor | Restricted | Cả 5 thành viên được chỉnh sửa để hoàn thành slide đúng hạn. |
| GopY_BanNhap.docx | Commenter | Restricted | Anh khóa trên chỉ cần đọc và góp ý, không sửa trực tiếp file. |
| ThongTin_CaNhan_NhomVien.xlsx | Viewer | Restricted | Hạn chế người truy cập vì file chứa CCCD và số điện thoại. |
```

### 2. Quy tắc Cờ Đỏ Bảo mật

Không kết hợp Anyone with the link + Editor đối với dữ liệu cá nhân. Người có đường link có thể truy cập và chỉnh sửa hoặc xóa dữ liệu, gây rò rỉ thông tin.

### 3. Hai thiết lập trong Settings

-   Tắt quyền Editor thay đổi quyền truy cập và chia sẻ file với người khác.
    
-   Tắt tùy chọn cho người xem và người nhận xét tải xuống, in hoặc sao chép file nếu cần hạn chế phát tán.
    

# Phần 3 – Tổ chức giao tiếp nhóm

### 1. Ba vấn đề trong hội thoại

-   No-Hello: Lan nhắn “có ai rảnh không” nhưng chưa nêu việc cần giúp.
    
-   Spam @all: Trưởng nhóm nhắn lúc 23:47, dễ làm phiền các thành viên.
    
-   Thiếu phân luồng: Tin nhắn công việc lẫn với ảnh mèo và tin nhắn trò chuyện.
    

### 2. Hai Channel nên tạo

-   `#thong-bao`: Deadline, lịch họp và thông báo quan trọng.
    
-   `#du-an-smartcampus`: Trao đổi công việc, cập nhật tiến độ và góp ý sản phẩm.
    

### 3. Viết lại tin nhắn của Lan

> Chào mọi người, mình đang hoàn thiện phần báo cáo SmartCampus và cần góp ý về mục kết quả thử nghiệm. Bạn nào có thể xem giúp mình trước 17h hôm nay thì phản hồi tại đây nhé. Cảm ơn mọi người!

### 4. Tin nhắn Schedule Send lúc 8h sáng

> Chào Nam và Hoa, hiện phần giao diện và nội dung slide vẫn chưa hoàn tất theo tiến độ. Hai bạn cập nhật tình trạng phần việc của mình trước 9h sáng nay để nhóm kịp tổng hợp báo cáo nhé.

Lưu ý: Chỉ tag Nam và Hoa nếu đúng là hai bạn còn thiếu phần việc.

# Phần 4 – Tin nhắn tổng hợp trên `#thong-bao`

``Chào mọi người, mình đã bật Auto Sync cho thư mục dự án SmartCampus và chia sẻ file `BaoCao_CuoiKy_SmartCampus.docx` cho giảng viên với quyền Viewer, phạm vi Restricted. Nam và Hoa vui lòng cập nhật phần việc còn thiếu trước 9h sáng nay để nhóm kịp hoàn thiện báo cáo. Mọi người nhớ kiểm tra trạng thái đồng bộ trước khi tắt máy nhé!``
