---
title: เพิ่มส่วนขยายเว็บ
linktitle: เพิ่มส่วนขยายเว็บ
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เพิ่มส่วนขยายเว็บลงในสมุดงาน Excel ของคุณได้อย่างง่ายดายด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 40
url: /th/net/excel-workbook/add-web-extension/
---
ในบทช่วยสอนทีละขั้นตอนนี้ เราจะอธิบายซอร์สโค้ด C# ที่ให้มาซึ่งจะช่วยให้คุณเพิ่มส่วนขยายเว็บโดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนด้านล่างเพื่อเพิ่มส่วนขยายเว็บลงในสมุดงาน Excel ของคุณ

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีผลลัพธ์

```csharp
// ไดเร็กทอรีเอาต์พุต
string outDir = RunExamples.Get_OutputDirectory();
```

ในขั้นตอนแรกนี้ เราจะกำหนดไดเร็กทอรีเอาต์พุตที่จะบันทึกสมุดงาน Excel ที่แก้ไข

## ขั้นตอนที่ 2: สร้างเวิร์กบุ๊กใหม่

```csharp
// สร้างสมุดงานใหม่
Workbook workbook = new Workbook();
```

ที่นี่เรากำลังสร้างสมุดงาน Excel ใหม่โดยใช้`Workbook` คลาสจาก Aspose.Cells

## ขั้นตอนที่ 3: เข้าถึงคอลเลกชันส่วนขยายของเว็บ

```csharp
// เข้าถึงคอลเลกชันของส่วนขยายเว็บ
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 เราเข้าถึงคอลเลกชันส่วนขยายเว็บของสมุดงาน Excel โดยใช้`WebExtensions` ทรัพย์สินของ`Worksheets` วัตถุ.

## ขั้นตอนที่ 4: เพิ่มส่วนขยายเว็บใหม่

```csharp
// เพิ่มส่วนขยายเว็บใหม่
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

เรากำลังเพิ่มส่วนขยายเว็บใหม่ให้กับคอลเลกชันส่วนขยาย เรากำหนดรหัสอ้างอิง ชื่อร้านค้า และประเภทร้านค้าของส่วนขยาย

## ขั้นตอนที่ 5: เข้าถึงคอลเลกชันบานหน้าต่างงานส่วนขยายของเว็บ

```csharp
// เข้าถึงคอลเลกชันบานหน้าต่างงานของส่วนขยายเว็บ
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 เราเข้าถึงคอลเลกชันบานหน้าต่างงาน Excel Workbook Web Extension โดยใช้`WebExtensionTaskPanes` ทรัพย์สินของ`Worksheets` วัตถุ.

## ขั้นตอนที่ 6: เพิ่มบานหน้าต่างงานใหม่

```csharp
// เพิ่มบานหน้าต่างงานใหม่
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

เรากำลังเพิ่มบานหน้าต่างงานใหม่ให้กับคอลเลกชันบานหน้าต่างงาน เราตั้งค่าการมองเห็นของบานหน้าต่าง สถานะการเชื่อมต่อ และส่วนขยายเว็บที่เกี่ยวข้อง

## ขั้นตอนที่ 7: บันทึกและปิดสมุดงาน

```csharp
// บันทึกและปิดสมุดงาน
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

เราบันทึกสมุดงานที่ถูกแก้ไขไปยังไดเร็กทอรีเอาต์พุตที่ระบุแล้วปิด

### ตัวอย่างซอร์สโค้ดสำหรับเพิ่มส่วนขยายเว็บโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## บทสรุป

ขอแสดงความยินดี! ตอนนี้คุณได้เรียนรู้วิธีเพิ่มส่วนขยายของเว็บโดยใช้ Aspose.Cells สำหรับ .NET แล้ว ทดลองใช้โค้ดและสำรวจคุณสมบัติเพิ่มเติมของ Aspose.Cells เพื่อรับประโยชน์สูงสุดจากการจัดการส่วนขยายเว็บในสมุดงาน Excel ของคุณ

## คำถามที่พบบ่อย

#### ถาม: ส่วนขยายเว็บในสมุดงาน Excel คืออะไร

ตอบ: ส่วนขยายเว็บในเวิร์กบุ๊ก Excel เป็นส่วนประกอบที่ช่วยให้คุณสามารถเพิ่มฟังก์ชันการทำงานเพิ่มเติมให้กับ Excel โดยการผสานรวมเว็บแอปพลิเคชัน มันสามารถนำเสนอคุณสมบัติเชิงโต้ตอบ แดชบอร์ดที่กำหนดเอง การบูรณาการภายนอก และอื่นๆ อีกมากมาย

#### ถาม: จะเพิ่มส่วนขยายเว็บลงในสมุดงาน Excel ด้วย Aspose.Cells ได้อย่างไร

 ตอบ: หากต้องการเพิ่มส่วนขยายเว็บลงในสมุดงาน Excel ด้วย Aspose.Cells คุณสามารถทำตามขั้นตอนที่ให้ไว้ในคำแนะนำทีละขั้นตอนของเรา ใช้`WebExtensionCollection` และ`WebExtensionTaskPaneCollection` คลาสเพื่อเพิ่มและกำหนดค่าส่วนขยายเว็บและบานหน้าต่างงานที่เกี่ยวข้อง

#### ถาม: ข้อมูลใดบ้างที่จำเป็นในการเพิ่มส่วนขยายเว็บ

ตอบ: เมื่อเพิ่มส่วนขยายของเว็บ คุณต้องระบุ ID SKU ของส่วนขยาย ชื่อร้านค้า และประเภทร้านค้า ข้อมูลนี้ช่วยในการระบุและโหลดส่วนขยายได้อย่างถูกต้อง

#### ถาม: ฉันสามารถเพิ่มส่วนขยายเว็บหลายรายการลงในสมุดงาน Excel เดียวได้หรือไม่

 ตอบ: ได้ คุณสามารถเพิ่มส่วนขยายเว็บหลายรายการลงในสมุดงาน Excel เดียวได้ ใช้`Add` วิธีการรวบรวมส่วนขยายเว็บเพื่อเพิ่มแต่ละส่วนขยาย จากนั้นเชื่อมโยงกับบานหน้าต่างงานที่เกี่ยวข้อง