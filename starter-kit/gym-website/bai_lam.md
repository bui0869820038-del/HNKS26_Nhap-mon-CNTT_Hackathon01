# bai_lam

# BÀI LÀM – HACKATHON 01

- **Mã đề:** 03
- **Họ tên: Bùi Nhật Minh**
- **Lớp: CNTT4**
- **Link repository:**
- **Hệ điều hành (Windows/macOS): Windows**

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```bash
- pwd
- dir -recurse -force
- mv .\lich_tap.txt docs
- mv .\logo_phong_gym.PNG media
- cp .\media\logo_phong_gym.PNG .\backup\
- rm .\temp_103.tmp
- cd .\logs\
- dir 

```

### Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)

```
 Directory: C:\Users\h\OneDrive\Documents\hackathon\starter-kit\gym-website

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/15/2026   7:44 AM                backup
d-----        10/15/2026   7:47 AM                data
d-----        10/15/2026   7:43 AM                docs
d-----        10/15/2026   7:47 AM                logs
d-----        10/15/2026   7:44 AM                media
------        10/12/2026   1:39 AM             68 .env
-a----        10/12/2026   1:39 AM           2224 bai_lam.md
-a----        10/12/2026   1:39 AM             75 lich_tap.txt
-a----        10/12/2026   1:39 AM           6194 logo_phong_gym.PNG
-a----        10/12/2026   1:39 AM           1085 member.log
------        10/12/2026   1:39 AM             22 temp_103.tmp

    Directory: C:\Users\h\OneDrive\Documents\hackathon\starter-kit\gym-website\data

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/12/2026   1:39 AM           6089 dang_ky_thang_11.xlsx

    Directory: C:\Users\h\OneDrive\Documents\hackathon\starter-kit\gym-website\logs

Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
-a----        10/12/2026   1:39 AM           1085 member.log
```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```bash
- sls "error" .\logs\member.log
- gc .\logs\member.log | sls "error" > .\logs\daily_report.txt
- gc .\logs\daily_report.txt

```

### 2 dòng lỗi đầu tiên trong daily_report.txt

```
2025-11-28 07:26:18 [ERROR] Khong tim thay trang /lich-tap (404)
2025-11-28 07:29:18 [ERROR] Het thoi gian cho (timeout)
```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.
> 
- [x]  Heading 1: tên dự án
- [x]  Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [x]  Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [x]  Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [x]  Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [x]  Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)

```bash
- Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
- .\auto_report.ps1
```

### Kết quả hiển thị

```
Dang loc log...
Hoan thanh!
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```bash
 (gc .\logs\member.log | sls "error").coun
```

### Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)

```
7
```

## 4.7. Báo cáo tổng hợp

### Các lệnh đã chạy

```bash
- echo "=== TONG HOP LOG ===" > .\logs\tong_hop.txt
- sls "error" .\logs\member.log >> .\logs\tong_hop.txt
- (sls "error" .\logs\member.log).count >> .\logs\tong_hop.txt

```

### Nội dung file logs/tong_hop.txt

```
=== TONG HOP LOG ===

logs\member.log:7:2025-11-28 07:26:18 [ERROR] Khong tim thay trang /lich-tap (404)
logs\member.log:8:2025-11-28 07:29:18 [ERROR] Het thoi gian cho (timeout)
logs\member.log:9:2025-11-28 07:32:18 [ERROR] Khong tim thay trang /lich-tap (404)
logs\member.log:10:2025-11-28 07:35:18 [ERROR] Het thoi gian cho (timeout)
logs\member.log:11:2025-11-28 07:38:18 [ERROR] Het thoi gian cho (timeout)
logs\member.log:14:2025-11-28 07:47:18 [ERROR] Khong doc duoc the tu hoi vien
logs\member.log:20:2025-11-28 08:05:18 [ERROR] Khong tim thay trang /lich-tap (404)
7
```

## 4.8. Excel

> Phần Excel được chấm trực tiếp trên file `data/dang_ky_thang_11.xlsx`, không cần ghi vào đây.
>