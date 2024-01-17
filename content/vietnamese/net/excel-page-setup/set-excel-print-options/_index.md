---
title: Đặt tùy chọn in Excel
linktitle: Đặt tùy chọn in Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách thao tác với tệp Excel và tùy chỉnh các tùy chọn in một cách dễ dàng bằng cách sử dụng Aspose.Cells for .NET.
type: docs
weight: 150
url: /vi/net/excel-page-setup/set-excel-print-options/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn cách đặt tùy chọn in cho sổ làm việc Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ hướng dẫn bạn từng bước qua mã nguồn C# được cung cấp để hoàn thành nhiệm vụ này.

## Bước 1: Thiết lập môi trường

Trước khi bắt đầu, hãy đảm bảo bạn đã thiết lập môi trường phát triển của mình và cài đặt Aspose.Cells cho .NET. Bạn có thể tải xuống phiên bản mới nhất của thư viện từ trang web chính thức của Aspose.

## Bước 2: Nhập các không gian tên bắt buộc

Trong dự án C# của bạn, hãy nhập các vùng tên cần thiết để hoạt động với Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Bước 3: Thiết lập đường dẫn đến thư mục tài liệu

 Khai báo một`dataDir` biến để chỉ định đường dẫn đến thư mục mà bạn muốn lưu tệp Excel đã tạo:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENT_DIRECTORY"` với đường dẫn chính xác trên hệ thống của bạn.

## Bước 4: Tạo đối tượng sổ làm việc

Khởi tạo một đối tượng Workbook đại diện cho sổ làm việc Excel mà bạn muốn tạo:

```csharp
Workbook workbook = new Workbook();
```

## Bước 5: Lấy tham chiếu PageSetup của bảng tính

Để đặt các tùy chọn in, trước tiên chúng ta cần lấy tham chiếu PageSetup từ bảng tính. Sử dụng đoạn mã sau để có được tài liệu tham khảo:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Bước 6: Kích hoạt tính năng in đường lưới

Để cho phép in các đường lưới, hãy sử dụng mã sau:

```csharp
pageSetup. PrintGridlines = true;
```

## Bước 7: Kích hoạt tính năng in tiêu đề hàng/cột

Để cho phép in tiêu đề hàng và cột, hãy sử dụng mã sau:

```csharp
pageSetup.PrintHeadings = true;
```

## Bước 8: Kích hoạt chế độ in đen trắng

Để bật in trang tính ở chế độ đen trắng, hãy sử dụng mã sau:

```csharp
pageSetup.BlackAndWhite = true;
```

## Bước 9: Kích hoạt tính năng in phản hồi

Để cho phép in nhận xét khi chúng xuất hiện trên bảng tính, hãy sử dụng mã sau:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Bước 10: Kích hoạt tính năng in ở chế độ nháp

Để bật in bảng tính ở chế độ nháp, hãy sử dụng mã sau:

```csharp
pageSetup.PrintDraft = true;
```

## Bước 11: Kích hoạt tính năng in lỗi ô dưới dạng N/A

Để cho phép in lỗi ô dưới dạng

  hơn N/A, hãy sử dụng mã sau:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Bước 12: Lưu sổ làm việc Excel

 Để lưu sổ làm việc Excel với bộ tùy chọn in, hãy sử dụng`Save` phương thức của đối tượng Workbook:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Thao tác này sẽ lưu sổ làm việc Excel có tên tệp "OtherPrintOptions_out.xls" trong thư mục đã chỉ định.

### Mã nguồn mẫu cho Đặt tùy chọn in Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Lấy tham chiếu PageSetup của bảng tính
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Cho phép in đường lưới
pageSetup.PrintGridlines = true;
// Cho phép in tiêu đề hàng/cột
pageSetup.PrintHeadings = true;
// Cho phép in bảng tính ở chế độ đen trắng
pageSetup.BlackAndWhite = true;
// Cho phép in chú thích hiển thị trên bảng tính
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Cho phép in bảng tính với chất lượng nháp
pageSetup.PrintDraft = true;
// Cho phép in lỗi ô dưới dạng N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Lưu sổ làm việc.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Phần kết luận

Bây giờ bạn đã học cách đặt tùy chọn in cho sổ làm việc Excel bằng Aspose.Cells for .NET. Thư viện mạnh mẽ và thân thiện với người dùng này cho phép bạn tùy chỉnh cài đặt in của sổ làm việc Excel một cách dễ dàng và hiệu quả.

### Câu hỏi thường gặp


#### 1. Tôi có thể tùy chỉnh thêm các tùy chọn in, chẳng hạn như lề hoặc hướng trang không?

Có, Aspose.Cells for .NET cung cấp nhiều tùy chọn in có thể tùy chỉnh, chẳng hạn như lề, hướng trang, tỷ lệ, v.v.

#### 2. Aspose.Cells for .NET có hỗ trợ các định dạng tệp Excel khác không?

Có, Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel khác nhau, chẳng hạn như XLSX, XLS, CSV, HTML, PDF, v.v.

#### 3. Aspose.Cells for .NET có tương thích với tất cả các phiên bản .NET Framework không?

Aspose.Cells for .NET tương thích với .NET Framework 2.0 trở lên, bao gồm các phiên bản 3.5, 4.0, 4.5, 4.6, v.v.