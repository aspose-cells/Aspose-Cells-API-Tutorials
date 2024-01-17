---
title: Đặt số trang đầu tiên của Excel
linktitle: Đặt số trang đầu tiên của Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách đặt số trang đầu tiên trong Excel bằng Aspose.Cells for .NET.
type: docs
weight: 90
url: /vi/net/excel-page-setup/set-excel-first-page-number/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn cách đặt số trang đầu tiên trong Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ sử dụng mã nguồn C# để minh họa quy trình.

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
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Thao tác này sẽ tạo một sổ làm việc trống có một trang tính.

## Bước 5: Đặt số trang đầu tiên

Đặt số trang đầu tiên của các trang bảng tính bằng mã sau:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Điều này sẽ đặt số trang đầu tiên thành 2.

## Bước 6: Lưu sổ làm việc đã sửa đổi

Lưu sổ làm việc đã sửa đổi bằng mã sau:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Điều này sẽ lưu sổ làm việc đã sửa đổi vào thư mục dữ liệu đã chỉ định.

### Mã nguồn mẫu cho Đặt số trang đầu tiên của Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Đặt số trang đầu tiên của trang bảng tính
worksheet.PageSetup.FirstPageNumber = 2;
// Lưu sổ làm việc.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Phần kết luận

Bây giờ bạn đã học cách đặt số trang đầu tiên trong Excel bằng Aspose.Cells for .NET. Hướng dẫn này hướng dẫn bạn từng bước của quy trình, từ thiết lập môi trường đến đặt số trang đầu tiên. Bây giờ bạn có thể sử dụng kiến thức này để tùy chỉnh việc đánh số trang trong tệp Excel của mình.

### Câu hỏi thường gặp

#### Câu hỏi 1: Tôi có thể đặt số trang đầu tiên khác nhau cho mỗi trang tính không?

 Đ1: Có, bạn có thể đặt số trang đầu tiên khác nhau cho mỗi trang tính bằng cách truy cập vào`FirstPageNumber`thuộc tính của bảng tính tương ứng`PageSetup` sự vật.

#### Câu hỏi 2: Làm cách nào để kiểm tra số trang đầu tiên của bảng tính hiện có?

 Câu trả lời 2: Bạn có thể kiểm tra số trang đầu tiên của bảng tính hiện có bằng cách truy cập vào`FirstPageNumber` tài sản của`PageSetup` đối tượng tương ứng với bảng tính đó.

#### Câu 3: Việc đánh số trang luôn bắt đầu từ 1 theo mặc định phải không?

Câu trả lời 3: Có, việc đánh số trang bắt đầu từ 1 theo mặc định trong Excel. Tuy nhiên, bạn có thể sử dụng mã được hiển thị trong hướng dẫn này để đặt số trang đầu tiên khác.

#### Q4: Những thay đổi đối với số trang đầu tiên có vĩnh viễn trong tệp Excel đã chỉnh sửa không?

A4: Có, những thay đổi được thực hiện đối với số trang đầu tiên sẽ được lưu vĩnh viễn trong tệp Excel đã sửa đổi.

#### Câu hỏi 5: Phương pháp này có áp dụng được với tất cả các định dạng tệp Excel, chẳng hạn như .xls và .xlsx không?

Câu trả lời 5: Có, phương pháp này hoạt động với tất cả các định dạng tệp Excel được Aspose.Cells hỗ trợ, bao gồm .xls và .xlsx.