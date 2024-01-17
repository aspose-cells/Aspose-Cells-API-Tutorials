---
title: Xem trước bản in sổ làm việc
linktitle: Xem trước bản in sổ làm việc
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách tạo bản xem trước in của sổ làm việc bằng Aspose.Cells cho .NET.
type: docs
weight: 170
url: /vi/net/excel-workbook/workbook-print-preview/
---
Xem trước bản in của Workbook là một tính năng cần thiết khi làm việc với các tệp Excel bằng Aspose.Cells for .NET. Bạn có thể dễ dàng tạo bản xem trước bản in bằng cách làm theo các bước sau:

## Bước 1: Chỉ định thư mục nguồn

Trước tiên, bạn cần chỉ định thư mục nguồn chứa tệp Excel bạn muốn xem trước. Đây là cách thực hiện:

```csharp
// thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Bước 2: Tải sổ làm việc

Sau đó, bạn cần tải sổ làm việc Workbook từ tệp Excel đã chỉ định. Đây là cách thực hiện:

```csharp
// Tải sổ làm việc Workbook
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Bước 3: Cấu hình tùy chọn hình ảnh và in

Trước khi tạo bản xem trước bản in, bạn có thể định cấu hình các tùy chọn hình ảnh và in nếu cần. Trong ví dụ này, chúng tôi đang sử dụng các tùy chọn mặc định. Đây là cách thực hiện:

```csharp
// Tùy chọn hình ảnh và in
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Bước 4: Tạo bản xem trước in của sổ làm việc

Bây giờ bạn có thể tạo bản xem trước in của sổ làm việc Workbook bằng cách sử dụng lớp WorkbookPrintingPreview. Đây là cách thực hiện:

```csharp
// In bản xem trước của sổ làm việc
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Bước 5: Tạo bản xem trước in của bảng tính

Nếu bạn muốn tạo bản xem trước bản in của một bảng tính cụ thể, bạn có thể sử dụng lớp SheetPrintingPreview. Đây là một ví dụ :

```csharp
// In bản xem trước của bảng tính
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Mã nguồn mẫu cho Xem trước bản in sổ làm việc bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Phần kết luận

Tạo bản xem trước bản in của sổ làm việc là một tính năng mạnh mẽ được Aspose.Cells cung cấp cho .NET. Bằng cách làm theo các bước nêu trên, bạn có thể dễ dàng xem trước sổ làm việc Excel của mình và nhận thông tin về số trang cần in.

### Câu hỏi thường gặp

#### Câu hỏi: Làm cách nào tôi có thể chỉ định một thư mục nguồn khác để tải Sổ làm việc của mình?
    
 Đáp: Bạn có thể sử dụng`Set_SourceDirectory` phương pháp để chỉ định một thư mục nguồn khác. Ví dụ:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Câu hỏi: Tôi có thể tùy chỉnh các tùy chọn hình ảnh và in khi tạo bản xem trước bản in không?
    
 Trả lời: Có, bạn có thể tùy chỉnh các tùy chọn hình ảnh và in bằng cách thay đổi các thuộc tính của`ImageOrPrintOptions` sự vật. Ví dụ: bạn có thể đặt độ phân giải hình ảnh, định dạng tệp đầu ra, v.v.

#### Câu hỏi: Có thể tạo bản xem trước in cho nhiều trang tính trong Sổ làm việc không?
    
Trả lời: Có, bạn có thể lặp lại các trang tính khác nhau trong Sổ làm việc và tạo bản xem trước bản in cho mỗi trang tính bằng cách sử dụng`SheetPrintingPreview` lớp học.

#### Hỏi: Làm cách nào để lưu bản xem trước bản in dưới dạng hình ảnh hoặc tệp PDF?
    
 Đáp: Bạn có thể sử dụng`ToImage` hoặc`ToPdf` phương pháp của`WorkbookPrintingPreview` hoặc`SheetPrintingPreview` đối tượng để lưu bản xem trước bản in dưới dạng hình ảnh hoặc tệp PDF.

#### Câu hỏi: Tôi có thể làm gì với bản xem trước bản in sau khi được tạo?
    
Đáp: Khi bạn đã tạo bản xem trước bản in, bạn có thể xem nó trên màn hình, lưu nó dưới dạng hình ảnh hoặc tệp PDF hoặc sử dụng nó cho các hoạt động khác như gửi qua email hoặc in.
	