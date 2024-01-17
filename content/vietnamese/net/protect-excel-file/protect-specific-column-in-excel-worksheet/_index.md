---
title: Bảo vệ cột cụ thể trong bảng tính Excel
linktitle: Bảo vệ cột cụ thể trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách bảo vệ một cột cụ thể trong trang tính Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 80
url: /vi/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
Khi làm việc với các bảng tính Excel trong C#, thường cần phải bảo vệ các cột cụ thể để ngăn chặn những sửa đổi vô tình. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn quy trình bảo vệ một cột cụ thể trong bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Chúng tôi sẽ cung cấp cho bạn giải thích từng bước về mã nguồn C# cần thiết cho tác vụ này. Vậy hãy bắt đầu!

## Tổng quan về bảo vệ các cột cụ thể trong bảng tính Excel

Việc bảo vệ các cột cụ thể trong bảng tính Excel đảm bảo rằng các cột đó vẫn bị khóa và không thể sửa đổi nếu không có sự cho phép thích hợp. Điều này đặc biệt hữu ích khi bạn muốn hạn chế quyền truy cập chỉnh sửa vào một số dữ liệu hoặc công thức nhất định trong khi cho phép người dùng tương tác với phần còn lại của trang tính. Thư viện Aspose.Cells for .NET cung cấp một bộ tính năng toàn diện để thao tác với các tệp Excel theo chương trình, bao gồm cả bảo vệ cột.

## Thiết lập môi trường

Trước khi chúng ta bắt đầu, hãy đảm bảo bạn đã cài đặt thư viện Aspose.Cells for .NET trong môi trường phát triển của mình. Bạn có thể tải xuống thư viện từ trang web chính thức của Aspose và cài đặt nó bằng trình cài đặt được cung cấp.

## Tạo một bảng tính và bảng tính mới

Để bắt đầu bảo vệ các cột cụ thể, chúng ta cần tạo một sổ làm việc và trang tính mới bằng Aspose.Cells cho .NET. Đây là đoạn mã:

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";

// Tạo thư mục nếu nó chưa có.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

// Tạo một sổ làm việc mới.
Workbook wb = new Workbook();

// Tạo một đối tượng trang tính và lấy trang tính đầu tiên.
Worksheet sheet = wb.Worksheets[0];
```

Đảm bảo thay thế "THƯ MỤC TÀI LIỆU CỦA BẠN" bằng đường dẫn thư mục thực tế mà bạn muốn lưu tệp Excel.

## Xác định đối tượng Style và Style Flag

Để đặt kiểu cụ thể và cờ bảo vệ cho các cột, chúng ta cần xác định đối tượng kiểu và cờ kiểu. Đây là đoạn mã:

```csharp
// Xác định đối tượng phong cách.
Style style;

// Xác định đối tượng cờ kiểu.
StyleFlag flag;
```

## Lặp qua các cột và mở khóa chúng

Tiếp theo, chúng ta cần lặp qua tất cả các cột trong bảng tính và mở khóa chúng. Điều này sẽ đảm bảo rằng tất cả các cột đều có thể chỉnh sửa được ngoại trừ cột mà chúng tôi muốn bảo vệ. Đây là đoạn mã:

```csharp
// Lặp lại tất cả các cột trong bảng tính và mở khóa chúng.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Khóa một cột cụ thể

Bây giờ, hãy khóa một cột cụ thể. Trong ví dụ này, chúng tôi sẽ khóa cột đầu tiên (chỉ mục cột 0). Đây là đoạn mã:

```csharp
// Lấy kiểu cột đầu tiên.
style = sheet.Cells.Columns[0].Style;

// Khóa nó lại.
style.IsLocked = true;
```

## Áp dụng kiểu cho cột

Sau khi khóa cột cụ thể, chúng ta cần áp dụng kiểu và gắn cờ cho cột đó. Đây là đoạn mã:

```csharp
//Khởi tạo cờ.
flag = new StyleFlag();

// Đặt cài đặt khóa.
flag.Locked = true;

// Áp dụng kiểu cho cột đầu tiên.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## Bảo vệ bảng tính

Để hoàn thiện việc bảo vệ, chúng ta cần bảo vệ bảng tính để đảm bảo rằng các cột bị khóa không thể sửa đổi được. Đây là đoạn mã:

```csharp
// Bảo vệ tờ giấy.
sheet.Protect(ProtectionType.All);
```

## Lưu tệp Excel

Cuối cùng, chúng ta sẽ lưu file Excel đã sửa đổi vào vị trí mong muốn. Đây là đoạn mã:

```csharp
// Lưu tập tin excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Đảm bảo thay thế "output.out.xls" bằng tên và phần mở rộng tệp mong muốn.

### Mã nguồn mẫu cho Bảo vệ cột cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo thư mục nếu nó chưa có.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Tạo một sổ làm việc mới.
Workbook wb = new Workbook();
// Tạo một đối tượng trang tính và lấy trang tính đầu tiên.
Worksheet sheet = wb.Worksheets[0];
// Xác định đối tượng phong cách.
Style style;
// Xác định đối tượng styleflag.
StyleFlag flag;
// Lặp lại tất cả các cột trong bảng tính và mở khóa chúng.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
// Lấy kiểu cột đầu tiên.
style = sheet.Cells.Columns[0].Style;
// Khóa nó lại.
style.IsLocked = true;
//Khởi tạo cờ.
flag = new StyleFlag();
// Đặt cài đặt khóa.
flag.Locked = true;
// Áp dụng kiểu cho cột đầu tiên.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
// Bảo vệ tờ giấy.
sheet.Protect(ProtectionType.All);
// Lưu tập tin excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã giải thích quy trình từng bước để bảo vệ một cột cụ thể trong bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Chúng tôi bắt đầu bằng cách tạo một sổ làm việc và trang tính mới, xác định kiểu và đối tượng cờ kiểu, sau đó tiến hành mở khóa và khóa các cột cụ thể. Cuối cùng, chúng tôi đã bảo vệ bảng tính và lưu tệp Excel đã sửa đổi. Bằng cách làm theo hướng dẫn này, giờ đây bạn có thể bảo vệ các cột cụ thể trong bảng tính Excel bằng C# và Aspose.Cells cho .NET.

### Câu hỏi thường gặp (FAQ)

#### Tôi có thể bảo vệ nhiều cột bằng phương pháp này không?

Có, bạn có thể bảo vệ nhiều cột bằng cách sửa đổi mã cho phù hợp. Chỉ cần lặp qua phạm vi cột mong muốn và áp dụng các kiểu khóa và cờ.

#### Có thể bảo vệ bảng tính được bảo vệ bằng mật khẩu không?

 Có, bạn có thể thêm bảo vệ bằng mật khẩu vào bảng tính được bảo vệ bằng cách chỉ định mật khẩu trong khi gọi`Protect` phương pháp.

#### Aspose.Cells for .NET có hỗ trợ các định dạng tệp Excel khác không?

Có, Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel khác nhau, bao gồm XLS, XLSX, XLSM, v.v.

#### Tôi có thể bảo vệ các hàng cụ thể thay vì các cột không?

Có, bạn có thể sửa đổi mã để bảo vệ các hàng cụ thể thay vì các cột bằng cách áp dụng kiểu và cờ cho các ô hàng thay vì ô cột.