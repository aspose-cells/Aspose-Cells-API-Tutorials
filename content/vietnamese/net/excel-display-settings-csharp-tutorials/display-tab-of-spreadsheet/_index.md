---
title: Tab hiển thị của bảng tính
linktitle: Tab hiển thị của bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hiển thị tab bảng tính Excel bằng Aspose.Cells for .NET.
type: docs
weight: 60
url: /vi/net/excel-display-settings-csharp-tutorials/display-tab-of-spreadsheet/
---
Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách hiển thị tab của bảng tính Excel bằng mã nguồn C# với Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để có được kết quả mong muốn.

## Bước 1: Nhập các thư viện cần thiết

Đảm bảo bạn đã cài đặt thư viện Aspose.Cells cho .NET và nhập các thư viện cần thiết vào dự án C# của bạn.

```csharp
using Aspose.Cells;
```

## Bước 2: Đặt đường dẫn thư mục và mở file Excel

 Đặt đường dẫn đến thư mục chứa tệp Excel của bạn, sau đó mở tệp bằng cách khởi tạo một`Workbook` sự vật.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Bước 3: Hiển thị tab trang tính

 Sử dụng`ShowTabs` tài sản của`Workbook.Settings` đối tượng để hiển thị tab trang tính Excel.

```csharp
workbook.Settings.ShowTabs = true;
```

## Bước 4: Lưu thay đổi

 Khi bạn đã thực hiện những thay đổi cần thiết, hãy lưu tệp Excel đã sửa đổi bằng cách sử dụng`Save` phương pháp của`Workbook` sự vật.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Mã nguồn mẫu cho Tab hiển thị của bảng tính bằng Aspose.Cells cho .NET 

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Ẩn các tab của file Excel
workbook.Settings.ShowTabs = true;
// Lưu tệp Excel đã sửa đổi
workbook.Save(dataDir + "output.xls");
```

### Phần kết luận

Hướng dẫn từng bước này chỉ cho bạn cách hiển thị tab của bảng tính Excel bằng Aspose.Cells cho .NET. Sử dụng mã nguồn C# được cung cấp, bạn có thể dễ dàng tùy chỉnh cách hiển thị các tab trong tệp Excel của mình.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện mạnh mẽ để thao tác các tệp Excel trong các ứng dụng .NET.

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

 Để cài đặt Aspose.Cells cho .NET, bạn cần tải xuống gói liên quan từ[Giả định phát hành](https://releases/aspose.com/cells/net/) và thêm nó vào dự án .NET của bạn.

#### Làm cách nào để hiển thị tab của bảng tính Excel bằng Aspose.Cells cho .NET?

 Bạn có thể dùng`ShowTabs` tài sản của`Workbook.Settings` đối tượng và đặt nó thành`true` để hiển thị tab bảng tính.

#### Những định dạng tệp Excel nào khác được Aspose.Cells hỗ trợ cho .NET?

Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel khác nhau, chẳng hạn như XLS, XLSX, CSV, HTML, PDF, v.v.
