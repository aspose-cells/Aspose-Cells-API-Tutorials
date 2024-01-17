---
title: Chỉ định tác giả khi viết bảo vệ sổ làm việc Excel
linktitle: Chỉ định tác giả khi viết bảo vệ sổ làm việc Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách bảo vệ và tùy chỉnh sổ làm việc Excel của bạn bằng Aspose.Cells for .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 30
url: /vi/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Trong hướng dẫn này, chúng tôi sẽ chỉ cho bạn cách chỉ định tác giả khi bảo vệ chống ghi cho sổ làm việc Excel bằng thư viện Aspose.Cells cho .NET.

## Bước 1: Chuẩn bị môi trường

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Tải xuống thư viện từ trang web chính thức của Aspose và làm theo hướng dẫn cài đặt được cung cấp.

## Bước 2: Cấu hình thư mục nguồn và đầu ra

Trong mã nguồn được cung cấp, bạn phải chỉ định thư mục nguồn và đầu ra. Sửa đổi`sourceDir` Và`outputDir` các biến bằng cách thay thế "THƯ MỤC NGUỒN CỦA BẠN" và "THƯ MỤC ĐẦU RA CỦA BẠN" bằng các đường dẫn tuyệt đối tương ứng trên máy của bạn.

```csharp
// Thư mục nguồn
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Thư mục đầu ra
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Bước 3: Tạo sổ làm việc Excel trống

Để bắt đầu, chúng ta tạo một đối tượng Workbook đại diện cho một sổ làm việc Excel trống.

```csharp
// Tạo sổ làm việc trống.
Workbook wb = new Workbook();
```

## Bước 4: Viết bảo vệ bằng mật khẩu

 Tiếp theo, chúng tôi chỉ định mật khẩu để ghi bảo vệ sổ làm việc Excel bằng cách sử dụng`WriteProtection.Password` thuộc tính của đối tượng Workbook.

```csharp
// Viết bảo vệ sổ làm việc bằng mật khẩu.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Bước 5: Đặc tả tác giả

 Bây giờ chúng ta chỉ định tác giả của sổ làm việc Excel bằng cách sử dụng`WriteProtection.Author` thuộc tính của đối tượng Workbook.

```csharp
// Chỉ định tác giả trong khi viết sổ làm việc bảo vệ.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Bước 6: Sao lưu sổ làm việc Excel được bảo vệ

 Sau khi chỉ định bảo vệ ghi và tác giả, chúng ta có thể lưu sổ làm việc Excel ở định dạng XLSX bằng cách sử dụng lệnh`Save()` phương pháp.

```csharp
// Lưu sổ làm việc ở định dạng XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Mã nguồn mẫu cho Chỉ định tác giả khi viết Bảo vệ sổ làm việc Excel bằng Aspose.Cells cho .NET 
```csharp
//Thư mục nguồn
string sourceDir = "YOUR SOURCE DIRECTORY";

//Thư mục đầu ra
string outputDir = "YOUR OUTPUT DIRECTORY";

// Tạo sổ làm việc trống.
Workbook wb = new Workbook();

// Viết bảo vệ sổ làm việc bằng mật khẩu.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Chỉ định tác giả trong khi viết sổ làm việc bảo vệ.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Lưu sổ làm việc ở định dạng XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách chỉ định tác giả khi bảo vệ chống ghi một sổ làm việc Excel bằng Aspose.Cells cho .NET. Bạn có thể áp dụng các bước này cho dự án của riêng mình để bảo vệ và tùy chỉnh sổ làm việc Excel của mình.

Vui lòng khám phá thêm các tính năng của Aspose.Cells for .NET để có các thao tác nâng cao hơn trên tệp Excel.

## Câu hỏi thường gặp

#### Hỏi: Tôi có thể viết bảo vệ sổ làm việc Excel mà không cần chỉ định mật khẩu không?

 Đáp: Có, bạn có thể sử dụng đối tượng Workbook`WriteProtect()` phương pháp mà không chỉ định mật khẩu để bảo vệ chống ghi sổ làm việc Excel. Điều này sẽ hạn chế những thay đổi đối với sổ làm việc mà không yêu cầu mật khẩu.

#### Hỏi: Làm cách nào để loại bỏ tính năng chống ghi khỏi sổ làm việc Excel?

 Đáp: Để loại bỏ tính năng chống ghi khỏi sổ làm việc Excel, bạn có thể sử dụng`Unprotect()` phương thức của đối tượng Worksheet hoặc`RemoveWriteProtection()` của đối tượng Workbook, tùy thuộc vào trường hợp sử dụng cụ thể của bạn. .

#### Hỏi: Tôi quên mật khẩu để bảo vệ sổ làm việc Excel của mình. Tôi có thể làm gì ?

Trả lời: Nếu bạn quên mật khẩu để bảo vệ sổ làm việc Excel của mình, bạn không thể xóa mật khẩu đó trực tiếp. Tuy nhiên, bạn có thể thử sử dụng các công cụ chuyên dụng của bên thứ ba cung cấp tính năng khôi phục mật khẩu cho các tệp Excel được bảo vệ.

#### Câu hỏi: Có thể chỉ định nhiều tác giả khi bảo vệ chống ghi cho sổ làm việc Excel không?

Trả lời: Không, thư viện Aspose.Cells for .NET cho phép chỉ định một tác giả duy nhất khi bảo vệ chống ghi cho sổ làm việc Excel. Nếu bạn muốn chỉ định nhiều tác giả, bạn sẽ cần xem xét các giải pháp tùy chỉnh bằng cách thao tác trực tiếp với tệp Excel.