---
title: Xóa bảng tính Excel theo tên Hướng dẫn C#
linktitle: Xóa bảng tính Excel theo tên
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng xóa một bảng tính Excel cụ thể theo tên bằng Aspose.Cells for .NET. Hướng dẫn chi tiết với các ví dụ về mã.
type: docs
weight: 40
url: /vi/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-name-csharp-tutorial/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# bên dưới, mã này có thể xóa bảng tính Excel bằng Aspose.Cells cho .NET bằng tên của nó. Chúng tôi sẽ bao gồm mã mẫu cho từng bước để giúp bạn hiểu chi tiết về quy trình.

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

## Bước 4: Xóa bảng tính theo tên

 Để xóa một bảng tính khỏi tên của nó, bạn có thể sử dụng`RemoveAt()` phương pháp của`Worksheets` đối tượng của`Workbook` sự vật. Tên của bảng tính bạn muốn xóa phải được chuyển dưới dạng tham số.

```csharp
// Xóa một bảng tính bằng tên trang tính của nó
workbook.Worksheets.RemoveAt("Sheet1");
```

## Bước 5: Lưu sổ làm việc

 Khi bạn đã xóa bảng tính, bạn có thể lưu sổ làm việc Excel đã sửa đổi bằng cách sử dụng`Save()` phương pháp của`Workbook` sự vật.

```csharp
// Lưu sổ làm việc Excel
workbook.Save(dataDir + "output.out.xls");
```


### Mã nguồn mẫu cho Hướng dẫn xóa bảng tính Excel theo tên C# bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel thông qua luồng tệp
Workbook workbook = new Workbook(fstream);
// Xóa một bảng tính bằng tên trang tính của nó
workbook.Worksheets.RemoveAt("Sheet1");
// Lưu sổ làm việc
workbook.Save(dataDir + "output.out.xls");
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã trình bày quy trình từng bước xóa bảng tính Excel theo tên bằng Aspose.Cells cho .NET. Bằng cách làm theo các ví dụ về mã và giải thích được cung cấp, giờ đây bạn sẽ hiểu rõ về cách thực hiện tác vụ này trong các ứng dụng C# của mình. Aspose.Cells for .NET cung cấp một bộ tính năng toàn diện để làm việc với các tệp Excel, cho phép bạn dễ dàng thao tác với bảng tính và dữ liệu liên quan.

### Câu hỏi thường gặp (FAQ)

#### Aspose.Cells cho .NET là gì?

Aspose.Cells for .NET là một thư viện mạnh mẽ cho phép các nhà phát triển tạo, thao tác và chuyển đổi các tệp Excel trong ứng dụng .NET của họ. Nó cung cấp nhiều tính năng để làm việc với bảng tính, ô, công thức, kiểu và hơn thế nữa.

#### Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

Để cài đặt Aspose.Cells cho .NET, bạn có thể tải xuống gói cài đặt từ Bản phát hành Aspose (https://releases.aspose.com/cells/net) và làm theo hướng dẫn được cung cấp. Bạn sẽ cần có giấy phép hợp lệ để sử dụng thư viện trong các ứng dụng của mình.

#### Tôi có thể xóa nhiều bảng tính cùng một lúc không?

Có, bạn có thể xóa nhiều trang tính bằng Aspose.Cells for .NET. Bạn chỉ cần lặp lại bước xóa cho mỗi bảng tính bạn muốn xóa.

#### Làm cách nào để biết bảng tính có tồn tại hay không trước khi xóa nó?

 Trước khi xóa một bảng tính, bạn có thể kiểm tra xem nó có tồn tại hay không bằng cách sử dụng`Contains()` phương pháp của`Worksheets` đối tượng của`Workbook` sự vật. Phương thức này lấy tên bảng tính làm tham số và trả về`true` nếu bảng tính tồn tại, nếu không nó sẽ trả về`false`.

#### Có thể khôi phục bảng tính đã xóa không?

Thật không may, khi bảng tính bị xóa, bạn không thể khôi phục bảng tính đó trực tiếp từ tệp Excel. Bạn nên tạo bản sao lưu tệp Excel trước khi xóa bảng tính để tránh mất dữ liệu.