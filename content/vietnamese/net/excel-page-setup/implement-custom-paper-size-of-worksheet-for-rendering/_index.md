---
title: Triển khai khổ giấy tùy chỉnh của bảng tính để hiển thị
linktitle: Triển khai khổ giấy tùy chỉnh của bảng tính để hiển thị
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hướng dẫn từng bước để triển khai kích thước bảng tính tùy chỉnh với Aspose.Cells cho .NET. Đặt kích thước, thêm tin nhắn và lưu dưới dạng PDF.
type: docs
weight: 50
url: /vi/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
Việc triển khai kích thước tùy chỉnh cho trang tính của bạn có thể rất hữu ích khi bạn muốn tạo tài liệu PDF có kích thước cụ thể. Trong hướng dẫn này, chúng ta sẽ tìm hiểu cách sử dụng Aspose.Cells cho .NET để đặt kích thước tùy chỉnh cho trang tính và sau đó lưu tài liệu dưới dạng PDF.

## Bước 1: Tạo thư mục đầu ra

Trước khi bắt đầu, bạn cần tạo một thư mục đầu ra để lưu tệp PDF đã tạo. Bạn có thể sử dụng bất kỳ đường dẫn nào bạn muốn cho thư mục đầu ra của mình.

```csharp
// Thư mục đầu ra
string outputDir = "YOUR_OUTPUT_FOLDER";
```

Đảm bảo bạn chỉ định đường dẫn chính xác đến thư mục đầu ra của mình.

## Bước 2: Tạo đối tượng Workbook

Để bắt đầu, bạn cần tạo một đối tượng Workbook bằng Aspose.Cells. Đối tượng này đại diện cho bảng tính của bạn.

```csharp
// Tạo đối tượng Workbook
Workbook wb = new Workbook();
```

## Bước 3: Truy cập vào bảng tính đầu tiên

Sau khi tạo đối tượng Workbook, bạn có thể truy cập trang tính đầu tiên bên trong nó.

```csharp
// Truy cập vào bảng tính đầu tiên
Worksheet ws = wb.Worksheets[0];
```

## Bước 4: Đặt kích thước trang tính tùy chỉnh

 Bây giờ bạn có thể đặt kích thước trang tính tùy chỉnh bằng cách sử dụng`CustomPaperSize(width, height)` phương thức của lớp PageSetup.

```csharp
// Đặt kích thước trang tính tùy chỉnh (tính bằng inch)
ws.PageSetup.CustomPaperSize(6, 4);
```

Trong ví dụ này, chúng tôi đã đặt kích thước trang tính là rộng 6 inch và cao 4 inch.

## Bước 5: Truy cập vào ô B4

Sau đó, chúng ta có thể truy cập vào một ô cụ thể trong bảng tính. Trong trường hợp này, chúng ta sẽ truy cập vào ô B4.

```csharp
// Truy cập vào ô B4
Cell b4 = ws.Cells["B4"];
```

## Bước 6: Thêm tin nhắn vào ô B4

 Bây giờ chúng ta có thể thêm tin nhắn vào ô B4 bằng cách sử dụng`PutValue(value)` phương pháp.

```csharp
// Thêm tin nhắn vào ô B4
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

Trong ví dụ này, chúng tôi đã thêm thông báo "Kích thước trang PDF: 6,00" x 4,00" vào ô B4.

## Bước 7: Lưu bảng tính ở định dạng PDF

 Cuối cùng, chúng ta có thể lưu bảng tính ở định dạng PDF bằng cách sử dụng`Save(filePath)` phương thức của đối tượng Workbook.

```csharp
// Lưu bảng tính ở định dạng PDF
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

Chỉ định đường dẫn mong muốn đến tệp PDF được tạo bằng cách sử dụng thư mục đầu ra được tạo trước đó.

### Mã nguồn mẫu để triển khai kích thước giấy tùy chỉnh của bảng tính để hiển thị bằng Aspose.Cells cho .NET 
```csharp
//Thư mục đầu ra
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Tạo đối tượng sổ làm việc
Workbook wb = new Workbook();
//Truy cập bảng tính đầu tiên
Worksheet ws = wb.Worksheets[0];
//Đặt khổ giấy tùy chỉnh theo đơn vị inch
ws.PageSetup.CustomPaperSize(6, 4);
//Truy cập ô B4
Cell b4 = ws.Cells["B4"];
//Thêm tin nhắn vào ô B4
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//Lưu sổ làm việc ở định dạng pdf
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## Kết luận

Trong hướng dẫn này, bạn đã học cách triển khai kích thước tùy chỉnh của trang tính bằng Aspose.Cells cho .NET. Bạn có thể sử dụng các bước này để đặt kích thước cụ thể cho bảng tính của mình rồi lưu tài liệu ở định dạng PDF. Chúng tôi hy vọng hướng dẫn này hữu ích trong việc hiểu quá trình triển khai kích thước bảng tính tùy chỉnh.

### Câu hỏi thường gặp (FAQ)

#### Câu hỏi 1: Tôi có thể tùy chỉnh thêm bố cục bảng tính không?

Có, Aspose.Cells cung cấp nhiều tùy chọn để tùy chỉnh bố cục bảng tính của bạn. Bạn có thể đặt kích thước tùy chỉnh, hướng trang, lề, đầu trang và chân trang, v.v.

#### Câu hỏi 2: Aspose.Cells hỗ trợ những định dạng đầu ra nào khác?

Aspose.Cells hỗ trợ nhiều định dạng đầu ra khác nhau, bao gồm PDF, XLSX, XLS, CSV, HTML, TXT và nhiều định dạng khác. Bạn có thể chọn định dạng đầu ra mong muốn theo nhu cầu của bạn.