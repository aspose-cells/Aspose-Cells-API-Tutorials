---
title: Xem trước ngắt trang của bảng tính
linktitle: Xem trước ngắt trang của bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hướng dẫn từng bước để hiển thị bản xem trước ngắt trang của bảng tính bằng Aspose.Cells cho .NET.
type: docs
weight: 110
url: /vi/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ giải thích cách hiển thị bản xem trước ngắt trang của bảng tính bằng Aspose.Cells cho .NET. Thực hiện theo các bước sau để có được kết quả mong muốn:

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và thiết lập môi trường phát triển của mình. Ngoài ra, hãy đảm bảo bạn có bản sao của tệp Excel mà bạn muốn hiển thị bản xem trước ngắt trang.

## Bước 2: Nhập các phụ thuộc cần thiết

Thêm các lệnh cần thiết để sử dụng các lớp từ Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Bước 3: Khởi tạo mã

Bắt đầu bằng cách khởi tạo đường dẫn đến thư mục chứa tài liệu Excel của bạn:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Bước 4: Mở file Excel

 Tạo một`FileStream` đối tượng chứa file Excel cần mở:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Khởi tạo một`Workbook` đối tượng và mở tệp Excel bằng luồng tệp:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Bước 5: Truy cập bảng tính

Điều hướng đến bảng tính đầu tiên trong tệp Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Bước 6: Hiển thị bản xem trước theo từng trang

Bật xem trước từng trang cho bảng tính:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Bước 7: Lưu thay đổi

Lưu các thay đổi được thực hiện vào tệp Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Bước 8: Đóng luồng tập tin

Đóng luồng tệp để giải phóng tất cả tài nguyên:

```csharp
fstream.Close();
```

### Mã nguồn mẫu cho Xem trước ngắt trang của bảng tính bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel thông qua luồng tệp
Workbook workbook = new Workbook(fstream);
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Hiển thị bảng tính trong bản xem trước ngắt trang
worksheet.IsPageBreakPreview = true;
// Lưu tệp Excel đã sửa đổi
workbook.Save(dataDir + "output.xls");
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Trong hướng dẫn này, bạn đã học cách hiển thị bản xem trước ngắt trang của một trang tính bằng Aspose.Cells cho .NET. Bằng cách làm theo các bước được mô tả, bạn có thể dễ dàng kiểm soát giao diện và bố cục của tệp Excel của mình.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện phần mềm phổ biến để thao tác với các tệp Excel trong các ứng dụng .NET.

#### Tôi có thể hiển thị bản xem trước từng trang cho một trang tính cụ thể thay vì toàn bộ trang tính không?

Có, bằng cách sử dụng Aspose.Cells, bạn có thể bật xem trước ngắt trang cho một trang tính cụ thể bằng cách truy cập vào đối tượng Trang tính tương ứng.

#### Aspose.Cells có hỗ trợ các tính năng chỉnh sửa tệp Excel khác không?

Có, Aspose.Cells cung cấp nhiều tính năng để chỉnh sửa và thao tác với tệp Excel, chẳng hạn như thêm dữ liệu, định dạng, tạo biểu đồ, v.v.

#### Aspose.Cells chỉ hoạt động với các tệp Excel ở định dạng .xls phải không?

Không, Aspose.Cells hỗ trợ nhiều định dạng tệp Excel khác nhau bao gồm .xls và .xlsx.
	