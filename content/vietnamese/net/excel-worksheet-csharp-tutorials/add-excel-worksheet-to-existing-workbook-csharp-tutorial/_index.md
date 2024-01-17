---
title: Thêm bảng tính Excel vào sổ làm việc hiện có Hướng dẫn C#
linktitle: Thêm bảng tính Excel vào sổ làm việc hiện có
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng thêm trang tính mới vào sổ làm việc Excel hiện có bằng Aspose.Cells for .NET. Hướng dẫn từng bước với các ví dụ về mã.
type: docs
weight: 10
url: /vi/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# bên dưới, giúp thêm trang tính mới vào sổ làm việc Excel hiện có bằng cách sử dụng Aspose.Cells cho .NET. Chúng tôi sẽ bao gồm mã mẫu cho từng bước để giúp bạn hiểu chi tiết về quy trình.

## Bước 1: Xác định thư mục tài liệu

Để bắt đầu, bạn cần đặt đường dẫn thư mục chứa tệp Excel của bạn. Thay thế "THƯ MỤC TÀI LIỆU CỦA BẠN" trong mã bằng đường dẫn thực tế của tệp Excel của bạn.

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Bước 2: Tạo luồng tệp và mở tệp Excel

 Tiếp theo, bạn cần tạo một luồng tệp và mở tệp Excel bằng cách sử dụng`FileStream` lớp học.

```csharp
// Tạo luồng file chứa file Excel cần mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Bước 3: Khởi tạo một đối tượng sổ làm việc

 Sau khi mở tệp Excel, bạn cần khởi tạo một`Workbook`sự vật. Đối tượng này đại diện cho sổ làm việc Excel và cung cấp các phương thức và thuộc tính khác nhau để thao tác với sổ làm việc.

```csharp
// Khởi tạo một đối tượng Workbook
// Mở file Excel theo luồng file
Workbook workbook = new Workbook(fstream);
```

## Bước 4: Thêm một trang tính mới vào sổ làm việc

 Để thêm một bảng tính mới vào sổ làm việc, bạn có thể sử dụng`Worksheets.Add()` phương pháp của`Workbook` sự vật. Phương thức này trả về chỉ mục của trang tính mới được thêm vào.

```csharp
// Thêm một trang tính mới vào sổ làm việc Workbook
int i = workbook. Worksheets. Add();
```

## Bước 5: Đặt tên trang tính mới

 Bạn có thể đặt tên của trang tính mới được thêm vào bằng cách sử dụng`Name` tài sản của`Worksheet` sự vật.

```csharp
// Lấy tham chiếu của trang tính mới được thêm bằng cách chuyển chỉ mục trang tính của nó
Worksheet worksheet = workbook.Worksheets[i];
// Xác định tên của sheet mới
worksheet.Name = "My Worksheet";
```

## Bước 6: Lưu tệp Excel

 Khi bạn đã thêm trang tính mới và đặt tên cho nó, bạn có thể lưu tệp Excel đã sửa đổi bằng cách sử dụng`Save()` phương pháp của`Workbook` sự vật.

```csharp
// Lưu tệp Excel
workbook.Save(dataDir + "output.out.xls");
```

## Bước 7: Đóng luồng tệp và giải phóng tài nguyên

Cuối cùng, điều quan trọng là phải đóng luồng tệp để giải phóng tất cả tài nguyên được liên kết với nó.

```csharp
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

### Mã nguồn mẫu cho Thêm bảng tính Excel vào sổ làm việc hiện có Hướng dẫn C# bằng cách sử dụng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel thông qua luồng tệp
Workbook workbook = new Workbook(fstream);
// Thêm một bảng tính mới vào đối tượng Workbook
int i = workbook.Worksheets.Add();
// Lấy tham chiếu của bảng tính mới được thêm bằng cách chuyển chỉ mục trang tính của nó
Worksheet worksheet = workbook.Worksheets[i];
// Đặt tên cho bảng tính mới được thêm vào
worksheet.Name = "My Worksheet";
// Lưu tệp Excel
workbook.Save(dataDir + "output.out.xls");
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã trình bày quy trình từng bước để thêm ngọn lửa mới Kết nối với sổ làm việc Excel hiện có bằng cách sử dụng Aspose.Cells cho .NET. Bằng cách làm theo các ví dụ về mã và giải thích được cung cấp, giờ đây bạn sẽ hiểu rõ về cách thực hiện tác vụ này trong các ứng dụng C# của mình. Aspose.Cells for .NET cung cấp một bộ tính năng toàn diện để làm việc với các tệp Excel, cho phép bạn tự động hóa các tác vụ liên quan đến Excel khác nhau một cách hiệu quả.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện .NET mạnh mẽ cho phép các nhà phát triển tạo, thao tác và chuyển đổi các tệp Excel trong ứng dụng của họ. Nó cung cấp nhiều tính năng để làm việc với bảng tính, ô, công thức, kiểu, v.v.

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

Để cài đặt Aspose.Cells cho .NET, bạn có thể tải xuống gói cài đặt từ Bản phát hành Aspose (https://releases.aspose.com/cells/net) và làm theo hướng dẫn cài đặt được cung cấp. Bạn cũng sẽ cần giấy phép hợp lệ để sử dụng thư viện trong ứng dụng của mình.

#### Tôi có thể thêm nhiều bảng tính bằng Aspose.Cells cho .NET không?

 Có, bạn có thể thêm nhiều trang tính vào một tệp Excel bằng Aspose.Cells for .NET. Bạn có thể dùng`Worksheets.Add()` phương pháp của`Workbook` đối tượng để thêm bảng tính mới ở các vị trí khác nhau trong sổ làm việc.

#### Làm cách nào để định dạng các ô trong tệp Excel?

Aspose.Cells for .NET cung cấp các phương thức và thuộc tính khác nhau để định dạng các ô trong tệp Excel. Bạn có thể đặt giá trị ô, áp dụng các tùy chọn định dạng như kiểu phông chữ, màu sắc, căn chỉnh, đường viền, v.v. Xem tài liệu và mã mẫu do Aspose.Cells cung cấp để biết thêm thông tin chi tiết về định dạng ô.

#### Aspose.Cells for .NET có tương thích với các phiên bản Excel khác nhau không?

Có, Aspose.Cells for .NET tương thích với các phiên bản Excel khác nhau, bao gồm Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 và Excel for Office 365. Nó hỗ trợ cả định dạng .xls và định dạng .xls mới hơn. định dạng xlsx.