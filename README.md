# HIS+
* Tải xuống phần mềm tại **[đây](https://github.com/ngocna1409/ehc_public/releases/latest)**.

## Yêu cầu hệ thống
* [**Khung dịch vụ .NET 4.8**](https://go.microsoft.com/fwlink/?LinkId=2085155).
* [**Runtime Visual Studio C++ 2010 Gói dịch vụ 1 MFC**](https://www.microsoft.com/en-US/download/details.aspx?id=26999).
* [**Windows 10/11/Server (2xH2)**](https://www.microsoft.com/en-us/software-download/).

## Khởi tạo môi trường phần mềm

* Tệp `Settings.xml` của bạn và đặt trong thư mục: `%LocalAppData%\Programs\HIS+\Data`.
* Cài đặt tham khảo mục [**Cài đặt .NET Framework**](#cài-đặt-net-framework).

_**Mẹo:** Các chương trình bổ sung có thể tìm thấy tại `%LocalAppData%\Programs\HIS+\Supplementary`._
## Cài đặt .NET Framework

Mặc định **.NET Framework** đã được bật sẵn khi cài đặt Windows xuất xưởng. Nếu chưa được bật, hãy tham khảo các bước sau:

### Cách 1: Mở Qua Giao diện

#### Bước 1: Mở Tính năng Windows
* Cách 1: Chạy lệnh sau ở hộp thoại Chạy/Dòng lệnh (Windows + R): `OptionalFeatures.exe`
* Cách 2: Mở **Bảng điều khiển** > **Chương trình** > **Chương trình & Tính năng** > Chọn **️Bật hoặc tắt tính năng Windows**.
* Cách 3: Mở **Trình quản lý Máy chủ** > **Quản lý** > **Thêm Vai trò và Tính năng** > Tab **Lựa chọn Máy chủ** > *Chọn máy của mình tại **Server Pool*** >  Chọn Tab **Tính năng** > Đánh dấu vào **"Các tính năng .NET Framework 4.8"**.

#### Bước 2: Bật tính năng
* Tìm tính năng và đánh hộp kiểm vào **.NET Framework 4.8 với Dịch vụ nâng cao**.
* Nếu được hỏi, hãy chọn **Để Windows cập nhật tải tệp xuống cho bạn**.
* **Khởi động lại máy**.

#### Bước 3: Chẩn đoán
* Nếu bị kẹt, hãy hoàn tất Windows Cập nhật trước.
* Khởi động lại máy và bật lại. Hoặc tham khảo bật ở cách mở qua dòng lệnh.

### Cách 2: Mở Qua Dòng lệnh
#### Cách 1: Qua Trình Triển khai và Quản lý ảnh đĩa.

`DISM.exe /Online /Enable_Feature /FeatureName:NetFx4*AdvSrvs /All`

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

**Kết quả bạn nên nhận được từ trình đầu cuối:**
```
Path          :
Online        : True
RestartNeeded : False/True
```
_**Quan trọng:** Khởi động lại máy nếu *RestartNeeded* là *true*._
