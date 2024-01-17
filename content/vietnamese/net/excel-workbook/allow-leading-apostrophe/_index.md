---
title: Cho phép dấu nháy đơn hàng đầu
linktitle: Cho phép dấu nháy đơn hàng đầu
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Cho phép dấu nháy đơn đứng đầu trong sổ làm việc Excel với Aspose.Cells for .NET.
type: docs
weight: 60
url: /vi/net/excel-workbook/allow-leading-apostrophe/
---
Trong hướng dẫn từng bước này, chúng tôi sẽ giải thích mã nguồn C# được cung cấp, mã này sẽ cho phép bạn cho phép sử dụng dấu nháy đơn ở đầu trong sổ làm việc Excel bằng Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để thực hiện thao tác này.

## Bước 1: Đặt thư mục nguồn và đầu ra

```csharp
// thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

Trong bước đầu tiên này, chúng tôi xác định thư mục nguồn và đầu ra cho các tệp Excel.

## Bước 2: Khởi tạo đối tượng WorkbookDesigner

```csharp
// Khởi tạo đối tượng WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Chúng tôi tạo một thể hiện của`WorkbookDesigner` lớp từ Aspose.Cells.

## Bước 3: Tải sổ làm việc Excel

```csharp
// Tải sổ làm việc Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Chúng tôi tải sổ làm việc Excel từ tệp đã chỉ định và tắt tính năng tự động chuyển đổi dấu nháy đơn ban đầu thành kiểu văn bản.

## Bước 4: Đặt nguồn dữ liệu

```csharp
// Xác định nguồn dữ liệu cho sổ làm việc của nhà thiết kế
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Chúng tôi xác định danh sách các đối tượng dữ liệu và sử dụng`SetDataSource` phương pháp đặt nguồn dữ liệu cho sổ làm việc của nhà thiết kế.

## Bước 5: Xử lý điểm đánh dấu thông minh

```csharp
// Xử lý điểm đánh dấu thông minh
designer. Process();
```

 Chúng tôi sử dụng`Process` phương pháp xử lý điểm đánh dấu thông minh trong sổ làm việc của nhà thiết kế.

## Bước 6: Lưu sổ làm việc Excel đã sửa đổi

```csharp
// Lưu sổ làm việc Excel đã sửa đổi
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Chúng tôi lưu sổ làm việc Excel đã sửa đổi với những thay đổi được thực hiện.

### Mã nguồn mẫu cho Cho phép dấu nháy đơn hàng đầu bằng Aspose.Cells for .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Khởi tạo đối tượng WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Mở bảng tính thiết kế có chứa các điểm đánh dấu thông minh
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Đặt nguồn dữ liệu cho bảng tính thiết kế
designer.SetDataSource("sampleData", list);
// Xử lý các điểm đánh dấu thông minh
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách cho phép sử dụng dấu nháy đơn ở đầu trong sổ làm việc Excel bằng Aspose.Cells for .NET. Thử nghiệm với dữ liệu của riêng bạn để tùy chỉnh thêm sổ làm việc Excel của bạn.

### Câu hỏi thường gặp

#### Hỏi: Quyền dấu nháy đơn đứng đầu trong sổ làm việc Excel là gì?

Trả lời: Việc cho phép dấu nháy đơn đầu tiên trong sổ làm việc Excel sẽ cho phép dữ liệu bắt đầu bằng dấu nháy đơn được hiển thị chính xác mà không cần chuyển đổi nó thành kiểu văn bản. Điều này rất hữu ích khi bạn muốn giữ dấu nháy đơn như một phần của dữ liệu.

#### Hỏi: Tại sao tôi cần tắt chức năng tự động chuyển đổi dấu nháy đơn đầu tiên?

Đáp: Bằng cách tắt tính năng tự động chuyển đổi các dấu ngoặc kép ở đầu, bạn có thể duy trì việc sử dụng chúng như trong dữ liệu của mình. Điều này tránh mọi sửa đổi ngoài ý muốn của dữ liệu trong khi mở hoặc thao tác với sổ làm việc Excel.

#### Câu hỏi: Làm cách nào để đặt nguồn dữ liệu trong sổ làm việc của nhà thiết kế?

 Đáp: Để đặt nguồn dữ liệu trong sổ làm việc của nhà thiết kế, bạn có thể sử dụng`SetDataSource` phương thức chỉ định tên của nguồn dữ liệu và danh sách các đối tượng dữ liệu tương ứng.

#### Hỏi: Việc cho phép dấu nháy đơn đứng đầu có ảnh hưởng đến dữ liệu khác trong sổ làm việc Excel không?

Đáp: Không, việc cho phép dấu nháy đơn ở đầu chỉ ảnh hưởng đến dữ liệu bắt đầu bằng dấu nháy đơn. Các dữ liệu khác trong sổ làm việc Excel không thay đổi.

#### Hỏi: Tôi có thể sử dụng tính năng này với các định dạng tệp Excel khác không?

Trả lời: Có, bạn có thể sử dụng tính năng này với các định dạng tệp Excel khác được Aspose.Cells hỗ trợ, chẳng hạn như .xls, .xlsm, v.v.