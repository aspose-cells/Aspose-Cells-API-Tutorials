---
title: Chia ngăn bảng tính
linktitle: Chia ngăn bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hướng dẫn từng bước để phân chia các ngăn trong bảng tính Excel bằng Aspose.Cells cho .NET.
type: docs
weight: 130
url: /vi/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ giải thích cách chia các ngăn trong bảng tính Excel bằng Aspose.Cells cho .NET. Thực hiện theo các bước sau để có được kết quả mong muốn:

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và thiết lập môi trường phát triển của mình. Ngoài ra, hãy đảm bảo bạn có bản sao của tệp Excel mà bạn muốn chia các ngăn.

## Bước 2: Nhập các phụ thuộc cần thiết

Thêm các lệnh cần thiết để sử dụng các lớp từ Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Bước 3: Khởi tạo mã

Bắt đầu bằng cách khởi tạo đường dẫn đến thư mục chứa tài liệu Excel của bạn:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Bước 4: Mở file Excel

 Khởi tạo một cái mới`Workbook` đối tượng và mở tệp Excel bằng cách sử dụng`Open` phương pháp:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Bước 5: Xác định ô hiện hoạt

 Đặt ô hiện hoạt của bảng tính bằng cách sử dụng`ActiveCell` tài sản:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Bước 6: Chia cánh tà

 Chia cửa sổ bảng tính bằng cách sử dụng`Split` phương pháp:

```csharp
book.Worksheets[0].Split();
```

## Bước 7: Lưu thay đổi

Lưu các thay đổi được thực hiện vào tệp Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Mã nguồn mẫu cho Split Panes Of Worksheet bằng Aspose.Cells for .NET 

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo sổ làm việc mới và mở tệp mẫu
Workbook book = new Workbook(dataDir + "Book1.xls");
// Đặt ô hiện hoạt
book.Worksheets[0].ActiveCell = "A20";
// Chia cửa sổ bảng tính
book.Worksheets[0].Split();
// Lưu tập tin excel
book.Save(dataDir + "output.xls");
```

## Phần kết luận

Trong hướng dẫn này, bạn đã học cách chia các ngăn trong bảng tính Excel bằng Aspose.Cells cho .NET. Bằng cách làm theo các bước được mô tả, bạn có thể dễ dàng tùy chỉnh giao diện và hoạt động của tệp Excel của mình.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện phần mềm phổ biến để thao tác với các tệp Excel trong các ứng dụng .NET.

#### Làm cách nào tôi có thể đặt ô hiện hoạt của trang tính trong Aspose.Cells?

 Bạn có thể đặt ô hiện hoạt bằng cách sử dụng`ActiveCell`thuộc tính của đối tượng Worksheet.

#### Tôi chỉ có thể chia các ô ngang hoặc dọc của cửa sổ trang tính được không?

 Có, khi sử dụng Aspose.Cells, bạn chỉ có thể chia các ô ngang hoặc dọc bằng các phương pháp thích hợp như`SplitColumn` hoặc`SplitRow`.

#### Aspose.Cells chỉ hoạt động với các tệp Excel ở định dạng .xls phải không?

Không, Aspose.Cells hỗ trợ nhiều định dạng tệp Excel khác nhau bao gồm .xls và .xlsx.