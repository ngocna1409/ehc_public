> Yêu cầu phần mềm:
- Phần mềm bổ trợ: Khung dịch vụ .NET (.NET Framework) 4.6 trở lên.
- Hệ điều hành: Windows 7 với Gói dịch vụ 1 (x86) trở lên.

> Sau khi cài đặt:
- Vui lòng tải xuống cấu hình cho bệnh viện của mình để cài đặt.
- Hoặc tự định nghĩa thông tin máy chủ cơ sở dữ liệu ở lần chạy đầu tiên của ứng dụng.
- Cập nhật ứng dụng, đợi hoàn tất cập nhật và ứng dụng sẵn sàng để chạy.

> Nếu ứng dụng chưa chạy
+ Đối với Windows 7 với Gói dịch vụ 1:
- Cài đặt .NET Framework 4.8.
https://go.microsoft.com/fwlink/?LinkId=2085155
https://dotnet.microsoft.com/en-us/download/dotnet-framework/thank-you/net48-web-installer

+ Đối với Windows 10 (20H2+)
- Vui lòng bật tính năng ".NET Framework 4.8 Advanced Services" tại mục Tìm kiếm Windows, gõ "Bật hoặc tắt tính năng Windows (Turn Windows features on or off)".

+ Dòng lệnh (Yêu cầu quyền quản trị):
Dism /Online /Enable-Feature /FeatureName:NetFx4-AdvSrvs /All

+ Kết quả nhận được:
Deployment Image Servicing and Management tool
Version: xx.x.xxxxx.x

Image Version: xx.x.xxxxx.x

Enabling feature(s)
[==========================100.0%==========================]
The operation completed successfully.