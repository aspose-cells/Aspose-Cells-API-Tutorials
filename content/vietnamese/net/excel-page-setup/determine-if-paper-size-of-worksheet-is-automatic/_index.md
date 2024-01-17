---
title: Xác định xem khổ giấy của bảng tính có tự động không
linktitle: Xác định xem khổ giấy của bảng tính có tự động không
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách xác định xem khổ giấy của bảng tính có tự động hay không bằng Aspose.Cells for .NET.
type: docs
weight: 20
url: /vi/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Trong bài viết này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# sau: Xác định xem khổ giấy của trang tính có tự động hay không bằng cách sử dụng Aspose.Cells for .NET. Chúng tôi sẽ sử dụng thư viện Aspose.Cells cho .NET để thực hiện thao tác này. Hãy làm theo các bước dưới đây để xác định xem khổ giấy của trang tính có tự động hay không.

## Bước 1: Tải sổ làm việc
Bước đầu tiên là tải sổ làm việc. Chúng ta sẽ có hai sổ làm việc: một sổ làm việc bị vô hiệu hóa khổ giấy tự động và sổ còn lại được bật khổ giấy tự động. Đây là mã để tải sổ làm việc:

```csharp
// thư mục nguồn
string sourceDir = "YOUR_SOURCE_DIR";
// Thư mục đầu ra
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// Nạp sổ làm việc đầu tiên với khổ giấy tự động bị tắt
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// Tải sổ làm việc thứ hai với kích thước giấy tự động được kích hoạt
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Bước 2: Truy cập bảng tính
Bây giờ chúng ta đã tải sổ làm việc, chúng ta cần truy cập vào các trang tính để có thể kiểm tra khổ giấy tự động. Chúng ta sẽ đi đến bảng tính đầu tiên của hai bảng tính. Đây là mã để truy cập nó:

```csharp
//Đi tới bảng tính đầu tiên của sổ làm việc đầu tiên
Worksheet ws11 = wb1.Worksheets[0];

// Đi tới bảng tính đầu tiên của sổ làm việc thứ hai
Worksheet ws12 = wb2.Worksheets[0];
```

## Bước 3: Kiểm tra khổ giấy tự động
 Ở bước này, chúng ta sẽ kiểm tra xem khổ giấy của bảng tính có tự động hay không. Chúng tôi sẽ sử dụng`PageSetup.IsAutomaticPaperSize` bất động sản để có được thông tin này. Sau đó chúng tôi sẽ hiển thị kết quả. Đây là mã cho điều đó:

```csharp
// Hiển thị thuộc tính IsAutomaticPaperSize của bảng tính đầu tiên trong sổ làm việc đầu tiên
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// Hiển thị thuộc tính IsAutomaticPaperSize của bảng tính đầu tiên trong sổ làm việc thứ hai
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Mã nguồn mẫu để xác định xem kích thước giấy của trang tính có tự động hay không bằng cách sử dụng Aspose.Cells for .NET 
```csharp
//Thư mục nguồn
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Thư mục đầu ra
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Nạp sổ làm việc đầu tiên có khổ giấy tự động sai
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Nạp sổ làm việc thứ hai có khổ giấy tự động đúng
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Truy cập bảng tính đầu tiên của cả hai sổ làm việc
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//In thuộc tính PageSetup.IsAutomaticPaperSize của cả hai trang tính
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Phần kết luận
Trong bài viết này, chúng ta đã tìm hiểu cách xác định xem kích thước giấy của trang tính có tự động hay không bằng cách sử dụng Aspose.Cells for .NET. Chúng tôi đã làm theo các bước sau: tải sổ làm việc,

truy cập vào bảng tính và kiểm tra khổ giấy tự động. Bây giờ bạn có thể sử dụng kiến thức này để xác định xem kích thước giấy của bảng tính của bạn có tự động hay không.

### Câu hỏi thường gặp

#### Câu hỏi: Làm cách nào tôi có thể tải sổ làm việc bằng Aspose.Cells cho .NET?

Đáp: Bạn có thể tải sổ làm việc bằng lớp Workbook từ thư viện Aspose.Cells. Sử dụng phương thức Workbook.Load để tải sổ làm việc từ một tệp.

#### Hỏi: Tôi có thể kiểm tra khổ giấy tự động cho các bảng tính khác không?

Trả lời: Có, bạn có thể kiểm tra khổ giấy tự động cho bất kỳ trang tính nào bằng cách truy cập thuộc tính PageSetup.IsAutomaticPaperSize của đối tượng Trang tính tương ứng.

#### Hỏi: Làm cách nào để thay đổi khổ giấy tự động của bảng tính?

Đáp: Để thay đổi khổ giấy tự động của một trang tính, bạn có thể sử dụng thuộc tính PageSetup.IsAutomaticPaperSize và đặt nó thành giá trị mong muốn (đúng hoặc sai).

#### Câu hỏi: Aspose.Cells for .NET cung cấp những tính năng nào khác?

Trả lời: Aspose.Cells for .NET cung cấp nhiều tính năng để làm việc với bảng tính, chẳng hạn như tạo, sửa đổi và chuyển đổi sổ làm việc cũng như thao tác dữ liệu, công thức và định dạng.