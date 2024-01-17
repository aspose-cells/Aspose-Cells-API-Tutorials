---
title: Xóa cài đặt máy in hiện có của bảng tính
linktitle: Xóa cài đặt máy in hiện có của bảng tính
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách xóa cài đặt máy in hiện có khỏi bảng tính Excel bằng Aspose.Cells for .NET.
type: docs
weight: 80
url: /vi/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước cách xóa cài đặt máy in hiện có khỏi bảng tính trong Excel bằng Aspose.Cells for .NET. Chúng tôi sẽ sử dụng mã nguồn C# để minh họa quy trình.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Đồng thời tạo một dự án mới trong môi trường phát triển ưa thích của bạn.

## Bước 2: Nhập các thư viện cần thiết

Trong tệp mã của bạn, hãy nhập các thư viện cần thiết để làm việc với Aspose.Cells. Đây là mã tương ứng:

```csharp
using Aspose.Cells;
```

## Bước 3: Đặt thư mục nguồn và đầu ra

Đặt thư mục nguồn và đầu ra nơi chứa tệp Excel gốc và nơi bạn muốn lưu tệp đã sửa đổi tương ứng. Sử dụng mã sau đây:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Hãy chắc chắn chỉ định đường dẫn thư mục đầy đủ.

## Bước 4: Tải tệp Excel nguồn

Tải tệp Excel nguồn bằng mã sau:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Thao tác này sẽ tải tệp Excel đã chỉ định vào đối tượng Workbook.

## Bước 5: Điều hướng các bảng tính

Lặp lại qua tất cả các trang tính trong sổ làm việc bằng vòng lặp. Sử dụng mã sau đây:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Phần còn lại của mã sẽ được thêm vào trong bước tiếp theo.
}
```

## Bước 6: Xóa cài đặt máy in hiện có

Kiểm tra xem cài đặt máy in có tồn tại cho mỗi bảng tính hay không và xóa chúng nếu cần. Sử dụng mã sau đây:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Bước 7: Lưu sổ làm việc đã sửa đổi

Lưu sổ làm việc đã sửa đổi bằng mã sau:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Điều này sẽ lưu sổ làm việc đã sửa đổi vào thư mục đầu ra được chỉ định.

### Mã nguồn mẫu để xóa cài đặt máy in hiện có của bảng tính bằng Aspose.Cells for .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
//Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
//Tải file Excel nguồn
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Lấy số trang tính của sổ làm việc
int sheetCount = wb.Worksheets.Count;
//Lặp lại tất cả các trang tính
for (int i = 0; i < sheetCount; i++)
{
    //Truy cập bảng tính thứ i
    Worksheet ws = wb.Worksheets[i];
    //Truy cập thiết lập trang bảng tính
    PageSetup ps = ws.PageSetup;
    //Kiểm tra xem cài đặt máy in cho bảng tính này có tồn tại không
    if (ps.PrinterSettings != null)
    {
        //In thông báo sau
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //In tên tờ và khổ giấy của nó
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Xóa cài đặt máy in bằng cách đặt chúng thành null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//nếu như
}//vì
//Lưu sổ làm việc
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Phần kết luận

Bây giờ bạn đã học cách xóa cài đặt máy in hiện có khỏi trang tính trong Excel bằng Aspose.Cells for .NET. Hướng dẫn này đã hướng dẫn bạn từng bước của quy trình, từ thiết lập môi trường đến điều hướng qua bảng tính và xóa cài đặt máy in. Bây giờ bạn có thể sử dụng kiến thức này để quản lý cài đặt máy in trong tệp Excel của mình.

### Câu hỏi thường gặp

#### Câu hỏi 1: Làm cách nào để biết bảng tính có cài đặt máy in hiện tại hay không?

 Đáp 1: Bạn có thể kiểm tra xem có cài đặt máy in cho một trang tính hay không bằng cách truy cập vào`PrinterSettings` tài sản của`PageSetup` sự vật. Nếu giá trị khác null, điều đó có nghĩa là có cài đặt máy in hiện có.

#### Câu hỏi 2: Tôi có thể xóa cài đặt máy in chỉ cho một bảng tính cụ thể không?

 Câu trả lời 2: Có, bạn có thể sử dụng phương pháp tương tự để xóa cài đặt máy in cho một trang tính cụ thể bằng cách truy cập vào trang tính đó`PageSetup` sự vật.

#### Câu hỏi 3: Phương pháp này có loại bỏ các cài đặt bố cục khác không?

A3: Không, phương pháp này chỉ xóa cài đặt máy in. Các cài đặt bố cục khác như lề, hướng giấy, v.v. vẫn không thay đổi.

#### Câu hỏi 4: Phương pháp này có áp dụng được với tất cả các định dạng tệp Excel, chẳng hạn như .xls và .xlsx không?

Câu trả lời 4: Có, phương pháp này hoạt động với tất cả các định dạng tệp Excel được Aspose.Cells hỗ trợ, bao gồm .xls và .xlsx.

#### Câu hỏi 5: Những thay đổi được thực hiện đối với cài đặt máy in có tồn tại vĩnh viễn trong tệp Excel đã chỉnh sửa không?

Câu trả lời 5: Có, những thay đổi đối với cài đặt máy in sẽ được lưu vĩnh viễn trong tệp Excel đã chỉnh sửa.