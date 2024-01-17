---
title: การจัดกลุ่มข้อมูลในตาราง Pivot
linktitle: การจัดกลุ่มข้อมูลในตาราง Pivot
second_title: Aspose.Cells Java Excel การประมวลผล API
description: เรียนรู้วิธีสร้างตารางสรุปข้อมูลใน Excel โดยใช้ Aspose.Cells สำหรับ Java จัดกลุ่มและวิเคราะห์ข้อมูลอัตโนมัติด้วยตัวอย่างซอร์สโค้ด
type: docs
weight: 14
url: /th/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

ตาราง Pivot เป็นเครื่องมือที่มีประสิทธิภาพสำหรับการวิเคราะห์และสรุปข้อมูลในสเปรดชีต ช่วยให้คุณสามารถจัดกลุ่มและจัดหมวดหมู่ข้อมูลเพื่อรับข้อมูลเชิงลึกอันมีค่า ในบทความนี้ เราจะสำรวจวิธีการจัดกลุ่มข้อมูลในตาราง Pivot อย่างมีประสิทธิภาพโดยใช้ Aspose.Cells สำหรับ Java พร้อมด้วยตัวอย่างซอร์สโค้ด

## การแนะนำ

ตาราง Pivot มอบวิธีที่ยืดหยุ่นในการจัดระเบียบและสรุปข้อมูลจากชุดข้อมูลขนาดใหญ่ ช่วยให้คุณสร้างมุมมองข้อมูลที่กำหนดเองได้โดยการจัดกลุ่มเป็นหมวดหมู่หรือลำดับชั้น วิธีนี้ช่วยให้คุณระบุแนวโน้ม รูปแบบ และค่าผิดปกติในข้อมูลของคุณได้ง่ายขึ้น

## ขั้นตอนที่ 1: สร้างตาราง Pivot

เริ่มต้นด้วยการสร้างตารางสาระสำคัญโดยใช้ Aspose.Cells สำหรับ Java ด้านล่างนี้คือตัวอย่างวิธีสร้างตารางสรุปข้อมูลจากไฟล์ Excel ตัวอย่าง

```java
// โหลดไฟล์ Excel
Workbook workbook = new Workbook("sample.xlsx");

// เข้าถึงแผ่นงานที่มีข้อมูล
Worksheet worksheet = workbook.getWorksheets().get(0);

// ระบุช่วงข้อมูล
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // สมมติว่ามีข้อมูล 20 แถว
sourceData.startColumn = 0;
sourceData.endColumn = 3; // สมมติว่ามีข้อมูล 4 คอลัมน์

// สร้างตารางสรุปข้อมูลตามช่วงข้อมูล
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// รับตารางเดือยตามดัชนี
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// เพิ่มเขตข้อมูลให้กับแถวและคอลัมน์
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// เพิ่มค่าและใช้การรวมกลุ่ม
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// บันทึกไฟล์ Excel ที่แก้ไข
workbook.save("output.xlsx");
```

## ขั้นตอนที่ 2: ข้อมูลกลุ่ม

 ใน Aspose.Cells สำหรับ Java คุณสามารถจัดกลุ่มข้อมูลภายในตารางสรุปข้อมูลได้โดยใช้`PivotField` ระดับ. ต่อไปนี้คือตัวอย่างวิธีจัดกลุ่มช่องในตารางสรุปข้อมูล:

```java
// เข้าถึงช่อง "ผลิตภัณฑ์" ในตารางสรุปข้อมูล
PivotField productField = pivotTable.getPivotFields().get("Product");

//จัดกลุ่มช่อง "ผลิตภัณฑ์" ตามเกณฑ์เฉพาะ เช่น ตามตัวอักษรเริ่มต้น
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// บันทึกไฟล์ Excel ที่แก้ไขด้วยข้อมูลที่จัดกลุ่ม
workbook.save("output_grouped.xlsx");
```

## ขั้นตอนที่ 3: ปรับแต่งการจัดกลุ่ม

คุณสามารถปรับแต่งการตั้งค่าการจัดกลุ่มเพิ่มเติมได้ เช่น การระบุช่วงเวลาการจัดกลุ่มตามวันที่หรือกฎการจัดกลุ่มแบบกำหนดเอง ต่อไปนี้คือตัวอย่างการปรับแต่งการจัดกลุ่มตามวันที่:

```java
// เข้าถึงช่อง "วันที่" ในตารางสรุป (สมมติว่าเป็นช่องวันที่)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// จัดกลุ่มวันที่ตามเดือน
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// บันทึกไฟล์ Excel ที่แก้ไขด้วยการจัดกลุ่มวันที่แบบกำหนดเอง
workbook.save("output_custom_grouping.xlsx");
```

## บทสรุป

การจัดกลุ่มข้อมูลในตารางสรุปข้อมูลเป็นเทคนิคที่มีประโยชน์สำหรับการวิเคราะห์และสรุปข้อมูลใน Excel และ Aspose.Cells สำหรับ Java ช่วยให้กระบวนการนี้เป็นไปโดยอัตโนมัติได้อย่างง่ายดาย ด้วยตัวอย่างซอร์สโค้ดที่ให้มา คุณสามารถสร้างตารางสรุปข้อมูล ปรับแต่งการจัดกลุ่ม และรับข้อมูลเชิงลึกจากข้อมูลของคุณได้อย่างมีประสิทธิภาพ

## คำถามที่พบบ่อย

### 1. จุดประสงค์ของตารางเดือยใน Excel คืออะไร

ตาราง Pivot ใน Excel ใช้เพื่อสรุปและวิเคราะห์ชุดข้อมูลขนาดใหญ่ ช่วยให้คุณสร้างมุมมองข้อมูลที่กำหนดเองได้ ทำให้ระบุรูปแบบและแนวโน้มได้ง่ายขึ้น

### 2. ฉันจะปรับแต่งการจัดกลุ่มข้อมูลในตารางสรุปได้อย่างไร

 คุณสามารถปรับแต่งการจัดกลุ่มข้อมูลในตารางสรุปได้โดยใช้`PivotField` คลาสใน Aspose.Cells สำหรับ Java ซึ่งจะทำให้คุณสามารถระบุเกณฑ์การจัดกลุ่ม เช่น ช่วงเวลาที่อิงตามวันที่หรือกฎที่กำหนดเอง

### 3. ฉันสามารถสร้างตาราง Pivot โดยอัตโนมัติโดยใช้ Aspose.Cells สำหรับ Java ได้หรือไม่

ใช่ คุณสามารถสร้างตารางสรุปข้อมูลใน Excel ได้โดยอัตโนมัติโดยใช้ Aspose.Cells for Java ดังที่แสดงในตัวอย่างซอร์สโค้ดที่ให้มา