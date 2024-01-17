---
title: Nhóm dữ liệu trong bảng tổng hợp
linktitle: Nhóm dữ liệu trong bảng tổng hợp
second_title: API xử lý Java Excel của Aspose.Cells
description: Tìm hiểu cách tạo bảng tổng hợp trong Excel bằng Aspose.Cells cho Java. Tự động hóa việc nhóm và phân tích dữ liệu với các ví dụ về mã nguồn.
type: docs
weight: 14
url: /vi/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Bảng tổng hợp là công cụ mạnh mẽ để phân tích và tóm tắt dữ liệu trong bảng tính. Chúng cho phép bạn nhóm và phân loại dữ liệu để có được những hiểu biết có giá trị. Trong bài viết này, chúng ta sẽ khám phá cách nhóm dữ liệu trong bảng tổng hợp một cách hiệu quả bằng Aspose.Cells cho Java, cùng với các ví dụ về mã nguồn.

## Giới thiệu

Bảng tổng hợp cung cấp một cách linh hoạt để sắp xếp và tóm tắt dữ liệu từ các tập dữ liệu lớn. Chúng cho phép bạn tạo chế độ xem tùy chỉnh cho dữ liệu của mình bằng cách nhóm dữ liệu đó thành các danh mục hoặc phân cấp. Điều này có thể giúp bạn xác định xu hướng, mẫu và các ngoại lệ trong dữ liệu của mình dễ dàng hơn.

## Bước 1: Tạo Bảng tổng hợp

Hãy bắt đầu bằng cách tạo bảng tổng hợp bằng Aspose.Cells cho Java. Dưới đây là ví dụ về cách tạo bảng tổng hợp từ tệp Excel mẫu.

```java
// Tải tệp Excel
Workbook workbook = new Workbook("sample.xlsx");

// Truy cập bảng tính chứa dữ liệu
Worksheet worksheet = workbook.getWorksheets().get(0);

// Chỉ định phạm vi dữ liệu
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // Giả sử 20 hàng dữ liệu
sourceData.startColumn = 0;
sourceData.endColumn = 3; // Giả sử 4 cột dữ liệu

// Tạo bảng tổng hợp dựa trên phạm vi dữ liệu
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Lấy bảng tổng hợp theo chỉ mục
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Thêm trường vào hàng và cột
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Thêm giá trị và áp dụng tổng hợp
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Lưu tệp Excel đã sửa đổi
workbook.save("output.xlsx");
```

## Bước 2: Dữ liệu nhóm

 Trong Aspose.Cells dành cho Java, bạn có thể nhóm dữ liệu trong bảng tổng hợp bằng cách sử dụng`PivotField` lớp học. Dưới đây là ví dụ về cách nhóm một trường trong bảng tổng hợp:

```java
// Truy cập trường "Sản phẩm" trong bảng tổng hợp
PivotField productField = pivotTable.getPivotFields().get("Product");

//Nhóm trường "Sản phẩm" theo một tiêu chí cụ thể, ví dụ: theo chữ cái bắt đầu
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Lưu tệp Excel đã sửa đổi với dữ liệu được nhóm
workbook.save("output_grouped.xlsx");
```

## Bước 3: Tùy chỉnh nhóm

Bạn có thể tùy chỉnh thêm cài đặt nhóm, chẳng hạn như chỉ định khoảng thời gian nhóm dựa trên ngày hoặc quy tắc nhóm tùy chỉnh. Dưới đây là ví dụ về tùy chỉnh nhóm dựa trên ngày:

```java
// Truy cập trường "Ngày" trong bảng tổng hợp (giả sử đó là trường ngày)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Nhóm ngày theo tháng
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Lưu tệp Excel đã sửa đổi với nhóm ngày tùy chỉnh
workbook.save("output_custom_grouping.xlsx");
```

## Phần kết luận

Nhóm dữ liệu trong bảng tổng hợp là một kỹ thuật có giá trị để phân tích và tóm tắt dữ liệu trong Excel và Aspose.Cells dành cho Java giúp bạn dễ dàng tự động hóa quy trình này. Với các ví dụ về mã nguồn được cung cấp, bạn có thể tạo bảng tổng hợp, tùy chỉnh nhóm và hiểu rõ hơn về dữ liệu của mình một cách hiệu quả.

## Câu hỏi thường gặp

### 1. Mục đích của Pivot Table trong Excel là gì?

Bảng tổng hợp trong Excel được sử dụng để tóm tắt và phân tích các tập dữ liệu lớn. Chúng cho phép bạn tạo chế độ xem tùy chỉnh cho dữ liệu của mình, giúp xác định các mẫu và xu hướng dễ dàng hơn.

### 2. Làm cách nào tôi có thể tùy chỉnh việc nhóm dữ liệu trong bảng tổng hợp?

 Bạn có thể tùy chỉnh việc nhóm dữ liệu trong bảng tổng hợp bằng cách sử dụng`PivotField` lớp trong Aspose.Cells cho Java. Điều này cho phép bạn chỉ định tiêu chí nhóm, chẳng hạn như khoảng thời gian dựa trên ngày hoặc quy tắc tùy chỉnh.

### 3. Tôi có thể tự động hóa việc tạo bảng tổng hợp bằng Aspose.Cells cho Java không?

Có, bạn có thể tự động hóa việc tạo bảng tổng hợp trong Excel bằng Aspose.Cells for Java, như được minh họa trong các ví dụ về mã nguồn được cung cấp.