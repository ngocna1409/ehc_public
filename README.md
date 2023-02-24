# Yêu cầu phần mềm
- **Khung dịch vụ .NET (.NET Framework)** _phiên bản 4.6 trở lên._
- **Visual Studio C++ 2010 Runtime** _(Bản phân phối lại)._
- **Hệ điều hành Windows 7 với Gói dịch vụ 1** trở lên. Hệ điều hành Windows 7 không có gói dịch vụ sẽ cần **phải** thực hiện việc [_**nâng cấp lên gói dịch vụ 1**_](https://support.microsoft.com/vi-vn/topic/information-about-service-pack-1-for-windows-7-and-for-windows-server-2008-r2-df044624-55b8-3a97-de80-5d99cb689063).

# Sau khi giải nén phần mềm

Vui lòng tải xuống cấu hình của Bệnh viện và đặt trong thư mục: ```%SystemDrive%\ehcHIS\Data\Settings.xml```

Ngoài ra nếu bạn có tệp `ListSettings.xml`, vui lòng cũng đặt tại thư mục `Data` được đề cập ở trên.

Nếu không có những tệp ở trên. Bạn sẽ cần phải đợi ứng dụng khởi động lên và nhập bằng tay chứng danh cơ sở dữ liệu.

Nếu chương trình chưa chạy, hãy tham khảo mục [Cài đặt .NET Framework](#tham%20kh%E1%BA%A3o%20m%E1%BB%A5c-,C%C3%A0i%20%C4%91%E1%BA%B7t%20.NET%20Framework,-.).

## Cài đặt .NET Framework

Cài đặt **.NET Framework 4.8** trực tuyến tại [đây](https://go.microsoft.com/fwlink/?LinkId=2085155), chỉ cài đặt nếu bạn đang sử dụng **Windows 7 với Gọi dịch vụ 1**.

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
Phiên bản **3.5**:
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
