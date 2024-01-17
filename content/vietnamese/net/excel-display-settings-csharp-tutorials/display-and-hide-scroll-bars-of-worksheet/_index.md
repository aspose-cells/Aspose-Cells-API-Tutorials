---
title: Hiển thị và ẩn thanh cuộn của bảng tính
linktitle: Hiển thị và ẩn thanh cuộn của bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hiển thị hoặc ẩn thanh cuộn trong bảng tính Excel bằng Aspose.Cells for .NET.
type: docs
weight: 50
url: /vi/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách hiển thị hoặc ẩn các thanh cuộn dọc và ngang trong bảng tính Excel bằng mã nguồn C# với Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để có được kết quả mong muốn.

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

## Bước 3: Ẩn thanh cuộn

 Sử dụng`IsVScrollBarVisible` Và`IsHScrollBarVisible` thuộc tính của`Workbook.Settings` đối tượng để ẩn thanh cuộn dọc và ngang của bảng tính.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Bước 4: Lưu thay đổi

 Khi bạn đã thực hiện những thay đổi cần thiết, hãy lưu tệp Excel đã sửa đổi bằng cách sử dụng`Save` phương pháp của`Workbook` sự vật.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Mã nguồn mẫu để hiển thị và ẩn thanh cuộn của bảng tính bằng Aspose.Cells for .NET 

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel thông qua luồng tệp
Workbook workbook = new Workbook(fstream);
// Ẩn thanh cuộn dọc file Excel
workbook.Settings.IsVScrollBarVisible = false;
// Ẩn thanh cuộn ngang file Excel
workbook.Settings.IsHScrollBarVisible = false;
// Lưu tệp Excel đã sửa đổi
workbook.Save(dataDir + "output.xls");
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

### Phần kết luận

Hướng dẫn từng bước này chỉ cho bạn cách hiển thị hoặc ẩn thanh cuộn dọc và ngang trong bảng tính Excel bằng Aspose.Cells for .NET. Sử dụng mã nguồn C# được cung cấp, bạn có thể dễ dàng tùy chỉnh cách hiển thị thanh cuộn trong tệp Excel của mình.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện mạnh mẽ để thao tác các tệp Excel trong các ứng dụng .NET.

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

 Để cài đặt Aspose.Cells cho .NET, bạn cần tải xuống gói liên quan từ[Giả định phát hành](https://releases/aspose.com/cells/net/) và thêm nó vào dự án .NET của bạn.

#### Làm cách nào tôi có thể hiển thị hoặc ẩn thanh cuộn trong bảng tính Excel bằng Aspose.Cells cho .NET?

 Bạn có thể dùng`IsVScrollBarVisible` Và`IsHScrollBarVisible` thuộc tính của`Workbook.Settings` đối tượng hiển thị hoặc ẩn thanh cuộn dọc và ngang tương ứng trong bảng tính Excel.

#### Những định dạng tệp Excel nào khác được Aspose.Cells hỗ trợ cho .NET?

Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel khác nhau, chẳng hạn như XLS, XLSX, CSV, HTML, PDF, v.v.