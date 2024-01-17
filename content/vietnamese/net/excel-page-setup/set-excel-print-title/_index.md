---
title: Đặt tiêu đề in Excel
linktitle: Đặt tiêu đề in Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách dễ dàng thao tác với tệp Excel và tùy chỉnh các tùy chọn in bằng Aspose.Cells cho .NET.
type: docs
weight: 170
url: /vi/net/excel-page-setup/set-excel-print-title/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn cách đặt tiêu đề in trong bảng tính Excel bằng Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để hoàn thành nhiệm vụ này.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã thiết lập môi trường phát triển của mình và cài đặt Aspose.Cells cho .NET. Bạn có thể tải xuống phiên bản mới nhất của thư viện từ trang web chính thức của Aspose.

## Bước 2: Nhập các không gian tên bắt buộc

Trong dự án C# của bạn, hãy nhập các vùng tên cần thiết để hoạt động với Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Bước 3: Thiết lập đường dẫn đến thư mục tài liệu

 Khai báo một`dataDir` biến để chỉ định đường dẫn đến thư mục mà bạn muốn lưu tệp Excel đã tạo:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENT_DIRECTORY"` với đường dẫn chính xác trên hệ thống của bạn.

## Bước 4: Tạo đối tượng sổ làm việc

Khởi tạo một đối tượng Workbook đại diện cho sổ làm việc Excel mà bạn muốn tạo:

```csharp
Workbook workbook = new Workbook();
```

## Bước 5: Truy cập vào bảng tính đầu tiên

Điều hướng đến trang tính đầu tiên trong sổ làm việc Excel bằng mã sau:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Bước 6: Xác định cột tiêu đề

Xác định các cột tiêu đề bằng mã sau:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Ở đây chúng tôi đã xác định cột A và B là cột tiêu đề. Bạn có thể điều chỉnh giá trị này theo nhu cầu của bạn.

## Bước 7: Xác định dòng tiêu đề

Xác định các dòng tiêu đề bằng mã sau:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

Chúng tôi đã xác định hàng 1 và 2 là hàng tiêu đề. Bạn có thể điều chỉnh các giá trị này theo nhu cầu của bạn.

## Bước 8: Lưu sổ làm việc Excel

 Để lưu sổ làm việc Excel với tiêu đề in được xác định, hãy sử dụng`Save` phương thức của đối tượng Workbook:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Thao tác này sẽ lưu sổ làm việc Excel có tên tệp "SetPrintTitle_out.xls" trong thư mục đã chỉ định.

### Mã nguồn mẫu cho Đặt tiêu đề in Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Lấy tham chiếu PageSetup của bảng tính
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Xác định số cột A & B làm cột tiêu đề
pageSetup.PrintTitleColumns = "$A:$B";
// Xác định số hàng 1 & 2 làm hàng tiêu đề
pageSetup.PrintTitleRows = "$1:$2";
// Lưu sổ làm việc.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách đặt tiêu đề in trong bảng tính Excel bằng Aspose.Cells cho .NET. Tiêu đề in cho phép bạn hiển thị các hàng và cột cụ thể trên mỗi trang in, giúp dữ liệu dễ đọc và tham khảo hơn.

### Câu hỏi thường gặp

#### 1. Tôi có thể đặt tiêu đề in cho các cột cụ thể trong Excel không?

 Có, với Aspose.Cells dành cho .NET, bạn có thể đặt các cột cụ thể làm tiêu đề in bằng cách sử dụng`PrintTitleColumns` tài sản của`PageSetup` sự vật.

#### 2. Có thể xác định cả tiêu đề cột và hàng in không?

 Có, bạn có thể đặt cả tiêu đề cột và hàng in bằng cách sử dụng`PrintTitleColumns` Và`PrintTitleRows` thuộc tính của`PageSetup` sự vật.

#### 3. Tôi có thể tùy chỉnh những cài đặt bố cục nào khác với Aspose.Cells cho .NET?

Với Aspose.Cells cho .NET, bạn có thể tùy chỉnh các cài đặt bố cục trang khác nhau, chẳng hạn như lề, hướng trang, tỷ lệ in, v.v.