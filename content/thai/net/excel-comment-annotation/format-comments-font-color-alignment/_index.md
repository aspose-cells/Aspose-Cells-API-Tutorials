---
title: รูปแบบความคิดเห็น - แบบอักษร, สี, การจัดตำแหน่ง
linktitle: รูปแบบความคิดเห็น - แบบอักษร, สี, การจัดตำแหน่ง
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: ค้นพบวิธีจัดรูปแบบความคิดเห็นใน Excel ได้อย่างง่ายดายโดยใช้ Aspose.Cells สำหรับ .NET ปรับแต่งแบบอักษร ขนาด และการจัดตำแหน่งเพื่อปรับปรุงสเปรดชีตของคุณ
type: docs
weight: 12
url: /th/net/excel-comment-annotation/format-comments-font-color-alignment/
---
## การแนะนำ
หากคุณเคยรู้สึกว่าแผ่นงาน Excel ของคุณต้องการความเก๋ไก๋หรือคำแนะนำที่เป็นประโยชน์มากกว่านี้ คุณไม่ได้เป็นคนเดียวอย่างแน่นอน ความคิดเห็นใน Excel เป็นเครื่องมือที่ยอดเยี่ยมสำหรับการทำงานร่วมกัน โดยให้บริบทและคำอธิบายที่ชัดเจนแก่สเปรดชีตของคุณโดยไม่ทำให้มุมมองดูรก หากคุณต้องการปรับแต่งแบบอักษร สี และการจัดตำแหน่งความคิดเห็นใน Excel โดยใช้ Aspose.Cells สำหรับ .NET คุณมาถูกที่แล้ว บทช่วยสอนนี้เต็มไปด้วยข้อมูลเชิงลึกที่เป็นประโยชน์ที่จะพาคุณจาก "ฉันควรทำอย่างไร" ไปสู่การเป็นผู้สร้างความคิดเห็นใน Excel ที่มีสไตล์และให้ข้อมูลอย่างภาคภูมิใจ
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะลงรายละเอียดเกี่ยวกับการจัดรูปแบบความคิดเห็นของคุณ มีบางสิ่งที่คุณต้องการ:
1. การตั้งค่าสภาพแวดล้อม: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งสภาพแวดล้อมการพัฒนา .NET โดยเฉพาะอย่างยิ่ง Visual Studio
2.  Aspose.Cells: ดาวน์โหลดและติดตั้ง Aspose.Cells จาก[ที่นี่](https://releases.aspose.com/cells/net/)ไลบรารีนี้ช่วยให้คุณโต้ตอบกับไฟล์ Excel ได้อย่างง่ายดาย
3. ความรู้พื้นฐานเกี่ยวกับ C#: แม้ว่าเราจะแนะนำคุณเกี่ยวกับโค้ด แต่ความเข้าใจพื้นฐานเกี่ยวกับ C# จะช่วยให้คุณปรับแต่งสิ่งต่าง ๆ ตามที่จำเป็นได้
4.  ใบอนุญาต Aspose: หากคุณวางแผนที่จะใช้ Aspose.Cells สำหรับเซสชันที่ขยายหรือในการผลิต โปรดพิจารณาซื้อใบอนุญาต[ที่นี่](https://purchase.aspose.com/buy) หรือใช้ใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).
## แพ็คเกจนำเข้า
หากต้องการเริ่มใช้ Aspose.Cells คุณต้องนำเข้าเนมสเปซที่จำเป็นลงในโปรเจ็กต์ของคุณ โดยคุณสามารถทำได้ดังนี้:
### สร้างโครงการใหม่
- เปิด Visual Studio และสร้างโปรเจ็กต์ใหม่
-  เลือกแอปคอนโซลเป็นประเภทโครงการของคุณ และตั้งชื่อตามความเหมาะสม เช่น`ExcelCommentsDemo`.
### เพิ่มไลบรารี Aspose.Cells
- คลิกขวาที่โครงการของคุณใน Solution Explorer
- เลือกจัดการแพ็คเกจ NuGet
-  ค้นหา`Aspose.Cells`และติดตั้งเวอร์ชันล่าสุด
### นำเข้าเนมสเปซที่จำเป็น
เปิดไฟล์ C# หลักของคุณและเพิ่มบรรทัดต่อไปนี้ที่ด้านบน:
```csharp
using System.IO;
using Aspose.Cells;
```
การดำเนินการนี้จะนำฟังก์ชันทั้งหมดของ Aspose.Cells มาสู่พื้นที่ทำงานของคุณ
ตอนนี้เราได้ตั้งค่าสภาพแวดล้อมแล้ว เรามาเริ่มสร้างและจัดรูปแบบความคิดเห็นในแผ่นงาน Excel กัน
## ขั้นตอนที่ 1: การตั้งค่าไดเรกทอรีเอกสาร
ก่อนที่คุณจะเริ่มสร้างเวิร์กบุ๊ก คุณต้องกำหนดว่าไฟล์ของคุณจะอยู่ที่ใด โดยมีวิธีดำเนินการดังนี้:
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
//สร้างไดเร็กทอรีหากยังไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
ในสไนปเป็ตนี้ เราจะกำหนดเส้นทางสำหรับบันทึกไฟล์ Excel ของเรา ถ้าไม่มีไดเร็กทอรีดังกล่าว เราจะสร้างขึ้นเอง! 
## ขั้นตอนที่ 2: การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
ขั้นต่อไป คุณจะต้องสร้างอ็อบเจ็กต์เวิร์กบุ๊กซึ่งโดยพื้นฐานแล้วคือไฟล์ Excel ในหน่วยความจำของคุณ
```csharp
// การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
Workbook workbook = new Workbook();
```
บรรทัดนี้จะเริ่มต้นเวิร์กบุ๊กใหม่ที่คุณสามารถเพิ่มแผ่นงาน แก้ไขข้อมูล และแน่นอน เพิ่มความคิดเห็นได้
## ขั้นตอนที่ 3: การเพิ่มเวิร์กชีตใหม่
เวิร์กบุ๊ก Excel ทุกอันสามารถมีแผ่นงานได้หลายแผ่น มาเพิ่มแผ่นงานหนึ่งแผ่นกัน:
```csharp
// การเพิ่มเวิร์กชีตใหม่ลงในวัตถุเวิร์กบุ๊ก
int sheetIndex = workbook.Worksheets.Add();
```
ด้วยวิธีนี้ คุณสามารถเพิ่มแผ่นงานใหม่และบันทึกดัชนีเพื่อใช้ในภายหลังได้
## ขั้นตอนที่ 4: การเข้าถึงแผ่นงานที่เพิ่มใหม่
ตอนนี้เรามีแผ่นงานแล้ว มาดูข้อมูลอ้างอิงกัน:
```csharp
// การรับการอ้างอิงของเวิร์กชีตที่เพิ่มใหม่โดยส่งดัชนีชีตของมัน
Worksheet worksheet = workbook.Worksheets[sheetIndex];
```
สิ่งนี้ช่วยให้คุณสามารถควบคุมแผ่นงานและทำให้คุณสามารถดำเนินการต่าง ๆ ได้
## ขั้นตอนที่ 5: การเพิ่มความคิดเห็นลงในเซลล์
ความสนุกเริ่มต้นที่นี่! มาเพิ่มความคิดเห็นในเซลล์ F5 กัน:
```csharp
// การเพิ่มความคิดเห็นลงในเซลล์ "F5"
int commentIndex = worksheet.Comments.Add("F5");
```
เราระบุตำแหน่งเซลล์และเพิ่มความคิดเห็นเพื่อให้เราปรับแต่งเพิ่มเติมได้
## ขั้นตอนที่ 6: การเข้าถึงความคิดเห็นที่เพิ่มเข้ามา
ตอนนี้เราต้องการทำงานกับความคิดเห็นนั้น วิธีเข้าถึงมีดังนี้:
```csharp
// การเข้าถึงความคิดเห็นที่เพิ่มใหม่
Comment comment = worksheet.Comments[commentIndex];
```
ตอนนี้เรามีความคิดเห็นแล้ว เราสามารถแก้ไขได้ตามที่เราต้องการ
## ขั้นตอนที่ 7: ตั้งค่าข้อความแสดงความคิดเห็น
มาเติมความคิดเห็นนั้นด้วยข้อความที่เป็นประโยชน์กัน:
```csharp
// การตั้งค่าหมายเหตุแสดงความคิดเห็น
comment.Note = "Hello Aspose!";
```
นี่คือส่วนที่จะแสดงบันทึกเมื่อคุณเลื่อนเมาส์ไปเหนือเซลล์ F5 
## ขั้นตอนที่ 8: ปรับแต่งขนาดตัวอักษรของความคิดเห็น
อยากให้ความคิดเห็นของคุณโดดเด่นใช่ไหม คุณสามารถปรับขนาดตัวอักษรได้อย่างง่ายดาย:
```csharp
// การกำหนดขนาดตัวอักษรของความคิดเห็นเป็น 14
comment.Font.Size = 14;
```
การขยายภาพที่กล้าหาญจะดึงดูดความสนใจอย่างแน่นอน!
## ขั้นตอนที่ 9: การทำตัวอักษรให้หนา
ต้องการก้าวไปอีกขั้นหรือไม่? แสดงความคิดเห็นของคุณให้ชัดเจน:
```csharp
// การตั้งค่าแบบอักษรของความคิดเห็นให้เป็นตัวหนา
comment.Font.IsBold = true;
```
เคล็ดลับเล็กๆ น้อยๆ นี้จะทำให้คุณไม่สามารถพลาดบันทึกใดๆ ได้!
## ขั้นตอนที่ 10: การตั้งค่าความสูงและความกว้าง
รู้สึกสร้างสรรค์ไหม คุณสามารถเปลี่ยนความสูงและความกว้างของความคิดเห็นของคุณได้เช่นกัน:
```csharp
// ตั้งค่าความสูงของตัวอักษรเป็น 10
comment.HeightCM = 10;
// ตั้งค่าความกว้างของตัวอักษรเป็น 2
comment.WidthCM = 2;
```
การปรับแต่งนี้จะทำให้ความคิดเห็นของคุณดูเรียบร้อยและน่าดึงดูดมากขึ้น
## ขั้นตอนที่ 11: การบันทึกสมุดงานของคุณ
สุดท้ายอย่าลืมบันทึกผลงานชิ้นเอกของคุณ:
```csharp
// การบันทึกไฟล์ Excel
workbook.Save(dataDir + "book1.out.xls");
```
และคุณก็ทำสำเร็จแล้ว! คุณได้สร้างและกำหนดรูปแบบความคิดเห็นใน Excel เรียบร้อยแล้ว ทำให้มันปรากฏออกจากหน้าจอทันที!
## บทสรุป
ขอแสดงความยินดี! คุณได้เสริมทักษะที่จำเป็นในการตกแต่งและเพิ่มความสวยงามให้กับความคิดเห็นใน Excel ของคุณด้วย Aspose.Cells สำหรับ .NET คุณไม่เพียงแต่สามารถเพิ่มความคิดเห็นอย่างง่ายได้เท่านั้น แต่ยังปรับแต่งแบบอักษร ขนาด และมิติได้ตามใจชอบอีกด้วย การทำเช่นนี้จะส่งเสริมการสื่อสารที่ดีขึ้นภายในทีมของคุณ และช่วยชี้แจงข้อมูลพื้นฐานโดยไม่ทำให้สเปรดชีตของคุณยุ่งเหยิง
อย่าลังเลที่จะสำรวจความสามารถอันกว้างขวางของ Aspose.Cells เพิ่มเติม ไม่ว่าจะสำหรับการใช้งานส่วนตัวหรือในสภาพแวดล้อมระดับมืออาชีพ เกม Excel ของคุณก็ก้าวจากศูนย์สู่ระดับสุดยอด!
## คำถามที่พบบ่อย
### Aspose.Cells คืออะไร?
Aspose.Cells เป็นไลบรารีอันทรงพลังสำหรับ .NET ที่ช่วยให้ผู้พัฒนาสามารถทำงานกับไฟล์ Excel ได้อย่างราบรื่น ช่วยให้สร้าง แก้ไข และจัดการแผ่นงาน Excel ได้ตามโปรแกรม
### ฉันจะได้รับทดลองใช้ Aspose.Cells ฟรีได้อย่างไร?
 คุณสามารถดาวน์โหลด Aspose.Cells รุ่นทดลองใช้งานฟรีได้จาก[ที่นี่](https://releases.aspose.com/).
### Aspose.Cells รองรับรูปแบบไฟล์ Excel อื่นนอกเหนือจาก XLS หรือไม่
ใช่ Aspose.Cells รองรับรูปแบบต่างๆ เช่น XLSX, XLSM, CSV, ODS และอื่นๆ อีกมากมาย!
### ฉันสามารถเพิ่มความคิดเห็นลงในหลายเซลล์พร้อมกันได้ไหม
ใช่ คุณสามารถวนซ้ำผ่านช่วงเซลล์และเพิ่มความคิดเห็นผ่านโปรแกรมได้โดยใช้วิธีการที่คล้ายกันตามที่อธิบายไว้ในบทช่วยสอนนี้
### ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Cells ได้จากที่ไหน
 หากต้องการความช่วยเหลือ คุณสามารถเยี่ยมชมฟอรัม Aspose[ที่นี่](https://forum.aspose.com/c/cells/9).