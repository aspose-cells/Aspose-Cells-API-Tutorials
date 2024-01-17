---
title: Tạo sổ làm việc được chia sẻ
linktitle: Tạo sổ làm việc được chia sẻ
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tạo sổ làm việc chia sẻ Excel với Aspose.Cells for .NET để cho phép cộng tác dữ liệu đồng thời.
type: docs
weight: 70
url: /vi/net/excel-workbook/create-shared-workbook/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn mã nguồn C# được cung cấp để cho phép bạn tạo sổ làm việc dùng chung bằng Aspose.Cells cho .NET. Thực hiện theo các bước dưới đây để thực hiện thao tác này.

## Bước 1: Đặt thư mục đầu ra

```csharp
// Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
```

Trong bước đầu tiên này, chúng tôi xác định thư mục đầu ra nơi sổ làm việc được chia sẻ sẽ được lưu.

## Bước 2: Tạo đối tượng sổ làm việc

```csharp
// Tạo đối tượng Workbook
Workbook wb = new Workbook();
```

Chúng tôi đang tạo một đối tượng Workbook mới sẽ đại diện cho sổ làm việc Excel của chúng tôi.

## Bước 3: Kích hoạt tính năng chia sẻ sổ làm việc

```csharp
// Chia sẻ sổ làm việc
wb.Settings.Shared = true;
```

 Chúng tôi kích hoạt tính năng chia sẻ của sổ làm việc bằng cách đặt`Shared` thuộc tính của đối tượng Workbook`true`.

## Bước 4: Lưu sổ làm việc được chia sẻ

```csharp
// Lưu sổ làm việc được chia sẻ
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Chúng tôi lưu sổ làm việc được chia sẻ bằng cách chỉ định đường dẫn và tên của tệp đầu ra.

### Mã nguồn mẫu để Tạo sổ làm việc được chia sẻ bằng Aspose.Cells cho .NET 
```csharp
//Thư mục đầu ra
string outputDir = RunExamples.Get_OutputDirectory();
//Tạo đối tượng Workbook
Workbook wb = new Workbook();
//Chia sẻ sổ làm việc
wb.Settings.Shared = true;
//Lưu sổ làm việc được chia sẻ
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách tạo sổ làm việc dùng chung bằng Aspose.Cells cho .NET. Sổ làm việc được chia sẻ có thể được nhiều người dùng sử dụng đồng thời để cộng tác trên dữ liệu. Thử nghiệm với dữ liệu của riêng bạn và khám phá thêm các tính năng của Aspose.Cells để tạo sổ làm việc Excel mạnh mẽ và được cá nhân hóa.

### Câu hỏi thường gặp

#### Câu hỏi: Sổ làm việc dùng chung là gì?

Đáp: Sổ làm việc được chia sẻ là một sổ làm việc Excel có thể được nhiều người dùng sử dụng đồng thời để cộng tác trên dữ liệu. Mỗi người dùng có thể thực hiện các thay đổi đối với sổ làm việc và những người dùng khác sẽ thấy thông tin cập nhật theo thời gian thực.

#### Câu hỏi: Làm cách nào để bật tính năng chia sẻ sổ làm việc trong Aspose.Cells cho .NET?

 Trả lời: Để cho phép chia sẻ sổ làm việc trong Aspose.Cells cho .NET, bạn phải đặt`Shared` thuộc tính của đối tượng Workbook`true`. Điều này sẽ cho phép người dùng làm việc trên sổ làm việc cùng một lúc.

#### Hỏi: Tôi có thể hạn chế quyền của người dùng trong sổ làm việc được chia sẻ không?

Đáp: Có, bạn có thể hạn chế quyền của người dùng trong sổ làm việc được chia sẻ bằng các tính năng bảo mật của Excel. Bạn có thể đặt các quyền cụ thể cho từng người dùng, chẳng hạn như khả năng chỉnh sửa, chỉ đọc, v.v.

#### Hỏi: Làm cách nào tôi có thể chia sẻ sổ làm việc với những người dùng khác?

Đáp: Khi bạn đã tạo sổ làm việc dùng chung, bạn có thể chia sẻ sổ làm việc đó với những người dùng khác bằng cách gửi cho họ tệp Excel. Những người dùng khác sẽ có thể mở tệp và làm việc trên đó cùng một lúc.

#### Hỏi: Có phải tất cả các tính năng của Excel đều được hỗ trợ trong sổ làm việc dùng chung không?

Đáp: Hầu hết các tính năng của Excel đều được hỗ trợ trong sổ làm việc dùng chung. Tuy nhiên, một số tính năng nâng cao, chẳng hạn như macro và phần bổ trợ, có thể có những hạn chế hoặc hạn chế khi sử dụng trong sổ làm việc chung.