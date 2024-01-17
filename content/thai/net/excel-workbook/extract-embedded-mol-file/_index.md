---
title: แยกไฟล์ Mol ที่ฝังไว้
linktitle: แยกไฟล์ Mol ที่ฝังไว้
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีแยกไฟล์ MOL ที่ฝังไว้จากสมุดงาน Excel ได้อย่างง่ายดายโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 90
url: /th/net/excel-workbook/extract-embedded-mol-file/
---
ในบทช่วยสอนนี้ เราจะแนะนำคุณทีละขั้นตอนในการแตกไฟล์ MOL ที่ฝังตัวจากสมุดงาน Excel โดยใช้ไลบรารี Aspose.Cells สำหรับ .NET คุณจะได้เรียนรู้วิธีเรียกดูแผ่นงานสมุดงาน แยกวัตถุ OLE ที่เกี่ยวข้อง และบันทึกไฟล์ MOL ที่แยกออกมา ทำตามขั้นตอนด้านล่างเพื่อทำงานนี้ให้สำเร็จ

## ขั้นตอนที่ 1: กำหนดไดเร็กทอรีต้นทางและเอาต์พุต
ขั้นแรก เราต้องกำหนดไดเร็กทอรีต้นทางและเอาต์พุตในโค้ดของเรา ไดเร็กทอรีเหล่านี้ระบุตำแหน่งของสมุดงาน Excel ต้นทาง และตำแหน่งที่ไฟล์ MOL ที่แตกออกมาจะถูกบันทึก นี่คือรหัสที่เกี่ยวข้อง:

```csharp
// ไดเรกทอรี
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

อย่าลืมระบุเส้นทางที่เหมาะสมตามความจำเป็น

## ขั้นตอนที่ 2: กำลังโหลดสมุดงาน Excel
ขั้นตอนต่อไปคือการโหลดเวิร์กบุ๊ก Excel ที่มีวัตถุ OLE และไฟล์ MOL ที่ฝังอยู่ นี่คือรหัสในการโหลดสมุดงาน:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

ตรวจสอบให้แน่ใจว่าได้ระบุชื่อไฟล์ต้นฉบับในโค้ดอย่างถูกต้อง

## ขั้นตอนที่ 3: สำรวจแผ่นงานและแตกไฟล์ MOL
ตอนนี้เราจะวนซ้ำแต่ละแผ่นงานในสมุดงานและแยกวัตถุ OLE ที่เกี่ยวข้องซึ่งมีไฟล์ MOL นี่คือรหัสที่เกี่ยวข้อง:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

รหัสนี้จะวนซ้ำแต่ละแผ่นงานในสมุดงาน ดึงข้อมูลออบเจ็กต์ OLE และบันทึกไฟล์ MOL ที่แยกออกมาไปยังไดเร็กทอรีเอาต์พุต

### ตัวอย่างซอร์สโค้ดสำหรับแยกไฟล์ Mol แบบฝังโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรี
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## บทสรุป
ขอแสดงความยินดี! คุณได้เรียนรู้วิธีแยกไฟล์ MOL ที่ฝังตัวจากสมุดงาน Excel โดยใช้ Aspose.Cells สำหรับ .NET ตอนนี้คุณสามารถใช้ความรู้นี้เพื่อแยกไฟล์ MOL จากสมุดงาน Excel ของคุณเองได้ รู้สึกอิสระที่จะสำรวจไลบรารี Aspose.Cells เพิ่มเติมและเรียนรู้เกี่ยวกับคุณสมบัติอันทรงพลังอื่นๆ

### คำถามที่พบบ่อย

#### ถาม: ไฟล์ MOL คืออะไร
 
ตอบ: ไฟล์ MOL เป็นรูปแบบไฟล์ที่ใช้เพื่อแสดงโครงสร้างทางเคมีในเคมีเชิงคำนวณ ประกอบด้วยข้อมูลเกี่ยวกับอะตอม พันธะ และคุณสมบัติโมเลกุลอื่นๆ

#### ถาม: วิธีนี้ใช้ได้กับไฟล์ Excel ทุกประเภทหรือไม่

ตอบ: ได้ วิธีนี้ใช้ได้กับไฟล์ Excel ทุกประเภทที่ Aspose.Cells รองรับ

#### ถาม: ฉันสามารถแยกไฟล์ MOL หลายไฟล์พร้อมกันได้หรือไม่

ตอบ: ได้ คุณสามารถแยกไฟล์ MOL หลายไฟล์พร้อมกันได้โดยการวนซ้ำวัตถุ OLE บนแต่ละแผ่นงานในสมุดงาน