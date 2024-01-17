---
title: Đặt lề Excel
linktitle: Đặt lề Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách đặt lề trong Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 110
url: /vi/net/excel-page-setup/set-excel-margins/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước cách đặt lề trong Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ sử dụng mã nguồn C# để minh họa quy trình.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Đồng thời tạo một dự án mới trong môi trường phát triển ưa thích của bạn.

## Bước 2: Nhập các thư viện cần thiết

Trong tệp mã của bạn, hãy nhập các thư viện cần thiết để làm việc với Aspose.Cells. Đây là mã tương ứng:

```csharp
using Aspose.Cells;
```

## Bước 3: Đặt thư mục dữ liệu

Đặt thư mục dữ liệu nơi bạn muốn lưu tệp Excel đã sửa đổi. Sử dụng mã sau đây:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Hãy chắc chắn chỉ định đường dẫn thư mục đầy đủ.

## Bước 4: Tạo sổ làm việc và bảng tính

Tạo một đối tượng Workbook mới và điều hướng đến trang tính đầu tiên trong sổ làm việc bằng mã sau:

```csharp
Workbook workbook = new Workbook();
WorksheetCollection worksheets = workbook. Worksheets;
Worksheet worksheet = worksheets[0];
```

Thao tác này sẽ tạo một sổ làm việc trống có một trang tính và cung cấp quyền truy cập vào trang tính đó.

## Bước 5: Đặt lề

Truy cập đối tượng PageSetup của trang tính và đặt lề bằng cách sử dụng các thuộc tính BottomMargin, LeftMargin, RightMargin và TopMargin. Đây là một mã mẫu:

```csharp
PageSetup pageSetup = worksheet.PageSetup;
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
```

Điều này sẽ đặt lề dưới, trái, phải và trên cùng của bảng tính tương ứng.

## Bước 6: Lưu sổ làm việc đã sửa đổi

Lưu sổ làm việc đã sửa đổi bằng mã sau:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Điều này sẽ lưu sổ làm việc đã sửa đổi vào thư mục dữ liệu đã chỉ định.

### Mã nguồn mẫu cho Đặt lề Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo một đối tượng sổ làm việc
Workbook workbook = new Workbook();
// Lấy các bảng tính trong sổ làm việc
WorksheetCollection worksheets = workbook.Worksheets;
// Lấy bảng tính (mặc định) đầu tiên
Worksheet worksheet = worksheets[0];
// Lấy đối tượng pagesetup
PageSetup pageSetup = worksheet.PageSetup;
// Đặt lề dưới, trái, phải và trên cùng của trang
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
// Lưu sổ làm việc.
workbook.Save(dataDir + "SetMargins_out.xls");
```

## Phần kết luận

Bây giờ bạn đã học cách đặt lề trong Excel bằng Aspose.Cells cho .NET. Hướng dẫn này hướng dẫn bạn từng bước của quy trình, từ thiết lập môi trường đến lưu sổ làm việc đã sửa đổi. Vui lòng khám phá thêm các tính năng của Aspose.Cells để thực hiện các thao tác tiếp theo trong tệp Excel của bạn.

### Câu hỏi thường gặp (Câu hỏi thường gặp)

#### 1. Làm cách nào tôi có thể chỉ định lề tùy chỉnh cho bảng tính của mình?

 Bạn có thể chỉ định lề tùy chỉnh bằng cách sử dụng`BottomMargin`, `LeftMargin`, `RightMargin` , Và`TopMargin` thuộc tính của`PageSetup` sự vật. Chỉ cần đặt các giá trị mong muốn cho từng thuộc tính để điều chỉnh lề khi cần.

#### 2. Tôi có thể đặt các lề khác nhau cho các trang tính khác nhau trong cùng một sổ làm việc không?

 Có, bạn có thể đặt các lề khác nhau cho mỗi trang tính trong cùng một sổ làm việc. Chỉ cần truy cập vào`PageSetup` đối tượng của từng trang tính riêng lẻ và đặt lề cụ thể cho từng trang tính.

#### 3. Các lề đã xác định có áp dụng cho việc in sổ làm việc không?

Có, lề được đặt bằng Aspose.Cells cũng được áp dụng khi in sổ làm việc. Các lề được chỉ định sẽ được tính đến khi tạo bản in của sổ làm việc.

#### 4. Tôi có thể thay đổi lề của tệp Excel hiện có bằng Aspose.Cells không?

 Có, bạn có thể thay đổi lề của tệp Excel hiện có bằng cách tải tệp bằng Aspose.Cells, truy cập vào từng trang tính`PageSetup` đối tượng và thay đổi giá trị của thuộc tính lề. Sau đó lưu tệp đã sửa đổi để áp dụng lề mới.

#### 5. Làm cách nào để xóa lề khỏi bảng tính?

 Để xóa lề khỏi trang tính, bạn chỉ cần đặt giá trị của`BottomMargin`, `LeftMargin`, `RightMargin` Và`TopMargin` thuộc tính về không. Điều này sẽ đặt lại lề về mặc định (thường là 0).