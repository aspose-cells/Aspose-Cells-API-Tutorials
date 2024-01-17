---
title: Mở khóa bảng tính Excel được bảo vệ bằng mật khẩu
linktitle: Mở khóa bảng tính Excel được bảo vệ bằng mật khẩu
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách mở khóa bảng tính Excel được bảo vệ bằng mật khẩu bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 10
url: /vi/net/unprotect-excel-sheet/unlock-password-protected-excel-worksheet/
---
Bảo vệ bằng mật khẩu của bảng tính Excel thường được sử dụng để bảo mật dữ liệu nhạy cảm. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để hiểu và triển khai mã nguồn C# được cung cấp để mở khóa bảng tính Excel được bảo vệ bằng mật khẩu bằng thư viện Aspose.Cells cho .NET.

## Bước 1: Chuẩn bị môi trường

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Bạn có thể tải xuống thư viện từ trang web chính thức của Aspose và cài đặt nó bằng cách làm theo hướng dẫn được cung cấp.

Sau khi quá trình cài đặt hoàn tất, hãy tạo dự án C# mới trong môi trường phát triển tích hợp (IDE) ưa thích của bạn và nhập thư viện Aspose.Cells cho .NET.

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

 Bây giờ chúng ta sẽ mở khóa bảng tính bằng cách sử dụng`Unprotect()` phương thức của đối tượng Worksheet. Để trống chuỗi mật khẩu (`""`) nếu bảng tính không được bảo vệ bằng mật khẩu.

```csharp
// Bỏ bảo vệ bảng tính bằng mật khẩu
worksheet.Unprotect("");
```

## Bước 6: Lưu file Excel đã mở khóa

Sau khi bảng tính được mở khóa, chúng ta có thể lưu tệp Excel cuối cùng. Sử dụng`Save()` phương pháp chỉ định đường dẫn đầy đủ của tệp đầu ra

.

```csharp
// Lưu sổ làm việc
workbook.Save(dataDir + "output.out.xls");
```

### Mã nguồn mẫu cho Bảng tính Excel được bảo vệ bằng mật khẩu mở khóa bằng Aspose.Cells cho .NET 
```csharp
try
{
    //Đường dẫn đến thư mục tài liệu.
    string dataDir = "YOUR DOCUMENT DIRECTORY";
    // Khởi tạo một đối tượng Workbook
    Workbook workbook = new Workbook(dataDir + "book1.xls");
    // Truy cập bảng tính đầu tiên trong tệp Excel
    Worksheet worksheet = workbook.Worksheets[0];
    // Bỏ bảo vệ bảng tính bằng mật khẩu
    worksheet.Unprotect("");
    // Lưu sổ làm việc
    workbook.Save(dataDir + "output.out.xls");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã tìm ra cách sử dụng Aspose.Cells cho .NET để mở khóa bảng tính Excel được bảo vệ bằng mật khẩu bằng mã nguồn C#. Bằng cách làm theo các bước trong hướng dẫn này, bạn có thể áp dụng chức năng này cho các dự án của riêng mình và làm việc với các tệp Excel một cách hiệu quả và an toàn.

Vui lòng khám phá thêm các tính năng do Aspose.Cells cung cấp để có các hoạt động nâng cao hơn.

### Câu hỏi thường gặp

#### Hỏi: Điều gì sẽ xảy ra nếu bảng tính được bảo vệ bằng mật khẩu?

 Đáp: Nếu bảng tính được bảo vệ bằng mật khẩu, bạn phải cung cấp mật khẩu thích hợp trong phần`Unprotect()` phương pháp để có thể mở khóa nó.

#### Hỏi: Có bất kỳ hạn chế hoặc biện pháp phòng ngừa nào khi mở khóa bảng tính Excel được bảo vệ không?

Đáp: Có, hãy đảm bảo bạn có các quyền cần thiết để mở khóa bảng tính. Ngoài ra, hãy đảm bảo tuân thủ các chính sách bảo mật của tổ chức bạn khi sử dụng tính năng này.