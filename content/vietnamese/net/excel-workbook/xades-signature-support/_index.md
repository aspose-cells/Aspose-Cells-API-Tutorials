---
title: Hỗ trợ chữ ký Xades
linktitle: Hỗ trợ chữ ký Xades
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách thêm chữ ký Xades vào tệp Excel bằng Aspose.Cells cho .NET.
type: docs
weight: 190
url: /vi/net/excel-workbook/xades-signature-support/
---
Trong bài viết này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# bên dưới, về hỗ trợ chữ ký Xades bằng thư viện Aspose.Cells cho .NET. Bạn sẽ tìm hiểu cách sử dụng thư viện này để thêm chữ ký số Xades vào tệp Excel. Chúng tôi cũng sẽ cung cấp cho bạn cái nhìn tổng quan về quá trình ký kết và việc thực hiện nó. Thực hiện theo các bước dưới đây để có được kết quả cuối cùng.

## Bước 1: Xác định thư mục nguồn và đầu ra
Để bắt đầu, chúng ta cần xác định thư mục nguồn và đầu ra trong mã của mình. Các thư mục này cho biết vị trí của tệp nguồn và nơi tệp đầu ra sẽ được lưu. Đây là mã tương ứng:

```csharp
// Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

Hãy chắc chắn điều chỉnh các đường dẫn thư mục nếu cần.

## Bước 2: Tải sổ làm việc Excel
Bước tiếp theo là tải sổ làm việc Excel mà chúng tôi muốn thêm chữ ký số Xades. Đây là mã để tải sổ làm việc:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Đảm bảo chỉ định chính xác tên tệp nguồn trong mã.

## Bước 3: Cấu hình chữ ký số
Bây giờ chúng tôi sẽ định cấu hình chữ ký số Xades bằng cách cung cấp thông tin cần thiết. Chúng tôi phải chỉ định tệp PFX chứa chứng chỉ kỹ thuật số cũng như mật khẩu liên quan. Đây là mã tương ứng:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Đảm bảo thay thế "pfxPassword" bằng mật khẩu thực của bạn và "pfxFile" bằng đường dẫn đến tệp PFX.

## Bước 4: Thêm chữ ký số
Bây giờ chúng ta đã cấu hình chữ ký điện tử, chúng ta có thể thêm nó vào sổ làm việc Excel. Đây là mã tương ứng:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Bước này thêm chữ ký số Xades vào sổ làm việc Excel.

## Bước 5: Lưu bảng tính có chữ ký
Cuối cùng, chúng ta lưu sổ làm việc Excel có thêm chữ ký điện tử. Đây là mã tương ứng:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Đảm bảo điều chỉnh tên của tệp đầu ra theo nhu cầu của bạn.

### Mã nguồn mẫu cho Hỗ trợ chữ ký Xades bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
//Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Phần kết luận
Xin chúc mừng! Bạn đã học cách sử dụng thư viện Aspose.Cells cho .NET để thêm chữ ký số Xades vào tệp Excel. Bằng cách làm theo các bước được cung cấp trong bài viết này, bạn sẽ có thể triển khai chức năng này trong các dự án của riêng mình. Hãy thoải mái thử nghiệm nhiều hơn với thư viện và khám phá các tính năng mạnh mẽ khác mà nó cung cấp.

### Câu hỏi thường gặp

#### Hỏi: Xades là gì?

Trả lời: Xades là một tiêu chuẩn chữ ký điện tử tiên tiến được sử dụng để đảm bảo tính toàn vẹn và xác thực của tài liệu kỹ thuật số.

#### Câu hỏi: Tôi có thể sử dụng các loại chữ ký số khác với Aspose.Cells không?

Trả lời: Có, Aspose.Cells cũng hỗ trợ các loại chữ ký số khác, chẳng hạn như chữ ký XMLDSig và chữ ký PKCS#7.

#### Hỏi: Tôi có thể áp dụng chữ ký cho các loại tệp khác ngoài tệp Excel không?
 
Trả lời: Có, Aspose.Cells cũng cho phép áp dụng chữ ký số cho các loại tệp được hỗ trợ khác như tệp Word, PDF và PowerPoint.