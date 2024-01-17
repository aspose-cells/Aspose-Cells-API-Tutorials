---
title: Sao chép bảng tính Excel từ sổ làm việc khác
linktitle: Sao chép bảng tính Excel từ sổ làm việc khác
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng sao chép bảng tính Excel từ sổ làm việc này sang sổ làm việc khác bằng Aspose.Cells for .NET.
type: docs
weight: 10
url: /vi/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn các bước để sao chép trang tính Excel từ sổ làm việc khác bằng thư viện Aspose.Cells cho .NET. Thực hiện theo các hướng dẫn dưới đây để hoàn thành nhiệm vụ này.

## Bước 1: Chuẩn bị

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và tạo dự án C# trong môi trường phát triển tích hợp (IDE) ưa thích của bạn.

## Bước 2: Đặt đường dẫn thư mục tài liệu

 Khai báo một`dataDir` biến và khởi tạo nó bằng đường dẫn đến thư mục tài liệu của bạn. Ví dụ :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENTS_DIRECTORY"` với đường dẫn thực tế đến thư mục của bạn.

## Bước 3: Tạo sổ làm việc Excel mới

 Sử dụng`Workbook` lớp từ Aspose.Cells để tạo sổ làm việc Excel mới:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Bước 4: Lấy bảng tính đầu tiên trong sổ làm việc

Điều hướng đến bảng tính đầu tiên trong sổ làm việc bằng chỉ mục 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Bước 5: Thêm dữ liệu vào các hàng tiêu đề (A1:A4)

 Sử dụng một`for` vòng lặp để thêm dữ liệu vào các hàng tiêu đề (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Bước 6: Thêm dữ liệu chi tiết (A5:A999)

 Sử dụng cái khác`for` vòng lặp để thêm dữ liệu chi tiết (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Bước 7: Đặt tùy chọn bố cục

 Đặt các tùy chọn thiết lập trang cho bảng tính bằng cách sử dụng`PageSetup` sự vật:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Bước 8: Tạo một bảng tính Excel khác

Tạo một sổ làm việc Excel khác:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Bước 9: Lấy bảng tính đầu tiên từ sổ làm việc thứ hai

Điều hướng đến bảng tính đầu tiên trong sổ làm việc thứ hai:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Bước 10: Đặt tên cho bảng tính

đặt tên cho ngọn lửa

đảo tính toán:

```csharp
ws1.Name = "MySheet";
```

## Bước 11: Sao chép dữ liệu từ bảng tính đầu tiên của sổ làm việc thứ nhất sang bảng tính đầu tiên của sổ làm việc thứ hai

Sao chép dữ liệu từ bảng tính đầu tiên của sổ làm việc đầu tiên sang bảng tính đầu tiên của sổ làm việc thứ hai:

```csharp
ws1.Copy(ws0);
```

## Bước 12: Lưu file Excel

Lưu tệp Excel:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Đảm bảo chỉ định đường dẫn và tên tệp mong muốn cho tệp đầu ra.

### Mã nguồn mẫu cho Bảng tính sao chép Excel từ sổ làm việc khác bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo một Workbook mới.
Workbook excelWorkbook0 = new Workbook();
// Lấy bảng tính đầu tiên trong cuốn sách.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Đặt một số dữ liệu vào các hàng tiêu đề (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Đặt một số dữ liệu chi tiết (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Xác định đối tượng pagesetup dựa trên bảng tính đầu tiên.
PageSetup pagesetup = ws0.PageSetup;
// Năm hàng đầu tiên được lặp lại trong mỗi trang...
// Nó có thể được nhìn thấy trong bản xem trước in.
pagesetup.PrintTitleRows = "$1:$5";
// Tạo một Workbook khác.
Workbook excelWorkbook1 = new Workbook();
// Lấy bảng tính đầu tiên trong cuốn sách.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Đặt tên cho bảng tính.
ws1.Name = "MySheet";
// Sao chép dữ liệu từ bảng tính đầu tiên của sổ làm việc đầu tiên vào
// bảng tính đầu tiên của bảng tính thứ hai.
ws1.Copy(ws0);
// Lưu tập tin excel.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách sao chép một bảng tính Excel từ một sổ làm việc khác bằng Aspose.Cells for .NET. Vui lòng sử dụng phương pháp này trong các dự án của riêng bạn để thao tác các tệp Excel một cách hiệu quả.

### Câu hỏi thường gặp

#### Câu hỏi: Cần có những thư viện nào để sử dụng Aspose.Cells cho .NET?

A. Để sử dụng Aspose.Cells cho .NET, bạn phải đưa thư viện Aspose.Cells vào dự án của mình. Đảm bảo rằng bạn đã tham chiếu chính xác thư viện này trong môi trường phát triển tích hợp (IDE) của mình.

#### H. Aspose.Cells có hỗ trợ các định dạng tệp Excel khác, chẳng hạn như XLSX không?

A. Có, Aspose.Cells hỗ trợ nhiều định dạng tệp Excel khác nhau bao gồm XLSX, XLS, CSV, HTML, v.v. Bạn có thể thao tác các định dạng tệp này bằng các tính năng của Aspose.Cells cho .NET.

#### H. Tôi có thể tùy chỉnh các tùy chọn bố cục khi sao chép trang tính không?

A.  Có, bạn có thể tùy chỉnh các tùy chọn thiết lập trang khi sao chép trang tính bằng cách sử dụng các thuộc tính của`PageSetup` sự vật. Bạn có thể chỉ định tiêu đề trang, chân trang, lề, hướng, v.v.