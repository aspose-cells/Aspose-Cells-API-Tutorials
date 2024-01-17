---
title: ฟังก์ชันข้อความ Excel ชัดเจน
linktitle: ฟังก์ชันข้อความ Excel ชัดเจน
second_title: Aspose.Cells Java Excel การประมวลผล API
description: ปลดล็อกความลับของฟังก์ชันข้อความ Excel ด้วย Aspose.Cells สำหรับ Java เรียนรู้วิธีจัดการ แยก และแปลงข้อความใน Excel ได้อย่างง่ายดาย
type: docs
weight: 18
url: /th/java/basic-excel-functions/excel-text-functions-demystified/
---

# ฟังก์ชันข้อความ Excel อธิบายให้กระจ่างโดยใช้ Aspose.Cells สำหรับ Java

ในบทช่วยสอนนี้ เราจะเจาะลึกโลกแห่งการจัดการข้อความใน Excel โดยใช้ Aspose.Cells สำหรับ Java API ไม่ว่าคุณจะเป็นผู้ใช้ Excel ที่มีประสบการณ์หรือเพิ่งเริ่มต้น การทำความเข้าใจฟังก์ชันข้อความสามารถพัฒนาทักษะสเปรดชีตของคุณได้อย่างมาก เราจะสำรวจฟังก์ชันข้อความต่างๆ และยกตัวอย่างที่เป็นประโยชน์เพื่อแสดงให้เห็นการใช้งาน

## เริ่มต้นใช้งาน

 ก่อนที่เราจะเริ่ม ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ Java แล้ว คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cells/java/). เมื่อคุณตั้งค่าแล้ว เรามาดำดิ่งสู่โลกอันน่าทึ่งของฟังก์ชันข้อความ Excel กัน

## CONCATENATE - การรวมข้อความ

 ที่`CONCATENATE`ฟังก์ชั่นช่วยให้คุณสามารถรวมข้อความจากเซลล์ต่างๆ มาดูวิธีการทำกับ Aspose.Cells สำหรับ Java:

```java
// รหัส Java เพื่อต่อข้อความโดยใช้ Aspose.Cells
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.getWorksheets().get(0);
Cell cell = worksheet.getCells().get("A1");

cell.putValue("Hello, ");
cell = worksheet.getCells().get("B1");
cell.putValue("World!");

// เชื่อมต่อ A1 และ B1 เข้ากับ C1
cell = worksheet.getCells().get("C1");
cell.setFormula("=CONCATENATE(A1,B1)");

workbook.calculateFormula();
```

ตอนนี้ เซลล์ C1 จะมีข้อความ "Hello, World!"

## ซ้ายและขวา - แยกข้อความ

 ที่`LEFT` และ`RIGHT` ฟังก์ชั่นช่วยให้คุณสามารถแยกอักขระตามจำนวนที่ระบุจากด้านซ้ายหรือขวาของสตริงข้อความ คุณสามารถใช้มันได้ดังต่อไปนี้:

```java
// รหัส Java เพื่อแยกข้อความโดยใช้ Aspose.Cells
Cell cell = worksheet.getCells().get("A2");
cell.putValue("Excel Rocks!");

// แยกอักขระ 5 ตัวแรก
cell = worksheet.getCells().get("B2");
cell.setFormula("=LEFT(A2, 5)");

// แยกอักขระ 5 ตัวสุดท้าย
cell = worksheet.getCells().get("C2");
cell.setFormula("=RIGHT(A2, 5)");

workbook.calculateFormula();
```

เซลล์ B2 จะมี "Excel" และเซลล์ C2 จะมี "Rocks!"

## LEN - การนับตัวอักษร

 ที่`LEN` ฟังก์ชั่นนับจำนวนตัวอักษรในสตริงข้อความ มาดูวิธีใช้กับ Aspose.Cells for Java กัน:

```java
// โค้ด Java เพื่อนับอักขระโดยใช้ Aspose.Cells
Cell cell = worksheet.getCells().get("A3");
cell.putValue("Excel");

// นับตัวอักษร
cell = worksheet.getCells().get("B3");
cell.setFormula("=LEN(A3)");

workbook.calculateFormula();
```

เซลล์ B3 จะมี "5" เนื่องจากมีอักขระ 5 ตัวใน "Excel"

## บนและล่าง - การเปลี่ยนตัวพิมพ์

 ที่`UPPER` และ`LOWER` ฟังก์ชั่นช่วยให้คุณสามารถแปลงข้อความเป็นตัวพิมพ์ใหญ่หรือตัวพิมพ์เล็ก ต่อไปนี้คือวิธีที่คุณสามารถทำได้:

```java
// รหัส Java เพื่อเปลี่ยนเคสโดยใช้ Aspose.Cells
Cell cell = worksheet.getCells().get("A4");
cell.putValue("java programming");

// แปลงเป็นตัวพิมพ์ใหญ่
cell = worksheet.getCells().get("B4");
cell.setFormula("=UPPER(A4)");

// แปลงเป็นตัวพิมพ์เล็ก
cell = worksheet.getCells().get("C4");
cell.setFormula("=LOWER(A4)");

workbook.calculateFormula();
```

เซลล์ B4 จะมี "การเขียนโปรแกรม Java" และเซลล์ C4 จะมี "การเขียนโปรแกรม Java"

## ค้นหาและแทนที่ - การค้นหาและการแทนที่ข้อความ

 ที่`FIND` ฟังก์ชั่นช่วยให้คุณค้นหาตำแหน่งของอักขระหรือข้อความเฉพาะภายในสตริงในขณะที่`REPLACE` ฟังก์ชั่นช่วยให้คุณแทนที่ข้อความได้ มาดูการทำงานกัน:

```java
// รหัส Java เพื่อค้นหาและแทนที่โดยใช้ Aspose.Cells
Cell cell = worksheet.getCells().get("A5");
cell.putValue("Search for me");

// ค้นหาตำแหน่งของ "สำหรับ"
cell = worksheet.getCells().get("B5");
cell.setFormula("=FIND(\"for\", A5)");

// แทนที่ "สำหรับ" ด้วย "กับ"
cell = worksheet.getCells().get("C5");
cell.setFormula("=REPLACE(A5, B5, 3, \"with\")");

workbook.calculateFormula();
```

เซลล์ B5 จะมี "9" (ตำแหน่งของ "สำหรับ") และเซลล์ C5 จะมี "ค้นหากับฉัน"

## บทสรุป

ฟังก์ชันข้อความใน Excel เป็นเครื่องมือที่มีประสิทธิภาพสำหรับการจัดการและวิเคราะห์ข้อมูลข้อความ ด้วย Aspose.Cells สำหรับ Java คุณสามารถรวมฟังก์ชันเหล่านี้เข้ากับแอปพลิเคชัน Java ของคุณ ทำให้งานที่เกี่ยวข้องกับข้อความเป็นอัตโนมัติ และปรับปรุงความสามารถ Excel ของคุณ สำรวจฟังก์ชันข้อความเพิ่มเติมและปลดปล่อยศักยภาพสูงสุดของ Excel ด้วย Aspose.Cells สำหรับ Java

## คำถามที่พบบ่อย

### ฉันจะต่อข้อความจากหลายเซลล์ได้อย่างไร

 หากต้องการต่อข้อความจากหลายเซลล์ ให้ใช้`CONCATENATE` การทำงาน. ตัวอย่างเช่น:
```java
Cell cell = worksheet.getCells().get("A1");
cell.setFormula("=CONCATENATE(A1, B1)");
```

### ฉันสามารถแยกอักขระตัวแรกและตัวสุดท้ายออกจากสตริงข้อความได้หรือไม่

 ใช่ คุณสามารถใช้`LEFT` และ`RIGHT` ฟังก์ชันเพื่อแยกอักขระจากจุดเริ่มต้นหรือจุดสิ้นสุดของสตริงข้อความ ตัวอย่างเช่น:
```java
Cell cell = worksheet.getCells().get("A2");
cell.setFormula("=LEFT(A2, 5)");
```

### ฉันจะนับอักขระในสตริงข้อความได้อย่างไร

 ใช้`LEN` ฟังก์ชั่นนับตัวอักษรในสตริงข้อความ ตัวอย่างเช่น:
```java
Cell cell = worksheet.getCells().get("A3");
cell.setFormula("=LEN(A3)");
```

### เป็นไปได้ไหมที่จะเปลี่ยนกรณีของข้อความ?

 ใช่ คุณสามารถแปลงข้อความเป็นตัวพิมพ์ใหญ่หรือตัวพิมพ์เล็กได้โดยใช้`UPPER` และ`LOWER` ฟังก์ชั่น. ตัวอย่างเช่น:
```java
Cell cell = worksheet.getCells().get("A4");
cell.setFormula("=UPPER(A4)");
```

### ฉันจะค้นหาและแทนที่ข้อความภายในสตริงได้อย่างไร

หากต้องการค้นหาและแทนที่ข้อความภายในสตริง ให้ใช้`FIND` และ`REPLACE` ฟังก์ชั่น. ตัวอย่างเช่น:
```java
Cell cell = worksheet.getCells().get("A5");
cell.setFormula("=FIND(\"for\", A5)");
```