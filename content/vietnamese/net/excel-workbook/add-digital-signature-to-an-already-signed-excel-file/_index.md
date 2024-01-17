---
title: Thêm chữ ký số vào tệp Excel đã được ký
linktitle: Thêm chữ ký số vào tệp Excel đã được ký
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Dễ dàng thêm chữ ký điện tử vào các tệp Excel hiện có với Aspose.Cells cho .NET.
type: docs
weight: 30
url: /vi/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Trong hướng dẫn từng bước này, chúng tôi sẽ giải thích mã nguồn C# được cung cấp để cho phép bạn thêm chữ ký điện tử vào tệp Excel đã được ký bằng Aspose.Cells cho .NET. Thực hiện theo các bước bên dưới để thêm chữ ký số mới vào tệp Excel hiện có.

## Bước 1: Đặt thư mục nguồn và đầu ra

```csharp
// thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();

// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

Trong bước đầu tiên này, chúng tôi xác định thư mục nguồn và đầu ra sẽ được sử dụng để tải tệp Excel hiện có và lưu tệp bằng chữ ký số mới.

## Bước 2: Tải file Excel hiện có

```csharp
// Tải sổ làm việc Excel đã được ký
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Ở đây chúng tôi tải tệp Excel đã được ký bằng cách sử dụng`Workbook` lớp Aspose.Cells.

## Bước 3: Tạo bộ sưu tập chữ ký số

```csharp
// Tạo bộ sưu tập chữ ký số
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Chúng tôi tạo ra một bộ sưu tập chữ ký số mới bằng cách sử dụng`DigitalSignatureCollection` lớp học.

## Bước 4: Tạo chứng chỉ mới

```csharp
// Tạo chứng chỉ mới
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Ở đây chúng tôi tạo chứng chỉ mới từ tệp và mật khẩu được cung cấp.

## Bước 5: Thêm chữ ký số mới vào bộ sưu tập

```csharp
// Tạo chữ ký số mới
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Thêm chữ ký số vào bộ sưu tập
dsCollection.Add(signature);
```

 Chúng tôi tạo chữ ký số mới bằng cách sử dụng`DigitalSignature` lớp và thêm nó vào bộ sưu tập chữ ký số.

## Bước 6: Thêm bộ sưu tập chữ ký số vào sổ làm việc

```csharp
//Thêm bộ sưu tập chữ ký điện tử vào sổ làm việc
workbook.AddDigitalSignature(dsCollection);
```

 Chúng tôi thêm bộ sưu tập chữ ký điện tử vào sổ làm việc Excel hiện có bằng cách sử dụng`AddDigitalSignature()` phương pháp.

## Bước 7: Lưu và đóng sổ làm việc

```csharp
// Lưu sổ làm việc và đóng nó
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Chúng tôi lưu sổ làm việc có chữ ký điện tử mới vào thư mục đầu ra được chỉ định, sau đó đóng nó lại và giải phóng các tài nguyên liên quan.

### Mã nguồn mẫu để Thêm chữ ký số vào tệp Excel đã được ký bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string sourceDir = RunExamples.Get_SourceDirectory();
//Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
//Tệp chứng chỉ và mật khẩu của nó
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Tải sổ làm việc đã được ký điện tử để thêm chữ ký số mới
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Tạo bộ sưu tập chữ ký số
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Tạo chứng chỉ mới
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Tạo chữ ký số mới và thêm nó vào bộ sưu tập chữ ký số
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Thêm bộ sưu tập chữ ký số bên trong sổ làm việc
workbook.AddDigitalSignature(dsCollection);
//Lưu sổ làm việc và loại bỏ nó.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách thêm chữ ký điện tử vào tệp Excel đã được ký bằng Aspose.Cells cho .NET. Chữ ký số bổ sung thêm một lớp bảo mật cho các tệp Excel của bạn, đảm bảo tính xác thực và tính toàn vẹn của chúng.

### Câu hỏi thường gặp

#### Câu hỏi: Aspose.Cells dành cho .NET là gì?

Trả lời: Aspose.Cells for .NET là một thư viện lớp mạnh mẽ cho phép các nhà phát triển .NET tạo, sửa đổi, chuyển đổi và thao tác các tệp Excel một cách dễ dàng.

#### Hỏi: Chữ ký số trong file Excel là gì?

Trả lời: Chữ ký số trong tệp Excel là dấu điện tử đảm bảo tính xác thực, tính toàn vẹn và nguồn gốc của tài liệu. Nó được sử dụng để xác minh rằng tệp chưa bị sửa đổi kể từ khi được ký và đến từ một nguồn đáng tin cậy.

#### Hỏi: Lợi ích của việc thêm chữ ký điện tử vào tệp Excel là gì?

Trả lời: Việc thêm chữ ký điện tử vào tệp Excel mang lại một số lợi ích, bao gồm bảo vệ khỏi những thay đổi trái phép, đảm bảo tính toàn vẹn của dữ liệu, xác thực tác giả của tài liệu và mang lại sự tin cậy về thông tin trong đó.

#### Hỏi: Tôi có thể thêm nhiều chữ ký điện tử vào một tệp Excel không?

Trả lời: Có, Aspose.Cells cho phép bạn thêm nhiều chữ ký điện tử vào một tệp Excel. Bạn có thể tạo một bộ sưu tập chữ ký điện tử và thêm chúng vào tệp chỉ bằng một thao tác.

#### Hỏi: Các yêu cầu để thêm chữ ký điện tử vào tệp Excel là gì?

Trả lời: Để thêm chữ ký điện tử vào tệp Excel, bạn cần có chứng chỉ kỹ thuật số hợp lệ sẽ được sử dụng để ký tài liệu. Đảm bảo bạn có chứng chỉ và mật khẩu chính xác trước khi thêm chữ ký điện tử.