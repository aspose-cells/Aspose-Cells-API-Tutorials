---
title: Trích xuất tập tin Mol nhúng
linktitle: Trích xuất tập tin Mol nhúng
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách dễ dàng trích xuất các tệp MOL được nhúng từ sổ làm việc Excel bằng Aspose.Cells cho .NET.
type: docs
weight: 90
url: /vi/net/excel-workbook/extract-embedded-mol-file/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước cách trích xuất tệp MOL được nhúng từ sổ làm việc Excel bằng thư viện Aspose.Cells cho .NET. Bạn sẽ học cách duyệt các trang tính trong sổ làm việc, trích xuất các đối tượng OLE tương ứng và lưu các tệp MOL đã được trích xuất. Thực hiện theo các bước dưới đây để hoàn thành nhiệm vụ này thành công.

## Bước 1: Xác định thư mục nguồn và đầu ra
Đầu tiên, chúng ta cần xác định thư mục nguồn và đầu ra trong mã của mình. Các thư mục này cho biết vị trí của sổ làm việc Excel nguồn và nơi lưu các tệp MOL được trích xuất. Đây là mã tương ứng:

```csharp
// Thư mục
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Hãy chắc chắn chỉ định các đường dẫn thích hợp nếu cần.

## Bước 2: Tải sổ làm việc Excel
Bước tiếp theo là tải sổ làm việc Excel có chứa các đối tượng OLE và tệp MOL được nhúng. Đây là mã để tải sổ làm việc:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Đảm bảo chỉ định chính xác tên tệp nguồn trong mã.

## Bước 3: Duyệt các trang tính và giải nén các tệp MOL
Bây giờ chúng ta sẽ lặp qua từng trang tính trong sổ làm việc và trích xuất các đối tượng OLE tương ứng, chứa các tệp MOL. Đây là mã tương ứng:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Mã này lặp qua từng trang tính trong sổ làm việc, tìm nạp các đối tượng OLE và lưu các tệp MOL đã trích xuất vào thư mục đầu ra.

### Mã nguồn mẫu để trích xuất tệp Mol nhúng bằng Aspose.Cells cho .NET 
```csharp
//thư mục
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Phần kết luận
Xin chúc mừng! Bạn đã học cách trích xuất tệp MOL được nhúng từ sổ làm việc Excel bằng Aspose.Cells cho .NET. Bây giờ bạn có thể áp dụng kiến thức này để trích xuất các tệp MOL từ sổ làm việc Excel của riêng bạn. Vui lòng khám phá thêm thư viện Aspose.Cells và tìm hiểu về các tính năng mạnh mẽ khác của nó.

### Câu hỏi thường gặp

#### Câu hỏi: Tệp MOL là gì?
 
Trả lời: Tệp MOL là định dạng tệp được sử dụng để biểu thị các cấu trúc hóa học trong hóa học tính toán. Nó chứa thông tin về các nguyên tử, liên kết và các tính chất phân tử khác.

#### Hỏi: Phương pháp này có hoạt động với tất cả các loại tệp Excel không?

Đáp: Có, phương pháp này hoạt động với tất cả các loại tệp Excel được Aspose.Cells hỗ trợ.

#### Hỏi: Tôi có thể trích xuất nhiều tệp MOL cùng một lúc không?

Trả lời: Có, bạn có thể trích xuất nhiều tệp MOL cùng một lúc bằng cách lặp qua các đối tượng OLE trên mỗi trang tính trong sổ làm việc.