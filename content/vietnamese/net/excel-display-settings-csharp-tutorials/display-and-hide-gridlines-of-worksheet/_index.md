---
title: Hiển thị và ẩn đường lưới của bảng tính
linktitle: Hiển thị và ẩn đường lưới của bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Kiểm soát việc hiển thị đường lưới trong bảng tính Excel bằng Aspose.Cells for .NET.
type: docs
weight: 30
url: /vi/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách hiển thị và ẩn đường lưới trong bảng tính Excel bằng mã nguồn C# với Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để có được kết quả mong muốn.

## Bước 1: Nhập các thư viện cần thiết

Đảm bảo bạn đã cài đặt thư viện Aspose.Cells cho .NET và nhập các thư viện cần thiết vào dự án C# của bạn.

```csharp
using Aspose.Cells;
using System.IO;
```

## Bước 2: Đặt đường dẫn thư mục và mở file Excel

 Đặt đường dẫn đến thư mục chứa tệp Excel của bạn, sau đó mở tệp bằng cách tạo luồng tệp và khởi tạo một`Workbook` sự vật.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Bước 3: Đi tới bảng tính đầu tiên và ẩn các đường lưới

 Truy cập bảng tính đầu tiên trong tệp Excel bằng cách sử dụng`Worksheets` tài sản của`Workbook` sự vật. Sau đó sử dụng`IsGridlinesVisible` tài sản của`Worksheet` đối tượng để ẩn các đường lưới.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## Bước 4: Lưu thay đổi

 Khi bạn đã thực hiện những thay đổi cần thiết, hãy lưu tệp Excel đã sửa đổi bằng cách sử dụng`Save` phương pháp của`Workbook` sự vật.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Mã nguồn mẫu để hiển thị và ẩn đường lưới của trang tính bằng Aspose.Cells cho .NET 

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
// Ẩn đường lưới của bảng tính đầu tiên của file Excel
worksheet.IsGridlinesVisible = false;
// Lưu tệp Excel đã sửa đổi
workbook.Save(dataDir + "output.xls");
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Hướng dẫn từng bước này chỉ cho bạn cách hiển thị và ẩn đường lưới trong bảng tính Excel bằng Aspose.Cells cho .NET. Bằng cách sử dụng mã nguồn C# được cung cấp, bạn có thể dễ dàng tùy chỉnh cách hiển thị đường lưới trong tệp Excel của mình.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện mạnh mẽ để thao tác các tệp Excel trong các ứng dụng .NET.

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

 Để cài đặt Aspose.Cells cho .NET, bạn cần tải xuống gói liên quan từ[Giả định phát hành](https://releases/aspose.com/cells/net/) và thêm nó vào dự án .NET của bạn.

#### Làm cách nào tôi có thể hiển thị hoặc ẩn đường lưới trong bảng tính Excel bằng Aspose.Cells cho .NET?

 Bạn có thể dùng`IsGridlinesVisible` tài sản của`Worksheet` đối tượng để hiển thị hoặc ẩn đường lưới. Đặt nó thành`true` để hiển thị chúng và để`false` để giấu chúng.

#### Những định dạng tệp Excel nào khác được Aspose.Cells hỗ trợ cho .NET?

Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel khác nhau, chẳng hạn như XLS, XLSX, CSV, HTML, PDF, v.v.

