---
title: Đóng băng các bảng tính
linktitle: Đóng băng các bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng thao tác các ngăn cố định của bảng tính Excel với Aspose.Cells for .NET.
type: docs
weight: 70
url: /vi/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách khóa các ngăn trong bảng tính Excel bằng mã nguồn C# với Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để có được kết quả mong muốn.

## Bước 1: Nhập các thư viện cần thiết

Đảm bảo bạn đã cài đặt thư viện Aspose.Cells cho .NET và nhập các thư viện cần thiết vào dự án C# của bạn.

```csharp
using Aspose.Cells;
```

## Bước 2: Đặt đường dẫn thư mục và mở file Excel

 Đặt đường dẫn đến thư mục chứa tệp Excel của bạn, sau đó mở tệp bằng cách khởi tạo một`Workbook` sự vật.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Bước 3: Đi tới bảng tính và áp dụng cài đặt khóa khung

 Điều hướng đến bảng tính đầu tiên trong tệp Excel bằng cách sử dụng`Worksheet` sự vật. Sau đó sử dụng`FreezePanes` phương pháp áp dụng cài đặt khóa khung.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

Trong ví dụ trên, các ô được khóa vào ô ở hàng 3 và cột 2.

## Bước 4: Lưu thay đổi

 Khi bạn đã thực hiện những thay đổi cần thiết, hãy lưu tệp Excel đã sửa đổi bằng cách sử dụng`Save` phương pháp của`Workbook` sự vật.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Mã nguồn mẫu cho Freeze Panes Of Worksheet bằng Aspose.Cells for .NET 

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
// Áp dụng cài đặt khung cố định
worksheet.FreezePanes(3, 2, 3, 2);
// Lưu tệp Excel đã sửa đổi
workbook.Save(dataDir + "output.xls");
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Hướng dẫn từng bước này chỉ cho bạn cách khóa các ngăn trong bảng tính Excel bằng Aspose.Cells cho .NET. Bằng cách sử dụng mã nguồn C# được cung cấp, bạn có thể dễ dàng tùy chỉnh cài đặt khóa ngăn để sắp xếp và trực quan hóa dữ liệu của mình tốt hơn trong tệp Excel.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện mạnh mẽ để thao tác các tệp Excel trong các ứng dụng .NET.

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

 Để cài đặt Aspose.Cells cho .NET, bạn cần tải xuống gói liên quan từ[Giả định phát hành](https://releases/aspose.com/cells/net/) và thêm nó vào dự án .NET của bạn.

#### Làm cách nào để khóa các ngăn trong bảng tính Excel bằng Aspose.Cells cho .NET?

 Bạn có thể dùng`FreezePanes` phương pháp của`Worksheet` đối tượng để khóa các ngăn của bảng tính. Chỉ định các ô cần khóa bằng cách cung cấp chỉ số hàng và cột.

#### Tôi có thể tùy chỉnh cài đặt khóa khung bằng Aspose.Cells cho .NET không?

 Có, sử dụng`FreezePanes` phương pháp này, bạn có thể chỉ định ô nào cần khóa khi cần, cung cấp chỉ mục hàng và cột thích hợp.
