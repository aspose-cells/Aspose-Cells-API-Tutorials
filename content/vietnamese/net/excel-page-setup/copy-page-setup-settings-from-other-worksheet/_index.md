---
title: Sao chép cài đặt thiết lập trang từ bảng tính khác
linktitle: Sao chép cài đặt thiết lập trang từ bảng tính khác
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách sao chép cài đặt cấu hình trang từ bảng tính này sang bảng tính khác bằng Aspose.Cells for .NET. Hướng dẫn từng bước để tối ưu hóa việc sử dụng thư viện này.
type: docs
weight: 10
url: /vi/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
Trong bài viết này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# sau: Sao chép cài đặt cấu hình trang từ một bảng tính khác bằng Aspose.Cells cho .NET. Chúng tôi sẽ sử dụng thư viện Aspose.Cells cho .NET để thực hiện thao tác này. Nếu bạn muốn sao chép cài đặt thiết lập trang từ trang tính này sang trang tính khác, hãy làm theo các bước bên dưới.

## Bước 1: Tạo sổ làm việc
Bước đầu tiên là tạo một bảng tính. Trong trường hợp của chúng tôi, chúng tôi sẽ sử dụng lớp Workbook do thư viện Aspose.Cells cung cấp. Đây là mã để tạo một sổ làm việc:

```csharp
Workbook wb = new Workbook();
```

## Bước 2: Thêm bảng kiểm tra
Sau khi tạo sổ làm việc, chúng ta cần thêm bảng tính kiểm tra. Trong ví dụ này, chúng tôi sẽ thêm hai bảng tính. Đây là mã để thêm hai bảng tính:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## Bước 3: Truy cập bảng tính
Bây giờ chúng ta đã thêm các trang tính, chúng ta cần truy cập chúng để có thể thay đổi cài đặt của chúng. Chúng tôi sẽ truy cập bảng tính "TestSheet1" và "TestSheet2" bằng tên của chúng. Đây là mã để truy cập nó:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## Bước 4: Cài đặt khổ giấy
 Trong bước này, chúng tôi sẽ đặt khổ giấy của bảng tính "TestSheet1". Chúng tôi sẽ sử dụng`PageSetup.PaperSize` thuộc tính để thiết lập kích thước giấy. Ví dụ: chúng tôi sẽ đặt khổ giấy thành "PaperA3ExtraTransverse". Đây là mã cho điều đó:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## Bước 5: Sao chép cài đặt thiết lập trang
Bây giờ chúng tôi sẽ sao chép cài đặt cấu hình trang từ bảng tính "TestSheet1" sang "TestSheet2". Chúng tôi sẽ sử dụng`PageSetup.Copy` phương pháp thực hiện thao tác này. Đây là mã cho điều đó:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## Bước 6: In khổ giấy
 Sau khi sao chép cài đặt thiết lập trang, chúng ta sẽ in khổ giấy của 2 bảng tính. Chúng tôi sẽ sử dụng`Console.WriteLine` để hiển thị kích thước giấy. Đây là mã cho điều đó:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Mã nguồn mẫu cho Cài đặt thiết lập trang sao chép từ bảng tính khác bằng Aspose.Cells cho .NET 
```csharp
//Tạo sổ làm việc
Workbook wb = new Workbook();
//Thêm hai bảng kiểm tra
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//Truy cập cả hai bảng tính dưới dạng TestSheet1 và TestSheet2
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//Đặt khổ giấy của TestSheet1 thành PaperA3ExtraTransverse
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//In khổ giấy của cả hai trang tính
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//Sao chép PageSetup từ TestSheet1 sang TestSheet2
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//In khổ giấy của cả hai trang tính
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## Phần kết luận
Trong bài viết này, chúng ta đã tìm hiểu cách sao chép cài đặt cấu hình trang từ trang tính này sang trang tính khác bằng Aspose.Cells for .NET. Chúng tôi đã thực hiện các bước sau: tạo sổ làm việc, thêm bảng tính kiểm tra, truy cập trang tính, đặt khổ giấy, sao chép cài đặt thiết lập trang và in khổ giấy. Bây giờ bạn có thể sử dụng kiến thức này để sao chép cài đặt cấu hình trang vào dự án của riêng bạn.

### Câu hỏi thường gặp

#### Câu hỏi: Tôi có thể sao chép cài đặt cấu hình trang giữa các phiên bản sổ làm việc khác nhau không?

 Đáp: Có, bạn có thể sao chép cài đặt thiết lập trang giữa các phiên bản sổ làm việc khác nhau bằng cách sử dụng`PageSetup.Copy` phương thức của thư viện Aspose.Cells.

#### Câu hỏi: Tôi có thể sao chép các cài đặt thiết lập trang khác như hướng hoặc lề không?

 Đáp: Có, bạn có thể sao chép các cài đặt thiết lập trang khác bằng cách sử dụng`PageSetup.Copy` bằng các phương án thích hợp. Ví dụ: bạn có thể sao chép hướng bằng cách sử dụng`CopyOptions.Orientation` và lợi nhuận bằng cách sử dụng`CopyOptions.Margins`.

#### Hỏi: Làm cách nào để biết có những tùy chọn nào cho khổ giấy?

Trả lời: Bạn có thể kiểm tra Tài liệu tham khảo API của thư viện Aspose.Cells để biết các tùy chọn có sẵn cho khổ giấy. Có một enum tên là`PaperSizeType` trong đó liệt kê các khổ giấy được hỗ trợ khác nhau.

#### Câu hỏi: Làm cách nào tôi có thể tải xuống thư viện Aspose.Cells cho .NET?

 Trả lời: Bạn có thể tải xuống thư viện Aspose.Cells cho .NET từ[Giả định phát hành](https://releases.aspose.com/cells/net). Có sẵn các phiên bản dùng thử miễn phí cũng như các giấy phép trả phí cho mục đích sử dụng thương mại.

#### Câu hỏi: Thư viện Aspose.Cells có hỗ trợ các ngôn ngữ lập trình khác không?

Trả lời: Có, thư viện Aspose.Cells hỗ trợ nhiều ngôn ngữ lập trình bao gồm C#, Java, Python và nhiều ngôn ngữ khác.