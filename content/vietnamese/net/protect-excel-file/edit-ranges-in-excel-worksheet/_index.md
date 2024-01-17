---
title: Chỉnh sửa phạm vi trong bảng tính Excel
linktitle: Chỉnh sửa phạm vi trong bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách chỉnh sửa các phạm vi cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 20
url: /vi/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel là một công cụ mạnh mẽ để tạo và quản lý bảng tính, cung cấp nhiều tính năng để kiểm soát và bảo mật dữ liệu. Một tính năng như vậy là cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính đồng thời bảo vệ các phần khác. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước cách triển khai chức năng này bằng Aspose.Cells for .NET, một thư viện phổ biến để làm việc với các tệp Excel theo chương trình.

Sử dụng Aspose.Cells cho .NET sẽ cho phép bạn thao tác các phạm vi trong bảng tính Excel một cách dễ dàng, cung cấp giao diện thân thiện với người dùng và các tính năng nâng cao. Thực hiện theo các bước bên dưới để cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính Excel bằng Aspose.Cells for .NET.
## Bước 1: Thiết lập môi trường

Đảm bảo bạn đã cài đặt Aspose.Cells for .NET trong môi trường phát triển của mình. Tải xuống thư viện từ trang web chính thức của Aspose và kiểm tra tài liệu để biết hướng dẫn cài đặt.

## Bước 2: Khởi tạo Workbook và Worksheet

Để bắt đầu, chúng ta cần tạo một sổ làm việc mới và lấy tham chiếu đến trang tính mà chúng ta muốn cho phép thay đổi phạm vi. Sử dụng đoạn mã sau để đạt được điều này:

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Tạo thư mục nếu nó chưa tồn tại.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Khởi tạo một sổ làm việc mới
Workbook workbook = new Workbook();

// Lấy bảng tính đầu tiên (mặc định)
Worksheet sheet = workbook.Worksheets[0];
```

 Trong đoạn mã này, trước tiên chúng ta xác định đường dẫn đến thư mục nơi tệp Excel sẽ được lưu. Tiếp theo, chúng ta tạo một phiên bản mới của`Workbook` lớp và lấy tham chiếu đến bảng tính đầu tiên bằng cách sử dụng`Worksheets` tài sản.

## Bước 3: Nhận phạm vi có thể chỉnh sửa

Bây giờ chúng ta cần truy xuất các phạm vi mà chúng ta muốn cho phép sửa đổi. Sử dụng mã sau đây:

```csharp
// Nhận phạm vi có thể sửa đổi
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## Bước 4: Đặt phạm vi được bảo vệ

Trước khi cho phép sửa đổi phạm vi, chúng ta cần xác định phạm vi được bảo vệ. Đây là cách thực hiện:

```csharp
// Xác định phạm vi được bảo vệ
ProtectedRange ProtectedRange;

// Tạo phạm vi
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

 Trong mã này, chúng tôi tạo một phiên bản mới của`ProtectedRange` lớp và sử dụng`Add` phương pháp xác định phạm vi cần bảo vệ.

## Bước 5: Chỉ định mật khẩu

Để tăng cường bảo mật, bạn có thể chỉ định mật khẩu cho phạm vi được bảo vệ. Đây là cách thực hiện:

```csharp
// Chỉ định mật khẩu
protectedBeach.Password = "YOUR_PASSWORD";
```

## Bước 6: Bảo vệ bảng tính

Bây giờ chúng ta đã thiết lập phạm vi được bảo vệ, chúng ta có thể bảo vệ bảng tính để ngăn chặn những sửa đổi trái phép. Sử dụng mã sau đây:

```csharp
// Bảo vệ bảng tính
leaf.Protect(ProtectionType.All);
```

## Bước 7: Lưu tệp Excel

Cuối cùng, chúng ta lưu file Excel với những thay đổi đã thực hiện. Đây là mã cần thiết:

```csharp
// Lưu tệp Excel
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Mã nguồn mẫu để chỉnh sửa phạm vi trong bảng tính Excel bằng Aspose.Cells cho .NET 
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
proteced_range.Password = "YOUR_PASSWORD";

// Bảo vệ tấm
sheet.Protect(ProtectionType.All);

// Lưu tệp Excel
book.Save(dataDir + "protectedrange.out.xls");
```

## Phần kết luận

Xin chúc mừng! Bạn đã học cách cho phép người dùng chỉnh sửa các phạm vi cụ thể trong bảng tính Excel bằng Aspose.Cells cho .NET. Bây giờ bạn có thể áp dụng kỹ thuật này trong các dự án của riêng mình và cải thiện tính bảo mật của tệp Excel.


#### Câu hỏi thường gặp

#### Câu hỏi: Tại sao tôi nên sử dụng Aspose.Cells for .NET để chỉnh sửa các phạm vi trong bảng tính Excel?

Trả lời: Aspose.Cells for .NET cung cấp API mạnh mẽ và dễ sử dụng để làm việc với các tệp Excel. Nó cung cấp các tính năng nâng cao, chẳng hạn như thao tác phạm vi, bảo vệ bảng tính, v.v.

#### Câu hỏi: Tôi có thể đặt nhiều phạm vi có thể chỉnh sửa trong một trang tính không?

 Đáp: Có, bạn có thể xác định nhiều phạm vi có thể chỉnh sửa bằng cách sử dụng`Add` phương pháp của`ProtectedRangeCollection` bộ sưu tập. Mỗi phạm vi có thể có cài đặt bảo vệ riêng.

####  Câu hỏi: Có thể xóa một phạm vi có thể chỉnh sửa sau khi xác định nó không?

 Đ: Có, bạn có thể sử dụng`RemoveAt` phương pháp của`ProtectedRangeCollection` bộ sưu tập để xóa một phạm vi có thể chỉnh sửa cụ thể bằng cách chỉ định chỉ mục của nó.

#### Hỏi: Làm cách nào tôi có thể mở tệp Excel được bảo vệ sau khi lưu?

Trả lời: Bạn sẽ cần cung cấp mật khẩu được chỉ định khi tạo phạm vi được bảo vệ để mở tệp Excel được bảo vệ. Đảm bảo giữ mật khẩu ở nơi an toàn để tránh mất quyền truy cập vào dữ liệu.