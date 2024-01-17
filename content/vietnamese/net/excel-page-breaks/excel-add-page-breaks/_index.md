---
title: Excel Thêm ngắt trang
linktitle: Excel Thêm ngắt trang
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách thêm ngắt trang trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước để tạo báo cáo có cấu trúc tốt.
type: docs
weight: 10
url: /vi/net/excel-page-breaks/excel-add-page-breaks/
---
Thêm ngắt trang trong file Excel là một tính năng cần thiết khi tạo các báo cáo hoặc tài liệu lớn. Trong hướng dẫn này, chúng ta sẽ khám phá cách thêm ngắt trang trong tệp Excel bằng thư viện Aspose.Cells cho .NET. Chúng tôi sẽ hướng dẫn bạn từng bước để hiểu và triển khai mã nguồn C# được cung cấp.

## Bước 1: Chuẩn bị môi trường

 Trước khi bắt đầu, hãy đảm bảo bạn đã cài đặt Aspose.Cells for .NET trên máy của mình. Bạn có thể tải xuống thư viện từ[Giả định phát hành](https://releases.aspose.com/cells/net)và cài đặt nó bằng cách làm theo hướng dẫn được cung cấp.

Sau khi quá trình cài đặt hoàn tất, hãy tạo dự án C# mới trong môi trường phát triển tích hợp (IDE) ưa thích của bạn và nhập thư viện Aspose.Cells cho .NET.

## Bước 2: Cấu hình đường dẫn thư mục tài liệu

 Trong mã nguồn được cung cấp, bạn cần chỉ định đường dẫn thư mục nơi bạn muốn lưu tệp Excel đã tạo. Sửa đổi`dataDir` bằng cách thay thế "THƯ VIỆN TÀI LIỆU CỦA BẠN" bằng đường dẫn tuyệt đối của thư mục trên máy của bạn.

```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Bước 3: Tạo đối tượng sổ làm việc

Để bắt đầu, chúng ta cần tạo một đối tượng Workbook đại diện cho tệp Excel của mình. Điều này có thể đạt được bằng cách sử dụng lớp Workbook do Aspose.Cells cung cấp.

```csharp
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
```

## Bước 4: Thêm ngắt trang ngang

Bây giờ hãy thêm ngắt trang ngang vào bảng tính Excel của chúng ta. Trong mã mẫu, chúng tôi thêm dấu ngắt trang theo chiều ngang vào ô "Y30" của trang tính đầu tiên.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
```

## Bước 5: Thêm ngắt trang dọc

Tương tự, chúng ta có thể thêm ngắt trang dọc bằng cách sử dụng`VerticalPageBreaks.Add()` phương pháp. Trong ví dụ của chúng tôi, chúng tôi đang thêm dấu ngắt trang dọc vào ô "Y30" của trang tính đầu tiên.

```csharp
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
```

## Bước 6: Lưu file Excel

 Bây giờ chúng ta đã thêm ngắt trang, chúng ta cần lưu tệp Excel cuối cùng. Sử dụng`Save()` phương pháp chỉ định đường dẫn đầy đủ của tệp đầu ra.

```csharp
// Lưu tệp Excel.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```
### Mã nguồn mẫu cho Excel Thêm ngắt trang bằng Aspose.Cells cho .NET 
```csharp
//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Thêm ngắt trang tại ô Y30
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
// Lưu tệp Excel.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã học cách thêm dấu ngắt của

  trang trong tệp Excel bằng Aspose.Cells cho .NET. Bằng cách làm theo các bước được cung cấp, bạn sẽ có thể dễ dàng chèn ngắt trang ngang và dọc trong các tệp Excel được tạo động của mình. Vui lòng thử nghiệm nhiều hơn với thư viện Aspose.Cells để khám phá các tính năng mạnh mẽ khác mà nó cung cấp.

### Câu hỏi thường gặp

#### Câu hỏi: Aspose.Cells dành cho .NET có phải là thư viện miễn phí không?

Đáp: Aspose.Cells for .NET là một thư viện thương mại nhưng nó cung cấp phiên bản dùng thử miễn phí mà bạn có thể sử dụng để đánh giá chức năng của nó.

#### Hỏi: Tôi có thể thêm nhiều dấu ngắt trang trong một tệp Excel không?

Đáp: Có, bạn có thể thêm bao nhiêu ngắt trang nếu cần trong các phần khác nhau của bảng tính.

#### Hỏi: Có thể xóa ngắt trang đã thêm trước đó không?

Trả lời: Có, Aspose.Cells cho phép bạn xóa các ngắt trang hiện có bằng cách sử dụng các phương thức thích hợp của đối tượng Trang tính.

#### Hỏi: Phương pháp này có hoạt động với các định dạng tệp Excel khác như XLSX hoặc XLSM không?

Đáp: Có, phương pháp được mô tả trong hướng dẫn này hoạt động với nhiều định dạng tệp Excel khác nhau được Aspose.Cells hỗ trợ.

#### Hỏi: Tôi có thể tùy chỉnh hình thức ngắt trang trong Excel không?

Trả lời: Có, Aspose.Cells cung cấp một loạt tính năng để tùy chỉnh ngắt trang, chẳng hạn như kiểu, màu sắc và kích thước.
