---
title: Quản lý khổ giấy Excel
linktitle: Quản lý khổ giấy Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách quản lý khổ giấy trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước với mã nguồn trong C#.
type: docs
weight: 70
url: /vi/net/excel-page-setup/manage-excel-paper-size/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước cách quản lý khổ giấy trong tài liệu Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ chỉ cho bạn cách định cấu hình khổ giấy bằng mã nguồn C#.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Đồng thời tạo một dự án mới trong môi trường phát triển ưa thích của bạn.

## Bước 2: Nhập các thư viện cần thiết

Trong tệp mã của bạn, hãy nhập các thư viện cần thiết để làm việc với Aspose.Cells. Đây là mã tương ứng:

```csharp
using Aspose.Cells;
```

## Bước 3: Đặt thư mục tài liệu

Đặt thư mục chứa tài liệu Excel mà bạn muốn làm việc. Sử dụng đoạn mã sau để thiết lập thư mục:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Hãy chắc chắn chỉ định đường dẫn thư mục đầy đủ.

## Bước 4: Tạo đối tượng sổ làm việc

Đối tượng Workbook đại diện cho tài liệu Excel mà bạn sẽ làm việc. Bạn có thể tạo nó bằng mã sau:

```csharp
Workbook workbook = new Workbook();
```

Điều này tạo ra một đối tượng Workbook trống mới.

## Bước 5: Truy cập vào bảng tính đầu tiên

Để truy cập bảng tính đầu tiên của tài liệu Excel, hãy sử dụng mã sau:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

Điều này sẽ cho phép bạn làm việc với bảng tính đầu tiên trong sổ làm việc.

## Bước 6: Thiết lập khổ giấy

Sử dụng thuộc tính PageSetup.PaperSize của đối tượng Worksheet để đặt khổ giấy. Trong ví dụ này, chúng tôi sẽ đặt khổ giấy là A4. Đây là mã tương ứng:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Thao tác này sẽ đặt kích thước giấy của bảng tính thành A4.

## Bước 7: Lưu sổ làm việc

Để lưu các thay đổi vào sổ làm việc, hãy sử dụng phương thức Save() của đối tượng Workbook. Đây là mã tương ứng:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Điều này sẽ lưu sổ làm việc với những thay đổi đối với thư mục đã chỉ định.

### Mã nguồn mẫu cho Quản lý kích thước giấy Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Đặt khổ giấy thành A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Lưu sổ làm việc.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Phần kết luận

Bây giờ bạn đã học cách quản lý khổ giấy trong tài liệu Excel bằng Aspose.Cells for .NET. Hướng dẫn này sẽ hướng dẫn bạn từng bước của quy trình, từ thiết lập môi trường đến lưu các thay đổi. Bây giờ bạn có thể sử dụng kiến thức này để tùy chỉnh khổ giấy của tài liệu Excel của mình.

### Câu hỏi thường gặp

#### Câu hỏi 1: Tôi có thể đặt khổ giấy tùy chỉnh khác ngoài A4 không?

Câu trả lời 1: Có, Aspose.Cells hỗ trợ nhiều kích thước giấy được xác định trước cũng như khả năng đặt kích thước giấy tùy chỉnh bằng cách chỉ định kích thước mong muốn.

#### Câu hỏi 2: Làm cách nào để biết khổ giấy hiện tại trong tài liệu Excel?

 A2: Bạn có thể sử dụng`PageSetup.PaperSize` tài sản của`Worksheet` object để có được khổ giấy hiện được đặt.

#### Câu hỏi 3: Có thể đặt thêm lề trang bằng khổ giấy không?

 A3: Có, bạn có thể sử dụng`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` Và`PageSetup.BottomMargin` thuộc tính để đặt lề trang bổ sung ngoài kích thước giấy.

#### Câu hỏi 4: Phương pháp này có áp dụng được với tất cả các định dạng tệp Excel, chẳng hạn như .xls và .xlsx không?

Đáp 4: Có, phương pháp này hoạt động với cả định dạng tệp .xls và .xlsx.

#### Câu hỏi 5: Tôi có thể áp dụng các khổ giấy khác nhau cho các trang tính khác nhau trong cùng một sổ làm việc không?

 Câu trả lời 5: Có, bạn có thể áp dụng các khổ giấy khác nhau cho các trang tính khác nhau trong cùng một sổ làm việc bằng cách sử dụng`PageSetup.PaperSize` thuộc tính của mỗi bảng tính.