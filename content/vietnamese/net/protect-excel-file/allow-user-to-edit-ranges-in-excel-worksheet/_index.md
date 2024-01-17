---
title: Cho phép người dùng chỉnh sửa phạm vi trong bảng tính Excel
linktitle: Cho phép người dùng chỉnh sửa phạm vi trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước với mã nguồn trong C#.
type: docs
weight: 10
url: /vi/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn cách sử dụng Aspose.Cells cho .NET để cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính Excel. Thực hiện theo các bước dưới đây để hoàn thành nhiệm vụ này.

## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã thiết lập môi trường phát triển của mình và cài đặt Aspose.Cells cho .NET. Bạn có thể tải xuống phiên bản mới nhất của thư viện từ trang web chính thức của Aspose.

## Bước 2: Nhập các không gian tên bắt buộc

Trong dự án C# của bạn, hãy nhập các vùng tên cần thiết để hoạt động với Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Bước 3: Thiết lập đường dẫn đến thư mục tài liệu

 Khai báo một`dataDir` biến để chỉ định đường dẫn đến thư mục mà bạn muốn lưu tệp Excel đã tạo:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENT_DIRECTORY"` với đường dẫn chính xác trên hệ thống của bạn.

## Bước 4: Tạo đối tượng sổ làm việc

Khởi tạo một đối tượng Workbook mới đại diện cho sổ làm việc Excel mà bạn muốn tạo:

```csharp
Workbook book = new Workbook();
```

## Bước 5: Truy cập vào bảng tính đầu tiên

Điều hướng đến trang tính đầu tiên trong sổ làm việc Excel bằng mã sau:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## Bước 6: Truy xuất phạm vi sửa đổi được ủy quyền

 Nhận bộ sưu tập các phạm vi chỉnh sửa được phép bằng cách sử dụng`AllowEditRanges` tài sản:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Bước 7: Xác định phạm vi được bảo vệ

 Xác định phạm vi được bảo vệ bằng cách sử dụng`Add` phương pháp của`AllowEditRanges` bộ sưu tập:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Ở đây chúng tôi đã tạo một phạm vi được bảo vệ "r2" trải dài từ ô A1 đến ô C3.

## Bước 8: Chỉ định mật khẩu

 Chỉ định mật khẩu cho phạm vi được bảo vệ bằng cách sử dụng`Password` tài sản:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Hãy chắc chắn để thay thế`"YOUR_PASSWORD"` với mật khẩu mong muốn.

## Bước 9: Bảo vệ bảng tính

 Bảo vệ bảng tính bằng cách sử dụng`Protect` phương pháp của`Worksheet` sự vật:

```csharp
sheet.Protect(ProtectionType.All);
```

Điều này sẽ bảo vệ bảng tính bằng cách ngăn chặn mọi sửa đổi ngoài phạm vi cho phép.

## Bước 10: Đăng ký

  tập tin Excel

 Lưu tệp Excel đã tạo bằng cách sử dụng`Save` phương pháp của`Workbook` sự vật:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

Đảm bảo chỉ định tên tệp mong muốn và đường dẫn chính xác.

### Mã nguồn mẫu cho Cho phép người dùng chỉnh sửa phạm vi trong bảng tính Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo thư mục nếu nó chưa có.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Khởi tạo một Workbook mới
Workbook book = new Workbook();
// Lấy bảng tính (mặc định) đầu tiên
Worksheet sheet = book.Worksheets[0];
// Nhận phạm vi cho phép chỉnh sửa
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Xác định phạm vi bảo vệ
ProtectedRange proteced_range;
// Tạo phạm vi
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Chỉ định mật khẩu
proteced_range.Password = "123";
// Bảo vệ tấm
sheet.Protect(ProtectionType.All);
// Lưu tệp Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Phần kết luận

Bây giờ bạn đã học cách sử dụng Aspose.Cells cho .NET để cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính Excel. Vui lòng khám phá thêm các tính năng do Aspose.Cells cung cấp để đáp ứng nhu cầu cụ thể của bạn.


### Câu hỏi thường gặp

#### 1. Làm cách nào để cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính Excel?

 Bạn có thể dùng`ProtectedRangeCollection` lớp để xác định phạm vi sửa đổi được phép. Sử dụng`Add` phương pháp để tạo một phạm vi được bảo vệ mới với các ô mong muốn.

#### 2. Tôi có thể đặt mật khẩu cho phạm vi sửa đổi được phép không?

 Có, bạn có thể chỉ định mật khẩu bằng cách sử dụng`Password` tài sản của`ProtectedRange` sự vật. Điều này sẽ hạn chế quyền truy cập chỉ đối với người dùng có mật khẩu.

#### 3. Làm cách nào để bảo vệ bảng tính khi phạm vi được phép được đặt?

 Sử dụng`Protect` phương pháp của`Worksheet` đối tượng để bảo vệ bảng tính. Điều này sẽ ngăn mọi thay đổi nằm ngoài phạm vi cho phép, có thể nhắc nhập mật khẩu nếu bạn đã chỉ định mật khẩu.