---
title: Đọc và ghi kết nối bên ngoài của tệp XLSB
linktitle: Đọc và ghi kết nối bên ngoài của tệp XLSB
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách đọc và sửa đổi các kết nối bên ngoài của tệp XLSB bằng Aspose.Cells cho .NET.
type: docs
weight: 130
url: /vi/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Đọc và ghi các kết nối bên ngoài vào tệp XLSB là điều cần thiết để thao tác dữ liệu từ các nguồn bên ngoài trong sổ làm việc Excel của bạn. Với Aspose.Cells for .NET, bạn có thể dễ dàng đọc và ghi các kết nối bên ngoài bằng các bước sau:

## Bước 1: Chỉ định thư mục nguồn và thư mục đầu ra

Trước tiên, bạn phải chỉ định thư mục nguồn chứa tệp XLSB chứa kết nối bên ngoài, cũng như thư mục đầu ra nơi bạn muốn lưu tệp đã sửa đổi. Đây là cách thực hiện bằng Aspose.Cells:

```csharp
// thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();

// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

## Bước 2: Tải file Excel XLSB nguồn

Tiếp theo, bạn cần tải tệp Excel XLSB nguồn mà bạn muốn thực hiện các thao tác đọc và ghi kết nối bên ngoài. Đây là một mã mẫu:

```csharp
// Tải tệp Excel XLSB nguồn
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Bước 3: Đọc và sửa đổi kết nối bên ngoài

Sau khi tải tệp, bạn có thể truy cập kết nối bên ngoài đầu tiên thực sự là kết nối cơ sở dữ liệu. Bạn có thể đọc và sửa đổi các thuộc tính khác nhau của kết nối bên ngoài. Đây là cách thực hiện:

```csharp
// Đọc kết nối bên ngoài đầu tiên là kết nối cơ sở dữ liệu
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Hiển thị tên kết nối cơ sở dữ liệu, lệnh và thông tin kết nối
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Sửa đổi tên của kết nối
dbCon.Name = "NewCustomer";
```

## Bước 4: Lưu file Excel XLSB đầu ra

Khi bạn đã thực hiện những thay đổi cần thiết, bạn có thể lưu tệp Excel XLSB đã sửa đổi vào thư mục đầu ra được chỉ định. Đây là cách thực hiện:

```csharp
// Lưu tệp Excel XLSB đầu ra
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Mã nguồn mẫu để đọc và ghi kết nối bên ngoài của tệp XLSB bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
//Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
//Tải tệp Excel Xlsb nguồn
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Đọc kết nối bên ngoài đầu tiên thực sự là Kết nối DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//In tên, lệnh và thông tin kết nối của kết nối DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Sửa đổi tên kết nối
dbCon.Name = "NewCust";
//Lưu tệp Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Phần kết luận

Đọc và ghi các kết nối bên ngoài vào tệp XLSB cho phép bạn thao tác dữ liệu từ các nguồn bên ngoài trong sổ làm việc Excel của mình. Với Aspose.Cells cho .NET, bạn có thể dễ dàng truy cập các kết nối bên ngoài, đọc và sửa đổi thông tin kết nối cũng như lưu các thay đổi. Thử nghiệm với các tệp XLSB của riêng bạn và khai thác sức mạnh của các kết nối bên ngoài trong ứng dụng Excel của bạn.

### Câu hỏi thường gặp

#### Câu hỏi: Kết nối bên ngoài trong tệp XLSB là gì?
    
Trả lời: Kết nối bên ngoài trong tệp XLSB đề cập đến kết nối được thiết lập với nguồn dữ liệu bên ngoài, chẳng hạn như cơ sở dữ liệu. Nó cho phép bạn nhập dữ liệu từ nguồn bên ngoài này vào sổ làm việc Excel.

#### Câu hỏi: Tôi có thể có nhiều kết nối bên ngoài trong một tệp XLSB không?
     
Đáp: Có, bạn có thể có nhiều kết nối bên ngoài trong một tệp XLSB. Bạn có thể quản lý chúng riêng lẻ bằng cách truy cập từng đối tượng kết nối.

#### Câu hỏi: Làm cách nào tôi có thể đọc chi tiết về kết nối bên ngoài trong tệp XLSB bằng Aspose.Cells?
     
Trả lời: Bạn có thể sử dụng chức năng do Aspose.Cells cung cấp để truy cập các thuộc tính của kết nối bên ngoài, chẳng hạn như tên kết nối, lệnh liên quan và thông tin kết nối.

#### Câu hỏi: Có thể sửa đổi kết nối bên ngoài trong tệp XLSB bằng Aspose.Cells không?
     
Trả lời: Có, bạn có thể sửa đổi các thuộc tính của kết nối bên ngoài, chẳng hạn như tên kết nối, để đáp ứng nhu cầu cụ thể của mình. Aspose.Cells cung cấp các phương thức để thực hiện những thay đổi này.

#### Câu hỏi: Làm cách nào tôi có thể lưu các thay đổi được thực hiện đối với kết nối bên ngoài vào tệp XLSB bằng Aspose.Cells?
     
Trả lời: Sau khi thực hiện các thay đổi cần thiết đối với kết nối bên ngoài, bạn chỉ cần lưu tệp Excel XLSB đã sửa đổi bằng phương pháp thích hợp do Aspose.Cells cung cấp.