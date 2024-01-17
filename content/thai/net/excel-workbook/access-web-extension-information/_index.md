---
title: เข้าถึงข้อมูลส่วนขยายของเว็บ
linktitle: เข้าถึงข้อมูลส่วนขยายของเว็บ
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เข้าถึงข้อมูลส่วนขยายของเว็บด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 10
url: /th/net/excel-workbook/access-web-extension-information/
---
การเข้าถึงข้อมูลส่วนขยายของเว็บเป็นคุณสมบัติที่สำคัญในการพัฒนาแอปพลิเคชันโดยใช้ Aspose.Cells สำหรับ .NET ในคำแนะนำทีละขั้นตอนนี้ เราจะอธิบายซอร์สโค้ด C# ที่ให้มาซึ่งจะช่วยให้คุณเข้าถึงข้อมูลส่วนขยายของเว็บโดยใช้ Aspose.Cells สำหรับ .NET นอกจากนี้เรายังมีบทสรุปและคำตอบให้คุณในรูปแบบ Markdown เพื่อให้เข้าใจได้ง่ายขึ้น ทำตามขั้นตอนด้านล่างเพื่อรับข้อมูลอันมีค่าเกี่ยวกับส่วนขยายของเว็บ

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทาง

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
```

ในขั้นตอนแรกนี้ เราจะกำหนดไดเร็กทอรีต้นทางที่จะใช้ในการโหลดไฟล์ Excel ที่มีข้อมูลส่วนขยายของเว็บ

## ขั้นตอนที่ 2: โหลดไฟล์ Excel

```csharp
// โหลดไฟล์ Excel ตัวอย่าง
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
```

ที่นี่เราโหลดไฟล์ Excel ตัวอย่างซึ่งมีข้อมูลส่วนขยายของเว็บที่เราต้องการดึงข้อมูล

## ขั้นตอนที่ 3: เข้าถึงข้อมูลจากหน้าต่างงานส่วนขยายเว็บ

```csharp
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach(WebExtensionTaskPane taskPane in taskPanes)
{
Console.WriteLine("Width: " + taskPane.Width);
Console.WriteLine("Is visible: " + taskPane.IsVisible);
Console.WriteLine("Is locked: " + taskPane.IsLocked);
Console.WriteLine("Docking State: " + taskPane.DockState);
Console.WriteLine("Store Name: " + taskPane.WebExtension.Reference.StoreName);
Console.WriteLine("Store type: " + taskPane.WebExtension.Reference.StoreType);
Console.WriteLine("Web Extension ID: " + taskPane.WebExtension.Id);
}
```

ในขั้นตอนนี้ เราจะเข้าถึงข้อมูลของหน้าต่างงานส่วนขยายเว็บแต่ละหน้าต่างที่มีอยู่ในไฟล์ Excel เราแสดงคุณสมบัติที่แตกต่างกัน เช่น ความกว้าง การมองเห็น สถานะการล็อค สถานะของบ้าน ชื่อร้านค้า ประเภทร้านค้า และ ID ส่วนขยายเว็บ

## ขั้นตอนที่ 4: แสดงข้อความแสดงความสำเร็จ

```csharp
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

สุดท้ายนี้ เราจะแสดงข้อความระบุว่ามีการเข้าถึงข้อมูลส่วนขยายของเว็บสำเร็จแล้ว

### ตัวอย่างซอร์สโค้ดสำหรับการเข้าถึงข้อมูลส่วนขยายเว็บโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
//โหลดไฟล์ Excel ตัวอย่าง
Workbook workbook = new Workbook(sourceDir + "WebExtensionsSample.xlsx");
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
foreach (WebExtensionTaskPane taskPane in taskPanes)
{
	Console.WriteLine("Width: " + taskPane.Width);
	Console.WriteLine("IsVisible: " + taskPane.IsVisible);
	Console.WriteLine("IsLocked: " + taskPane.IsLocked);
	Console.WriteLine("DockState: " + taskPane.DockState);
	Console.WriteLine("StoreName: " + taskPane.WebExtension.Reference.StoreName);
	Console.WriteLine("StoreType: " + taskPane.WebExtension.Reference.StoreType);
	Console.WriteLine("WebExtension.Id: " + taskPane.WebExtension.Id);
}
Console.WriteLine("AccessWebExtensionInformation executed successfully.");
```

## บทสรุป

ในบทช่วยสอนนี้ เราได้เรียนรู้วิธีการเข้าถึงข้อมูลส่วนขยายของเว็บโดยใช้ Aspose.Cells สำหรับ .NET เมื่อทำตามขั้นตอนที่ให้ไว้ คุณจะสามารถดึงข้อมูลหน้าต่างงานจากส่วนขยายของเว็บไปเป็นไฟล์ Excel ได้อย่างง่ายดาย


### คำถามที่พบบ่อย

#### ถาม: Aspose.Cells สำหรับ .NET คืออะไร

ตอบ: Aspose.Cells for .NET เป็นไลบรารีคลาสที่มีประสิทธิภาพซึ่งช่วยให้นักพัฒนา .NET สามารถสร้าง แก้ไข แปลง และจัดการไฟล์ Excel ได้อย่างง่ายดาย

#### ถาม: Aspose.Cells รองรับภาษาการเขียนโปรแกรมอื่นๆ หรือไม่

ตอบ: ใช่ Aspose.Cells รองรับภาษาการเขียนโปรแกรมหลายภาษา เช่น C#, VB.NET, Java, PHP, Python ฯลฯ

#### ถาม: ฉันสามารถใช้ Aspose.Cells ในโครงการเชิงพาณิชย์ได้หรือไม่

ตอบ: ได้ Aspose.Cells เป็นห้องสมุดเชิงพาณิชย์และสามารถใช้ในโครงการเชิงพาณิชย์ตามข้อตกลงใบอนุญาต

#### ถาม: มีเอกสารเพิ่มเติมเกี่ยวกับ Aspose.Cells หรือไม่

ตอบ: ได้ คุณสามารถตรวจสอบเอกสาร Aspose.Cells ฉบับเต็มได้บนเว็บไซต์ทางการของ Aspose เพื่อดูข้อมูลและแหล่งข้อมูลเพิ่มเติม