---
title: Đặt đầu trang và chân trang Excel
linktitle: Đặt đầu trang và chân trang Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách đặt đầu trang và chân trang trong Excel bằng Aspose.Cells cho .NET.
type: docs
weight: 100
url: /vi/net/excel-page-setup/set-excel-headers-and-footers/
---

Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn từng bước cách đặt đầu trang và chân trang trong Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ sử dụng mã nguồn C# để minh họa quy trình.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Đồng thời tạo một dự án mới trong môi trường phát triển ưa thích của bạn.

## Bước 2: Nhập các thư viện cần thiết

Trong tệp mã của bạn, hãy nhập các thư viện cần thiết để làm việc với Aspose.Cells. Đây là mã tương ứng:

```csharp
using Aspose.Cells;
```

## Bước 3: Đặt thư mục dữ liệu

Đặt thư mục dữ liệu nơi bạn muốn lưu tệp Excel đã sửa đổi. Sử dụng mã sau đây:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Hãy chắc chắn chỉ định đường dẫn thư mục đầy đủ.

## Bước 4: Tạo sổ làm việc và bảng tính

Tạo một đối tượng Workbook mới và điều hướng đến trang tính đầu tiên trong sổ làm việc bằng mã sau:

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

Thao tác này sẽ tạo một sổ làm việc trống có một trang tính và cung cấp quyền truy cập vào đối tượng PageSetup của trang tính đó.

## Bước 5: Đặt tiêu đề

 Đặt tiêu đề bảng tính bằng cách sử dụng`SetHeader` các phương thức của đối tượng PageSetup. Đây là một mã mẫu:

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

Điều này sẽ đặt tên bảng tính, ngày giờ hiện tại và tên tệp tương ứng trong các tiêu đề.

## Bước 6: Xác định footer

 Đặt chân trang bảng tính bằng cách sử dụng`SetFooter` các phương thức của đối tượng PageSetup. Đây là một mã mẫu:

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

Điều này sẽ lần lượt đặt một chuỗi văn bản, số trang hiện tại và tổng số trang ở phần chân trang.

## Bước 7: Lưu sổ làm việc đã sửa đổi

Lưu sổ làm việc đã sửa đổi bằng mã sau:

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

Điều này sẽ lưu sổ làm việc đã sửa đổi vào thư mục dữ liệu đã chỉ định.

### Mã nguồn mẫu cho Đặt đầu trang và chân trang Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook excel = new Workbook();
// Lấy tham chiếu PageSetup của bảng tính
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
// Đặt tên bảng tính ở phần bên trái của tiêu đề
pageSetup.SetHeader(0, "&A");
//Đặt ngày và giờ hiện tại ở phần trung tâm của tiêu đề
// và thay đổi phông chữ của tiêu đề
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
// Đặt tên tệp hiện tại ở phần bên phải của tiêu đề và thay đổi
// phông chữ của tiêu đề
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
// Đặt chuỗi ở phần bên trái của chân trang và thay đổi phông chữ
// của một phần của chuỗi này ("123")
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
// Đặt số trang hiện tại ở phần trung tâm của footer
pageSetup.SetFooter(1, "&P");
// Đặt số trang ở phần bên phải chân trang
pageSetup.SetFooter(2, "&N");
// Lưu sổ làm việc.
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## Phần kết luận

Bây giờ bạn đã học cách đặt đầu trang và chân trang trong Excel bằng Aspose.Cells cho .NET. Hướng dẫn này hướng dẫn bạn từng bước của quy trình, từ thiết lập môi trường đến lưu sổ làm việc đã sửa đổi. Vui lòng khám phá thêm các tính năng của Aspose.Cells để thực hiện các thao tác tiếp theo trong tệp Excel của bạn.

### Câu hỏi thường gặp (FAQ)

#### 1. Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET trên hệ thống của mình?
Để cài đặt Aspose.Cells cho .NET, bạn cần tải xuống gói cài đặt từ trang web chính thức của Aspose và làm theo hướng dẫn được cung cấp trong tài liệu.

#### 2. Phương pháp này có áp dụng được với mọi phiên bản Excel không?
Có, phương pháp đặt đầu trang và chân trang bằng Aspose.Cells cho .NET hoạt động với tất cả các phiên bản Excel được hỗ trợ.

#### 3. Tôi có thể tùy chỉnh thêm đầu trang và chân trang không?
Có, Aspose.Cells cung cấp nhiều tính năng để tùy chỉnh đầu trang và chân trang, bao gồm vị trí văn bản, màu sắc, phông chữ, số trang, v.v.

#### 4. Làm cách nào tôi có thể thêm thông tin động vào đầu trang và chân trang?
Bạn có thể sử dụng các biến đặc biệt và mã định dạng để thêm thông tin động như ngày, giờ hiện tại, tên tệp, số trang, v.v. vào đầu trang và chân trang.

#### 5. Tôi có thể xóa đầu trang và chân trang sau khi cài đặt không?
 Có, bạn có thể xóa đầu trang và chân trang bằng cách sử dụng`ClearHeaderFooter` phương pháp của`PageSetup` sự vật. Điều này sẽ khôi phục các đầu trang và chân trang mặc định.