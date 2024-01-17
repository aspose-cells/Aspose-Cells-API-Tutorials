---
title: Tùy chọn trang phù hợp với Excel
linktitle: Tùy chọn trang phù hợp với Excel
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách tự động điều chỉnh các trang trong bảng tính Excel bằng Aspose.Cells dành cho .NET.
type: docs
weight: 30
url: /vi/net/excel-page-setup/fit-to-excel-pages-options/
---
Trong bài viết này, chúng tôi sẽ hướng dẫn bạn từng bước để giải thích mã nguồn C# sau: Phù hợp với các tùy chọn trang Excel bằng cách sử dụng Aspose.Cells cho .NET. Chúng tôi sẽ sử dụng thư viện Aspose.Cells cho .NET để thực hiện thao tác này. Thực hiện theo các bước bên dưới để định cấu hình phù hợp với các trang trong Excel.

## Bước 1: Tạo sổ làm việc
Bước đầu tiên là tạo một bảng tính. Chúng ta sẽ khởi tạo một đối tượng Workbook. Đây là mã để tạo một sổ làm việc:

```csharp
// Đường dẫn đến thư mục tài liệu
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
```

## Bước 2: Truy cập bảng tính
Bây giờ chúng ta đã tạo sổ làm việc, chúng ta cần điều hướng đến trang tính đầu tiên. Chúng ta sẽ sử dụng chỉ số 0 để truy cập vào sheet đầu tiên. Đây là mã để truy cập nó:

```csharp
// Truy cập vào bảng tính đầu tiên trong sổ làm việc
Worksheet worksheet = workbook.Worksheets[0];
```

## Bước 3: Đặt Fit cho trang
 Trong bước này, chúng tôi sẽ định cấu hình điều chỉnh cho các trang của bảng tính. Chúng tôi sẽ sử dụng`FitToPagesTall` Và`FitToPagesWide` thuộc tính của`PageSetup` đối tượng để chỉ định số trang mong muốn cho chiều cao và chiều rộng của bảng tính. Đây là mã cho điều đó:

```csharp
// Cấu hình số trang theo chiều cao của bảng tính
worksheet.PageSetup.FitToPagesTall = 1;

// Cấu hình số trang theo chiều rộng của bảng tính
worksheet.PageSetup.FitToPagesWide = 1;
```

## Bước 4: Lưu sổ làm việc
 Bây giờ chúng ta đã cấu hình phù hợp với các trang, chúng ta có thể lưu sổ làm việc. Chúng tôi sẽ sử dụng`Save` phương thức của đối tượng Workbook cho việc này. Đây là mã để lưu sổ làm việc:

```csharp
// Lưu sổ làm việc
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Mã nguồn mẫu cho Tùy chọn trang Fit To Excel bằng Aspose.Cells for .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Truy cập bảng tính đầu tiên trong tệp Excel
Worksheet worksheet = workbook.Worksheets[0];
// Đặt số trang mà độ dài của bảng tính sẽ được kéo dài
worksheet.PageSetup.FitToPagesTall = 1;
//Đặt số trang mà chiều rộng của bảng tính sẽ được kéo dài
worksheet.PageSetup.FitToPagesWide = 1;
// Lưu sổ làm việc.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Phần kết luận
Trong bài viết này, chúng ta đã tìm hiểu cách định cấu hình vừa với các trang trong Excel bằng Aspose.Cells cho .NET. Chúng tôi đã thực hiện các bước sau: tạo sổ làm việc, truy cập trang tính, định cấu hình vừa với các trang và lưu sổ làm việc. Bây giờ bạn có thể sử dụng kiến thức này để điều chỉnh bảng tính của mình đến các trang mong muốn.

### Câu hỏi thường gặp

#### Câu hỏi: Làm cách nào tôi có thể cài đặt Aspose.Cells cho .NET?

Trả lời: Để cài đặt Aspose.Cells cho .NET, bạn có thể sử dụng trình quản lý gói NuGet trong Visual Studio. Tìm gói "Aspose.Cells" và cài đặt nó trong dự án của bạn.

#### Hỏi: Tôi có thể điều chỉnh các trang theo cả chiều cao và chiều rộng không?

 Đáp: Có, bạn có thể điều chỉnh cả chiều cao và chiều rộng của trang tính bằng cách sử dụng`FitToPagesTall` Và`FitToPagesWide` của cải. Bạn có thể chỉ định số lượng trang mong muốn cho mỗi thứ nguyên.

#### Câu hỏi: Làm cách nào tôi có thể tùy chỉnh tùy chọn Fit to Pages?

Trả lời: Ngoài việc chỉ định số trang, bạn cũng có thể tùy chỉnh các tùy chọn phù hợp với trang khác như tỷ lệ trang tính, hướng giấy, lề, v.v. Sử dụng các thuộc tính có sẵn trong`PageSetup` đối tượng cho việc này.

#### Câu hỏi: Tôi có thể sử dụng Aspose.Cells cho .NET để xử lý sổ làm việc hiện có không?

Trả lời: Có, bạn có thể sử dụng Aspose.Cells for .NET để mở và chỉnh sửa sổ làm việc hiện có. Bạn có thể truy cập trang tính, ô, công thức, kiểu và các mục sổ làm việc khác để thực hiện các thao tác khác nhau.