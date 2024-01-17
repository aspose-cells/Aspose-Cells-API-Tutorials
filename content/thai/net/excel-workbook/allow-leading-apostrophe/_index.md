---
title: อนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้า
linktitle: อนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้า
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: อนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้าในสมุดงาน Excel ด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 60
url: /th/net/excel-workbook/allow-leading-apostrophe/
---
ในบทช่วยสอนทีละขั้นตอนนี้ เราจะอธิบายซอร์สโค้ด C# ที่ให้มาซึ่งจะช่วยให้คุณสามารถอนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้าในสมุดงาน Excel โดยใช้ Aspose.Cells for .NET ทำตามขั้นตอนด้านล่างเพื่อดำเนินการนี้

## ขั้นตอนที่ 1: ตั้งค่าไดเร็กทอรีต้นทางและเอาต์พุต

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

ในขั้นตอนแรกนี้ เราจะกำหนดไดเร็กทอรีต้นทางและเอาต์พุตสำหรับไฟล์ Excel

## ขั้นตอนที่ 2: สร้างอินสแตนซ์วัตถุ WorkbookDesigner

```csharp
// สร้างอินสแตนซ์วัตถุ WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 เราสร้างอินสแตนซ์ของ`WorkbookDesigner` คลาสจาก Aspose.Cells

## ขั้นตอนที่ 3: โหลดสมุดงาน Excel

```csharp
// โหลดสมุดงาน Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

เราโหลดสมุดงาน Excel จากไฟล์ที่ระบุและปิดใช้งานการแปลงเครื่องหมายอะพอสทรอฟีเริ่มต้นเป็นสไตล์ข้อความโดยอัตโนมัติ

## ขั้นตอนที่ 4: ตั้งค่าแหล่งข้อมูล

```csharp
// กำหนดแหล่งข้อมูลสำหรับเวิร์กบุ๊กตัวออกแบบ
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 เรากำหนดรายการของวัตถุข้อมูลและใช้`SetDataSource` วิธีการตั้งค่าแหล่งข้อมูลสำหรับสมุดงานของนักออกแบบ

## ขั้นตอนที่ 5: ประมวลผลมาร์กเกอร์อัจฉริยะ

```csharp
// ประมวลผลมาร์กเกอร์อัจฉริยะ
designer. Process();
```

 เราใช้`Process` วิธีการประมวลผลมาร์กเกอร์อัจฉริยะในสมุดงานของนักออกแบบ

## ขั้นตอนที่ 6: บันทึกสมุดงาน Excel ที่แก้ไข

```csharp
// บันทึกสมุดงาน Excel ที่แก้ไข
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

เราบันทึกสมุดงาน Excel ที่แก้ไขพร้อมกับการเปลี่ยนแปลงที่เกิดขึ้น

### ตัวอย่างซอร์สโค้ดสำหรับ Allow Leading Apostrophe โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// การสร้างอินสแตนซ์วัตถุ WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// เปิดสเปรดชีตของนักออกแบบที่มีมาร์กเกอร์อัจฉริยะ
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// ตั้งค่าแหล่งข้อมูลสำหรับสเปรดชีตของนักออกแบบ
designer.SetDataSource("sampleData", list);
// ประมวลผลมาร์กเกอร์อัจฉริยะ
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## บทสรุป

ขอแสดงความยินดี! คุณได้เรียนรู้วิธีอนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้าในสมุดงาน Excel โดยใช้ Aspose.Cells for .NET ทดลองใช้ข้อมูลของคุณเองเพื่อปรับแต่งสมุดงาน Excel ของคุณเพิ่มเติม

### คำถามที่พบบ่อย

#### ถาม: สิทธิ์เครื่องหมายอะพอสทรอฟี่นำหน้าในเวิร์กบุ๊ก Excel คืออะไร

ตอบ: การอนุญาตให้ใช้เครื่องหมายอะพอสทรอฟีเริ่มต้นในเวิร์กบุ๊ก Excel ช่วยให้ข้อมูลที่ขึ้นต้นด้วยเครื่องหมายอะพอสทรอฟี่สามารถแสดงได้อย่างถูกต้องโดยไม่ต้องแปลงเป็นลักษณะข้อความ สิ่งนี้มีประโยชน์เมื่อคุณต้องการเก็บเครื่องหมายอะพอสทรอฟีไว้เป็นส่วนหนึ่งของข้อมูล

#### ถาม: เหตุใดฉันจึงต้องปิดการแปลงอะพอสทรอฟีเริ่มต้นโดยอัตโนมัติ

ตอบ: ด้วยการปิดใช้งานการแปลงเครื่องหมายคำพูดนำหน้าโดยอัตโนมัติ คุณสามารถคงการใช้งานไว้ได้เช่นเดียวกับที่อยู่ในข้อมูลของคุณ วิธีนี้จะหลีกเลี่ยงการปรับเปลี่ยนข้อมูลโดยไม่ได้ตั้งใจในขณะที่เปิดหรือจัดการเวิร์กบุ๊ก Excel

#### ถาม: วิธีการตั้งค่าแหล่งข้อมูลในสมุดงานของนักออกแบบ

 ตอบ: เมื่อต้องการตั้งค่าแหล่งข้อมูลในเวิร์กบุ๊กตัวออกแบบ คุณสามารถใช้`SetDataSource` วิธีการระบุชื่อของแหล่งข้อมูลและรายการของวัตถุข้อมูลที่เกี่ยวข้อง

#### ถาม: การอนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้าจะส่งผลต่อข้อมูลอื่นๆ ในเวิร์กบุ๊ก Excel หรือไม่

ตอบ: ไม่ การอนุญาตให้ใช้เครื่องหมายอะพอสทรอฟี่นำหน้าจะส่งผลต่อข้อมูลที่ขึ้นต้นด้วยเครื่องหมายอะพอสทรอฟีเท่านั้น ข้อมูลอื่นๆ ในเวิร์กบุ๊ก Excel ยังคงไม่เปลี่ยนแปลง

#### ถาม: ฉันสามารถใช้ฟีเจอร์นี้กับไฟล์ Excel รูปแบบอื่นได้หรือไม่

ตอบ: ได้ คุณสามารถใช้คุณสมบัตินี้กับรูปแบบไฟล์ Excel อื่นๆ ที่ Aspose.Cells รองรับ เช่น .xls, .xlsm เป็นต้น