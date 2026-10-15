


BÀI LÀM – HACKATHON 01
Mã đề: 03
Họ tên: Chu Gia Huy
Lớp: CNTT4-K26
Link repository:
Hệ điều hành (Windows/macOS): Windows
4.2. Thao tác máy tính cơ bản bằng CLI
Các lệnh đã chạy
```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng
1.pwd
2.ls
3. Move-Item .\lich_tap.txt .\docs\
		+  Move-Item .\logo_phong_gym.PNG .\media\
4. Copy-Item .\media\logo_phong_gym.PNG .\backup\
5.  rm .\temp_103.tmp
6. cd .\logs\
		+ ls
		+ cd ..
	
```
Kết quả liệt kê toàn bộ dự án (Windows: Get-ChildItem -Recurse -Force; macOS: ls -aR)
```text
PS C:\Users\AD\Downloads\Đề 003 - Phòng tập Gym-20261015T005725Z-1-001\Đề 003 - Phòng tập Gym\starter-kit\starter-kit\gym-website> ls


    Directory: C:\Users\AD\Downloads\Đề 003 - Phòng tập Gym-20261015T005725Z-1-001\Đề 003 - Phòng tập
    Gym\starter-kit\starter-kit\gym-website


Mode                 LastWriteTime         Length Name
----                 -------------         ------ ----
d-----        10/15/2026   8:07 AM                backup
d-----        10/15/2026   8:01 AM                data
d-----        10/15/2026   8:05 AM                docs
d-----        10/15/2026   8:01 AM                logs
d-----        10/15/2026   8:05 AM                media
-a----        10/15/2026   7:57 AM             68 .env
-a----        10/15/2026   7:57 AM           2224 bai_lam.md


PS C:\Users\AD\Downloads\Đề 003 - Phòng tập Gym-20261015T005725Z-1-001\Đề 003 - Phòng tập Gym\starter-kit\starter-kit\gym-website>



```
4.3. Lọc log thủ công
Lệnh đã chạy
```shell
1.  Get-Content .\logs\Member.log | Select-String "ERROR" > .\logs\daily_report.txt

```
2 dòng lỗi đầu tiên trong daily_report.txt
```text
2025-11-28 07:26:18 [ERROR] Khong tim thay trang /lich-tap (404)
2025-11-28 07:29:18 [ERROR] Het thoi gian cho (timeout)

```
4.4. Thao tác với tài liệu Markdown (README.md)
> README.md được chấm trực tiếp trên file `README.md` ở gốc dự án. Đánh dấu `[x]` vào các mục đã làm để tự kiểm tra.
[ X ] Heading 1: tên dự án
[ X ] Mô tả ngắn có cả in đậm và in nghiêng
[ x ] Bảng `Thư mục | Nội dung`, ít nhất 3 dòng dữ liệu
[ x ] Code block chứa lệnh PowerShell/Terminal liệt kê nội dung dự án
[ x ] Task list ít nhất 2 công việc, có ít nhất 1 mục đã hoàn thành
[ x ] Blockquote nhắc không upload `.env`

4.5. Chạy script auto_report (.ps1 hoặc .sh)
Lệnh chạy (Windows: nếu dùng Phụ lục 2 thì ghi cả 2 lệnh)
```shell
# # Script: auto_report.ps1
# Tac gia: Chu Gia Huy
# Ngay tao: 15/10/2026

Write-Host "Dang loc log ... "

"=== BAO CAO LOI === ">HOAN_THIEN
Get-Content .\logs\member.log | Select-String "ERROR">> .\log\auto_report.txt

Write-Host "Hoan thanh!"

```
Kết quả hiển thị
```text
(Dán kết quả vào đây – xoá dòng này)

```
4.6. Đếm số dòng lỗi
Lệnh
```shell
 (Get-Content .\logs\Member.log | Select-String "ERROR" ).count

```
Kết quả đếm (Windows: giá trị Count; macOS: con số in ra)
```text
7

```
4.7. Báo cáo tổng hợp
Các lệnh đã chạy
```shell
# Ghi lần lượt các lệnh đã chạy, mỗi lệnh một dòng (xoá dòng này)

```
Nội dung file logs/tong_hop.txt
```text
(Dán kết quả vào đây – xoá dòng này)

```
4.8. Excel
> Phần Excel được chấm trực tiếp trên file `data/dang_ky_thang_11.xlsx`, không cần ghi vào đây.
