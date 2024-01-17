---
title: Thêm trang tính mới trong Excel Hướng dẫn C#
linktitle: Thêm trang tính mới vào Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách thêm trang tính mới trong Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước với mã nguồn trong C#.
type: docs
weight: 20
url: /vi/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
Trong hướng dẫn này, chúng tôi sẽ giải thích từng bước mã nguồn C# để thêm một trang tính mới trong Excel bằng Aspose.Cells cho .NET. Thêm một bảng tính mới vào sổ làm việc Excel là thao tác phổ biến khi tạo báo cáo hoặc thao tác với dữ liệu. Aspose.Cells là một thư viện mạnh mẽ giúp bạn dễ dàng thao tác và tạo các tệp Excel bằng .NET. Hãy làm theo các bước dưới đây để hiểu và triển khai mã này.

## Bước 1: Thiết lập thư mục tài liệu

Bước đầu tiên là xác định thư mục tài liệu nơi tệp Excel sẽ được lưu. Nếu thư mục không tồn tại, chúng tôi tạo nó bằng đoạn mã sau:

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Tạo thư mục nếu nó chưa tồn tại.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

Đảm bảo thay thế "THƯ MỤC TÀI LIỆU CỦA BẠN" bằng đường dẫn thích hợp đến thư mục tài liệu của bạn.

## Bước 2: Khởi tạo một đối tượng Workbook

Bước thứ hai là khởi tạo một đối tượng Workbook, đại diện cho sổ làm việc Excel. Sử dụng mã sau đây:

```csharp
Workbook workbook = new Workbook();
```

Đối tượng này sẽ được sử dụng để thêm một bảng tính mới và thực hiện các thao tác khác trên sổ làm việc Excel.

## Bước 3: Thêm một bảng tính mới

Bước thứ ba là thêm một bảng tính mới vào đối tượng Workbook. Sử dụng mã sau đây:

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

Điều này sẽ thêm một bảng tính mới vào đối tượng Workbook và bạn sẽ nhận được một tham chiếu đến bảng tính này bằng cách sử dụng chỉ mục của nó.

## Bước 4: Đặt tên cho bảng tính mới

Bước thứ tư là đặt tên cho bảng tính mới. Bạn có thể sử dụng đoạn mã sau để đặt tên bảng tính:

```csharp
worksheet.Name = "My Worksheet";
```

Thay thế "Bảng tính của tôi" bằng tên mong muốn cho trang tính mới.

## Bước 5: Lưu file Excel

Cuối cùng, bước cuối cùng là lưu file Excel. Sử dụng mã sau đây:

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

Thao tác này sẽ lưu sổ làm việc Excel cùng với trang tính mới vào thư mục tài liệu mà bạn đã chỉ định.

### Mã nguồn mẫu cho Hướng dẫn Thêm trang tính mới trong Excel C# bằng cách sử dụng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo thư mục nếu nó chưa có.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Thêm một bảng tính mới vào đối tượng Workbook
int i = workbook.Worksheets.Add();
// Lấy tham chiếu của bảng tính mới được thêm bằng cách chuyển chỉ mục trang tính của nó
Worksheet worksheet = workbook.Worksheets[i];
// Đặt tên cho bảng tính mới được thêm vào
worksheet.Name = "My Worksheet";
// Lưu tệp Excel
workbook.Save(dataDir + "output.out.xls");
```

## Phần kết luận

Bây giờ bạn đã học cách thêm một bảng tính mới trong Excel bằng Aspose.Cells cho .NET. Bạn có thể sử dụng phương pháp này để thao tác và tạo tệp Excel bằng C#. Aspose.Cells cung cấp nhiều tính năng mạnh mẽ để đơn giản hóa việc xử lý tệp Excel trong ứng dụng của bạn.

### Câu hỏi thường gặp (FAQ)

#### Tôi có thể sử dụng Aspose.Cells với các ngôn ngữ lập trình khác ngoài C# không?

Có, Aspose.Cells hỗ trợ nhiều ngôn ngữ lập trình như Java, Python, Ruby và nhiều ngôn ngữ khác.

#### Tôi có thể thêm định dạng cho các ô trong trang tính mới tạo không?

Có, bạn có thể áp dụng định dạng cho ô bằng các phương thức được cung cấp bởi lớp Worksheet của Aspose.Cells. Bạn có thể đặt kiểu ô, thay đổi màu nền, áp dụng đường viền, v.v.

#### Làm cách nào tôi có thể truy cập dữ liệu ô từ trang tính mới?

Bạn có thể truy cập dữ liệu ô bằng cách sử dụng các thuộc tính và phương thức được cung cấp bởi lớp Worksheet của Aspose.Cells. Ví dụ: bạn có thể sử dụng thuộc tính Ô để truy cập vào một ô cụ thể và truy xuất hoặc sửa đổi giá trị của ô đó.

#### Aspose.Cells có hỗ trợ các công thức trong Excel không?

Có, Aspose.Cells hỗ trợ các công thức Excel. Bạn có thể đặt công thức trong các ô của trang tính bằng phương thức SetFormula của lớp Ô.
