---
title: Bảo vệ bảng tính Excel
linktitle: Bảo vệ bảng tính Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Khám phá trong hướng dẫn này cách bảo vệ bảng tính Excel bằng Aspose.Cells cho .NET. Hướng dẫn từng bước trong C#.
type: docs
weight: 50
url: /vi/net/protect-excel-file/protect-excel-worksheet/
---
Trong hướng dẫn này, chúng ta sẽ xem xét một số mã nguồn C# sử dụng thư viện Aspose.Cells để bảo vệ bảng tính Excel. Chúng tôi sẽ đi qua từng bước của mã và giải thích cách hoạt động của mã. Hãy chắc chắn làm theo hướng dẫn cẩn thận để có được kết quả mong muốn.

## Bước 1: Điều kiện tiên quyết

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt thư viện Aspose.Cells cho .NET. Bạn có thể lấy nó từ trang web chính thức của Aspose. Ngoài ra, hãy đảm bảo rằng bạn có phiên bản Visual Studio mới hoặc bất kỳ môi trường phát triển C# nào khác.

## Bước 2: Nhập các không gian tên bắt buộc

Để sử dụng thư viện Aspose.Cells, chúng ta cần nhập các vùng tên cần thiết vào mã của mình. Thêm các dòng sau vào đầu tệp nguồn C# của bạn:

```csharp
using Aspose.Cells;
using System.IO;
```

## Bước 3: Tải file Excel

Trong bước này, chúng tôi sẽ tải tệp Excel mà chúng tôi muốn bảo vệ. Đảm bảo chỉ định đúng đường dẫn đến thư mục chứa tệp Excel. Sử dụng đoạn mã sau để tải tệp lên:

```csharp
// Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Tạo một luồng tệp chứa tệp Excel để mở.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Khởi tạo một đối tượng Workbook.
//Mở tệp Excel qua luồng tệp.
Workbook excel = new Workbook(fstream);
```

 Hãy chắc chắn để thay thế`"YOUR_DOCUMENTS_DIR"` với đường dẫn thích hợp tới thư mục tài liệu của bạn.

## Bước 4: Truy cập bảng tính

Bây giờ chúng ta đã tải tệp Excel, chúng ta có thể truy cập trang tính đầu tiên. Sử dụng đoạn mã sau để truy cập bảng tính đầu tiên:

```csharp
// Truy cập vào bảng tính đầu tiên trong tệp Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Bước 5: Bảo vệ bảng tính

Ở bước này, chúng tôi sẽ bảo vệ bảng tính bằng mật khẩu. Sử dụng mã sau đây để bảo vệ bảng tính:

```csharp
// Bảo vệ bảng tính bằng mật khẩu.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Thay thế`"YOUR_PASSWORD"` với mật khẩu bạn muốn sử dụng để bảo vệ bảng tính.

## Bước 6: Lưu tệp Excel đã sửa đổi Bây giờ chúng tôi đã bảo vệ

é bảng tính, chúng ta sẽ lưu file Excel đã sửa đổi ở định dạng mặc định. Sử dụng đoạn mã sau để lưu tệp Excel:

```csharp
// Lưu tệp Excel đã sửa đổi ở định dạng mặc định.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Đảm bảo chỉ định đúng đường dẫn để lưu tệp Excel đã sửa đổi.

## Bước 7: Đóng luồng tệp

Để giải phóng tất cả tài nguyên, chúng ta cần đóng luồng tệp được sử dụng để tải tệp Excel. Sử dụng đoạn mã sau để đóng luồng tệp:

```csharp
// Đóng luồng tệp để giải phóng tất cả tài nguyên.
fstream.Close();
```

Hãy chắc chắn bao gồm bước này ở cuối mã của bạn.


### Mã nguồn mẫu cho Bảng tính Bảo vệ Excel bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Tạo luồng tệp chứa tệp Excel sẽ được mở
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Khởi tạo một đối tượng Workbook
// Mở tệp Excel thông qua luồng tệp
Workbook excel = new Workbook(fstream);
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = excel.Worksheets[0];
// Bảo vệ bảng tính bằng mật khẩu
worksheet.Protect(ProtectionType.All, "aspose", null);
// Lưu tệp Excel đã sửa đổi ở định dạng mặc định
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Đóng luồng tệp để giải phóng tất cả tài nguyên
fstream.Close();
```

## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã có mã nguồn C# cho phép bạn bảo vệ bảng tính Excel bằng thư viện Aspose.Cells cho .NET. Hãy nhớ làm theo các bước một cách cẩn thận và tùy chỉnh mã theo nhu cầu cụ thể của bạn.

### Câu hỏi thường gặp (Câu hỏi thường gặp)

#### Có thể bảo vệ nhiều bảng tính trong một tệp Excel không?

Trả lời: Có, bạn có thể bảo vệ nhiều trang tính trong một tệp Excel bằng cách lặp lại các bước 4-6 cho mỗi trang tính.

#### Làm cách nào tôi có thể chỉ định các quyền cụ thể cho người dùng được ủy quyền?

 Đáp: Bạn có thể sử dụng các tùy chọn bổ sung được cung cấp bởi`Protect`phương pháp để chỉ định quyền cụ thể cho người dùng được ủy quyền. Xem tài liệu Aspose.Cells để biết thêm thông tin.

#### Tôi có thể bảo vệ tệp Excel bằng mật khẩu không?

Trả lời: Có, bạn có thể bảo vệ tệp Excel bằng mật khẩu bằng các phương pháp khác do thư viện Aspose.Cells cung cấp. Vui lòng tham khảo tài liệu để biết ví dụ cụ thể.

#### Thư viện Aspose.Cells có hỗ trợ các định dạng tệp Excel khác không?

Trả lời: Có, thư viện Aspose.Cells hỗ trợ nhiều định dạng tệp Excel, bao gồm XLSX, XLSM, XLSB, CSV, v.v.