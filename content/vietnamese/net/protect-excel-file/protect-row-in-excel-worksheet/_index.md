---
title: Bảo vệ hàng trong bảng tính Excel
linktitle: Bảo vệ hàng trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Khám phá trong hướng dẫn này cách bảo vệ các hàng của bảng tính Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 60
url: /vi/net/protect-excel-file/protect-row-in-excel-worksheet/
---
Trong hướng dẫn này, chúng ta sẽ xem xét một số mã nguồn C# sử dụng thư viện Aspose.Cells để bảo vệ các hàng trong bảng tính Excel. Chúng tôi sẽ đi qua từng bước của mã và giải thích cách hoạt động của mã. Thực hiện theo các hướng dẫn cẩn thận để có được kết quả mong muốn.

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

Trong bước này, chúng ta sẽ xác định kiểu áp dụng cho các hàng của bảng tính. Sử dụng mã sau đây:

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

## Bước 7: Khóa dòng đầu tiên

Ở bước này, chúng ta sẽ khóa hàng đầu tiên của bảng tính. Sử dụng mã sau đây:

```csharp
// Lấy phong cách của dòng đầu tiên.
style = sheet.Cells.Rows[0].Style;
// Khóa phong cách.
style. IsLocked = true;
// Áp dụng kiểu cho dòng đầu tiên.
sheet.Cells.ApplyRowStyle(0, style);
```

## Bước 8: Bảo vệ bảng tính

Bây giờ chúng ta đã đặt kiểu và khóa các hàng, hãy bảo vệ bảng tính. Sử dụng mã sau đây:

```csharp
// Bảo vệ bảng tính.
sheet.Protect(ProtectionType.All);
```

## Bước 9: Lưu file Excel

Cuối cùng chúng ta sẽ lưu file Excel đã sửa đổi. Sử dụng mã sau đây:

```csharp
// Lưu tệp Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Đảm bảo chỉ định đúng đường dẫn để lưu tệp Excel đã sửa đổi.

### Mã nguồn mẫu cho Bảng tính Bảo vệ Hàng Trong Excel bằng Aspose.Cells cho .NET 
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
// Lấy kiểu hàng đầu tiên.
style = sheet.Cells.Rows[0].Style;
// Khóa nó lại.
style.IsLocked = true;
//Khởi tạo cờ.
flag = new StyleFlag();
// Đặt cài đặt khóa.
flag.Locked = true;
// Áp dụng kiểu cho hàng đầu tiên.
sheet.Cells.ApplyRowStyle(0, style, flag);
// Bảo vệ tờ giấy.
sheet.Protect(ProtectionType.All);
// Lưu tập tin excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn có mã nguồn C# cho phép bạn bảo vệ các hàng trong bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Hãy nhớ làm theo các bước một cách cẩn thận và tùy chỉnh mã theo nhu cầu cụ thể của bạn.

### Câu hỏi thường gặp (Câu hỏi thường gặp)

#### Mã này có hoạt động với các phiên bản Excel gần đây không?

Có, mã này hoạt động với các phiên bản Excel gần đây, bao gồm các tệp ở định dạng Excel 2010 trở lên.

#### Tôi có thể chỉ bảo vệ các hàng cụ thể thay vì tất cả các hàng trong trang tính không?

Có, bạn có thể sửa đổi mã để chỉ định các hàng cụ thể mà bạn muốn bảo vệ. Bạn sẽ cần phải điều chỉnh vòng lặp và các chỉ số cho phù hợp.

#### Làm cách nào tôi có thể mở khóa lại các dòng bị khóa?

 Bạn có thể dùng`IsLocked` phương pháp của`Style` đối tượng để đặt giá trị thành`false` và mở khóa các hàng.

#### Có thể bảo vệ nhiều bảng tính trong cùng một sổ làm việc Excel không?

Có, bạn có thể lặp lại các bước tạo trang tính, đặt kiểu và bảo vệ cho từng trang tính trong sổ làm việc.

#### Làm cách nào để thay đổi mật khẩu bảo vệ bảng tính?

 Bạn có thể thay đổi mật khẩu bằng cách sử dụng`Protect` phương thức và chỉ định mật khẩu mới làm đối số.