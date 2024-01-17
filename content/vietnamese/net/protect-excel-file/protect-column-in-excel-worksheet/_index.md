---
title: Bảo vệ cột trong bảng tính Excel
linktitle: Bảo vệ cột trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách bảo vệ một cột cụ thể trong Excel bằng Aspose.Cells for .NET. Các bước chi tiết và mã nguồn được bao gồm.
type: docs
weight: 40
url: /vi/net/protect-excel-file/protect-column-in-excel-worksheet/
---
Microsoft Excel là một ứng dụng phổ biến để quản lý và phân tích dữ liệu dưới dạng bảng tính. Việc bảo vệ dữ liệu nhạy cảm là điều cần thiết để đảm bảo tính toàn vẹn và bảo mật thông tin. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để bảo vệ một cột cụ thể trong bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Aspose.Cells for .NET cung cấp các tính năng mạnh mẽ để xử lý và bảo vệ các tệp Excel. Hãy làm theo các bước được cung cấp để tìm hiểu cách bảo vệ dữ liệu của bạn trong một cột cụ thể và bảo mật bảng tính Excel của bạn.
## Bước 1: Thiết lập thư mục

Bắt đầu bằng cách xác định thư mục nơi bạn muốn lưu tệp Excel. Sử dụng mã sau đây:

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Tạo thư mục nếu nó không tồn tại.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);
```

Mã này kiểm tra xem thư mục đã tồn tại chưa và tạo nó nếu chưa.

## Bước 2: Tạo sổ làm việc mới

Tiếp theo, chúng ta sẽ tạo một sổ làm việc Excel mới và lấy bảng tính đầu tiên. Sử dụng mã sau đây:

```csharp
// Tạo một sổ làm việc mới.
Workbook workbook = new Workbook();
// Tạo một đối tượng bảng tính và lấy trang tính đầu tiên.
Worksheet sheet = workbook.Worksheets[0];
```

 Mã này tạo ra một cái mới`Workbook` đối tượng và lấy bảng tính đầu tiên bằng cách sử dụng`Worksheets[0]`.

## Bước 3: Mở khóa cột

Để mở khóa tất cả các cột trong trang tính, chúng tôi sẽ sử dụng vòng lặp để lặp qua tất cả các cột và áp dụng kiểu mở khóa. Sử dụng mã sau đây:

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
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

 Mã này lặp qua từng cột trong bảng tính và mở khóa kiểu bằng cách cài đặt`IsLocked` ĐẾN`false`.

## Bước 4: Khóa một cột cụ thể

Bây giờ chúng ta sẽ khóa một cột cụ thể bằng cách áp dụng kiểu bị khóa. Sử dụng mã sau đây:

```csharp
// Lấy phong cách của cột đầu tiên.
style = sheet.Cells.Columns[0].Style;
// Khóa nó lại.
style. IsLocked = true;
// Khởi tạo đối tượng cờ.
flag = new StyleFlag();
// Đặt tham số khóa.
flag. Locked = true;
// Áp dụng kiểu cho cột đầu tiên.
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

 Mã này chọn cột đầu tiên bằng cách sử dụng`Columns[0]` , sau đó đặt kiểu`IsLocked` ĐẾN`true` để khóa cột. Cuối cùng, chúng tôi áp dụng kiểu cho cột đầu tiên bằng cách sử dụng`ApplyStyle` phương pháp.

## Bước 5: Bảo vệ bảng tính

Bây giờ chúng ta đã khóa cột cụ thể, chúng ta có thể bảo vệ bảng tính đó. Sử dụng mã sau đây:



```csharp
// Bảo vệ bảng tính.
leaf.Protect(ProtectionType.All);
```

 Mã này sử dụng`Protect` phương pháp bảo vệ bảng tính bằng cách chỉ định loại bảo vệ.

## Bước 6: Lưu file Excel

Cuối cùng, chúng ta lưu file Excel bằng đường dẫn thư mục và tên file mong muốn. Sử dụng mã sau đây:

```csharp
// Lưu tệp Excel.
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

 Mã này sử dụng`Save` phương pháp của`Workbook` đối tượng lưu file Excel với tên và định dạng file đã chỉ định.

### Mã nguồn mẫu cho Bảo vệ cột trong bảng tính Excel bằng Aspose.Cells cho .NET 
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

Bạn vừa làm theo hướng dẫn từng bước để bảo vệ một cột trong bảng tính Excel bằng Aspose.Cells cho .NET. Bạn đã học cách mở khóa tất cả các cột, khóa một cột cụ thể và bảo vệ trang tính. Giờ đây, bạn có thể áp dụng những khái niệm này cho dự án của riêng mình và bảo mật dữ liệu Excel của mình.

## Các câu hỏi thường gặp

#### Hỏi: Tại sao việc bảo vệ các cột cụ thể trong bảng tính Excel lại quan trọng?

Trả lời: Bảo vệ các cột cụ thể trong bảng tính Excel giúp hạn chế quyền truy cập và sửa đổi dữ liệu nhạy cảm, do đó đảm bảo tính toàn vẹn và bảo mật thông tin.

#### Câu hỏi: Aspose.Cells for .NET có hỗ trợ các tính năng khác để xử lý tệp Excel không?

Trả lời: Có, Aspose.Cells for .NET cung cấp nhiều tính năng bao gồm tạo, chỉnh sửa, chuyển đổi và báo cáo tệp Excel.

#### Hỏi: Làm cách nào tôi có thể mở khóa tất cả các cột trong bảng tính Excel?

Trả lời: Trong Aspose.Cells dành cho .NET, bạn có thể sử dụng vòng lặp để lặp qua tất cả các cột và đặt kiểu khóa thành "false" để mở khóa tất cả các cột.

#### Câu hỏi: Làm cách nào tôi có thể bảo vệ bảng tính Excel bằng Aspose.Cells cho .NET?

 Đáp: Bạn có thể sử dụng`Protect` phương pháp của đối tượng bảng tính để bảo vệ bảng tính với các mức độ bảo vệ khác nhau như bảo vệ cấu trúc, bảo vệ ô, v.v.

#### Hỏi: Tôi có thể áp dụng các khái niệm bảo vệ cột này trong các loại tệp Excel khác không?

Đáp: Có, các khái niệm bảo vệ cột trong Aspose.Cells dành cho .NET có thể áp dụng cho tất cả các loại tệp Excel, chẳng hạn như tệp Excel 97-2003 (.xls) và các tệp Excel mới hơn (.xlsx).