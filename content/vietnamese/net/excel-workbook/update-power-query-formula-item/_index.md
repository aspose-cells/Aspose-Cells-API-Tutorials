---
title: Cập nhật mục công thức Power Query
linktitle: Cập nhật mục công thức Power Query
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách cập nhật các thành phần công thức Power Query trong tệp Excel bằng Aspose.Cells cho .NET.
type: docs
weight: 160
url: /vi/net/excel-workbook/update-power-query-formula-item/
---
Cập nhật mục công thức Power Query là thao tác phổ biến khi làm việc với dữ liệu trong tệp Excel. Với Aspose.Cells dành cho .NET, bạn có thể dễ dàng cập nhật mục công thức Power Query bằng cách làm theo các bước sau:

## Bước 1: Chỉ định thư mục nguồn và đầu ra

Trước tiên, bạn cần chỉ định thư mục nguồn chứa tệp Excel chứa công thức Power Query cần cập nhật, cũng như thư mục đầu ra nơi bạn muốn lưu tệp đã sửa đổi. Đây là cách thực hiện bằng Aspose.Cells:

```csharp
// thư mục nguồn
string SourceDir = RunExamples.Get_SourceDirectory();

// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

## Bước 2: Tải sổ làm việc Excel nguồn

Tiếp theo, bạn cần tải sổ làm việc Excel nguồn mà bạn muốn cập nhật mục công thức Power Query. Đây là cách thực hiện:

```csharp
// Tải sổ làm việc Excel nguồn
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Bước 3: Duyệt và cập nhật các mục công thức Power Query

Sau khi tải sổ làm việc, bạn có thể dẫn hướng đến bộ sưu tập công thức Power Query và duyệt qua từng công thức cũng như các thành phần của nó. Trong ví dụ này, chúng tôi đang tìm kiếm mục công thức có tên "Nguồn" và cập nhật giá trị của nó. Đây là mã mẫu để cập nhật mục công thức Power Query:

```csharp
// Truy cập bộ sưu tập công thức Power Query
DataMashup mashupData = workbook.DataMashup;

// Lặp lại các công thức Power Query và các thành phần của chúng
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Bước 4: Lưu sổ làm việc Excel đầu ra

Sau khi cập nhật mục công thức Power Query, bạn có thể lưu sổ làm việc Excel đã sửa đổi vào thư mục đầu ra được chỉ định. Đây là cách thực hiện:

```csharp
// Lưu sổ làm việc Excel đầu ra
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Mã nguồn mẫu để cập nhật Mục công thức Power Query bằng Aspose.Cells cho .NET 
```csharp
// Thư mục làm việc
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Lưu sổ làm việc đầu ra.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Phần kết luận

Cập nhật các thành phần công thức Power Query là một thao tác thiết yếu khi sử dụng Aspose.Cells để thao tác và xử lý dữ liệu trong tệp Excel. Bằng cách làm theo các bước nêu trên, bạn có thể dễ dàng cập nhật các thành phần công thức

### Câu hỏi thường gặp

#### Hỏi: Power Query trong Excel là gì?
     
Trả lời: Power Query là một tính năng trong Excel giúp thu thập, chuyển đổi và tải dữ liệu từ các nguồn khác nhau. Nó cung cấp các công cụ mạnh mẽ để dọn dẹp, kết hợp và định hình lại dữ liệu trước khi nhập vào Excel.

#### Câu hỏi: Làm cách nào để biết mục công thức Power Query đã được cập nhật thành công hay chưa?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Câu hỏi: Tôi có thể cập nhật nhiều mục công thức Power Query cùng một lúc không?
    
Trả lời: Có, bạn có thể lặp qua bộ sưu tập mục công thức Power Query và cập nhật nhiều mục trong một vòng lặp, tùy thuộc vào nhu cầu cụ thể của bạn.

#### Câu hỏi: Tôi có thể thực hiện các thao tác nào khác trên công thức Power Query bằng Aspose.Cells không?
    
Trả lời: Có, Aspose.Cells cung cấp đầy đủ các tính năng để làm việc với công thức Power Query, bao gồm tạo, xóa, sao chép và tìm kiếm công thức trong sổ làm việc Excel.