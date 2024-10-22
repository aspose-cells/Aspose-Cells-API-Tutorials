---
title: เพิ่มความคิดเห็นลงในเซลล์หรือรูปร่างใน Excel
linktitle: เพิ่มความคิดเห็นลงในเซลล์หรือรูปร่างใน Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีเพิ่มความคิดเห็นในเซลล์ใน Excel โดยใช้ Aspose.Cells สำหรับ .NET คำแนะนำทีละขั้นตอนสำหรับผู้เริ่มต้นเพื่อปรับปรุงฟังก์ชันการทำงานของ Excel
type: docs
weight: 11
url: /th/net/excel-comment-annotation/add-comments-to-cells-or-shapes-excel/
---
## การแนะนำ
คุณกำลังมองหาวิธีปรับปรุงเอกสาร Excel ของคุณโดยการเพิ่มคำอธิบายลงในเซลล์หรือรูปร่างอยู่ใช่หรือไม่? คุณมาถูกที่แล้ว! บทความนี้จะแนะนำคุณเกี่ยวกับการใช้ Aspose.Cells สำหรับ .NET เพื่อเพิ่มคำอธิบายลงในไฟล์ Excel ของคุณอย่างมีประสิทธิภาพ ไม่ว่าคุณต้องการให้ข้อเสนอแนะ คำอธิบายประกอบ หรือเพียงแค่ข้อความทักทาย เราจะอธิบายให้คุณทราบทีละขั้นตอนเพื่อให้คุณทำตามได้อย่างราบรื่น ดังนั้น หยิบกล่องเครื่องมือเสมือนจริงของคุณขึ้นมาแล้วเริ่มใช้งานกันเลย!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มขั้นตอนการเพิ่มความคิดเห็นลงในแผ่นงาน Excel เรามาตรวจสอบกันก่อนว่าคุณได้เตรียมทุกอย่างที่จำเป็นแล้ว นี่คือสิ่งที่คุณควรมี:
- ติดตั้ง Visual Studio แล้ว: คุณจะต้องมี IDE ที่สามารถเขียนและคอมไพล์แอปพลิเคชัน .NET ได้ Visual Studio เป็นตัวเลือกยอดนิยมสำหรับนักพัฒนาหลายๆ คน
-  แพ็กเกจ Aspose.Cells: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้งไลบรารี Aspose.Cells แล้ว เป็นเครื่องมือที่มีประสิทธิภาพในการจัดการไฟล์ Excel คุณสามารถดาวน์โหลดได้จาก[หน้าวางจำหน่าย](https://releases.aspose.com/cells/net/).
- ความรู้พื้นฐานเกี่ยวกับ C#: ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# จะเป็นประโยชน์ เนื่องจากตัวอย่างทั้งหมดจะใช้ภาษาโปรแกรมนี้
-  ใบอนุญาต Aspose.Cells: สำหรับคุณสมบัติเพิ่มเติม โปรดพิจารณาซื้อใบอนุญาต แต่คุณสามารถเริ่มต้นด้วย[ทดลองใช้งานฟรี](https://releases.aspose.com/)ซึ่งมีข้อจำกัดอยู่
## แพ็คเกจนำเข้า
หากต้องการเริ่มทำงานกับ Aspose.Cells สิ่งแรกที่คุณต้องทำคือ นำเข้าแพ็คเกจที่จำเป็นลงในโปรเจ็กต์ C# ของคุณ โดยทำดังนี้
### เปิดโครงการของคุณ
เปิดโปรเจ็กต์ที่มีอยู่ของคุณใน Visual Studio หรือสร้างโปรเจ็กต์ใหม่หากคุณเริ่มต้นจากศูนย์
### ติดตั้ง Aspose.Cells
คุณสามารถติดตั้งแพ็กเกจ Aspose.Cells ได้อย่างง่ายดายจาก NuGet ดังต่อไปนี้:
1. คลิกขวาที่โครงการของคุณใน Solution Explorer
2. เลือก "จัดการแพ็คเกจ NuGet"
3. ค้นหา "Aspose.Cells" และติดตั้งเวอร์ชันล่าสุด
### เพิ่มคำสั่งการใช้งาน
ที่ด้านบนสุดของไฟล์โค้ดของคุณ ให้รวมคำสั่ง using ต่อไปนี้:
```csharp
using System.IO;
using Aspose.Cells;
```
ตอนนี้ คุณพร้อมที่จะจัดการไฟล์ Excel ด้วย Aspose.Cells แล้ว 

เมื่อจัดการข้อกำหนดเบื้องต้นเรียบร้อยแล้ว มาดูเนื้อหาหลักของคู่มือกันเลย: การเพิ่มคำอธิบายลงในเซลล์หรือรูปร่างในไฟล์ Excel เราจะดำเนินการทีละขั้นตอน
## ขั้นตอนที่ 1: การตั้งค่าไดเรกทอรีเอกสาร
ก่อนที่เราจะเริ่มจัดการเวิร์กบุ๊ก เราก็ต้องกำหนดก่อนว่าเอกสารของเราจะถูกจัดเก็บไว้ที่ไหน ต่อไปนี้เป็นวิธีตั้งค่าไดเร็กทอรีเอกสารของคุณ
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
//สร้างไดเร็กทอรีหากยังไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
ที่นี่ เรากำลังตรวจสอบว่าไดเร็กทอรีมีอยู่หรือไม่ ถ้าไม่มี เราจะสร้างขึ้นเอง เหมือนกับการให้แน่ใจว่าคุณมีบ้านก่อนที่จะเริ่มจัดวางเฟอร์นิเจอร์!
## ขั้นตอนที่ 2: การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
ตอนนี้เราต้องสร้างอินสแตนซ์เวิร์กบุ๊กใหม่ซึ่งเราจะได้ทำสิ่งมหัศจรรย์ทั้งหมด
```csharp
// การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
Workbook workbook = new Workbook();
```
คิดว่าสมุดงานเป็นผืนผ้าใบเปล่าที่คุณสามารถวาดผลงานชิ้นเอก Excel ของคุณได้ 
## ขั้นตอนที่ 3: การเพิ่มเวิร์กชีตใหม่
ไฟล์ Excel สามารถมีแผ่นงานได้หลายแผ่น มาเพิ่มแผ่นงานใหม่ลงในสมุดงานของเรา
```csharp
// การเพิ่มเวิร์กชีตใหม่ลงในวัตถุเวิร์กบุ๊ก
int sheetIndex = workbook.Worksheets.Add();
```
ศิลปินผู้ยิ่งใหญ่ทุกคนต้องมีผืนผ้าใบเปล่า เรามาเพิ่มผืนผ้าใบเปล่ากันที่นี่!
## ขั้นตอนที่ 4: การเข้าถึงแผ่นงานใหม่
ขั้นตอนต่อไป คือ ดึงข้อมูลอ้างอิงไปยังเวิร์กชีตใหม่เพื่อเริ่มทำการเปลี่ยนแปลง
```csharp
// การรับการอ้างอิงของเวิร์กชีตที่เพิ่มใหม่โดยส่งดัชนีชีตของมัน
Worksheet worksheet = workbook.Worksheets[sheetIndex];
```
ขั้นตอนนี้มีความสำคัญเนื่องจากทำให้คุณสามารถทำงานกับชีตใหม่ที่คุณเพิ่งเพิ่มได้โดยตรง เช่นเดียวกับการเข้าถึงเวิร์กเบนช์ของคุณ
## ขั้นตอนที่ 5: เพิ่มความคิดเห็นลงในเซลล์ F5
ตอนนี้มาดูส่วนที่น่าตื่นเต้นกัน นั่นคือการเพิ่มคำอธิบายลงในเซลล์ที่ต้องการ ในกรณีนี้ เราจะใส่คำอธิบายลงในเซลล์ “F5”
```csharp
// การเพิ่มความคิดเห็นลงในเซลล์ "F5"
int commentIndex = worksheet.Comments.Add("F5");
```
ลองนึกถึงการติดโน้ตลงบนส่วนใดส่วนหนึ่งของงานของคุณดูสิ จะช่วยให้คุณจำความคิดของคุณได้!
## ขั้นตอนที่ 6: การเข้าถึงความคิดเห็นที่เพิ่มใหม่
เพื่อปรับแต่งความคิดเห็นของเรา เราจะต้องเข้าถึงได้ทันทีหลังจากเพิ่มความคิดเห็น
```csharp
// การเข้าถึงความคิดเห็นที่เพิ่มใหม่
Comment comment = worksheet.Comments[commentIndex];
```
ในขั้นตอนนี้ เราจะดึงโน้ตติดตัวออกมาเพื่อเขียนความคิดของเราลงไป
## ขั้นตอนที่ 7: ตั้งค่าหมายเหตุความคิดเห็น
ตอนนี้ถึงเวลาจดบันทึกแล้ว มาเพิ่มข้อความลงในความคิดเห็นกัน
```csharp
// การตั้งค่าหมายเหตุแสดงความคิดเห็น
comment.Note = "Hello Aspose!";
```
ลองนึกภาพว่าคุณกำลังเขียนข้อความลงในกระดาษโน้ตของคุณ คุณกำลังถ่ายทอดความคิดของคุณออกมาเป็นคำพูด!
## ขั้นตอนที่ 8: บันทึกไฟล์ Excel
สุดท้ายแต่ไม่ท้ายสุด เราต้องบันทึกงานหนักของเราไว้ด้วย การทำเช่นนี้จะบันทึกสมุดงานพร้อมคำอธิบายของเราไว้ด้วย!
```csharp
// การบันทึกไฟล์ Excel
workbook.Save(dataDir + "book1.out.xls");
```
ขั้นตอนนี้เปรียบเสมือนการปิดหนังสือของคุณหลังจากเขียนเรื่องราวที่ยอดเยี่ยมเสร็จแล้ว นั่นคือคุณต้องแน่ใจว่าเรื่องราวนั้นได้รับการบันทึก!
## บทสรุป
และแล้วคุณก็ทำได้สำเร็จ! คุณได้เพิ่มความคิดเห็นลงในเซลล์ในไฟล์ Excel สำเร็จแล้วโดยใช้ Aspose.Cells สำหรับ .NET ความคิดเห็นสามารถเป็นประโยชน์สำหรับโครงการที่ทำงานร่วมกันหรือเพียงแค่แสดงคำเตือนสำหรับตัวคุณเอง ตอนนี้คุณได้ผ่านขั้นตอนทั้งหมดแล้ว คุณก็พร้อมที่จะพัฒนาทักษะ Excel ของคุณไปสู่อีกระดับ
## คำถามที่พบบ่อย
### ฉันสามารถเพิ่มความคิดเห็นลงในรูปร่างโดยใช้ Aspose.Cells ได้หรือไม่
ใช่! คุณสามารถเพิ่มคำอธิบายลงในรูปร่างได้ในลักษณะเดียวกับที่คุณทำกับเซลล์
### Aspose.Cells รองรับรูปแบบไฟล์อะไรบ้าง?
Aspose.Cells รองรับรูปแบบต่างๆ รวมถึง XLS, XLSX, CSV และอื่นๆ
### การใช้ Aspose.Cells ฟรีหรือไม่?
Aspose.Cells เสนอการทดลองใช้ฟรี แต่หากต้องการใช้ฟีเจอร์ครบถ้วน คุณอาจต้องซื้อใบอนุญาต
### ฉันสามารถค้นหาการสนับสนุนสำหรับ Aspose.Cells ได้ที่ไหน
 คุณสามารถรับการสนับสนุนได้โดยการเยี่ยมชม[ฟอรั่ม Aspose](https://forum.aspose.com/c/cells/9).
### ฉันจะขอใบอนุญาตชั่วคราวสำหรับ Aspose.Cells ได้อย่างไร
 สามารถขอใบอนุญาตชั่วคราวได้ที่[หน้าลิขสิทธิ์ Aspose](https://purchase.aspose.com/temporary-license/).