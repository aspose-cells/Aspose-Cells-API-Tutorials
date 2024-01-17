---
title: Bảo vệ bằng mật khẩu hoặc không bảo vệ sổ làm việc được chia sẻ
linktitle: Bảo vệ bằng mật khẩu hoặc không bảo vệ sổ làm việc được chia sẻ
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách bảo vệ bằng mật khẩu hoặc bỏ bảo vệ sổ làm việc được chia sẻ bằng Aspose.Cells cho .NET.
type: docs
weight: 120
url: /vi/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Bảo vệ sổ làm việc dùng chung bằng mật khẩu là điều quan trọng để đảm bảo quyền riêng tư của dữ liệu. Với Aspose.Cells cho .NET, bạn có thể dễ dàng bảo vệ hoặc bỏ bảo vệ sổ làm việc dùng chung bằng mật khẩu. Thực hiện theo các bước dưới đây để có được kết quả mong muốn:

## Bước 1: Chỉ định thư mục đầu ra

Trước tiên, bạn cần chỉ định thư mục đầu ra nơi tệp Excel được bảo vệ sẽ được lưu. Đây là cách thực hiện bằng Aspose.Cells:

```csharp
// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

## Bước 2: Tạo một file Excel trống

Sau đó, bạn có thể tạo một tệp Excel trống mà bạn muốn áp dụng chế độ bảo vệ hoặc không bảo vệ. Đây là một mã mẫu:

```csharp
// Tạo một sổ làm việc Excel trống
Workbook wb = new Workbook();
```

## Bước 3: Bảo vệ hoặc bỏ bảo vệ sổ làm việc được chia sẻ

Sau khi tạo sổ làm việc, bạn có thể bảo vệ hoặc bỏ bảo vệ sổ làm việc được chia sẻ bằng cách chỉ định mật khẩu thích hợp. Đây là cách thực hiện:

```csharp
// Bảo vệ sổ làm việc được chia sẻ bằng mật khẩu
wb.ProtectSharedWorkbook("1234");

// Bỏ ghi chú dòng này để bỏ bảo vệ sổ làm việc được chia sẻ
// wb.UnprotectSharedWorkbook("1234");
```

## Bước 4: Lưu file Excel đầu ra

Sau khi áp dụng biện pháp bảo vệ hoặc không bảo vệ, bạn có thể lưu tệp Excel được bảo vệ vào thư mục đầu ra được chỉ định. Đây là cách thực hiện:

```csharp
// Lưu tệp Excel đầu ra
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Mã nguồn mẫu cho Sổ làm việc được chia sẻ được bảo vệ bằng mật khẩu hoặc không bảo vệ bằng Aspose.Cells for .NET 
```csharp
//Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
//Tạo tệp Excel trống
Workbook wb = new Workbook();
//Bảo vệ sổ làm việc được chia sẻ bằng mật khẩu
wb.ProtectSharedWorkbook("1234");
//Bỏ ghi chú dòng này để bỏ bảo vệ sổ làm việc được chia sẻ
//wb.UnprotectSharedWorkbook("1234");
//Lưu tệp Excel đầu ra
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Phần kết luận

Việc bảo vệ hoặc bỏ bảo vệ sổ làm việc dùng chung bằng mật khẩu là điều cần thiết để đảm bảo an toàn dữ liệu. Với Aspose.Cells for .NET, bạn có thể dễ dàng thêm chức năng này vào tệp Excel của mình. Bằng cách làm theo các bước trong hướng dẫn này, bạn có thể bảo vệ hoặc bỏ bảo vệ sổ làm việc được chia sẻ của mình một cách hiệu quả bằng mật khẩu. Thử nghiệm với các tệp Excel của riêng bạn và đảm bảo duy trì tính bảo mật cho dữ liệu nhạy cảm của bạn.

### Câu hỏi thường gặp

#### Câu hỏi: Tôi có thể áp dụng những loại bảo vệ nào cho sổ làm việc được chia sẻ với Aspose.Cells?
    
Trả lời: Với Aspose.Cells, bạn có thể bảo vệ sổ làm việc dùng chung bằng cách chỉ định mật khẩu để ngăn chặn truy cập trái phép, sửa đổi hoặc xóa dữ liệu.

#### Câu hỏi: Tôi có thể bảo vệ sổ làm việc được chia sẻ mà không cần chỉ định mật khẩu không?
    
Trả lời: Có, bạn có thể bảo vệ sổ làm việc được chia sẻ mà không cần chỉ định mật khẩu. Tuy nhiên, nên sử dụng mật khẩu mạnh để bảo mật tốt hơn.

#### Câu hỏi: Làm cách nào tôi có thể bỏ bảo vệ sổ làm việc được chia sẻ với Aspose.Cells?
    
Trả lời: Để bỏ bảo vệ sổ làm việc được chia sẻ, bạn phải chỉ định cùng một mật khẩu đã được sử dụng khi bảo vệ sổ làm việc. Điều này cho phép loại bỏ sự bảo vệ và dữ liệu được truy cập tự do.

#### Hỏi: Việc bảo vệ sổ làm việc dùng chung có ảnh hưởng đến các tính năng và công thức trong sổ làm việc không?
    
Trả lời: Khi bạn bảo vệ sổ làm việc được chia sẻ, người dùng vẫn có thể truy nhập các tính năng và công thức có trong sổ làm việc. Bảo vệ chỉ ảnh hưởng đến những thay đổi về cấu trúc đối với sổ làm việc.