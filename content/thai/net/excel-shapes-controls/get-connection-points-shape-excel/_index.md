---
title: รับจุดเชื่อมต่อของรูปร่างใน Excel
linktitle: รับจุดเชื่อมต่อของรูปร่างใน Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีรับจุดเชื่อมต่อรูปร่างใน Excel ด้วย Aspose.Cells สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนของเราเพื่อแยกและแสดงจุดรูปร่างในโปรแกรมได้อย่างง่ายดาย
type: docs
weight: 11
url: /th/net/excel-shapes-controls/get-connection-points-shape-excel/
---
## การแนะนำ
เมื่อทำงานกับไฟล์ Excel โดยโปรแกรม เรามักจะต้องโต้ตอบกับรูปร่างที่ฝังอยู่ในแผ่นงาน หนึ่งในงานขั้นสูงที่คุณสามารถทำได้คือการแยกจุดเชื่อมต่อจากรูปร่าง จุดเชื่อมต่อใช้เพื่อแนบรูปร่างกับตัวเชื่อมต่อและจัดการเค้าโครงของรูปร่างได้แม่นยำยิ่งขึ้น หากคุณต้องการรับจุดเชื่อมต่อของรูปร่างใน Excel Aspose.Cells สำหรับ .NET คือเครื่องมือที่คุณต้องการ ในบทช่วยสอนนี้ เราจะพาคุณผ่านกระบวนการทีละขั้นตอนเพื่อให้บรรลุสิ่งนี้
## ข้อกำหนดเบื้องต้น
ก่อนที่จะดำดิ่งลงไปในโค้ด ให้แน่ใจว่าคุณมีข้อกำหนดเบื้องต้นดังต่อไปนี้:
- Aspose.Cells สำหรับ .NET: คุณจะต้องติดตั้ง Aspose.Cells ในสภาพแวดล้อมการพัฒนาของคุณ หากคุณยังไม่มี คุณสามารถทำได้[ดาวน์โหลดเวอร์ชันล่าสุดได้ที่นี่](https://releases.aspose.com/cells/net/).
- สภาพแวดล้อมการพัฒนา: ตรวจสอบให้แน่ใจว่าคุณมีการติดตั้ง Visual Studio หรือ IDE ที่เข้ากันได้กับ .NET อื่น ๆ ที่ใช้งานได้
- ความรู้พื้นฐานเกี่ยวกับ C#: บทช่วยสอนนี้ถือว่าคุณมีความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# และหลักการเชิงวัตถุ
 คุณยังสามารถลงทะเบียนได้[ทดลองใช้ Aspose.Cells ฟรี](https://releases.aspose.com/) หากคุณยังไม่ได้ทำ การดำเนินการนี้จะทำให้คุณสามารถเข้าถึงฟีเจอร์ทั้งหมดที่จำเป็นสำหรับคู่มือนี้

## แพ็คเกจนำเข้า
ในการใช้งาน Aspose.Cells ในโปรเจ็กต์ของคุณ คุณต้องรวมเนมสเปซที่จำเป็นไว้ด้วย คำสั่งนำเข้าต่อไปนี้ควรวางไว้ที่ด้านบนสุดของโค้ดของคุณ:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
เนมสเปซเหล่านี้ช่วยให้คุณเข้าถึงฟังก์ชันหลักของ Aspose.Cells และช่วยให้คุณสามารถจัดการเวิร์กชีตและรูปร่างได้

## คู่มือทีละขั้นตอนในการรับจุดเชื่อมต่อของรูปทรงต่างๆ
ในส่วนนี้ เราจะแนะนำคุณเกี่ยวกับวิธีการแยกจุดเชื่อมต่อของรูปร่างภายในเวิร์กชีต Excel ปฏิบัติตามแต่ละขั้นตอนอย่างระมัดระวังเพื่อความเข้าใจที่ชัดเจน
## ขั้นตอนที่ 1: สร้างเวิร์กบุ๊กใหม่
 สิ่งแรกที่ต้องทำคือเราต้องสร้างอินสแตนซ์ของ`Workbook` คลาสนี้แสดงไฟล์ Excel ใน Aspose.Cells หากคุณไม่มีไฟล์อยู่แล้ว ก็ไม่ต้องกังวล คุณสามารถเริ่มต้นด้วยเวิร์กบุ๊กเปล่าได้
```csharp
// สร้างเวิร์กบุ๊กใหม่
Workbook workbook = new Workbook();
```
 ในขั้นตอนนี้ เราได้สร้างเวิร์กบุ๊ก Excel ที่ว่างเปล่า แต่คุณสามารถโหลดเวิร์กบุ๊กที่มีอยู่ได้โดยส่งเส้นทางไฟล์ไปยัง`Workbook` ผู้สร้าง
## ขั้นตอนที่ 2: เข้าถึงแผ่นงานแรก
ต่อไปเราต้องเข้าถึงเวิร์กชีตที่เราต้องการทำงานกับรูปร่าง ในกรณีนี้ เราจะใช้เวิร์กชีตแรกของเวิร์กบุ๊ก
```csharp
// รับแผ่นงานแรกในสมุดงาน
Worksheet worksheet = workbook.Worksheets[0];
```
 บรรทัดนี้จะเข้าถึงเวิร์กชีตแรกจากคอลเลกชันของเวิร์กชีตในเวิร์กบุ๊ก หากคุณกำลังทำงานกับชีตเฉพาะ คุณสามารถแทนที่ดัชนีได้`0` ด้วยดัชนีที่ต้องการ
## ขั้นตอนที่ 3: เพิ่มกล่องข้อความใหม่ (รูปร่าง)
ตอนนี้เรามาเพิ่มรูปร่างใหม่ลงในเวิร์กชีตกัน เราจะสร้างกล่องข้อความ ซึ่งเป็นรูปร่างประเภทหนึ่ง คุณสามารถเพิ่มรูปร่างประเภทอื่นๆ ได้ด้วย แต่เพื่อความเรียบง่าย เราจะใช้กล่องข้อความในบทช่วยสอนนี้
```csharp
// เพิ่มกล่องข้อความใหม่ลงในคอลเลกชัน
int textboxIndex = worksheet.TextBoxes.Add(2, 1, 160, 200);
```
นี่คือสิ่งที่เราได้ทำ:
-  เพิ่มกล่องข้อความที่แถว`2` , คอลัมน์`1`.
-  ตั้งค่าขนาดของกล่องข้อความเป็น`160` หน่วยความกว้างและ`200` หน่วยความสูง
## ขั้นตอนที่ 4: เข้าถึงรูปร่างจากคอลเลกชันรูปร่าง
 เมื่อเราเพิ่มกล่องข้อความแล้ว กล่องข้อความนั้นจะกลายเป็นส่วนหนึ่งของคอลเลกชันรูปร่างของเวิร์กชีต ตอนนี้เราจะเข้าถึงรูปร่างนั้นโดยใช้`Shapes`ของสะสม.
```csharp
// เข้าถึงรูปร่าง (กล่องข้อความ) จากคอลเลกชันรูปร่าง
Shape shape = workbook.Worksheets[0].Shapes[0];
```
ในขั้นตอนนี้ เราจะดึงรูปร่างแรก (กล่องข้อความของเรา) จากคอลเลกชัน หากคุณมีรูปร่างหลายรูปร่าง คุณสามารถระบุดัชนีหรือแม้แต่ค้นหารูปร่างตามชื่อก็ได้
## ขั้นตอนที่ 5: ดึงจุดเชื่อมต่อ
ตอนนี้เรามีรูปร่างแล้ว มาแยกจุดเชื่อมต่อกัน จุดเหล่านี้ใช้สำหรับยึดตัวเชื่อมต่อเข้ากับรูปร่าง`ConnectionPoints` คุณสมบัติของรูปร่างส่งคืนจุดเชื่อมต่อทั้งหมดที่มีอยู่
```csharp
// รับจุดเชื่อมต่อทั้งหมดเป็นรูปร่างนี้
var connectionPoints = shape.ConnectionPoints;
```
นี่จะช่วยให้เรารวบรวมจุดเชื่อมต่อทั้งหมดที่มีสำหรับรูปร่างนั้น
## ขั้นตอนที่ 6: แสดงจุดเชื่อมต่อ
สุดท้าย เราต้องการแสดงพิกัดของจุดเชื่อมต่อแต่ละจุด นี่คือจุดที่เราวนซ้ำผ่านจุดเชื่อมต่อและพิมพ์ออกมาที่คอนโซล
```csharp
// แสดงจุดรูปร่างทั้งหมด
foreach (var pt in connectionPoints)
{
    System.Console.WriteLine(string.Format("X = {0}, Y = {1}", pt.X, pt.Y));
}
```
 ลูปนี้จะวนซ้ำผ่านจุดเชื่อมต่อแต่ละจุดและพิมพ์`X` และ`Y` พิกัด ซึ่งอาจมีประโยชน์ในการดีบักหรือยืนยันจุดเชื่อมต่อของรูปร่างด้วยภาพ
## ขั้นตอนที่ 7: ดำเนินการและเสร็จสิ้น
เมื่อคุณตั้งค่าขั้นตอนทั้งหมดข้างต้นแล้ว คุณสามารถรันโค้ดได้ นี่คือบรรทัดสุดท้ายที่ช่วยให้แน่ใจว่ากระบวนการเสร็จสมบูรณ์:
```csharp
System.Console.WriteLine("GetShapeConnectionPoints executed successfully.");
```
บรรทัดนี้เพียงบันทึกข้อความไปยังคอนโซลเพื่อระบุว่ากระบวนการเสร็จสมบูรณ์แล้ว

## บทสรุป
ในบทช่วยสอนนี้ เราได้กล่าวถึงวิธีการดึงจุดเชื่อมต่อของรูปร่างใน Excel โดยใช้ Aspose.Cells สำหรับ .NET โดยการแบ่งงานออกเป็นขั้นตอนย่อยๆ ที่เข้าใจง่าย เราได้สำรวจกระบวนการสร้างเวิร์กบุ๊ก การเพิ่มรูปร่าง และการแยกจุดเชื่อมต่อ
การเข้าใจวิธีการจัดการรูปร่างด้วยโปรแกรมจะช่วยให้คุณเปิดโลกแห่งความเป็นไปได้ในการสร้างแผ่นงาน Excel แบบไดนามิกและโต้ตอบได้ ไม่ว่าคุณจะกำลังสร้างรายงาน ออกแบบแดชบอร์ด หรือสร้างไดอะแกรม ความรู้เหล่านี้จะเป็นประโยชน์
## คำถามที่พบบ่อย
### จุดเชื่อมต่อในรูปร่างคืออะไร?
จุดเชื่อมต่อคือจุดเฉพาะบนรูปร่างซึ่งคุณสามารถเชื่อมต่อตัวเชื่อมต่อหรือเชื่อมโยงกับรูปร่างอื่นๆ ได้
### ฉันสามารถดึงจุดเชื่อมต่อสำหรับรูปร่างทั้งหมดในเวิร์กชีตได้หรือไม่
ใช่ Aspose.Cells ช่วยให้คุณเรียกค้นจุดเชื่อมต่อสำหรับรูปร่างใดๆ ที่รองรับจุดเชื่อมต่อนั้นได้ เพียงวนซ้ำผ่านคอลเลกชันรูปร่างในเวิร์กชีต
### ฉันต้องมีใบอนุญาตเพื่อใช้ Aspose.Cells หรือไม่?
ใช่ แม้ว่าคุณจะสามารถทดลองใช้งานฟรีได้ แต่จำเป็นต้องมีใบอนุญาตจึงจะใช้งานฟีเจอร์ทั้งหมดได้[ซื้อใบอนุญาตที่นี่](https://purchase.aspose.com/buy) หรือรับ[ใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/).
### ฉันจะเพิ่มประเภทรูปร่างต่างๆ ลงใน Aspose.Cells ได้อย่างไร
 คุณสามารถใช้`Add` วิธีการสำหรับรูปร่างต่างๆ เช่น สี่เหลี่ยมผืนผ้า วงรี และอื่นๆ โดยแต่ละรูปร่างจะมีพารามิเตอร์เฉพาะที่คุณสามารถปรับแต่งได้
### ฉันจะโหลดไฟล์ Excel ที่มีอยู่แทนที่จะสร้างไฟล์ใหม่ได้อย่างไร?
 หากต้องการโหลดไฟล์ที่มีอยู่ ให้ส่งเส้นทางไฟล์ไปที่`Workbook` ผู้สร้าง เช่นนี้:  
```csharp
Workbook workbook = new Workbook("path_to_file.xlsx");
```