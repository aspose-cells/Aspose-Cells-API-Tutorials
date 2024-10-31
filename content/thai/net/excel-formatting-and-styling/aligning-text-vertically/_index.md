---
title: การจัดตำแหน่งข้อความในแนวตั้งในเซลล์ Excel
linktitle: การจัดตำแหน่งข้อความในแนวตั้งในเซลล์ Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีจัดตำแหน่งข้อความในแนวตั้งในเซลล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยบทช่วยสอนทีละขั้นตอนนี้
type: docs
weight: 21
url: /th/net/excel-formatting-and-styling/aligning-text-vertically/
---
## การแนะนำ
ยินดีต้อนรับสู่การเดินทางที่น่าสนใจซึ่งเราจะพาคุณดำดิ่งสู่โลกของ Excel และเรียนรู้วิธีการจัดแนวข้อความในแนวตั้งในเซลล์ Excel โดยใช้ไลบรารี Aspose.Cells อันทรงพลังสำหรับ .NET Excel เป็นเครื่องมือที่ยอดเยี่ยมสำหรับการจัดการข้อมูล แต่บางครั้งการนำเสนอข้อมูลนั้นก็มีความสำคัญพอๆ กับข้อมูลนั้นเอง คุณเคยรู้สึกหงุดหงิดกับลักษณะที่ข้อความของคุณปรากฏบนเซลล์เหล่านั้นหรือไม่ ไม่ต้องกังวล ในบทช่วยสอนนี้ เราจะแสดงวิธีการปรับปรุงลักษณะภาพของแผ่นงาน Excel ของคุณด้วยขั้นตอนง่ายๆ สองสามขั้นตอน!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงรายละเอียดเกี่ยวกับการจัดตำแหน่งข้อความในเซลล์ Excel มีบางสิ่งที่คุณควรเตรียมให้พร้อม:
1.  Visual Studio: ตรวจสอบว่าคุณมี Visual Studio เวอร์ชันที่ใช้งานได้หรือ IDE ที่เข้ากันได้อื่น ๆ หากคุณยังไม่ได้ติดตั้ง คุณยังรออะไรอยู่ คุณสามารถดาวน์โหลดได้เลย[ที่นี่](https://visualstudio.microsoft.com/).
2. ไลบรารี Aspose.Cells: คุณจะต้องมีไลบรารี Aspose.Cells คุณสามารถดาวน์โหลดเวอร์ชันล่าสุดได้จาก[ลิงค์นี้](https://releases.aspose.com/cells/net/)ตั้งค่าอย่างรวดเร็ว และคุณก็พร้อมแล้ว!
3. ความรู้พื้นฐานเกี่ยวกับ C#: ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# จะเป็นประโยชน์ ไม่จำเป็นต้องมีความรู้ด้านการเขียนโค้ดมากนัก แต่ความคุ้นเคยจะทำให้ชีวิตของคุณง่ายขึ้น
4. .NET Framework: ตรวจสอบให้แน่ใจว่าโครงการของคุณได้รับการตั้งค่าให้กำหนดเป้าหมายเป็นเวอร์ชัน .NET Framework ที่เข้ากันได้กับ Aspose.Cells
5. ความเต็มใจที่จะเรียนรู้: จริงๆ แล้ว นั่นคือข้อกำหนดเบื้องต้นที่สำคัญที่สุด! คุณพร้อมหรือยัง? มาเริ่มกันเลย!
## แพ็คเกจนำเข้า
ตอนนี้เรามีทุกอย่างแล้ว ขั้นตอนทางเทคนิคแรกคือการนำเข้าแพ็คเกจที่จำเป็น สำหรับ Aspose.Cells คุณจะต้องแน่ใจว่าได้รวมเนมสเปซต่อไปนี้ไว้ในโปรเจ็กต์ C# ของคุณ:
```csharp
using System.IO;
using Aspose.Cells;
```
สิ่งนี้จะทำให้คุณสามารถเข้าถึงคลาสและวิธีการทั้งหมดที่จำเป็นในการจัดการไฟล์ Excel ได้อย่างมีประสิทธิภาพ
## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสารของคุณ
สิ่งแรกที่ต้องทำคือ เราจะเก็บไฟล์ Excel ใหม่ล่าสุดนี้ไว้ที่ไหน มาตั้งค่าไดเร็กทอรีเอกสารกัน คุณสามารถปรับแต่งไดเร็กทอรีนี้ตามความต้องการของโครงการของคุณได้
```csharp
string dataDir = "Your Document Directory";
```
## ขั้นตอนที่ 2: สร้างไดเรกทอรีหากไม่มีอยู่
ตอนนี้ เราต้องการให้แน่ใจว่าไดเร็กทอรีสำหรับเอกสารของเรามีอยู่ หากไม่มี เราจะสร้างมันขึ้นมา:
```csharp
// สร้างไดเร็กทอรีหากยังไม่มีอยู่
bool isExists = System.IO.Directory.Exists(dataDir);
if (!isExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
โค้ดนี้จะตรวจสอบการมีอยู่ของไดเรกทอรีที่ระบุ และสร้างขึ้นหากจำเป็น เหมือนกับการตรวจสอบว่าตู้ของคุณว่างหรือไม่ก่อนไปซื้อของ!
## ขั้นตอนที่ 3: สร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
เวิร์กบุ๊กคืออะไร? เวิร์กบุ๊กเป็นเหมือนผืนผ้าใบที่ข้อมูลทั้งหมดของคุณจะถูกวาดขึ้น ที่นี่เราจะสร้างวัตถุเวิร์กบุ๊กใหม่:
```csharp
Workbook workbook = new Workbook();
```
## ขั้นตอนที่ 4: ล้างเวิร์กชีตที่มีอยู่ทั้งหมด
บางครั้งคุณอาจมีข้อมูลเก่าหลงเหลืออยู่ในสมุดงานของคุณ มาเคลียร์กัน:
```csharp
// การเคลียร์แผ่นงานทั้งหมด
workbook.Worksheets.Clear();
```
การทำเช่นนี้จะทำให้คุณมีจุดเริ่มต้นใหม่ในการทำงาน! 
## ขั้นตอนที่ 5: การเพิ่มเวิร์กชีตใหม่
ตอนนี้เรามาเพิ่มเวิร์กชีตใหม่ลงในเวิร์กบุ๊กกัน ซึ่งจะเป็นพื้นที่เล่นสำหรับข้อมูลของเรา:
```csharp
int i = workbook.Worksheets.Add();
```
ขอแสดงความยินดี! คุณเพิ่งเพิ่มเวิร์กชีตใหม่!
## ขั้นตอนที่ 6: รับการอ้างอิงถึงเวิร์กชีตที่เพิ่มใหม่
ต่อไปเราต้องมีตัวจัดการเวิร์กชีตใหม่นี้ ดังนั้นเราจึงสามารถทำงานกับมันได้โดยตรง:
```csharp
// การรับข้อมูลอ้างอิงของแผ่นงานที่เพิ่มใหม่
Worksheet worksheet = workbook.Worksheets[i];
```
## ขั้นตอนที่ 7: เข้าถึงเซลล์ที่คุณต้องการแก้ไข
ตอนนี้เรามีเวิร์กชีตแล้ว เราจะเข้าถึงเซลล์ "A1" ซึ่งเราจะใส่ข้อความของเรา:
```csharp
// การเข้าถึงเซลล์ "A1" จากเวิร์กชีต
Aspose.Cells.Cell cell = worksheet.Cells["A1"];
```
## ขั้นตอนที่ 8: เพิ่มค่าลงในเซลล์
ถึงเวลาที่จะใส่เนื้อหาลงในเซลล์ของเราแล้ว เราจะเพิ่มข้อความที่เป็นมิตร:
```csharp
// การเพิ่มค่าบางอย่างลงในเซลล์ "A1"
cell.PutValue("Visit Aspose!");
```
มันดูน่ารักดีใช่ไหมล่ะ? 
## ขั้นตอนที่ 9: รับรูปแบบปัจจุบันของเซลล์
เราต้องการจัดตำแหน่งข้อความตามแนวตั้ง แต่ก่อนอื่น เราต้องได้รูปแบบปัจจุบันของเซลล์ของเราก่อน:
```csharp
// การตั้งค่าการจัดตำแหน่งแนวนอนของข้อความในเซลล์ "A1"
Style style = cell.GetStyle();
```
## ขั้นตอนที่ 10: ตั้งค่าการจัดตำแหน่งแนวตั้ง
นี่คือดาวเด่นของการแสดง! เราจะจัดตำแหน่งข้อความในเซลล์ตามแนวตั้ง:
```csharp
// การตั้งค่าการจัดตำแหน่งแนวตั้งของข้อความในเซลล์
style.VerticalAlignment = TextAlignmentType.Center;
```
เส้นนี้จะเปลี่ยนการจัดแนวแนวตั้งให้เป็นศูนย์กลาง ทำให้เซลล์ของคุณดูสวยงาม
## ขั้นตอนที่ 11: นำสไตล์กลับไปใช้กับเซลล์
หลังจากปรับแต่งสไตล์แล้ว เราต้องตั้งค่ากลับเป็นเซลล์ของเราเพื่อให้การเปลี่ยนแปลงมีผล:
```csharp
cell.SetStyle(style);
```
## ขั้นตอนที่ 12: บันทึกสมุดงาน
สุดท้ายนี้ ให้บันทึกสมุดงานของเราด้วยข้อความที่จัดตำแหน่งใหม่ อย่าลืมเลือกรูปแบบที่เหมาะกับความต้องการของคุณ:
```csharp
// การบันทึกไฟล์ Excel
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
ตบหลังตัวเองซะหน่อย คุณเพิ่งสร้างไฟล์ Excel ที่ข้อความในเซลล์ A1 เรียงตามแนวตั้ง น่าพอใจไหมล่ะ
## บทสรุป
การจัดแนวข้อความในแนวตั้งในเซลล์ Excel อาจดูเป็นเรื่องเล็กน้อย แต่สามารถปรับปรุงการอ่านและรูปลักษณ์ที่ดูเป็นมืออาชีพของสเปรดชีตของคุณได้อย่างแท้จริง ด้วยการใช้ไลบรารี Aspose.Cells สำหรับ .NET คุณไม่เพียงแต่เรียนรู้วิธีการจัดการการจัดแนวข้อความเท่านั้น แต่ยังฝึกฝนทักษะการเขียนโปรแกรมอันมีค่าอีกด้วย 
## คำถามที่พบบ่อย
### Aspose.Cells คืออะไร?  
Aspose.Cells เป็นไลบรารีอันทรงพลังสำหรับการจัดการไฟล์ Excel ใน .NET ช่วยให้นักพัฒนาสามารถดำเนินการที่ซับซ้อนได้โดยไม่ต้องติดตั้ง Microsoft Excel
### ฉันจำเป็นต้องซื้อ Aspose.Cells หรือไม่?  
แม้ว่าจะมีเวอร์ชันที่ต้องชำระเงิน แต่คุณสามารถเริ่มต้นด้วยรุ่นทดลองใช้งานฟรีเพื่อทดสอบฟีเจอร์ทั้งหมด คุณสามารถรับรุ่นทดลองใช้งาน[ที่นี่](https://releases.aspose.com).
### ฉันสามารถค้นหาเอกสารสำหรับ Aspose.Cells ได้ที่ไหน  
 เอกสารประกอบสามารถพบได้ที่[ลิงค์นี้](https://reference.aspose.com/cells/net/).
### ฉันสามารถใช้ Aspose.Cells สำหรับแอพพลิเคชันเว็บได้หรือไม่  
แน่นอน! Aspose.Cells สามารถใช้ได้ในแอปพลิเคชัน .NET ต่าง ๆ รวมถึงแอปพลิเคชันเว็บ แอปพลิเคชันเดสก์ท็อป และบริการต่าง ๆ
### ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Cells ได้อย่างไร  
 หากคุณมีคำถามหรือต้องการความช่วยเหลือ คุณสามารถติดต่อฟอรัมสนับสนุน Aspose ได้[ที่นี่](https://forum.aspose.com/c/cells/9).