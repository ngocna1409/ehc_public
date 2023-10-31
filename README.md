# ehcHIS
* Tải xuống phần mềm tại **[đây](https://github.com/ngocna1409/ehc_public/releases/latest)**.

## Yêu cầu hệ thống
* [**Khung dịch vụ .NET (.NET Framework)**](https://go.microsoft.com/fwlink/?LinkId=2085155) phiên bản *4.8*.
* [**Visual Studio C++ 2010 Runtime**](https://www.microsoft.com/en-US/download/details.aspx?id=26999) (Bản phân phối lại với Gói dịch vụ 1 với Cập nhật bảo mật MFC).
* **Hệ điều hành Windows 7 với [Gói dịch vụ 1](https://support.microsoft.com/vi-vn/windows/c%C3%A0i-%C4%91%E1%BA%B7t-windows-7-g%C3%B3i-d%E1%BB%8Bch-v%E1%BB%A5-1-sp1-b3da2c0f-cdb6-0572-8596-bab972897f61)/Windows Server 2008 R2 với [Gói dịch vụ 1](https://www.catalog.update.microsoft.com/Search.aspx?q=KB976932)** trở lên. Nếu chưa có, [**nâng cấp lên gói dịch vụ 1**](https://support.microsoft.com/vi-vn/topic/th%C3%B4ng-tin-v%E1%BB%81-g%C3%B3i-d%E1%BB%8Bch-v%E1%BB%A5-1-d%C3%A0nh-cho-windows-7-v%C3%A0-d%C3%A0nh-cho-windows-server-2008-r2-df044624-55b8-3a97-de80-5d99cb689063).

## Khởi tạo môi trường phần mềm

* Vui lòng tải xuống 1 trong 2 tệp `ListSettings.xml` và `Settings.xml` của bạn và đặt trong thư mục: `%LocalAppData%\Programs\ehcHIS\Data`.
* Nếu không có những tệp ở trên. Bạn sẽ cần phải đợi ứng dụng khởi động lên và nhập bằng tay chứng danh cơ sở dữ liệu.
* Nếu chương trình chưa chạy, cài đặt tham khảo mục [Cài đặt .NET Framework](#cài-đặt-net-framework).

## Cài đặt .NET Framework

* Cài đặt **.NET Framework 4.8** tại [đây](https://go.microsoft.com/fwlink/?LinkId=2085155) (Trực tuyến) và [đây](https://go.microsoft.com/fwlink/?linkid=2088631) (Ngoại tuyến), chỉ cài đặt nếu bạn đang sử dụng **Windows 7 (Gói Dịch vụ 1), Windows 8.1 với Cập nhật 1 trở lên, Windows 10 (1607 - 1809)**. Tìm hiểu thêm tại [đây](https://support.microsoft.com/vi-vn/topic/microsoft-net-framework-4-8-gi%C3%A1n-tuy%E1%BA%BFn-c%C3%A0i-%C4%91%E1%BA%B7t-cho-windows-9d23f658-3b97-68ab-d013-aa3c3e7495e0).
* Nếu bạn đang gặp vấn đề về chứng chỉ khi cài đặt .NET Framework, vui lòng cập nhật [**Chứng chỉ gốc đáng tin cậy Microsoft 2014**](https://support.microsoft.com/vi-vn/topic/h%E1%BB%97-tr%E1%BB%A3-kh%E1%BA%A9n-c%E1%BA%A5p-g%E1%BB%91c-tin-c%E1%BA%ADy-c%E1%BA%ADp-nh%E1%BA%ADt-ch%C6%B0%C6%A1ng-tr%C3%ACnh-ch%E1%BB%A9ng-ch%E1%BB%89-g%E1%BB%91c-windows-trong-windows-a4ac4d6c-7c62-3b6e-dfd2-377982bf3ea5).
* Tham khảo mục [Bật .NET Framework](#bật-net-framework) nếu bạn sử dụng **Windows 10 (1903)** trở lên.

## Bật .NET Framework

Để bật **.NET Framework** hãy tham khảo các bước sau:

### Mở Tính năng Tùy chọn (Giao diện)

#### Cách 1: Chạy lệnh sau ở hộp thoại Chạy/Dòng lệnh (Windows + R):
`OptionalFeatures.exe`

#### Cách 2: Mở qua Bảng điều khiển cũ (Control Panel)
* Mở **Bảng điều khiển** (Control Panel, `control`)
* Chọn **Chương trình** (Programs)
* Chọn  **Chương trình & Tính năng** (Program & Features)
* Chọn **️Bật hoặc tắt tính năng Windows** (Turn Windows features on or off)

#### Bật tính năng
* Chấp nhận quyền **Điều khiển Tài khoản Người dùng** (User Account Control).
* Tìm tính năng và đánh hộp kiểm vào **.NET Framework {Số phiên bản} {Ấn bản}**.
* Chọn phiên bản: Ví dụ **4.8 với Dịch vụ nâng cao** (4.8 Advanced Services)
* Nếu được hỏi, hãy chọn **Để Windows cập nhật tải tệp xuống cho bạn** (Let Windows Update download files for you).
* **Khởi động lại máy**.

### Mở Tính năng Tùy chọn (Dòng lệnh)
#### Cách 1: Qua Dấu nhắc lệnh (Command Prompt)

Phiên bản **4.8 với Dịch vụ nâng cao** (Windows 10.x):
`DISM.exe /Online /Enable_Feature /FeatureName:NetFx4*AdvSrvs /All`

Phiên bản **4.0** (Windows 8.x):
`DISM.exe /Online /Enable_Feature /FeatureName:NetFx4 /All`

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
_**Quan trọng:** Khởi động lại máy._

#### Cách 2: Qua Windows PowerShell (Không qua PowerShell Core)

Phiên bản **4.8 với Dịch vụ nâng cao** (Windows 10.x):
`Enable-WindowsOptionalFeature -Online -FeatureName "NetFx4-AdvSrvs"`

Phiên bản **4.0** (Windows 8.x):
`Enable-WindowsOptionalFeature -Online -FeatureName "NetFx4"`

Phiên bản **3.5 (Bao gồm .NET 3.0 và 2.0)**:
`Enable-WindowsOptionalFeature -Online -FeatureName "NetFx3"`

**Kết quả bạn nên nhận được từ trình đầu cuối:**
```
Path          :
Online        : True
RestartNeeded : False/True
```
_**Quan trọng:** Khởi động lại máy nếu *RestartNeeded* là *true*._
