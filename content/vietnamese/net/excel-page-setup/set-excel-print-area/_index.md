---
title: Đặt vùng in Excel
linktitle: Đặt vùng in Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hướng dẫn từng bước để đặt vùng in Excel bằng Aspose.Cells cho .NET. Tối ưu hóa và tùy chỉnh sổ làm việc Excel của bạn một cách dễ dàng.
type: docs
weight: 140
url: /vi/net/excel-page-setup/set-excel-print-area/
---
Sử dụng Aspose.Cells cho .NET có thể hỗ trợ rất nhiều cho việc quản lý và thao tác với các tệp Excel trong các ứng dụng .NET. Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách đặt vùng in của sổ làm việc Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ hướng dẫn bạn từng bước thông qua mã nguồn C# được cung cấp để hoàn thành nhiệm vụ này.

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

Để đặt vùng in, trước tiên chúng ta cần lấy tham chiếu từ PageSetup của bảng tính. Sử dụng đoạn mã sau để có được tài liệu tham khảo:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Bước 6: Xác định phạm vi ô vùng in

Bây giờ chúng ta có tham chiếu PageSetup, chúng ta có thể chỉ định phạm vi ô tạo nên vùng in. Trong ví dụ này, chúng tôi sẽ đặt phạm vi ô từ A1 đến T35 làm vùng in. Sử dụng mã sau đây:

```csharp
pageSetup.PrintArea = "A1:T35";
```

Bạn có thể điều chỉnh phạm vi ô theo nhu cầu của bạn.

## Bước 7: Lưu sổ làm việc Excel

 Để lưu sổ làm việc Excel với vùng in được xác định, hãy sử dụng`Save` phương thức của đối tượng Workbook:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

Thao tác này sẽ lưu sổ làm việc Excel có tên tệp "SetPrintArea_out.xls" trong thư mục đã chỉ định.

### Mã nguồn mẫu cho Đặt vùng in Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Lấy tham chiếu PageSetup của bảng tính
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Chỉ định phạm vi ô (từ ô A1 đến ô T35) của vùng in
pageSetup.PrintArea = "A1:T35";
// Lưu sổ làm việc.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách đặt vùng in của sổ làm việc Excel bằng Aspose.Cells cho .NET. Thư viện mạnh mẽ và thân thiện với người dùng này giúp bạn làm việc với các tệp Excel trong ứng dụng .NET của mình dễ dàng hơn nhiều. Nếu bạn có thêm câu hỏi hoặc gặp bất kỳ khó khăn nào, vui lòng xem tài liệu chính thức của Aspose.Cells để biết thêm thông tin và tài nguyên.

### Câu hỏi thường gặp

#### 1. Tôi có thể tùy chỉnh thêm bố cục của vùng in, chẳng hạn như hướng và lề không?

Có, bạn có thể truy cập các thuộc tính PageSetup khác như hướng trang, lề, tỷ lệ, v.v. để tùy chỉnh thêm bố cục vùng in của mình.

#### 2. Aspose.Cells for .NET có hỗ trợ các định dạng tệp Excel khác, chẳng hạn như XLSX và CSV không?

Có, Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel bao gồm XLSX, XLS, CSV, HTML, PDF và nhiều định dạng khác.

#### 3. Aspose.Cells for .NET có tương thích với tất cả các phiên bản .NET Framework không?

Aspose.Cells for .NET tương thích với .NET Framework 2.0 trở lên, bao gồm các phiên bản 3.5, 4.0, 4.5, 4.6, v.v.