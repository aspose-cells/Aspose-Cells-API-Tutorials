---
title: Bảo vệ các ô trong bảng tính Excel
linktitle: Bảo vệ các ô trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách bảo vệ các ô cụ thể trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 30
url: /vi/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel là một công cụ được sử dụng rộng rãi để tạo và quản lý bảng tính. Một trong những tính năng cốt lõi của Excel là khả năng bảo vệ một số ô nhất định để duy trì tính toàn vẹn của dữ liệu. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để bảo vệ các ô cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET. Aspose.Cells for .NET là một thư viện lập trình mạnh mẽ giúp bạn dễ dàng thao tác với các tệp Excel với tính linh hoạt cao và các tính năng nâng cao. Hãy làm theo các bước được cung cấp để tìm hiểu cách bảo vệ các ô quan trọng và giữ an toàn cho dữ liệu của bạn.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells for .NET trong môi trường phát triển của mình. Tải xuống thư viện từ trang web chính thức của Aspose và kiểm tra tài liệu để biết hướng dẫn cài đặt.

## Bước 2: Khởi tạo Workbook và Worksheet

Để bắt đầu, chúng ta cần tạo một sổ làm việc mới và lấy tham chiếu đến trang tính mà chúng ta muốn bảo vệ các ô. Sử dụng mã sau đây:

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Tạo thư mục nếu nó chưa tồn tại.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Tạo một sổ làm việc mới
Workbook workbook = new Workbook();

// Nhận bảng tính đầu tiên
Worksheet sheet = workbook.Worksheets[0];
```

 Trong đoạn mã này, trước tiên chúng ta xác định đường dẫn đến thư mục nơi tệp Excel sẽ được lưu. Tiếp theo, chúng ta tạo một phiên bản mới của`Workbook` lớp và lấy tham chiếu đến bảng tính đầu tiên bằng cách sử dụng`Worksheets` tài sản.

## Bước 3: Xác định kiểu ô

Bây giờ chúng ta cần xác định kiểu của các ô mà chúng ta muốn bảo vệ. Sử dụng mã sau đây:

```csharp
// Xác định đối tượng kiểu
Styling styling;

// Lặp lại tất cả các cột trong bảng tính và mở khóa chúng
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 Trong mã này, chúng tôi sử dụng vòng lặp để lặp qua tất cả các cột trong trang tính và mở khóa các ô của chúng bằng cách đặt kiểu`IsLocked` tài sản để`false` . Sau đó chúng tôi sử dụng`ApplyStyle` phương pháp áp dụng kiểu cho các cột bằng`StyleFlag` cờ để khóa các ô.

## Bước 4: Bảo vệ các tế bào cụ thể

Bây giờ chúng ta sẽ bảo vệ các ô cụ thể mà chúng ta muốn khóa. Sử dụng mã sau đây:

```csharp
// Khóa 3 ô: A1, B1, C1
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

 Trong mã này, chúng ta lấy kiểu của từng ô cụ thể bằng cách sử dụng`GetStyle` phương pháp, và sau đó chúng tôi thiết lập`IsLocked` thuộc tính của phong cách để`true`để khóa ô. Cuối cùng, chúng tôi áp dụng kiểu đã cập nhật cho từng ô bằng cách sử dụng`SetStyle` phương pháp.

## Bước 5: Bảo vệ bảng tính

Bây giờ chúng ta đã xác định được các ô cần bảo vệ, chúng ta có thể bảo vệ chính bảng tính đó. Sử dụng mã sau đây:

```csharp
// Bảo vệ bảng tính
leaf.Protect(ProtectionType.All);
```

 Mã này sử dụng`Protect` phương pháp bảo vệ bảng tính với loại bảo vệ được chỉ định, trong trường hợp này`ProtectionType.All` để bảo vệ tất cả các mục trong bảng tính.

## Bước 6: Lưu file Excel

Cuối cùng, chúng ta lưu file Excel với những thay đổi đã thực hiện. Sử dụng mã sau đây:

```csharp
// Lưu tệp Excel
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 Trong mã này, chúng tôi sử dụng`Save` phương pháp lưu sổ làm việc vào thư mục đã chỉ định bằng`Excel97To2003` định dạng.

### Mã nguồn mẫu cho Bảo vệ ô trong bảng tính Excel bằng Aspose.Cells cho .NET 
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
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách bảo vệ các ô cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET. Bây giờ bạn có thể áp dụng kỹ thuật này trong các dự án của riêng mình và cải thiện tính bảo mật của tệp Excel.


### Câu hỏi thường gặp

#### Hỏi: Tại sao tôi nên sử dụng Aspose.Cells cho .NET để bảo vệ các ô trong bảng tính Excel?

Đáp: Aspose.Cells for .NET là một thư viện mạnh mẽ giúp bạn dễ dàng làm việc với các tệp Excel. Nó cung cấp các tính năng nâng cao để bảo vệ các ô, mở khóa phạm vi, v.v.

#### Câu hỏi: Có thể bảo vệ phạm vi ô thay vì từng ô riêng lẻ không?

 Đáp: Có, bạn có thể xác định các phạm vi ô cụ thể để bảo vệ bằng cách sử dụng`ApplyStyle` bằng phương pháp thích hợp`StyleFlag`.

#### Hỏi: Làm cách nào tôi có thể mở tệp Excel được bảo vệ sau khi lưu?

Trả lời: Khi mở tệp Excel được bảo vệ, bạn sẽ cần cung cấp mật khẩu được chỉ định khi bảo vệ bảng tính.

#### Hỏi: Có loại bảo vệ nào khác mà tôi có thể áp dụng cho bảng tính Excel không?

Trả lời: Có, Aspose.Cells for .NET hỗ trợ nhiều loại bảo vệ, chẳng hạn như bảo vệ cấu trúc, bảo vệ cửa sổ, v.v. Bạn có thể chọn loại bảo vệ thích hợp theo nhu cầu của mình.