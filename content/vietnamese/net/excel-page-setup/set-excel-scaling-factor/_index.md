---
title: Đặt hệ số tỷ lệ Excel
linktitle: Đặt hệ số tỷ lệ Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách dễ dàng thao tác với tệp Excel và tùy chỉnh hệ số tỷ lệ bằng Aspose.Cells cho .NET.
type: docs
weight: 180
url: /vi/net/excel-page-setup/set-excel-scaling-factor/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn cách đặt hệ số tỷ lệ trong bảng tính Excel bằng Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để hoàn thành nhiệm vụ này.

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

## Bước 6: Đặt hệ số tỷ lệ

Đặt hệ số tỷ lệ bằng mã sau:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Ở đây chúng tôi đã đặt hệ số tỷ lệ thành 100, nghĩa là bảng tính sẽ được hiển thị ở kích thước 100% bình thường khi được in.

## Bước 7: Lưu sổ làm việc Excel

 Để lưu sổ làm việc Excel với hệ số tỷ lệ đã xác định, hãy sử dụng`Save` phương thức của đối tượng Workbook:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Thao tác này sẽ lưu sổ làm việc Excel có tên tệp "ScalingFactor_out.xls" trong thư mục đã chỉ định.

### Mã nguồn mẫu cho Đặt hệ số tỷ lệ Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Đặt hệ số tỷ lệ thành 100
worksheet.PageSetup.Zoom = 100;
// Lưu sổ làm việc.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách đặt hệ số tỷ lệ trong bảng tính Excel bằng Aspose.Cells cho .NET. Hệ số chia tỷ lệ cho phép bạn điều chỉnh kích thước của bảng tính khi in để hiển thị tối ưu.

### Câu hỏi thường gặp

#### 1. Làm cách nào để đặt hệ số tỷ lệ trong bảng tính Excel bằng Aspose.Cells cho .NET?

 Sử dụng`Zoom` tài sản của`PageSetup`đối tượng để thiết lập hệ số tỷ lệ. Ví dụ,`worksheet.PageSetup.Zoom = 100;` sẽ đặt hệ số tỷ lệ thành 100%.

#### 2. Tôi có thể tùy chỉnh hệ số tỷ lệ theo nhu cầu của mình không?

 Có, bạn có thể điều chỉnh hệ số tỷ lệ bằng cách thay đổi giá trị được gán cho`Zoom` tài sản. Ví dụ,`worksheet.PageSetup.Zoom = 75;` sẽ đặt hệ số tỷ lệ thành 75%.

#### 3. Có thể lưu sổ làm việc Excel với hệ số tỷ lệ đã xác định không?

 Có, bạn có thể sử dụng`Save` phương pháp của`Workbook` đối tượng để lưu sổ làm việc Excel với hệ số tỷ lệ được xác định.