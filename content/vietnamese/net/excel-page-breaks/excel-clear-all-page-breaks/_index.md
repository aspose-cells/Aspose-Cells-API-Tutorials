---
title: Excel Xóa tất cả các ngắt trang
linktitle: Excel Xóa tất cả các ngắt trang
second_title: Aspose.Cells cho tài liệu tham khảo API .NET
description: Tìm hiểu cách loại bỏ tất cả các ngắt trang trong Excel bằng Aspose.Cells for .NET. Hướng dẫn từng bước để dọn dẹp các tệp Excel của bạn.
type: docs
weight: 20
url: /vi/net/excel-page-breaks/excel-clear-all-page-breaks/
---

Loại bỏ ngắt trang trong file Excel là bước cần thiết khi xử lý các báo cáo hoặc bảng tính. Trong hướng dẫn này, chúng tôi sẽ hướng dẫn bạn từng bước để hiểu và triển khai mã nguồn C# được cung cấp để loại bỏ tất cả các ngắt trang trong tệp Excel bằng thư viện Aspose.Cells cho .NET.

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

## Bước 4: Xóa ngắt trang

 Bây giờ chúng tôi sẽ xóa tất cả các ngắt trang trong bảng tính Excel của chúng tôi. Trong mã mẫu, chúng tôi sử dụng`Clear()` các phương pháp ngắt trang ngang và dọc để loại bỏ tất cả.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## Bước 5: Lưu file Excel

 Khi tất cả các ngắt trang đã được xóa, chúng ta có thể lưu tệp Excel cuối cùng. Sử dụng`Save()` phương pháp chỉ định đường dẫn đầy đủ của tệp đầu ra.

```csharp
// Lưu tệp Excel.
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### Mã nguồn mẫu cho Excel Xóa tất cả ngắt trang bằng Aspose.Cells for .NET 

```csharp

//Đường dẫn đến thư mục tài liệu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Khởi tạo một đối tượng Workbook
Workbook workbook = new Workbook();
// Xóa tất cả các ngắt trang
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
// Lưu tệp Excel.
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã tìm hiểu cách loại bỏ tất cả các ngắt trang trong tệp Excel bằng Aspose.Cells cho .NET. Bằng cách làm theo các bước được cung cấp, bạn có thể dễ dàng quản lý và dọn sạch các ngắt trang không mong muốn trong các tệp Excel được tạo động của mình. Vui lòng khám phá thêm các tính năng do Aspose.Cells cung cấp để có các hoạt động nâng cao hơn.

### Câu hỏi thường gặp

#### Câu hỏi: Aspose.Cells dành cho .NET có phải là thư viện miễn phí không?

Đáp: Aspose.Cells for .NET là một thư viện thương mại nhưng nó cung cấp phiên bản dùng thử miễn phí mà bạn có thể sử dụng để đánh giá chức năng của nó.

#### Câu hỏi: Việc xóa ngắt trang có ảnh hưởng đến các thành phần trang tính khác không?

Đáp: Không, việc xóa ngắt trang chỉ thay đổi chính ngắt trang đó và không ảnh hưởng đến bất kỳ dữ liệu hoặc định dạng nào khác trong trang tính.

#### Hỏi: Tôi có thể loại bỏ có chọn lọc một số dấu ngắt trang cụ thể trong Excel không?

Trả lời: Có, với Aspose.Cells, bạn có thể truy cập riêng từng ngắt trang và xóa nó nếu cần bằng các phương pháp thích hợp.

#### Câu hỏi: Aspose.Cells hỗ trợ những định dạng tệp Excel nào khác cho .NET?

Trả lời: Aspose.Cells for .NET hỗ trợ nhiều định dạng tệp Excel khác nhau, chẳng hạn như XLSX, XLSM, CSV, HTML, PDF, v.v.

