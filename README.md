# CNTT1-nh-p-m-n-c-ng-ngh-th-ng-tin-Hackathon01
# BÀI LÀM – HACKATHON 01

- **Mã đề:** 13
- **Họ tên:** Đoàn Bảo Duy
- **Lớp:** CNTT1
- **Link repository:** Chưa có URL repository (bản làm việc: `C:\Users\ASUS\Downloads\starter-kit\starter-kit\Ngoai Ngu Website FINAL`)
- **Hệ điều hành (Windows/macOS):** Windows

## 4.2. Thao tác máy tính cơ bản bằng CLI

### Các lệnh đã chạy

```powershell
$root = 'C:\Users\ASUS\Downloads\starter-kit\starter-kit\Ngoai Ngu Website FINAL'
Move-Item -LiteralPath (Join-Path $root 'Thoi Khoa Bieu.txt') -Destination $docs
Move-Item -LiteralPath (Join-Path $root 'Logo Trung Tam Ngoai Ngu.PNG') -Destination $media
Get-ChildItem -Recurse -File -Force $root
```

### Kết quả liệt kê toàn bộ dự án

```text
(Dán kết quả vào đây – xoá dòng này)

```

## 4.3. Lọc log thủ công

### Lệnh đã chạy

```powershell
Test-Path (Join-Path $root 'daily_report.txt')
Select-String -Path (Join-Path $root 'Course.log') -Pattern '\[ERROR\]' | Select-Object -First 2
```

### 2 dòng lỗi đầu tiên

```text
daily_report.txt không có trong bộ starter-kit. Hai dòng đầu dưới đây lấy từ file log sẵn có Course.log:
2026-03-28 08:24:28 [ERROR] Het thoi gian cho (timeout)
2026-03-28 08:30:28 [ERROR] Het thoi gian cho (timeout)
```

## 4.4. Thao tác với tài liệu Markdown (README.md)

> README.md chưa có trong bộ starter-kit nên các mục dưới đây chưa được xác nhận.

- [ ] Heading 1: tên dự án
- [ ] Mô tả ngắn có cả **in đậm** và *in nghiêng*
- [ ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
- [ ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
- [ ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
- [ ] Blockquote nhắc không upload `.env`

## 4.5. Chạy script auto_report (.ps1 hoặc .sh)

### Lệnh kiểm tra

```powershell
Test-Path (Join-Path $root 'auto_report.ps1')
```

### Kết quả

```text
False — không có script auto_report.ps1 hoặc auto_report.sh trong starter-kit nên chưa chạy được.
```

## 4.6. Đếm số dòng lỗi

### Lệnh

```powershell
(Select-String -Path (Join-Path $root 'Course.log') -Pattern '\[ERROR\]').Count
```

### Kết quả đếm

```text
6
```

## 4.7. Báo cáo tổng hợp

### Kiểm tra file đầu ra

```powershell
Test-Path (Join-Path $root 'logs\tong_hop.txt')
```

### Nội dung file logs/tong_hop.txt

```text
Chưa có file logs\tong_hop.txt hoặc thư mục logs trong starter-kit nên chưa thể ghi nội dung báo cáo.
```
