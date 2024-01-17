---
title: Lấy chiều rộng và chiều cao của giấy của bảng tính
linktitle: Lấy chiều rộng và chiều cao của giấy của bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tạo hướng dẫn từng bước để giải thích mã nguồn C# sau đây nhằm lấy chiều rộng và chiều cao của giấy của bảng tính bằng Aspose.Cells cho .NET.
type: docs
weight: 80
url: /vi/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# sau đây để lấy chiều rộng và chiều cao của giấy của trang tính bằng Aspose.Cells cho .NET. Làm theo các bước dưới đây:

## Bước 1: Tạo sổ làm việc
 Bắt đầu bằng cách tạo một sổ làm việc mới bằng cách sử dụng`Workbook` lớp học:

```csharp
Workbook wb = new Workbook();
```

## Bước 2: Truy cập bảng tính đầu tiên
 Tiếp theo, điều hướng đến bảng tính đầu tiên trong sổ làm việc bằng cách sử dụng`Worksheet` lớp học:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## Bước 3: Đặt khổ giấy thành A2 và hiển thị chiều rộng và chiều cao của giấy tính bằng inch
 Sử dụng`PaperSize` tài sản của`PageSetup` để đặt khổ giấy thành A2, sau đó sử dụng`PaperWidth` Và`PaperHeight` Properties để có được chiều rộng và chiều cao của giấy tương ứng. Hiển thị các giá trị này bằng cách sử dụng`Console.WriteLine` phương pháp:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## Bước 4: Lặp lại các bước cho các khổ giấy khác
Lặp lại các bước trước đó, thay đổi khổ giấy thành A3, A4 và Letter, sau đó hiển thị giá trị chiều rộng và chiều cao của giấy cho từng khổ:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Mã nguồn mẫu để lấy chiều rộng và chiều cao của trang tính bằng Aspose.Cells cho .NET 

```csharp
//Tạo sổ làm việc
Workbook wb = new Workbook();
//Truy cập bảng tính đầu tiên
Worksheet ws = wb.Worksheets[0];
//Đặt khổ giấy thành A2 và in chiều rộng và chiều cao của giấy tính bằng inch
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Đặt khổ giấy thành A3 và in chiều rộng và chiều cao của giấy tính bằng inch
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Đặt khổ giấy thành A4 và in chiều rộng và chiều cao của giấy tính bằng inch
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//Đặt khổ giấy thành Letter và in chiều rộng và chiều cao của giấy tính bằng inch
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## Phần kết luận

Bạn đã học cách sử dụng Aspose.Cells cho .NET để lấy chiều rộng và chiều cao của giấy của bảng tính. Tính năng này có thể hữu ích cho việc cấu hình và bố cục chính xác các tài liệu Excel của bạn.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện mạnh mẽ để thao tác và xử lý các tệp Excel trong các ứng dụng .NET. Nó cung cấp nhiều tính năng để tạo, sửa đổi, chuyển đổi và phân tích các tệp Excel.

#### Làm cách nào tôi có thể lấy khổ giấy của bảng tính bằng Aspose.Cells cho .NET?

 Bạn có thể dùng`PageSetup` lớp học của`Worksheet` đối tượng để truy cập kích thước giấy. Sử dụng`PaperSize` thuộc tính để thiết lập khổ giấy và`PaperWidth` Và`PaperHeight` Properties để có được chiều rộng và chiều cao của giấy tương ứng.

#### Aspose.Cells for .NET hỗ trợ những khổ giấy nào?

Aspose.Cells for .NET hỗ trợ nhiều loại khổ giấy thường được sử dụng, chẳng hạn như A2, A3, A4 và Letter, cũng như nhiều kích thước tùy chỉnh khác.

#### Tôi có thể tùy chỉnh kích thước giấy của bảng tính bằng Aspose.Cells cho .NET không?

 Có, bạn có thể đặt khổ giấy tùy chỉnh bằng cách chỉ định kích thước chiều rộng và chiều cao chính xác bằng cách sử dụng`PaperWidth` Và`PaperHeight` thuộc tính của`PageSetup` lớp học.