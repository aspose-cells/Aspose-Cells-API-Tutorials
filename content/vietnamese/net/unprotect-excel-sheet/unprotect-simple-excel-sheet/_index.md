---
title: Bỏ bảo vệ bảng Excel đơn giản
linktitle: Bỏ bảo vệ bảng Excel đơn giản
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách Bỏ bảo vệ bảng tính Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 30
url: /vi/net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn các bước cần thiết để mở khóa bảng tính Excel đơn giản bằng thư viện Aspose.Cells cho .NET.

## Bước 1: Chuẩn bị môi trường

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Tải xuống thư viện từ trang web chính thức của Aspose và làm theo hướng dẫn cài đặt được cung cấp.

## Bước 2: Cấu hình đường dẫn thư mục tài liệu

 Trong mã nguồn được cung cấp, bạn cần chỉ định đường dẫn thư mục chứa tệp Excel bạn muốn mở khóa. Sửa đổi`dataDir` bằng cách thay thế "THƯ VIỆN TÀI LIỆU CỦA BẠN" bằng đường dẫn tuyệt đối của thư mục trên máy của bạn.

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Bước 3: Tạo đối tượng sổ làm việc

Để bắt đầu, chúng ta cần tạo một đối tượng Workbook đại diện cho tệp Excel của mình. Sử dụng hàm tạo của lớp Workbook và chỉ định đường dẫn đầy đủ của tệp Excel để mở.

```csharp
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## Bước 4: Truy cập bảng tính

 Tiếp theo, chúng ta cần điều hướng đến bảng tính đầu tiên trong tệp Excel. Sử dụng`Worksheets` thuộc tính của đối tượng Workbook để truy cập vào bộ sưu tập các trang tính, sau đó sử dụng thuộc tính`[0]` chỉ mục để truy cập trang tính đầu tiên.

```csharp
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## Bước 5: Mở khóa bảng tính

 Bây giờ chúng ta sẽ mở khóa bảng tính bằng cách sử dụng`Unprotect()` phương thức của đối tượng Worksheet. Phương pháp này không yêu cầu mật khẩu.

```csharp
// Bỏ bảo vệ bảng tính không cần mật khẩu
worksheet.Unprotect();
```

## Bước 6: Lưu file Excel đã mở khóa

Sau khi bảng tính được mở khóa, chúng ta có thể lưu tệp Excel cuối cùng. Sử dụng`Save()` phương pháp chỉ định đường dẫn đầy đủ của tệp đầu ra và định dạng lưu.

```csharp
// Lưu sổ làm việc
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
### Mã nguồn mẫu cho Bảng tính Excel đơn giản không bảo vệ bằng Aspose.Cells for .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook(dataDir + "book1.xls");
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Bỏ bảo vệ bảng tính không cần mật khẩu
worksheet.Unprotect();
// Lưu sổ làm việc
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã học cách mở khóa bảng tính Excel đơn giản bằng Aspose.Cells cho .NET. Bằng cách làm theo các bước trong hướng dẫn này, bạn có thể dễ dàng áp dụng tính năng này cho các dự án của riêng mình.

Hãy thoải mái khám phá thêm các tính năng của Aspose.Cells
để biết thêm các thao tác nâng cao trên tệp Excel.

### Câu hỏi thường gặp

#### Hỏi: Tôi nên thực hiện các biện pháp phòng ngừa nào khi mở khóa bảng tính Excel?

Đáp: Khi mở khóa bảng tính Excel, hãy đảm bảo bạn có các quyền cần thiết để truy cập vào tệp. Ngoài ra, hãy đảm bảo sử dụng đúng phương pháp mở khóa và cung cấp mật khẩu chính xác, nếu có.

#### Hỏi: Làm cách nào để biết bảng tính có được bảo vệ bằng mật khẩu hay không?

 Đáp: Bạn có thể kiểm tra xem một trang tính có được bảo vệ bằng mật khẩu hay không bằng cách sử dụng các thuộc tính hoặc phương thức do thư viện Aspose.Cells dành cho .NET cung cấp. Ví dụ: bạn có thể sử dụng`IsProtected()` của đối tượng Worksheet để kiểm tra xem bảng tính có được bảo vệ hay không.

#### Hỏi: Tôi gặp ngoại lệ khi cố gắng mở khóa bảng tính. Tôi nên làm gì ?

Đáp: Nếu bạn gặp phải ngoại lệ khi mở khóa bảng tính, vui lòng đảm bảo rằng bạn đã chỉ định chính xác đường dẫn đến tệp Excel và kiểm tra xem bạn có các quyền cần thiết để truy cập vào tệp đó hay không. Nếu sự cố vẫn tiếp diễn, vui lòng liên hệ với bộ phận hỗ trợ của Aspose.Cells để được hỗ trợ thêm.