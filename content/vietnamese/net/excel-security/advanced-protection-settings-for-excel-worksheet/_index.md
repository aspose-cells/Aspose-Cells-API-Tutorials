---
title: Cài đặt bảo vệ nâng cao cho bảng tính Excel
linktitle: Cài đặt bảo vệ nâng cao cho bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Bảo vệ các tệp Excel của bạn bằng cách đặt cài đặt bảo vệ nâng cao với Aspose.Cells for .NET.
type: docs
weight: 10
url: /vi/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn các bước để đặt cài đặt bảo vệ nâng cao cho bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Thực hiện theo các hướng dẫn dưới đây để hoàn thành nhiệm vụ này.

## Bước 1: Chuẩn bị

Đảm bảo bạn đã cài đặt Aspose.Cells cho .NET và tạo dự án C# trong môi trường phát triển tích hợp (IDE) ưa thích của bạn.

## Bước 2: Đặt đường dẫn thư mục tài liệu

 Khai báo một`dataDir` biến và khởi tạo nó bằng đường dẫn đến thư mục tài liệu của bạn. Ví dụ :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENTS_DIRECTORY"` với đường dẫn thực tế đến thư mục của bạn.

## Bước 3: Tạo luồng file mở file Excel

 Tạo một`FileStream` đối tượng chứa file Excel cần mở:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Đảm bảo bạn có tệp Excel`book1.xls` trong thư mục tài liệu của bạn hoặc chỉ định tên tệp và vị trí chính xác.

## Bước 4: Khởi tạo đối tượng Workbook và mở tệp Excel

 Sử dụng`Workbook`lớp từ Aspose.Cells để khởi tạo một đối tượng Workbook và mở tệp Excel được chỉ định thông qua luồng tệp:

```csharp
Workbook excel = new Workbook(fstream);
```

## Bước 5: Truy cập bảng tính đầu tiên

Điều hướng đến bảng tính đầu tiên của tệp Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Bước 6: Đặt cài đặt bảo vệ bảng tính

Sử dụng thuộc tính đối tượng Trang tính để đặt cài đặt bảo vệ trang tính nếu cần. Ví dụ :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Đặt các cài đặt bảo vệ khác nếu cần...
```

## Bước 7: Lưu file Excel đã sửa đổi

 Lưu tệp Excel đã sửa đổi bằng cách sử dụng`Save` phương thức của đối tượng Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Đảm bảo chỉ định đường dẫn và tên tệp mong muốn cho tệp đầu ra.

## Bước 8: Đóng luồng tệp

Sau khi lưu, hãy đóng luồng tệp để giải phóng tất cả các tài nguyên liên quan:

```csharp
fstream.Close();
```
	
### Mã nguồn mẫu cho Cài đặt bảo vệ nâng cao cho bảng tính Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel thông qua luồng tệp
Workbook excel = new Workbook(fstream);
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = excel.Worksheets[0];
// Hạn chế người dùng xóa các cột của bảng tính
worksheet.Protection.AllowDeletingColumn = false;
// Hạn chế người dùng xóa hàng của bảng tính
worksheet.Protection.AllowDeletingRow = false;
// Hạn chế người dùng chỉnh sửa nội dung của bảng tính
worksheet.Protection.AllowEditingContent = false;
// Hạn chế người dùng chỉnh sửa các đối tượng của bảng tính
worksheet.Protection.AllowEditingObject = false;
// Hạn chế người dùng chỉnh sửa các kịch bản của bảng tính
worksheet.Protection.AllowEditingScenario = false;
//Hạn chế người dùng lọc
worksheet.Protection.AllowFiltering = false;
// Cho phép người dùng định dạng các ô của bảng tính
worksheet.Protection.AllowFormattingCell = true;
// Cho phép người dùng định dạng các hàng của bảng tính
worksheet.Protection.AllowFormattingRow = true;
// Cho phép người dùng chèn cột vào bảng tính
worksheet.Protection.AllowFormattingColumn = true;
// Cho phép người dùng chèn siêu liên kết vào bảng tính
worksheet.Protection.AllowInsertingHyperlink = true;
// Cho phép người dùng chèn hàng vào bảng tính
worksheet.Protection.AllowInsertingRow = true;
// Cho phép người dùng chọn các ô bị khóa của bảng tính
worksheet.Protection.AllowSelectingLockedCell = true;
// Cho phép người dùng chọn các ô đã mở khóa của bảng tính
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Cho phép người dùng sắp xếp
worksheet.Protection.AllowSorting = true;
// Cho phép người dùng sử dụng bảng tổng hợp trong bảng tính
worksheet.Protection.AllowUsingPivotTable = true;
// Lưu tệp Excel đã sửa đổi
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách đặt cài đặt bảo vệ nâng cao cho bảng tính Excel bằng Aspose.Cells for .NET. Sử dụng kiến thức này để bảo mật các tệp Excel của bạn và hạn chế hành động của người dùng.

### Câu hỏi thường gặp

#### Câu hỏi: Làm cách nào để tạo dự án C# mới trong IDE của tôi?

Đáp: Các bước để tạo dự án C# mới có thể khác nhau tùy thuộc vào IDE bạn đang sử dụng. Tham khảo tài liệu IDE của bạn để biết hướng dẫn chi tiết.

#### Hỏi: Có thể đặt cài đặt bảo vệ tùy chỉnh khác với những cài đặt được đề cập trong hướng dẫn không?

Trả lời: Có, Aspose.Cells cung cấp nhiều cài đặt bảo vệ mà bạn có thể tùy chỉnh theo nhu cầu cụ thể của mình. Xem tài liệu Aspose.Cells để biết thêm chi tiết.

#### Hỏi: Định dạng tệp được sử dụng để lưu tệp Excel đã sửa đổi trong mã mẫu là gì?

Đáp: Trong mã mẫu, tệp Excel đã sửa đổi được lưu ở định dạng Excel 97-2003 (.xls). Bạn có thể chọn các định dạng khác được Aspose.Cells hỗ trợ nếu cần.

#### Hỏi: Làm cách nào tôi có thể truy cập các trang tính khác trong tệp Excel?

 Đáp: Bạn có thể truy cập các trang tính khác bằng chỉ mục hoặc tên trang tính, ví dụ:`Worksheet worksheet = excel.Worksheets[1];` hoặc`Worksheet worksheet = excel.Worksheets[" SheetName"];`.