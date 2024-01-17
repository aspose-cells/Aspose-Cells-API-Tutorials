---
title: Bảo vệ các ô cụ thể trong bảng tính Excel
linktitle: Bảo vệ các ô cụ thể trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách bảo vệ các ô cụ thể trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 70
url: /vi/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Trong hướng dẫn này, chúng ta sẽ xem xét mã nguồn C# sử dụng thư viện Aspose.Cells để bảo vệ các ô cụ thể trong bảng tính Excel. Chúng tôi sẽ đi qua từng bước của mã và giải thích cách hoạt động của mã. Thực hiện theo các hướng dẫn cẩn thận để có được kết quả mong muốn.

## Bước 1: Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt thư viện Aspose.Cells cho .NET. Bạn có thể lấy nó từ trang web chính thức của Aspose. Ngoài ra, hãy đảm bảo rằng bạn có phiên bản Visual Studio mới hoặc bất kỳ môi trường phát triển C# nào khác.

## Bước 2: Nhập các không gian tên bắt buộc

Để sử dụng thư viện Aspose.Cells, chúng ta cần nhập các vùng tên cần thiết vào mã của mình. Thêm các dòng sau vào đầu tệp nguồn C# của bạn:

```csharp
using Aspose.Cells;
```

## Bước 3: Tạo sổ làm việc Excel

Trong bước này, chúng ta sẽ tạo một sổ làm việc Excel mới. Sử dụng đoạn mã sau để tạo sổ làm việc Excel:

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Tạo một sổ làm việc mới.
Workbook wb = new Workbook();
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENTS_DIR"` với đường dẫn thích hợp tới thư mục tài liệu của bạn.

## Bước 4: Tạo bảng tính

Bây giờ chúng ta đã tạo sổ làm việc Excel, hãy tạo một bảng tính và lấy trang tính đầu tiên. Sử dụng mã sau đây:

```csharp
// Tạo một đối tượng bảng tính và lấy trang tính đầu tiên.
Worksheet sheet = wb.Worksheets[0];
```

## Bước 5: Xác định kiểu

Trong bước này, chúng ta sẽ xác định kiểu để áp dụng cho các ô cụ thể. Sử dụng mã sau đây:

```csharp
// Định nghĩa đối tượng phong cách
Styling styling;
```

## Bước 6: Lặp lại để mở khóa tất cả các cột

Bây giờ chúng ta sẽ lặp qua tất cả các cột trong bảng tính và mở khóa chúng. Sử dụng mã sau đây:

```csharp
// Lặp lại tất cả các cột trong bảng tính và mở khóa chúng.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Bước 7: Khóa các ô cụ thể

Ở bước này, chúng ta sẽ khóa các ô cụ thể. Sử dụng mã sau đây:

```csharp
//Khóa cả 3 ô... tức là A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Bước 8: Bảo vệ bảng tính

Cuối cùng, chúng tôi sẽ bảo vệ bảng tính để ngăn các ô cụ thể bị sửa đổi. Sử dụng mã sau đây:

```csharp
// Bảo vệ bảng tính.
sheet.Protect(ProtectionType.All);
```

## Bước 9: Lưu file Excel

Bây giờ chúng ta sẽ lưu tệp Excel đã sửa đổi. Sử dụng mã sau đây:

```csharp
// Lưu tệp Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Đảm bảo chỉ định đúng đường dẫn để lưu tệp Excel đã sửa đổi.

### Mã nguồn mẫu cho Bảo vệ các ô cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET 
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
// Xác định đối tượng styleflag
StyleFlag styleflag;
// Lặp lại tất cả các cột trong bảng tính và mở khóa chúng.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Khóa 3 ô... tức là A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Cuối cùng, Bảo vệ trang tính ngay bây giờ.
sheet.Protect(ProtectionType.All);
// Lưu tập tin excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Phần kết luận

Xin chúc mừng! Bây giờ bạn có mã nguồn C# cho phép bạn bảo vệ các ô cụ thể trong bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Hãy thoải mái tùy chỉnh mã cho phù hợp với nhu cầu cụ thể của bạn.

### Câu hỏi thường gặp (Câu hỏi thường gặp)

#### Mã này có hoạt động với các phiên bản Excel gần đây không?

Có, mã này hoạt động với các phiên bản Excel gần đây, bao gồm các tệp ở định dạng Excel 2010 trở lên.

#### Tôi có thể bảo vệ các ô khác ngoài A1, B1 và C1 không?

Có, bạn có thể sửa đổi mã để khóa các ô cụ thể khác bằng cách điều chỉnh tham chiếu ô trong các dòng mã tương ứng.

#### Làm cách nào tôi có thể mở khóa lại các ô bị khóa?

 Bạn có thể dùng`SetStyle` phương pháp với`IsLocked` đặt thành`false` để mở khóa các tế bào.

#### Tôi có thể thêm nhiều bảng tính vào sổ làm việc không?

 Có, bạn có thể thêm các trang tính khác vào sổ làm việc bằng cách sử dụng`Worksheets.Add()`và lặp lại các bước bảo vệ ô cho mỗi bảng tính.

#### Làm cách nào để thay đổi định dạng lưu của tệp Excel?

 Bạn có thể thay đổi định dạng lưu bằng cách sử dụng`SaveFormat` phương thức với định dạng mong muốn, ví dụ`SaveFormat.Xlsx` cho Excel 2007 trở lên.