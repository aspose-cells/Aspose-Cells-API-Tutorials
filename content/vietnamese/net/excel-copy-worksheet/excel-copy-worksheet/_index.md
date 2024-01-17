---
title: Bảng tính sao chép Excel
linktitle: Bảng tính sao chép Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Sao chép một bảng tính Excel sang một bảng tính khác bằng Aspose.Cells for .NET.
type: docs
weight: 20
url: /vi/net/excel-copy-worksheet/excel-copy-worksheet/
---

Trong hướng dẫn này, chúng tôi sẽ giải thích cách sao chép bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Chúng tôi sẽ cung cấp cho bạn mã nguồn C# và hướng dẫn bạn các bước cần thiết để hoàn thành nhiệm vụ này. Cuối cùng, chúng tôi sẽ cho bạn thấy kết quả mong đợi. Thực hiện theo các hướng dẫn dưới đây để bắt đầu.

## Bước 1: Chuẩn bị

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và tạo dự án C# trong môi trường phát triển tích hợp (IDE) ưa thích của bạn. Ngoài ra, hãy đảm bảo rằng bạn có bản sao của tệp Excel mà bạn muốn thao tác.

## Bước 2: Nhập thư viện cần thiết

 Trong tệp nguồn C# của bạn, hãy nhập các thư viện cần thiết từ Aspose.Cells bằng cách sử dụng`using` chỉ thị:

```csharp
using Aspose.Cells;
```

## Bước 3: Đặt đường dẫn file

 Khai báo một`dataDir` biến và khởi tạo nó bằng thư mục chứa tệp Excel của bạn. Ví dụ :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Hãy chắc chắn để thay thế`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` với đường dẫn thực tế đến thư mục của bạn.

## Bước 4: Tải file Excel hiện có

 Sử dụng`Workbook` lớp từ Aspose.Cells để mở tệp Excel hiện có. Sử dụng`InputPath` biến để chỉ định đường dẫn tệp:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Hãy chắc chắn rằng bạn đã thay thế`"book1.xls"` bằng tên thật của tệp Excel của bạn.

## Bước 5: Sao chép bảng tính

 Bây giờ chúng ta sẽ sao chép bảng tính hiện có sang một bảng tính mới. Sử dụng`Worksheets` tài sản của`Workbook` đối tượng để truy cập vào bộ sưu tập các bảng tính:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Sau đó sử dụng`AddCopy` phương pháp sao chép bảng tính được chỉ định. Ví dụ: để sao chép "Sheet1":

```csharp
sheets.AddCopy("Sheet1");
```

## Bước 6: Lưu file Excel

 Sử dụng`Save` phương pháp của`Workbook` đối tượng để lưu các thay đổi vào một tệp mới:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Đảm bảo chỉ định đường dẫn và tên tệp mong muốn cho tệp đầu ra.

### Mã nguồn mẫu cho Bảng tính sao chép Excel bằng Aspose.Cells cho .NET 

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Mở một tệp Excel hiện có.
Workbook wb = new Workbook(InputPath);
// Tạo một đối tượng Worksheets có tham chiếu đến
// các trang của Workbook.
WorksheetCollection sheets = wb.Worksheets;
// Sao chép dữ liệu sang một trang tính mới từ một trang tính hiện có
// trang tính trong Workbook.
sheets.AddCopy("Sheet1");
// Lưu tệp Excel.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách sao chép bảng tính Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước này chỉ ra cách nhập các thư viện cần thiết, tải tệp Excel hiện có, sao chép trang tính và lưu tệp đã sửa đổi. Vui lòng sử dụng phương pháp này trong các dự án của riêng bạn để thao tác các tệp Excel một cách hiệu quả.

### Câu hỏi thường gặp

#### Câu hỏi: Aspose.Cells có tương thích với các ngôn ngữ lập trình khác không?

A. Có, Aspose.Cells hỗ trợ nhiều ngôn ngữ lập trình bao gồm C#, Java, Python và nhiều ngôn ngữ khác.

#### H. Tôi có thể sao chép một trang tính sang một sổ làm việc Excel khác không?

A.  Có, bạn có thể sử dụng`AddCopy` phương pháp sao chép một bảng tính sang một bảng tính Excel khác.

#### Hỏi. Aspose.Cells có giữ nguyên công thức và định dạng khi sao chép trang tính không?

A. Có, Aspose.Cells giữ nguyên công thức, định dạng và các thuộc tính khác khi sao chép trang tính.

#### Câu hỏi: Aspose.Cells có yêu cầu giấy phép sử dụng thương mại không?

A. Có, Aspose.Cells là sản phẩm thương mại và yêu cầu mua giấy phép để sử dụng cho mục đích thương mại. Bạn có thể tìm thêm thông tin cấp phép trên trang web chính thức của Aspose.