---
title: Đặt thứ tự trang Excel
linktitle: Đặt thứ tự trang Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Hướng dẫn từng bước để đặt thứ tự trang trong Excel bằng Aspose.Cells for .NET. Có hướng dẫn chi tiết và mã nguồn kèm theo.
type: docs
weight: 120
url: /vi/net/excel-page-setup/set-excel-page-order/
---
Trong bài viết này, chúng tôi sẽ hướng dẫn bạn từng bước giải thích mã nguồn C# sau để đặt thứ tự trang Excel bằng Aspose.Cells cho .NET. Chúng tôi sẽ chỉ cho bạn cách thiết lập thư mục tài liệu, khởi tạo đối tượng Workbook, lấy tham chiếu PageSetup, đặt thứ tự in trang và lưu sổ làm việc.

## Bước 1: Thiết lập thư mục tài liệu

 Trước khi bắt đầu, bạn cần định cấu hình thư mục tài liệu nơi bạn muốn lưu tệp Excel. Bạn có thể chỉ định đường dẫn thư mục bằng cách thay thế giá trị của`dataDir` biến bằng đường dẫn của riêng bạn.

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Bước 2: Khởi tạo một đối tượng Workbook

Bước đầu tiên là khởi tạo một đối tượng Workbook. Điều này thể hiện sổ làm việc Excel mà chúng ta sẽ làm việc.

```csharp
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
```

## Bước 3: Lấy tham chiếu PageSetup

Tiếp theo, chúng ta cần lấy tham chiếu đối tượng PageSetup của bảng tính mà chúng ta muốn đặt thứ tự trang.

```csharp
// Lấy tham chiếu PageSetup của bảng tính
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Bước 4: Đặt thứ tự in các trang

Bây giờ chúng ta có thể thiết lập thứ tự in của các trang. Trong ví dụ này, chúng tôi đang sử dụng tùy chọn "OverThenDown", có nghĩa là các trang sẽ được in từ trái sang phải, sau đó từ trên xuống dưới.

```csharp
// Đặt thứ tự in trang thành "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Bước 5: Lưu sổ làm việc

Cuối cùng, chúng ta lưu sổ làm việc Excel với những thay đổi về thứ tự trang.

```csharp
// Lưu sổ làm việc
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Mã nguồn mẫu cho Đặt thứ tự trang Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Lấy tham chiếu PageSetup của bảng tính
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Cài đặt thứ tự in trang trên rồi xuống
pageSetup.Order = PrintOrderType.OverThenDown;
// Lưu sổ làm việc.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Phần kết luận

Trong hướng dẫn này, chúng tôi đã giải thích cách đặt thứ tự trang trong tệp Excel bằng Aspose.Cells cho .NET. Bằng cách làm theo các bước được cung cấp, bạn có thể dễ dàng đặt cấu hình thư mục tài liệu, khởi tạo đối tượng Workbook, lấy tham chiếu PageSetup, đặt thứ tự in trang và lưu sổ làm việc.

### Câu hỏi thường gặp

#### Q1: Tại sao việc đặt thứ tự trang trong tệp Excel lại quan trọng?

Việc xác định thứ tự các trang trong file Excel rất quan trọng vì nó quyết định cách các trang sẽ được in hoặc hiển thị. Bằng cách chỉ định một thứ tự cụ thể, bạn có thể sắp xếp dữ liệu một cách hợp lý và làm cho tệp dễ đọc hoặc in hơn.

#### Câu hỏi 2: Tôi có thể sử dụng các đơn đặt hàng in trang khác bằng Aspose.Cells cho .NET không?

Có, Aspose.Cells for .NET hỗ trợ nhiều lệnh in trang như "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", v.v. Bạn có thể chọn thứ tự phù hợp nhất với nhu cầu của mình.

#### Câu hỏi 3: Tôi có thể đặt các tùy chọn bổ sung để in trang bằng Aspose.Cells cho .NET không?

Có, bạn có thể đặt các tùy chọn in trang khác nhau như tỷ lệ, hướng, lề, v.v. bằng cách sử dụng các thuộc tính của đối tượng PageSetup trong Aspose.Cells cho .NET.

#### Câu hỏi 4: Aspose.Cells for .NET có hỗ trợ các định dạng tệp Excel khác không?

Có, Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel như XLSX, XLS, CSV, HTML, PDF, v.v. Bạn có thể dễ dàng chuyển đổi giữa các định dạng này bằng các tính năng do thư viện cung cấp.