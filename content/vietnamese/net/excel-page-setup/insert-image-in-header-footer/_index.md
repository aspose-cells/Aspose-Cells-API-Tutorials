---
title: Chèn hình ảnh vào đầu trang chân trang
linktitle: Chèn hình ảnh vào đầu trang chân trang
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách chèn hình ảnh vào đầu trang hoặc chân trang của tài liệu Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước với mã nguồn trong C#.
type: docs
weight: 60
url: /vi/net/excel-page-setup/insert-image-in-header-footer/
---
Khả năng chèn hình ảnh vào đầu trang hoặc chân trang của tài liệu Excel có thể rất hữu ích để tùy chỉnh báo cáo của bạn hoặc thêm logo công ty. Trong bài viết này, chúng tôi sẽ hướng dẫn bạn từng bước chèn hình ảnh vào đầu trang hoặc chân trang của tài liệu Excel bằng Aspose.Cells for .NET. Bạn sẽ học cách thực hiện điều này bằng mã nguồn C#.

## Bước 1: Thiết lập môi trường

Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Đồng thời tạo một dự án mới trong môi trường phát triển ưa thích của bạn.

## Bước 2: Nhập các thư viện cần thiết

Trong tệp mã của bạn, hãy nhập các thư viện cần thiết để làm việc với Aspose.Cells. Đây là mã tương ứng:

```csharp
using Aspose.Cells;
```

## Bước 3: Đặt thư mục tài liệu

Đặt thư mục chứa tài liệu Excel mà bạn muốn làm việc. Sử dụng đoạn mã sau để thiết lập thư mục:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Hãy chắc chắn chỉ định đường dẫn thư mục đầy đủ.

## Bước 4: Tạo đối tượng sổ làm việc

Đối tượng Workbook đại diện cho tài liệu Excel mà bạn sẽ làm việc. Bạn có thể tạo nó bằng mã sau:

```csharp
Workbook workbook = new Workbook();
```

Điều này tạo ra một đối tượng Workbook trống mới.

## Bước 5: Lưu trữ URL hình ảnh

Xác định URL hoặc đường dẫn của hình ảnh bạn muốn chèn vào đầu trang hoặc chân trang. Sử dụng đoạn mã sau để lưu trữ URL hình ảnh:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Đảm bảo đường dẫn được chỉ định là chính xác và hình ảnh tồn tại ở vị trí đó.

## Bước 6: Mở file ảnh

Để mở tệp hình ảnh, chúng tôi sẽ sử dụng đối tượng FileStream và đọc dữ liệu nhị phân từ hình ảnh. Đây là mã tương ứng:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Đảm bảo đường dẫn hình ảnh là chính xác và bạn có quyền chính xác để truy cập vào nó.

## Bước 7: Định cấu hình PageSetup

Đối tượng PageSetup được sử dụng để thiết lập cài đặt trang tài liệu Excel bao gồm đầu trang và chân trang. Sử dụng đoạn mã sau để lấy đối tượng PageSetup của trang tính đầu tiên:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Điều này sẽ cho phép bạn truy cập cài đặt trang cho bảng tính đầu tiên trong sổ làm việc.

## Bước 8: Thêm hình ảnh vào tiêu đề

Sử dụng phương thức SetHeaderPicture() của đối tượng PageSetup để đặt hình ảnh ở phần giữa của tiêu đề trang. Đây là mã tương ứng:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Điều này sẽ thêm hình ảnh được chỉ định vào tiêu đề trang.

## Bước 9: Thêm script vào tiêu đề

Để thêm tập lệnh vào tiêu đề trang, hãy sử dụng phương thức SetHeader() của đối tượng PageSetup. Đây là mã tương ứng:

```csharp
pageSetup.SetHeader(1, "&G");
```

Điều này sẽ thêm tập lệnh được chỉ định vào tiêu đề trang. Trong ví dụ này, tập lệnh "&G" hiển thị số trang.

## Bước 10: Thêm tên trang tính vào tiêu đề

Để hiển thị tên trang tính trong tiêu đề trang, hãy sử dụng lại phương thức SetHeader() của đối tượng PageSetup. Đây là mã tương ứng:

```csharp
pageSetup.SetHeader(2, "&A");
```

Điều này sẽ thêm tên trang tính vào tiêu đề trang. Tập lệnh "&A" được sử dụng để thể hiện tên trang tính.

## Bước 11: Lưu sổ làm việc

Để lưu các thay đổi vào sổ làm việc, hãy sử dụng phương thức Save() của đối tượng Workbook. Đây là mã tương ứng:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Điều này sẽ lưu sổ làm việc với những thay đổi đối với thư mục đã chỉ định.

## Bước 12: Đóng FileStream

Sau khi đọc dữ liệu nhị phân từ hình ảnh, hãy nhớ đóng FileStream để giải phóng tài nguyên. Sử dụng đoạn mã sau để đóng FileStream:

```csharp
inFile.Close();
```

Đảm bảo luôn đóng FileStream khi bạn sử dụng xong.

### Mã nguồn mẫu cho Chèn hình ảnh vào chân trang đầu trang bằng Aspose.Cells for .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Tạo đối tượng Workbook
Workbook workbook = new Workbook();
// Tạo biến chuỗi để lưu trữ url của logo/hình ảnh
string logo_url = dataDir + "aspose-logo.jpg";
// Khai báo đối tượng FileStream
FileStream inFile;
// Khai báo một mảng byte
byte[] binaryData;
// Tạo phiên bản của đối tượng FileStream để mở logo/hình ảnh trong luồng
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Khởi tạo mảng byte có kích thước của đối tượng FileStream
binaryData = new Byte[inFile.Length];
// Đọc một khối byte từ luồng và ghi dữ liệu vào bộ đệm nhất định của mảng byte.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Tạo đối tượng PageSetup để lấy cài đặt trang của bảng tính đầu tiên của sổ làm việc
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Đặt logo/hình ảnh ở phần trung tâm của tiêu đề trang
pageSetup.SetHeaderPicture(1, binaryData);
// Đặt script cho logo/hình ảnh
pageSetup.SetHeader(1, "&G");
// Đặt tên Trang tính ở phần bên phải của tiêu đề trang bằng tập lệnh
pageSetup.SetHeader(2, "&A");
// Lưu sổ làm việc
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Đóng đối tượng FileStream
inFile.Close();       
```
## Phần kết luận

Xin chúc mừng! Bây giờ bạn đã biết cách chèn hình ảnh vào đầu trang hoặc chân trang của tài liệu Excel bằng Aspose.Cells for .NET. Hướng dẫn này hướng dẫn bạn từng bước của quy trình, từ thiết lập môi trường đến lưu sổ làm việc đã sửa đổi. Vui lòng thử nghiệm nhiều hơn với các tính năng của Aspose.Cells để tạo tài liệu Excel chuyên nghiệp và được cá nhân hóa.

### Câu hỏi thường gặp

#### Q1: Có thể chèn nhiều hình ảnh vào đầu trang hoặc chân trang của tài liệu Excel không?

Câu trả lời 1: Có, bạn có thể chèn nhiều hình ảnh vào đầu trang hoặc chân trang của tài liệu Excel bằng cách lặp lại bước 8 và 9 cho mỗi hình ảnh bổ sung.

#### Câu hỏi 2: Định dạng hình ảnh nào được hỗ trợ để chèn vào đầu trang hoặc chân trang?
Câu trả lời 2: Aspose.Cells hỗ trợ nhiều định dạng hình ảnh phổ biến như JPEG, PNG, GIF, BMP, v.v.

#### Câu hỏi 3: Tôi có thể tùy chỉnh thêm hình thức của đầu trang hoặc chân trang không?

A3: Có, bạn có thể sử dụng các tập lệnh và mã đặc biệt để định dạng thêm và tùy chỉnh hình thức của đầu trang hoặc chân trang. Tham khảo tài liệu Aspose.Cells để biết thêm thông tin về các tùy chọn tùy chỉnh.

#### Câu hỏi 4: Aspose.Cells có hoạt động với các phiên bản Excel khác nhau không?

Trả lời 4: Có, Aspose.Cells tương thích với các phiên bản Excel khác nhau bao gồm Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 và Excel 2019.

#### Câu hỏi 5: Có thể chèn hình ảnh vào các phần khác của tài liệu Excel, chẳng hạn như ô hoặc biểu đồ không?

Câu trả lời 5: Có, Aspose.Cells cung cấp chức năng mở rộng để chèn hình ảnh vào các phần khác nhau của tài liệu Excel, bao gồm ô, biểu đồ và đối tượng vẽ.