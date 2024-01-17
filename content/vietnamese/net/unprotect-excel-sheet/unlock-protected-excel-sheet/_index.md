---
title: Mở khóa bảng Excel được bảo vệ
linktitle: Mở khóa bảng Excel được bảo vệ
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách mở khóa bảng tính Excel được bảo vệ bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 20
url: /vi/net/unprotect-excel-sheet/unlock-protected-excel-sheet/
---
Bảo vệ bảng tính Excel thường được sử dụng để hạn chế quyền truy cập và sửa đổi dữ liệu. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để hiểu và triển khai mã nguồn C# được cung cấp để mở khóa bảng tính Excel được bảo vệ bằng thư viện Aspose.Cells cho .NET.

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

Sau khi bảng tính được mở khóa, chúng ta có thể lưu tệp Excel cuối cùng. Sử dụng`Save()` phương pháp chỉ định đường dẫn đầy đủ của tệp đầu ra.

```csharp
// Lưu sổ làm việc


workbook.Save(dataDir + "output.out.xls");
```

### Mã nguồn mẫu để mở khóa Bảng Excel được bảo vệ bằng Aspose.Cells for .NET 
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
catch(Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã tìm ra cách sử dụng Aspose.Cells cho .NET để mở khóa bảng tính Excel được bảo vệ bằng mã nguồn C#. Bằng cách làm theo các bước trong hướng dẫn này, bạn có thể áp dụng chức năng này cho các dự án của riêng mình và làm việc với các tệp Excel một cách hiệu quả và an toàn.

Vui lòng khám phá thêm các tính năng do Aspose.Cells cung cấp để có các hoạt động nâng cao hơn.

### Câu hỏi thường gặp

#### Hỏi: Tôi nên thực hiện các biện pháp phòng ngừa nào khi mở khóa bảng tính Excel được bảo vệ?

Đáp: Khi mở khóa bảng tính Excel được bảo vệ, hãy đảm bảo bạn có các quyền cần thiết để truy cập vào tệp. Ngoài ra, hãy kiểm tra xem bạn có đang sử dụng đúng phương pháp mở khóa không và cung cấp mật khẩu chính xác, nếu có.

#### Hỏi: Làm cách nào để biết bảng tính có được bảo vệ bằng mật khẩu hay không?

 Trả lời: Bạn có thể kiểm tra xem trang tính có được bảo vệ bằng mật khẩu hay không bằng cách sử dụng các thuộc tính hoặc phương thức từ thư viện Aspose.Cells cho .NET. Ví dụ: bạn có thể sử dụng`IsProtected()` phương thức của đối tượng Worksheet để kiểm tra trạng thái bảo vệ của trang tính.

#### Hỏi: Tôi gặp ngoại lệ khi cố gắng mở khóa bảng tính. Tôi nên làm gì ?

Đáp: Nếu bạn gặp phải ngoại lệ khi mở khóa bảng tính, hãy đảm bảo rằng bạn đã chỉ định chính xác đường dẫn tệp Excel và xác minh rằng bạn có các quyền cần thiết để truy cập vào tệp. Nếu sự cố vẫn tiếp diễn, vui lòng liên hệ với bộ phận Hỗ trợ của Aspose.Cells để được hỗ trợ thêm.