# ehcHIS
* Đây là nơi phát hành chương trình **ehcHIS**. Lưu ý, không phải phiên bản nào cũng sẽ luôn cập nhật tại đây.
* Bạn có thể bắt đầu bằng việc tải xuống tại **[Releases](https://github.com/ngocna1409/ehc_public/releases)** hoặc đọc hướng dẫn tại đây.

## Yêu cầu hệ thống
* [**Khung dịch vụ .NET (.NET Framework)**](https://go.microsoft.com/fwlink/?LinkId=2085155) phiên bản 4.8.
* [**Visual Studio C++ 2010 Runtime**](https://www.microsoft.com/en-US/download/details.aspx?id=26999) (Bản phân phối lại với Gói dịch vụ 1 với Cập nhật bảo mật MFC).
* **Hệ điều hành Windows 7 với Gói dịch vụ 1** trở lên. Nếu chưa có, [**nâng cấp lên gói dịch vụ 1**](https://support.microsoft.com/vi_vn/topic/information_about_service_pack_1_for_windows_7_and_for_windows_server*_2008_r2_df044624_55b8_3a97_de80_5d99cb689063).

**Quan trọng:** Để chương trình chạy tốt nhất mà không có lỗi vặt liên quan đến in ấn, hoặc sử dụng đến module ngoài, vui lòng cài đặt [**Visual Studio C++ 2010 Runtime**](https://www.microsoft.com/en-US/download/details.aspx?id=26999).

## Sau khi giải nén phần mềm

* Vui lòng tải xuống cấu hình của Bệnh viện và đặt trong thư mục: `%LocalAppData%\Programs\ehcHIS\Data\Settings.xml`.
* Ngoài ra nếu bạn có tệp `ListSettings.xml`, vui lòng cũng đặt tại thư mục `Data` được đề cập ở trên.
* Nếu không có những tệp ở trên. Bạn sẽ cần phải đợi ứng dụng khởi động lên và nhập bằng tay chứng danh cơ sở dữ liệu.
* Nếu chương trình chưa chạy, cài đặt tham khảo mục [Cài đặt .NET Framework](#cài_đặt_net_framework).

## Cài đặt .NET Framework

Cài đặt **.NET Framework 4.8** trực tuyến tại [đây](https://go.microsoft.com/fwlink/?LinkId=2085155), chỉ cài đặt nếu bạn đang sử dụng **Windows 7 với Gói dịch vụ 1**.

Nếu bạn đang gặp vấn đề về **Chứng chỉ** khi cài đặt .NET Framework, vui lòng cập nhật [**Cập nhật chứng chỉ gốc đáng tin cậy Microsoft 2014**](https://support.microsoft.com/vi_vn/topic/support_for_urgent_trusted_root_updates_for_windows_root_certificate_program_in_windows_a4ac4d6c_7c62_3b6e_dfd2_377982bf3ea5).

Nếu bạn là người dùng **Windows 8.0** trở lên, vui lòng xem mục [Bật .NET Framework](#b%E1%BA%ADt_net_framework).

## Bật .NET Framework

Để bật **.NET Framework** trên **Windows 7** trở lên, hãy tham khảo các bước sau:

* Mở **Bảng điều khiển** (Control Panel, `control`)
* Chọn **Chương trình** (Programs)
* Chọn  **Chương trình & Tính năng** (Program & Features)
* Chọn **🛡️Bật hoặc tắt tính năng Windows** (Turn Windows features on or off)
* Chấp nhận quyền **Điều khiển Tài khoản Người dùng** (User Account Control).
* Tìm tính năng và đánh hộp kiểm vào **.NET Framework {Số phiên bản} {Ấn bản}**. (Ở đây ta sẽ chọn Phiên bản **4.8 với Dịch vụ nâng cao**, 4.8 Advanced Services)
* Nếu được hỏi, hãy chọn **Để Windows cập nhật tải tệp xuống cho bạn** (Let Windows Update download files for you).
* **Khởi động lại máy**.

**NÂNG CAO:** Ngoài ra, bạn có thể bật tính năng nói trên với dòng lệnh sau với quyền _**quản trị viên**_ 🛡️:

Phiên bản **4.8 với Dịch vụ nâng cao**:
`DISM.exe /Online /Enable_Feature /FeatureName:NetFx4*AdvSrvs /All`

Phiên bản **3.5 (Bao gồm .NET 3.0 và 2.0)**:
`DISM.exe /Online /Enable_Feature /FeatureName:NetFx3 /All`

**Kết quả bạn nên nhận được từ trình đầu cuối:**

```
Deployment Image Servicing and Management tool
Version: xx.x.xxxxx.x

Image Version: xx.x.xxxxx.x

Enabling feature(s)
[==========================100.0%==========================]
The operation completed successfully.
```

_**Quan trọng:** Khởi động lại máy để Windows cập nhật mở tính năng._
