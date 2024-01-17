---
title: Tạo xác thực dữ liệu tùy chỉnh
linktitle: Tạo xác thực dữ liệu tùy chỉnh
second_title: API xử lý Java Excel của Aspose.Cells
description: Tìm hiểu cách tạo xác thực dữ liệu tùy chỉnh bằng Aspose.Cells cho Java. Hướng dẫn từng bước với mã nguồn.
type: docs
weight: 10
url: /vi/java/data-validation-rules/creating-custom-data-validation/
---

## Giới thiệu

Xác thực dữ liệu giúp duy trì tính toàn vẹn của dữ liệu bằng cách ngăn người dùng nhập dữ liệu không chính xác hoặc không hợp lệ vào bảng tính Excel. Mặc dù Excel cung cấp các tùy chọn xác thực dữ liệu tích hợp sẵn nhưng có những trường hợp bạn cần xác định quy tắc xác thực tùy chỉnh. Aspose.Cells for Java trao quyền cho bạn để đạt được điều này một cách hiệu quả.

## Điều kiện tiên quyết

Trước khi đi sâu vào mã, hãy đảm bảo bạn có các điều kiện tiên quyết sau:

-  Aspose.Cells for Java: Tải xuống và cài đặt thư viện từ[đây](https://releases.aspose.com/cells/java/).

## Bước 1: Thiết lập dự án Java của bạn

Để bắt đầu, hãy tạo một dự án Java mới trong Môi trường phát triển tích hợp (IDE) ưa thích của bạn. Thêm thư viện Aspose.Cells for Java vào đường dẫn lớp của dự án của bạn.

## Bước 2: Tạo sổ làm việc Excel

Hãy bắt đầu bằng cách tạo một sổ làm việc Excel mới bằng Aspose.Cells for Java.

```java
// Mã Java để tạo sổ làm việc Excel mới
Workbook workbook = new Workbook();
```

## Bước 3: Thêm bảng tính

Bây giờ, hãy thêm một trang tính vào sổ làm việc nơi chúng tôi sẽ áp dụng xác thực dữ liệu tùy chỉnh của mình.

```java
// Mã Java để thêm một bảng tính
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## Bước 4: Xác định tiêu chí xác thực tùy chỉnh

Trong bước này, chúng tôi sẽ xác định tiêu chí xác thực tùy chỉnh mà dữ liệu của chúng tôi phải tuân thủ. Giả sử chúng ta muốn giới hạn độ tuổi được nhập vào ô là từ 18 đến 60.

```java
// Mã Java để xác định tiêu chí xác thực tùy chỉnh
Validation validation = worksheet.getValidations().add();
validation.setType(ValidationType.WHOLE);
validation.setOperator(OperatorType.BETWEEN);
validation.setFormula1("18");
validation.setFormula2("60");
validation.setShowError(true);
validation.setAlertStyle(ValidationAlertType.STOP);
validation.setErrorTitle("Invalid Age");
validation.setErrorMessage("Age must be between 18 and 60.");
```

## Bước 5: Áp dụng xác thực dữ liệu cho một phạm vi

Bây giờ chúng ta đã xác định được tiêu chí xác thực tùy chỉnh của mình, hãy áp dụng tiêu chí đó cho một phạm vi ô cụ thể.

```java
// Mã Java để áp dụng xác thực dữ liệu cho một phạm vi
CellArea area = new CellArea();
area.startRow = 0;
area.startColumn = 0;
area.endRow = 9; // Áp dụng xác thực cho mười hàng đầu tiên
area.endColumn = 0;

validation.addArea(area);
```

## Bước 6: Lưu tệp Excel

Cuối cùng, lưu tệp Excel có áp dụng quy tắc xác thực dữ liệu tùy chỉnh.

```java
// Mã Java để lưu tệp Excel
workbook.save("CustomDataValidation.xlsx");
```

## Phần kết luận

Trong hướng dẫn này, chúng ta đã khám phá cách tạo quy tắc xác thực dữ liệu tùy chỉnh bằng Aspose.Cells cho Java. Bằng cách làm theo các bước này, bạn có thể đảm bảo rằng dữ liệu Excel của mình tuân thủ các tiêu chí cụ thể, nâng cao tính toàn vẹn và chính xác của dữ liệu.

## Câu hỏi thường gặp

### Làm cách nào để tải xuống Aspose.Cells cho Java?

 Bạn có thể tải xuống Aspose.Cells cho Java từ trang web tại[đây](https://releases.aspose.com/cells/java/).

### Tôi có thể áp dụng xác thực dữ liệu tùy chỉnh cho nhiều phạm vi trong cùng một bảng tính không?

Có, bạn có thể áp dụng xác thực dữ liệu tùy chỉnh cho nhiều phạm vi trong cùng một trang tính bằng cách lặp lại Bước 5 cho từng phạm vi mong muốn.

### Có loại xác thực dữ liệu nào khác được Aspose.Cells hỗ trợ cho Java không?

Có, Aspose.Cells for Java hỗ trợ nhiều loại xác thực dữ liệu khác nhau, bao gồm số nguyên, số thập phân, ngày, giờ, độ dài văn bản, v.v.

### Làm cách nào để tùy chỉnh thông báo lỗi hiển thị khi xác thực dữ liệu không thành công?

 Bạn có thể tùy chỉnh thông báo lỗi bằng cách sửa đổi`setErrorMessage` phương pháp ở Bước 4, nơi bạn xác định tiêu chí xác thực.

### Aspose.Cells for Java có hoạt động với các tệp Excel ở các định dạng khác nhau không?

Có, Aspose.Cells for Java hỗ trợ nhiều định dạng tệp Excel, bao gồm XLS, XLSX, XLSM, v.v.