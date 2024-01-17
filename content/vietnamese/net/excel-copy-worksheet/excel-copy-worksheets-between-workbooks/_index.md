---
title: Sao chép bảng tính Excel giữa các sổ làm việc
linktitle: Sao chép bảng tính Excel giữa các sổ làm việc
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng sao chép các trang tính giữa các sổ làm việc Excel bằng Aspose.Cells for .NET.
type: docs
weight: 30
url: /vi/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn các bước để sao chép trang tính giữa các sổ làm việc Excel bằng thư viện Aspose.Cells cho .NET. Thực hiện theo các hướng dẫn dưới đây để hoàn thành nhiệm vụ này.

## Bước 1: Chuẩn bị

Đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và tạo dự án C# trong môi trường phát triển tích hợp (IDE) ưa thích của bạn.

## Bước 2: Đặt đường dẫn thư mục tài liệu

 Khai báo một`dataDir` biến và khởi tạo nó bằng đường dẫn đến thư mục tài liệu của bạn. Ví dụ :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENTS_DIRECTORY"` với đường dẫn thực tế đến thư mục của bạn.

## Bước 3: Xác định đường dẫn file đầu vào

 Khai báo một`InputPath` biến và khởi tạo nó bằng đường dẫn đầy đủ của tệp Excel mà bạn muốn sao chép bảng tính. Ví dụ :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Đảm bảo bạn có tệp Excel`book1.xls` trong thư mục tài liệu của bạn hoặc chỉ định tên tệp và vị trí chính xác.

## Bước 4: Tạo sổ làm việc Excel đầu tiên

 Sử dụng`Workbook` lớp Aspose.Cells để tạo sổ làm việc Excel đầu tiên và mở tệp đã chỉ định:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Bước 5: Tạo sổ làm việc Excel thứ hai

Tạo sổ làm việc Excel thứ hai:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Bước 6: Sao chép bảng tính từ sổ làm việc đầu tiên sang sổ làm việc thứ hai

 Sử dụng`Copy`phương pháp sao chép bảng tính đầu tiên từ sổ làm việc đầu tiên sang sổ làm việc thứ hai:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Bước 7: Lưu file Excel

Lưu file Excel chứa bảng tính đã sao chép:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Đảm bảo chỉ định đường dẫn và tên tệp mong muốn cho tệp đầu ra.

### Mã nguồn mẫu cho Excel Sao chép bảng tính giữa các sổ làm việc bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Tạo một sổ làm việc.
// Mở một tập tin vào cuốn sách đầu tiên.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Tạo một Workbook khác.
Workbook excelWorkbook1 = new Workbook();
// Sao chép trang đầu tiên của cuốn sách đầu tiên vào cuốn sách thứ hai.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Lưu các tập tin.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách sao chép các trang tính giữa các sổ làm việc Excel bằng Aspose.Cells for .NET. Vui lòng sử dụng phương pháp này trong các dự án của riêng bạn để thao tác các tệp Excel một cách hiệu quả.

### Câu hỏi thường gặp

#### Câu hỏi: Cần có những thư viện nào để sử dụng Aspose.Cells cho .NET?

A. Để sử dụng Aspose.Cells cho .NET, bạn phải đưa thư viện Aspose.Cells vào dự án của mình. Đảm bảo rằng bạn đã tham chiếu chính xác thư viện này trong môi trường phát triển tích hợp (IDE) của mình.

#### H. Aspose.Cells có hỗ trợ các định dạng tệp Excel khác, chẳng hạn như XLSX không?

A. Có, Aspose.Cells hỗ trợ nhiều định dạng tệp Excel khác nhau bao gồm XLSX, XLS, CSV, HTML, v.v. Bạn có thể thao tác các định dạng tệp này bằng các tính năng của Aspose.Cells cho .NET.

#### H. Tôi có thể tùy chỉnh các tùy chọn bố cục khi sao chép bảng tính không?

A.  Có, bạn có thể tùy chỉnh các tùy chọn thiết lập trang khi sao chép bảng tính bằng các thuộc tính của`PageSetup` sự vật. Bạn có thể chỉ định tiêu đề trang, chân trang, lề, hướng, v.v.