---
title: Ẩn và bỏ ẩn bảng tính
linktitle: Ẩn và bỏ ẩn bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Một thư viện mạnh mẽ để làm việc với các tệp Excel, bao gồm tạo, sửa đổi và thao tác dữ liệu.
type: docs
weight: 90
url: /vi/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# sau đây được sử dụng để ẩn và hiển thị trang tính bằng Aspose.Cells cho .NET. Làm theo các bước dưới đây:

## Bước 1: Chuẩn bị môi trường

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên hệ thống của mình. Nếu bạn chưa cài đặt nó, bạn có thể tải xuống từ trang web chính thức của Aspose. Sau khi cài đặt, bạn có thể tạo một dự án mới trong môi trường phát triển tích hợp (IDE) ưa thích của mình.

## Bước 2: Nhập các không gian tên bắt buộc

Trong tệp nguồn C# của bạn, hãy thêm các vùng tên cần thiết để sử dụng các tính năng của Aspose.Cells. Thêm các dòng sau vào đầu tập tin của bạn:

```csharp
using Aspose.Cells;
using System.IO;
```

## Bước 3: Tải file Excel

Trước khi ẩn hoặc hiện một bảng tính, bạn phải tải tệp Excel vào ứng dụng của mình. Đảm bảo rằng bạn có tệp Excel mà bạn muốn sử dụng trong cùng thư mục với dự án của bạn. Sử dụng đoạn mã sau để tải tệp Excel:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

Đảm bảo thay thế "ĐƯỜNG ĐƯỜNG ĐẾN THƯ MỤC TÀI LIỆU CỦA BẠN" bằng đường dẫn thực tế đến thư mục chứa tệp Excel của bạn.

## Bước 4: Truy cập bảng tính

Sau khi tải tệp Excel, bạn có thể điều hướng đến trang tính mà bạn muốn ẩn hoặc hiện. Sử dụng đoạn mã sau để truy cập trang tính đầu tiên trong tệp:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Bước 5: Ẩn bảng tính

 Bây giờ bạn đã truy cập trang tính, bạn có thể ẩn nó bằng cách sử dụng`IsVisible` tài sản. Sử dụng đoạn mã sau để ẩn bảng tính đầu tiên trong tệp:

```csharp
worksheet. IsVisible = false;
```

## Bước 6: Hiển thị lại bảng tính

Nếu bạn muốn hiển thị lại bảng tính bị ẩn trước đó, bạn có thể sử dụng mã tương tự bằng cách thay đổi giá trị của`IsVisible` tài sản. Sử dụng đoạn mã sau để hiển thị lại bảng tính đầu tiên:

```csharp
worksheet. IsVisible = true;
```

## Bước 7: Lưu thay đổi

Một khi bạn

  đã ẩn hoặc hiện bảng tính nếu cần, bạn phải lưu các thay đổi vào tệp Excel. Sử dụng đoạn mã sau để lưu các thay đổi:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Đảm bảo chỉ định đường dẫn đầu ra chính xác để lưu tệp Excel đã sửa đổi.

### Mã nguồn mẫu cho Ẩn và Hiện bảng tính bằng Aspose.Cells for .NET 

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo đối tượng Workbook bằng cách mở tệp Excel thông qua luồng tệp
Workbook workbook = new Workbook(fstream);
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Ẩn bảng tính đầu tiên của file Excel
worksheet.IsVisible = false;
// Hiển thị bảng tính đầu tiên của tệp Excel
//Bảng tính.IsVisible = true;
// Lưu tệp Excel đã sửa đổi ở định dạng mặc định (đó là Excel 2003)
workbook.Save(dataDir + "output.out.xls");
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách ẩn và hiển thị bảng tính bằng Aspose.Cells cho .NET. Bây giờ bạn có thể sử dụng tính năng này để kiểm soát khả năng hiển thị của bảng tính trong tệp Excel của mình.

### Câu hỏi thường gặp (FAQ)

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

 Bạn có thể cài đặt Aspose.Cells cho .NET bằng cách tải xuống gói NuGet có liên quan từ[Giả định phát hành](https://releases/aspose.com/cells/net/) và thêm nó vào dự án Visual Studio của bạn.

#### Phiên bản .NET Framework yêu cầu tối thiểu để sử dụng Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET hỗ trợ .NET Framework 2.0 trở lên.

#### Tôi có thể mở và chỉnh sửa các tệp Excel hiện có bằng Aspose.Cells cho .NET không?

Có, bạn có thể mở và chỉnh sửa các tệp Excel hiện có bằng Aspose.Cells for .NET. Bạn có thể truy cập trang tính, ô, công thức và các thành phần khác của tệp Excel.

#### Aspose.Cells for .NET có hỗ trợ báo cáo và xuất sang các định dạng tệp khác không?

Có, Aspose.Cells for .NET hỗ trợ tạo và xuất báo cáo sang các định dạng như PDF, HTML, CSV, TXT, v.v.

#### Việc sửa đổi tệp Excel có phải là vĩnh viễn không?

Có, việc chỉnh sửa tệp Excel sẽ có hiệu lực vĩnh viễn sau khi bạn lưu nó. Đảm bảo lưu bản sao lưu trước khi thực hiện bất kỳ thay đổi nào đối với tệp gốc.