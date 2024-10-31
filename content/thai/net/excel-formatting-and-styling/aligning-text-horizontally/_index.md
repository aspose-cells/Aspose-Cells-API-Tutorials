---
title: การจัดตำแหน่งข้อความในแนวนอนในเซลล์ Excel
linktitle: การจัดตำแหน่งข้อความในแนวนอนในเซลล์ Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีจัดตำแหน่งข้อความในแนวนอนในเซลล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยคู่มือทีละขั้นตอนโดยละเอียดนี้
type: docs
weight: 20
url: /th/net/excel-formatting-and-styling/aligning-text-horizontally/
---
## การแนะนำ
เมื่อต้องสร้างและจัดการสเปรดชีต Excel ด้วยโปรแกรม Aspose.Cells สำหรับ .NET เป็นเครื่องมืออันทรงพลังที่ช่วยให้นักพัฒนาสามารถจัดการไฟล์ Excel ได้อย่างง่ายดาย ไม่ว่าคุณจะกำลังสร้างรายงาน วิเคราะห์ข้อมูล หรือเพียงแค่พยายามทำให้สเปรดชีตของคุณดูน่าสนใจขึ้น การจัดตำแหน่งข้อความอย่างถูกต้องสามารถปรับปรุงการอ่านและประสบการณ์ของผู้ใช้ได้อย่างมาก ในบทความนี้ เราจะมาดูวิธีจัดตำแหน่งข้อความในแนวนอนในเซลล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET กัน
## ข้อกำหนดเบื้องต้น
ก่อนจะลงลึกถึงรายละเอียดในการจัดตำแหน่งข้อความ สิ่งสำคัญคือต้องแน่ใจว่าคุณได้ตั้งค่าอย่างถูกต้อง นี่คือสิ่งที่คุณต้องทำเพื่อเริ่มต้น:
1. ความรู้พื้นฐานเกี่ยวกับ C#: เนื่องจาก Aspose.Cells เป็นไลบรารี .NET คุณจึงสามารถเขียนโค้ด C# ได้อย่างคล่องแคล่ว
2.  ไลบรารี Aspose.Cells: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells แล้ว คุณสามารถดาวน์โหลดได้อย่างง่ายดายจาก[ลิงค์ดาวน์โหลด](https://releases.aspose.com/cells/net/).
3. Visual Studio: ใช้ Visual Studio หรือ IDE ที่เข้ากันได้เพื่อจัดการโครงการของคุณอย่างมีประสิทธิภาพ
4. .NET Framework: ตรวจสอบให้แน่ใจว่าโครงการของคุณกำหนดเป้าหมายไปที่ .NET Framework เวอร์ชันที่เข้ากันได้
เมื่อข้อกำหนดเบื้องต้นเหล่านี้พร้อมแล้ว คุณก็พร้อมที่จะไปได้เลย!
## แพ็คเกจนำเข้า
ก่อนที่คุณจะเริ่มเขียนโค้ด คุณจะต้องนำเข้าเนมสเปซที่จำเป็นเสียก่อน วิธีนี้จะช่วยให้คุณใช้ประโยชน์จากไลบรารี Aspose.Cells ได้อย่างเต็มที่ในโปรเจ็กต์ของคุณ
```csharp
using System.IO;
using Aspose.Cells;
```
ตรวจสอบให้แน่ใจว่าได้เพิ่มเนมสเปซเหล่านี้ไว้ที่ด้านบนของไฟล์ C# เพื่อหลีกเลี่ยงข้อผิดพลาดในระหว่างการคอมไพล์
ตอนนี้คุณพร้อมแล้ว มาดูขั้นตอนการจัดตำแหน่งข้อความในแนวนอนในเซลล์ Excel ทีละขั้นตอนกัน เราจะสร้างไฟล์ Excel ง่ายๆ เพิ่มข้อความลงในเซลล์ และปรับการจัดตำแหน่ง
## ขั้นตอนที่ 1: ตั้งค่าพื้นที่ทำงานของคุณ
ขั้นแรก คุณต้องตั้งค่าไดเร็กทอรีที่คุณต้องการบันทึกไฟล์ Excel ขั้นตอนนี้จะช่วยให้คุณมีพื้นที่ทำงานที่สะอาดสำหรับเอกสารของคุณ
```csharp
string dataDir = "Your Document Directory"; // ตั้งค่าไดเรกทอรีเอกสารของคุณ
// สร้างไดเรกทอรีหากยังไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
 ในสคริปท์นี้ ให้แทนที่`"Your Document Directory"` ด้วยเส้นทางที่คุณต้องการเก็บไฟล์ Excel ของคุณ หากไม่มีไดเร็กทอรี โค้ดจะสร้างไดเร็กทอรีนั้นให้กับคุณ
## ขั้นตอนที่ 2: สร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
ขั้นต่อไป คุณต้องสร้างวัตถุเวิร์กบุ๊ก วัตถุนี้ทำหน้าที่เป็นอินเทอร์เฟซหลักที่คุณใช้โต้ตอบกับสเปรดชีตของคุณ
```csharp
Workbook workbook = new Workbook();
```
 ที่นี่เราเพียงแต่สร้างตัวอย่างใหม่`Workbook` วัตถุที่จะแสดงถึงไฟล์ Excel ที่คุณกำลังจะสร้าง 
## ขั้นตอนที่ 3: รับการอ้างอิงถึงแผ่นงาน
ไฟล์ Excel ประกอบด้วยเวิร์กชีต และคุณจะต้องมีการอ้างอิงถึงเวิร์กชีตที่คุณต้องการจัดการ
```csharp
Worksheet worksheet = workbook.Worksheets[0]; // การเข้าถึงแผ่นงานแรก
```
ในตัวอย่างนี้ เราจะเข้าถึงเวิร์กชีตแรกของเวิร์กบุ๊ก (ดัชนี 0) หากคุณมีเวิร์กชีตหลายแผ่น คุณสามารถเข้าถึงได้โดยใช้ดัชนีที่เกี่ยวข้อง
## ขั้นตอนที่ 4: เข้าถึงเซลล์เฉพาะ
ตอนนี้เรามาเน้นที่เซลล์หนึ่งโดยเฉพาะที่คุณจะจัดตำแหน่งข้อความ ในกรณีนี้ เราจะเลือกเซลล์ "A1"
```csharp
Aspose.Cells.Cell cell = worksheet.Cells["A1"]; // การเข้าถึงเซลล์ A1
```
 โดยระบุ`"A1"`คุณกำลังสั่งให้โปรแกรมจัดการเซลล์เฉพาะนั้น 
## ขั้นตอนที่ 5: เพิ่มค่าให้กับเซลล์
มาใส่ข้อความลงในเซลล์กัน นี่คือข้อความที่คุณจะจัดตำแหน่งในภายหลัง
```csharp
cell.PutValue("Visit Aspose!"); //เพิ่มค่าบางอย่างลงในเซลล์ A1
```
 ตรงนี้เราจะใส่ประโยค`"Visit Aspose!"` ลงในเซลล์ A1 คุณสามารถแทนที่ด้วยข้อความใดๆ ก็ได้ตามที่คุณต้องการ
## ขั้นตอนที่ 6: ตั้งค่ารูปแบบการจัดแนวแนวนอน
ตอนนี้มาถึงส่วนที่น่าตื่นเต้น—การจัดตำแหน่งข้อความ! คุณสามารถตั้งค่าการจัดตำแหน่งแนวนอนของข้อความได้อย่างง่ายดายด้วย Aspose.Cells
```csharp
Style style = cell.GetStyle(); // การได้รับสไตล์ปัจจุบัน
style.HorizontalAlignment = TextAlignmentType.Center; // การจัดตำแหน่งกึ่งกลาง
cell.SetStyle(style); // การนำรูปแบบไปใช้
```
โค้ดตัวอย่างนี้ทำสองสามสิ่ง:
- ดึงรูปแบบปัจจุบันของเซลล์ A1
- ตั้งค่าการจัดตำแหน่งแนวนอนให้เป็นศูนย์กลาง
- สุดท้ายก็นำรูปแบบนี้กลับมาใช้กับเซลล์
## ขั้นตอนที่ 7: บันทึกไฟล์ Excel
ขั้นตอนต่อไปคือการบันทึกงานของคุณ ขั้นตอนนี้จะเขียนการเปลี่ยนแปลงที่คุณทำในเอกสาร
```csharp
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003); // การบันทึกไฟล์ Excel
```
ในบรรทัดนี้ ให้แน่ใจว่าชื่อไฟล์ (`"book1.out.xls"`) เป็นไปตามที่ตั้งใจไว้ รูปแบบไฟล์ที่ระบุคือ Excel 97-2003 คุณสามารถปรับเปลี่ยนได้ตามความต้องการของคุณ
## บทสรุป
ขอแสดงความยินดี! คุณเพิ่งเรียนรู้วิธีการจัดแนวข้อความในแนวนอนในเซลล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET แล้ว หากทำตามขั้นตอนง่ายๆ ที่ระบุไว้ข้างต้น คุณจะสามารถปรับปรุงรูปลักษณ์และการอ่านสเปรดชีตของคุณได้อย่างมาก ไม่ว่าคุณจะกำลังสร้างรายงานอัตโนมัติหรือจัดการการป้อนข้อมูล การนำความรู้เหล่านี้ไปใช้จะทำให้เอกสารดูเป็นมืออาชีพมากขึ้นและให้ประสบการณ์การใช้งานที่ดีขึ้น
## คำถามที่พบบ่อย
### Aspose.Cells คืออะไร?
Aspose.Cells เป็นไลบรารี .NET อันทรงพลังที่ช่วยให้นักพัฒนาสามารถสร้าง จัดการ และแปลงไฟล์ Excel โดยโปรแกรมได้
### ฉันสามารถใช้ Aspose.Cells ได้ฟรีหรือไม่?
 ใช่ Aspose เสนอ[ทดลองใช้งานฟรี](https://releases.aspose.com/) เพื่อทดสอบคุณสมบัติของห้องสมุด
### เป็นไปได้หรือไม่ที่จะกำหนดการจัดรูปแบบเซลล์นอกเหนือจากการจัดเรียงข้อความ?
แน่นอน! Aspose.Cells มีตัวเลือกมากมายสำหรับการจัดรูปแบบเซลล์ รวมถึงแบบอักษร สี ขอบ และอื่นๆ อีกมากมาย
### Aspose.Cells รองรับ Excel เวอร์ชันใดบ้าง
Aspose.Cells รองรับรูปแบบ Excel หลากหลาย รวมถึง XLS, XLSX และอื่นๆ อีกมากมาย
### ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Cells ได้จากที่ไหน
 คุณสามารถค้นหาความช่วยเหลือได้ที่[ฟอรั่มสนับสนุน Aspose.Cells](https://forum.aspose.com/c/cells/9).