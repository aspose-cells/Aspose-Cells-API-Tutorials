---
title: Điều chỉnh mức nén
linktitle: Điều chỉnh mức nén
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Giảm kích thước sổ làm việc Excel của bạn bằng cách điều chỉnh mức nén bằng Aspose.Cells for .NET.
type: docs
weight: 50
url: /vi/net/excel-workbook/adjust-compression-level/
---
Trong hướng dẫn từng bước này, chúng tôi sẽ giải thích mã nguồn C# được cung cấp để cho phép bạn điều chỉnh mức độ nén bằng Aspose.Cells cho .NET. Hãy làm theo các bước bên dưới để điều chỉnh mức độ nén trong sổ làm việc Excel của bạn.

## Bước 1: Đặt thư mục nguồn và đầu ra

```csharp
// thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
// Thư mục đầu ra
string outDir = RunExamples.Get_OutputDirectory();
```

Trong bước đầu tiên này, chúng tôi xác định thư mục nguồn và đầu ra cho các tệp Excel.

## Bước 2: Tải sổ làm việc Excel

```csharp
// Tải sổ làm việc Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Chúng tôi tải sổ làm việc Excel từ tệp được chỉ định bằng cách sử dụng`Workbook` lớp từ Aspose.Cells.

## Bước 3: Đặt tùy chọn sao lưu

```csharp
// Xác định các tùy chọn sao lưu
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Chúng tôi tạo một thể hiện của`XlsbSaveOptions` class để thiết lập các tùy chọn lưu.

## Bước 4: Điều chỉnh mức độ nén (Level 1)

```csharp
// Điều chỉnh mức độ nén (Cấp 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Chúng tôi điều chỉnh mức độ nén bằng cách cài đặt`CompressionType` ĐẾN`Level1`. Sau đó, chúng tôi lưu sổ làm việc Excel với tùy chọn nén được chỉ định này.

## Bước 5: Điều chỉnh mức độ nén (Level 6)

```csharp
// Điều chỉnh mức độ nén (Cấp 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Chúng tôi lặp lại quá trình để điều chỉnh mức độ nén thành`Level6` và lưu sổ làm việc Excel với tùy chọn này.

## Bước 6: Điều chỉnh mức độ nén (Level 9)

```csharp
// Điều chỉnh mức độ nén (Cấp 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Chúng tôi lặp lại quy trình lần cuối để điều chỉnh mức nén thành`Level9` và lưu sổ làm việc Excel với tùy chọn này.

### Mã nguồn mẫu để Điều chỉnh mức nén bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách điều chỉnh mức độ nén trong sổ làm việc Excel bằng Aspose.Cells for .NET. Hãy thử nghiệm với nhiều mức độ nén khác nhau để tìm ra mức nén phù hợp nhất với nhu cầu của bạn.

### Câu hỏi thường gặp

#### Hỏi: Nén trong sổ làm việc Excel là gì?

Đáp: Nén trong sổ làm việc Excel là một quá trình giảm kích thước tệp bằng cách sử dụng thuật toán nén. Điều này làm giảm dung lượng lưu trữ cần thiết và cải thiện hiệu suất khi tải và thao tác với tệp.

#### Câu hỏi: Aspose.Cells có những mức độ nén nào?

Trả lời: Với Aspose.Cells, bạn có thể điều chỉnh mức nén từ 1 đến 9. Mức nén càng cao thì kích thước tệp sẽ càng nhỏ nhưng cũng có thể tăng thời gian xử lý.

#### Hỏi: Làm cách nào để chọn mức nén phù hợp cho sổ làm việc Excel của tôi?

Đáp: Việc lựa chọn mức độ nén tùy thuộc vào nhu cầu cụ thể của bạn. Nếu muốn thời gian nén và xử lý tối đa không phải là vấn đề, bạn có thể chọn cấp độ 9. Nếu muốn thỏa hiệp giữa kích thước tệp và thời gian xử lý, bạn có thể chọn cấp độ trung gian.

#### Hỏi: Việc nén có ảnh hưởng đến chất lượng dữ liệu trong sổ làm việc Excel không?

Trả lời: Không, việc nén không ảnh hưởng đến chất lượng dữ liệu trong sổ làm việc Excel. Nó chỉ đơn giản là giảm kích thước tệp bằng cách sử dụng các kỹ thuật nén mà không làm thay đổi dữ liệu.

#### Hỏi: Tôi có thể điều chỉnh mức độ nén sau khi lưu file Excel không?

Trả lời: Không, khi bạn lưu tệp Excel với mức nén cụ thể, bạn không thể điều chỉnh mức nén sau này. Bạn sẽ cần lưu lại tệp với mức nén mới nếu bạn muốn sửa đổi nó.