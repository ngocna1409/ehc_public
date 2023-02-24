# ehcHIS
Đây là repo public của chương trình **ehcHIS**. Bạn có thể bắt đầu bằng việc tải xuống tại **[Releases](https://github.com/ngocna1409/ehc_public/releases)** hoặc đọc hướng dẫn tại đây.

## Yêu cầu hệ thống
- [**Khung dịch vụ .NET (.NET Framework)**](https://go.microsoft.com/fwlink/?LinkId=2085155) _phiên bản 4.6 trở lên, ưu tiên 4.8._
- [**Visual Studio C++ 2010 Runtime**](https://www.microsoft.com/en-us/download/details.aspx?id=26999) _(Bản phân phối lại với Gói dịch vụ 1 với Cập nhật bảo mật MFC)._
- **Hệ điều hành Windows 7 với Gói dịch vụ 1** trở lên. Hệ điều hành Windows 7 không có gói dịch vụ sẽ cần **phải** thực hiện việc [_**nâng cấp lên gói dịch vụ 1**_](https://support.microsoft.com/vi-vn/topic/information-about-service-pack-1-for-windows-7-and-for-windows-server-2008-r2-df044624-55b8-3a97-de80-5d99cb689063).

_**Quan trọng:** Để chương trình chạy tốt nhất mà không có lỗi vặt liên quan đến in ấn, hoặc sử dụng đến module ngoài, vui lòng cài đặt **_Visual Studio C++ Runtime 2010_**._

## Sau khi giải nén phần mềm

Vui lòng tải xuống cấu hình của Bệnh viện và đặt trong thư mục: ```%SystemDrive%\ehcHIS\Data\Settings.xml```

Ngoài ra nếu bạn có tệp `ListSettings.xml`, vui lòng cũng đặt tại thư mục `Data` được đề cập ở trên.

Nếu không có những tệp ở trên. Bạn sẽ cần phải đợi ứng dụng khởi động lên và nhập bằng tay chứng danh cơ sở dữ liệu.

Nếu chương trình chưa chạy, cài đặt tham khảo mục [Cài đặt .NET Framework](#tham%20kh%E1%BA%A3o%20m%E1%BB%A5c-,C%C3%A0i%20%C4%91%E1%BA%B7t%20.NET%20Framework,-.).

## Cài đặt .NET Framework

Cài đặt **.NET Framework 4.8** trực tuyến tại [đây](https://go.microsoft.com/fwlink/?LinkId=2085155), chỉ cài đặt nếu bạn đang sử dụng **Windows 7 với Gọi dịch vụ 1**.

Nếu bạn đang gặp vấn đề về **Chứng chỉ** khi cài đặt .NET Framework, vui lòng cập nhật [**Cập nhật chứng chỉ gốc đáng tin cậy Microsoft 2014**](https://support.microsoft.com/vi-vn/topic/support-for-urgent-trusted-root-updates-for-windows-root-certificate-program-in-windows-a4ac4d6c-7c62-3b6e-dfd2-377982bf3ea5).

Nếu bạn là người dùng **Windows 8.0** trở lên, vui lòng xem mục [Bật .NET Framework](#l%C3%B2ng%20xem%20m%E1%BB%A5c-,B%E1%BA%ADt%20.NET%20Framework,-.).

## Bật .NET Framework

Để bật **.NET Framework** trên **_Windows 7_** trở lên, hãy tham khảo các bước sau:

- Mở **Bảng điều khiển** (Control Panel, `control`)
- Chọn **Chương trình** (Programs)
- Chọn  **Chương trình & Tính năng** (Program & Features)
- Chọn **🛡️Bật hoặc tắt tính năng Windows** (Turn Windows features on or off)
- Chấp nhận quyền **Điều khiển Tài khoản Người dùng** (User Account Control).
- Tìm tính năng và đánh hộp kiểm vào **.NET Framework {Số phiên bản} {Ấn bản}**. (Ở đây ta sẽ chọn Phiên bản **4.8 với Dịch vụ nâng cao**, 4.8 Advanced Services)
- Nếu được hỏi, hãy chọn **Để Windows cập nhật tải tệp xuống cho bạn** (Let Windows Update download files for you).
- **Khởi động lại máy**.

**NÂNG CAO:** Ngoài ra, bạn có thể bật tính năng nói trên với dòng lệnh sau với quyền _**quản trị viên**_ 🛡️:

Phiên bản **4.8 với Dịch vụ nâng cao**:
`DISM.exe /Online /Enable-Feature /FeatureName:NetFx4-AdvSrvs /All`

Phiên bản **3.5 (Bao gồm .NET 3.0 và 2.0)**:
`DISM.exe /Online /Enable-Feature /FeatureName:NetFx3 /All`

**Kết quả nhận được từ console:**

```
Deployment Image Servicing and Management tool
Version: xx.x.xxxxx.x

Image Version: xx.x.xxxxx.x

Enabling feature(s)
[==========================100.0%==========================]
The operation completed successfully.
```

_**Quan trọng:** Khởi động lại máy để Windows cập nhật mở tính năng._
