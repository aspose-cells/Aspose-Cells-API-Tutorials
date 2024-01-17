---
title: Bảo vệ hàng cụ thể trong bảng tính Excel
linktitle: Bảo vệ hàng cụ thể trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Bảo vệ một hàng cụ thể trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước để bảo mật dữ liệu bí mật của bạn.
type: docs
weight: 90
url: /vi/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Việc bảo vệ dữ liệu bí mật trong bảng tính Excel là điều cần thiết để đảm bảo an toàn thông tin. Aspose.Cells for .NET cung cấp một giải pháp mạnh mẽ để bảo vệ các hàng cụ thể trong bảng tính Excel. Hướng dẫn này sẽ hướng dẫn bạn cách bảo vệ một hàng cụ thể trong bảng tính Excel bằng mã nguồn C# được cung cấp. Hãy làm theo các bước đơn giản sau để thiết lập tính năng bảo vệ hàng trong tệp Excel của bạn.

## Bước 1: Nhập thư viện cần thiết

Để bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên hệ thống của mình. Bạn cũng cần thêm các tham chiếu thích hợp vào dự án C# của mình để có thể sử dụng chức năng của Aspose.Cells. Đây là mã để nhập các thư viện cần thiết:

```csharp
// Thêm tài liệu tham khảo cần thiết
using Aspose.Cells;
```

## Bước 2: Tạo sổ làm việc và bảng tính Excel

Sau khi nhập các thư viện cần thiết, bạn có thể tạo sổ làm việc Excel mới và trang tính mới. Đây là cách thực hiện:

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENTS DIRECTORY";

// Tạo một thư mục nếu nó chưa tồn tại.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

// Tạo một sổ làm việc mới.
Workbook wb = new Workbook();

// Tạo một đối tượng bảng tính và lấy trang tính đầu tiên.
Worksheet sheet = wb.Worksheets[0];
```

## Bước 3: Đặt kiểu và cờ kiểu

Bây giờ chúng ta sẽ đặt kiểu ô và cờ kiểu để mở khóa tất cả các cột trong bảng tính. Đây là mã cần thiết:

```csharp
// Đặt đối tượng kiểu.
Styling styling;

// Đặt đối tượng styleflag.
StyleFlag flag;

// Lặp lại tất cả các cột trong bảng tính và mở khóa chúng.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## Bước 4: Bảo vệ dòng cụ thể

Bây giờ chúng ta sẽ bảo vệ hàng cụ thể trong bảng tính. Chúng tôi sẽ khóa hàng đầu tiên để ngăn chặn mọi sửa đổi. Đây là cách thực hiện:

```csharp
// Lấy phong cách của dòng đầu tiên.
style = sheet.Cells.Rows[0].Style;

// Khóa nó lại.
style. IsLocked = true;

//Khởi tạo cờ.
flag = new StyleFlag();

// Đặt tham số khóa.
flag. Locked = true;

// Áp dụng kiểu cho dòng đầu tiên.
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## Bước 5: Bảo vệ bảng tính

Cuối cùng, chúng ta sẽ bảo vệ toàn bộ bảng tính Excel để ngăn chặn những sửa đổi trái phép. Đây là cách thực hiện:

```csharp
// Bảo vệ bảng tính.
sheet.Protect(ProtectionType.All);
```

## Bước 6: Lưu file Excel được bảo vệ

Khi bạn hoàn tất việc bảo vệ hàng cụ thể trong bảng tính Excel, bạn có thể lưu tệp Excel được bảo vệ vào hệ thống của mình. Đây là cách thực hiện:

```csharp
// Lưu tệp Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Sau khi làm theo các bước này, bạn sẽ bảo vệ thành công một hàng cụ thể trong bảng tính Excel của mình bằng Aspose.Cells for .NET.

### Mã nguồn mẫu cho Bảo vệ hàng cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET 
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

Việc bảo vệ dữ liệu trong file Excel là rất quan trọng để ngăn chặn sự truy cập trái phép hoặc sửa đổi không mong muốn. Bằng cách sử dụng thư viện Aspose.Cells cho .NET, bạn có thể dễ dàng bảo vệ các hàng cụ thể trong bảng tính Excel bằng mã nguồn C# được cung cấp. Hãy làm theo hướng dẫn từng bước này để thêm lớp bảo mật bổ sung cho tệp Excel của bạn.

### Câu hỏi thường gặp

#### Tính năng bảo vệ hàng cụ thể có hoạt động trong tất cả các phiên bản Excel không?

Có, tính năng bảo vệ hàng cụ thể bằng Aspose.Cells for .NET hoạt động trong tất cả các phiên bản Excel được hỗ trợ.

#### Tôi có thể bảo vệ nhiều hàng cụ thể trong bảng tính Excel không?

Có, bạn có thể bảo vệ nhiều hàng cụ thể bằng các phương pháp tương tự được mô tả trong hướng dẫn này.

#### Làm cách nào tôi có thể mở khóa một hàng cụ thể trong bảng tính Excel?

 Để mở khóa một hàng cụ thể, bạn phải sửa đổi mã nguồn cho phù hợp bằng cách sử dụng`IsLocked` phương pháp của`Style` sự vật.