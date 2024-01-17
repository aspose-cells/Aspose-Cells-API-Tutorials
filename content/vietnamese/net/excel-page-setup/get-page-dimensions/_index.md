---
title: Nhận kích thước trang
linktitle: Nhận kích thước trang
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách truy xuất kích thước trang trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước với mã nguồn trong C#.
type: docs
weight: 40
url: /vi/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET là một thư viện mạnh mẽ cho phép các nhà phát triển làm việc với các tệp Microsoft Excel theo chương trình. Nó cung cấp nhiều tính năng để thao tác với tài liệu Excel, bao gồm khả năng lấy kích thước trang. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn các bước để truy xuất kích thước trang bằng Aspose.Cells cho .NET.

## Bước 1: Tạo một thể hiện của lớp Workbook

Để bắt đầu, chúng ta cần tạo một thể hiện của lớp Workbook, đại diện cho sổ làm việc Excel. Điều này có thể đạt được bằng cách sử dụng đoạn mã sau:

```csharp
Workbook book = new Workbook();
```

## Bước 2: Truy cập bảng tính

Tiếp theo, chúng ta cần điều hướng đến trang tính trong sổ làm việc nơi chúng ta muốn đặt kích thước trang. Trong ví dụ này, giả sử chúng ta muốn làm việc với bảng tính đầu tiên. Chúng ta có thể truy cập nó bằng mã sau:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Bước 3: Đặt khổ giấy thành A2 và in chiều rộng và chiều cao tính bằng inch

Bây giờ chúng ta sẽ đặt khổ giấy thành A2 và in chiều rộng và chiều cao của trang tính bằng inch. Điều này có thể đạt được bằng cách sử dụng đoạn mã sau:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Bước 4: Đặt khổ giấy thành A3 và in chiều rộng và chiều cao tính bằng inch

Tiếp theo, chúng ta sẽ đặt khổ giấy thành A3 và in chiều rộng và chiều cao của trang tính bằng inch. Đây là mã tương ứng:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Bước 5: Đặt khổ giấy thành A4 và in chiều rộng và chiều cao tính bằng inch

Bây giờ chúng ta sẽ đặt khổ giấy thành A4 và in chiều rộng và chiều cao của trang tính bằng inch. Đây là mã:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## Bước 6: Đặt khổ giấy thành Letter và in chiều rộng và chiều cao tính bằng inch

Cuối cùng, chúng ta sẽ đặt khổ giấy thành Letter và in chiều rộng và chiều cao của trang tính bằng inch. Đây là mã:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Mã nguồn mẫu để Nhận kích thước trang bằng Aspose.Cells cho .NET 
```csharp
// Tạo một thể hiện của lớp Workbook
Workbook book = new Workbook();
// Truy cập bảng tính đầu tiên
Worksheet sheet = book.Worksheets[0];
// Đặt khổ giấy thành A2 và in chiều rộng và chiều cao của giấy tính bằng inch
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Đặt khổ giấy thành A3 và in chiều rộng và chiều cao của giấy tính bằng inch
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Đặt khổ giấy thành A4 và in chiều rộng và chiều cao của giấy tính bằng inch
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// Đặt khổ giấy thành Letter và in chiều rộng và chiều cao của giấy tính bằng inch
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách truy xuất kích thước trang bằng Aspose.Cells cho .NET. Tính năng này có thể hữu ích khi bạn cần thực hiện các thao tác cụ thể dựa trên kích thước trang trong tệp Excel của mình.

Đừng quên khám phá thêm tài liệu của Aspose.Cells để khám phá tất cả các tính năng mạnh mẽ mà nó cung cấp.

### Câu hỏi thường gặp

#### 1. Aspose.Cells for .NET hỗ trợ những khổ giấy nào khác?

Aspose.Cells for .NET hỗ trợ nhiều khổ giấy khác nhau bao gồm A1, A5, B4, B5, Executive, Legal, Letter và nhiều khổ giấy khác. Bạn có thể kiểm tra tài liệu để biết danh sách đầy đủ các khổ giấy được hỗ trợ.

#### 2. Tôi có thể đặt kích thước trang tùy chỉnh bằng Aspose.Cells cho .NET không?

Có, bạn có thể đặt kích thước trang tùy chỉnh bằng cách chỉ định chiều rộng và chiều cao mong muốn. Aspose.Cells cung cấp đầy đủ tính linh hoạt để tùy chỉnh kích thước trang theo nhu cầu của bạn.

#### 3. Tôi có thể lấy kích thước trang theo đơn vị khác inch không?

Có, Aspose.Cells for .NET cho phép bạn lấy kích thước trang theo các đơn vị khác nhau, bao gồm inch, cm, milimét và điểm.

#### 4. Aspose.Cells for .NET có hỗ trợ các tính năng chỉnh sửa cài đặt trang khác không?

Có, Aspose.Cells cung cấp đầy đủ các tính năng để chỉnh sửa cài đặt trang, bao gồm cài đặt lề, hướng, đầu trang và chân trang, v.v.