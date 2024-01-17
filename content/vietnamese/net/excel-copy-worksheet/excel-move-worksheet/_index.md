---
title: Bảng tính di chuyển Excel
linktitle: Bảng tính di chuyển Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng di chuyển bảng tính vào sổ làm việc Excel bằng Aspose.Cells for .NET.
type: docs
weight: 40
url: /vi/net/excel-copy-worksheet/excel-move-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn các bước để di chuyển một trang tính vào sổ làm việc Excel bằng thư viện Aspose.Cells cho .NET. Thực hiện theo các hướng dẫn dưới đây để hoàn thành nhiệm vụ này.


## Bước 1: Chuẩn bị

Đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và tạo dự án C# trong môi trường phát triển tích hợp (IDE) ưa thích của bạn.

## Bước 2: Đặt đường dẫn thư mục tài liệu

 Khai báo một`dataDir` biến và khởi tạo nó bằng đường dẫn đến thư mục tài liệu của bạn. Ví dụ :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENTS_DIRECTORY"` với đường dẫn thực tế đến thư mục của bạn.

## Bước 3: Xác định đường dẫn file đầu vào

 Khai báo một`InputPath` biến và khởi tạo nó bằng đường dẫn đầy đủ của tệp Excel hiện có mà bạn muốn sửa đổi. Ví dụ :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Đảm bảo bạn có tệp Excel`book1.xls` trong thư mục tài liệu của bạn hoặc chỉ định tên tệp và vị trí chính xác.

## Bước 4: Mở file Excel

 Sử dụng`Workbook` lớp Aspose.Cells để mở tệp Excel đã chỉ định:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Bước 5: Lấy bộ sưu tập bảng tính

 Tạo một`WorksheetCollection` đối tượng để tham chiếu đến các bảng tính trong sổ làm việc:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Bước 6: Lấy bảng tính đầu tiên

Lấy bảng tính đầu tiên trong sổ làm việc:

```csharp
Worksheet worksheet = sheets[0];
```

## Bước 7: Di chuyển bảng tính

 Sử dụng`MoveTo` phương pháp di chuyển bảng tính đầu tiên đến vị trí thứ ba trong sổ làm việc:

```csharp
worksheet.MoveTo(2);
```

## Bước 8: Lưu file Excel đã sửa đổi

Lưu file Excel với bảng tính đã di chuyển:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Đảm bảo chỉ định đường dẫn và tên tệp mong muốn cho tệp đầu ra.

### Mã nguồn mẫu cho Bảng tính Di chuyển Excel bằng Aspose.Cells for .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Mở một tập tin excel hiện có.
Workbook wb = new Workbook(InputPath);
// Tạo một đối tượng Worksheets có tham chiếu đến
// các trang của Workbook.
WorksheetCollection sheets = wb.Worksheets;
// Nhận bảng tính đầu tiên.
Worksheet worksheet = sheets[0];
// Di chuyển trang đầu tiên đến vị trí thứ ba trong sổ làm việc.
worksheet.MoveTo(2);
// Lưu tập tin excel.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách di chuyển một trang tính vào sổ làm việc Excel bằng Aspose.Cells for .NET. Vui lòng sử dụng phương pháp này trong các dự án của riêng bạn để thao tác các tệp Excel một cách hiệu quả.

### Câu hỏi thường gặp

#### H. Tôi có thể di chuyển trang tính sang vị trí khác trong cùng một sổ làm việc Excel không?

A.  Có, bạn có thể di chuyển trang tính sang vị trí khác trong cùng sổ làm việc Excel bằng cách sử dụng`MoveTo` phương thức của đối tượng Worksheet. Chỉ cần xác định chỉ mục của vị trí đích trong sổ làm việc.

#### H. Tôi có thể di chuyển một trang tính sang một sổ làm việc Excel khác không?

A.  Có, bạn có thể di chuyển một trang tính sang một sổ làm việc Excel khác bằng cách sử dụng`MoveTo` phương thức của đối tượng Worksheet. Chỉ cần xác định chỉ mục của vị trí đích trong sổ làm việc đích.

#### H. Mã nguồn được cung cấp có hoạt động với các định dạng tệp Excel khác, chẳng hạn như XLSX không?

A. Có, mã nguồn được cung cấp hoạt động với các định dạng tệp Excel khác, bao gồm XLSX. Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel, cho phép bạn thao tác và di chuyển bảng tính thành các loại tệp khác nhau.

#### H. Làm cách nào tôi có thể chỉ định đường dẫn và tên tệp đầu ra khi lưu tệp Excel đã sửa đổi?

A.  Khi lưu tệp Excel đã sửa đổi, hãy sử dụng`Save` phương thức của đối tượng Workbook chỉ định đường dẫn đầy đủ và tên của tệp đầu ra. Đảm bảo chỉ định phần mở rộng tệp thích hợp, chẳng hạn như`.xls` hoặc`.xlsx`, tùy thuộc vào định dạng tệp mong muốn.