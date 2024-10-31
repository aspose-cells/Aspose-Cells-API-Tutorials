---
title: การสร้างเอฟเฟกต์การขีดฆ่าข้อความใน Excel
linktitle: การสร้างเอฟเฟกต์การขีดฆ่าข้อความใน Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีการใช้เอฟเฟ็กต์ขีดฆ่าข้อความใน Excel ด้วย Aspose.Cells สำหรับ .NET ในบทช่วยสอนทีละขั้นตอนโดยละเอียดนี้
type: docs
weight: 15
url: /th/net/working-with-fonts-in-excel/creating-strike-out-effect/
---
## การแนะนำ
เมื่อพูดถึง Excel องค์ประกอบภาพมีความสำคัญพอๆ กับข้อมูล ไม่ว่าคุณจะเน้นการเปลี่ยนแปลงที่สำคัญหรือทำเครื่องหมายรายการที่ไม่เกี่ยวข้องอีกต่อไป เอฟเฟกต์การขีดฆ่าข้อความเป็นวิธีคลาสสิกในการจัดการการแสดงภาพในสเปรดชีต ในคู่มือนี้ เราจะแนะนำคุณเกี่ยวกับกระบวนการนำเอฟเฟกต์การขีดฆ่าไปใช้กับข้อความใน Excel โดยใช้ Aspose.Cells สำหรับ .NET บทช่วยสอนนี้จะไม่เพียงแต่ครอบคลุมข้อกำหนดเบื้องต้นที่จำเป็นเท่านั้น แต่ยังให้แนวทางทีละขั้นตอนเพื่อให้แน่ใจว่าคุณสามารถจำลองเอฟเฟกต์นี้ได้อย่างง่ายดาย
## ข้อกำหนดเบื้องต้น
ก่อนจะเข้าสู่บทช่วยสอนนี้ โปรดตรวจสอบให้แน่ใจว่าคุณได้ปฏิบัติตามข้อกำหนดเบื้องต้นต่อไปนี้:
1. สภาพแวดล้อมการพัฒนา: คุณควรมีการตั้งค่าสภาพแวดล้อมการพัฒนา .NET ไว้ ซึ่งอาจเป็น Visual Studio หรือ IDE อื่น ๆ ที่คุณต้องการที่รองรับการพัฒนา .NET
2. Aspose.Cells สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells ไว้ในโปรเจ็กต์ของคุณแล้ว คุณสามารถดาวน์โหลดได้จากลิงก์ต่อไปนี้:[ดาวน์โหลด Aspose.Cells](https://releases.aspose.com/cells/net/).
3. ความรู้พื้นฐานเกี่ยวกับ C#: ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# จะเป็นประโยชน์เนื่องจากตัวอย่างต่างๆ จะถูกเข้ารหัสด้วย C#
4. .NET Framework: ตรวจสอบให้แน่ใจว่าโครงการของคุณกำหนดเป้าหมายไปที่เวอร์ชัน .NET Framework ที่เข้ากันได้ โดยทั่วไปคือ .NET Core หรือ .NET Framework 4.5 ขึ้นไป
## แพ็คเกจนำเข้า
ก่อนที่คุณจะเขียนโค้ดใดๆ คุณต้องนำเข้าเนมสเปซที่จำเป็นจาก Aspose.Cells ซึ่งเป็นสิ่งสำคัญสำหรับการเข้าถึงฟีเจอร์ต่างๆ ที่ไลบรารีจัดเตรียมไว้ให้ ต่อไปนี้คือวิธีที่คุณสามารถนำเข้าเนมสเปซที่จำเป็น:
```csharp
using System.IO;
using Aspose.Cells;
```
ด้วยการนำเข้าเหล่านี้ คุณจะสามารถเข้าถึงคลาสเวิร์กบุ๊ก เวิร์กชีต และสไตล์ที่จะใช้ตลอดบทช่วยสอนนี้
ตอนนี้เราได้เตรียมขั้นตอนเรียบร้อยแล้ว เรามาแบ่งกระบวนการออกเป็นขั้นตอนที่จัดการได้ แต่ละขั้นตอนจะมีคำแนะนำที่ชัดเจนเพื่อแนะนำคุณตลอดขั้นตอนการสร้างเอฟเฟกต์การขีดฆ่าข้อความใน Excel
## ขั้นตอนที่ 1: กำหนดไดเรกทอรีเอกสาร
เริ่มต้นด้วยการกำหนดเส้นทางที่จะเก็บเอกสาร Excel ของคุณ ซึ่งจะเป็นตำแหน่งสำหรับบันทึกไฟล์เอาต์พุตของคุณ
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```
 แทนที่`"Your Document Directory"` ด้วยเส้นทางไดเรกทอรีจริงที่คุณต้องการบันทึกไฟล์ Excel ของคุณ ซึ่งจะตั้งค่าไดเรกทอรีสำหรับผลลัพธ์ของคุณ
## ขั้นตอนที่ 2: สร้างไดเรกทอรี
ขั้นต่อไป คุณต้องแน่ใจว่าไดเร็กทอรีที่คุณระบุไว้ในขั้นตอนก่อนหน้านั้นมีอยู่ หากไม่มี คุณสามารถสร้างไดเร็กทอรีนั้นขึ้นมาโดยใช้โปรแกรมได้
```csharp
// สร้างไดเร็กทอรีหากยังไม่มีอยู่
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
โค้ดนี้จะตรวจสอบว่าไดเรกทอรีมีอยู่หรือไม่ และจะสร้างไดเรกทอรีขึ้นมาใหม่หากไม่พบ วิธีนี้จะช่วยหลีกเลี่ยงข้อผิดพลาดเมื่อคุณพยายามบันทึกไฟล์ในภายหลัง
## ขั้นตอนที่ 3: สร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
ตอนนี้ถึงเวลาสร้างวัตถุเวิร์กบุ๊กใหม่แล้ว นี่คือรากฐานของไฟล์ Excel ที่คุณจะเพิ่มข้อมูลและใช้รูปแบบต่างๆ
```csharp
// การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
Workbook workbook = new Workbook();
```
 การ`Workbook` คลาสนี้แสดงถึงไฟล์ Excel โดยการสร้างอินสแตนซ์ของคลาสนี้ คุณก็จะสร้างเอกสาร Excel ใหม่ขึ้นมา
## ขั้นตอนที่ 4: เพิ่มเวิร์กชีตใหม่
สมุดงานแต่ละเล่มสามารถมีแผ่นงานได้หลายแผ่น มาสร้างแผ่นงานใหม่ในสมุดงานของคุณกันเลย
```csharp
// การเพิ่มเวิร์กชีตใหม่ลงในวัตถุ Excel
int i = workbook.Worksheets.Add();
```
 การ`Add` วิธีการของ`Worksheets` คอลเลกชันเพิ่มเวิร์กชีตใหม่ลงในเวิร์กบุ๊กและส่งคืนดัชนีของเวิร์กชีตนั้น 
## ขั้นตอนที่ 5: รับการอ้างอิงของเวิร์กชีตใหม่
เมื่อคุณสร้างแผ่นงานแล้ว คุณต้องอ้างอิงแผ่นงานนั้นสำหรับการดำเนินการในอนาคต
```csharp
// การรับการอ้างอิงของเวิร์กชีตที่เพิ่มใหม่โดยส่งดัชนีชีตของมัน
Worksheet worksheet = workbook.Worksheets[i];
```
ที่นี่ คุณกำลังดึงเวิร์กชีตที่เพิ่งสร้างใหม่โดยใช้ดัชนี (`i`) นี้ทำให้คุณสามารถเข้าถึงเพื่อจัดการแผ่นงานได้
## ขั้นตอนที่ 6: เข้าถึงเซลล์
 คุณต้องการเข้าถึงเซลล์เฉพาะในเวิร์กชีตของคุณซึ่งคุณจะใช้รูปแบบการขีดฆ่า ในตัวอย่างนี้ เราจะใช้เซลล์`A1`.
```csharp
// การเข้าถึงเซลล์ "A1" จากเวิร์กชีต
Aspose.Cells.Cell cell = worksheet.Cells["A1"];
```
 ใน Excel เซลล์จะถูกอ้างอิงตามตัวระบุคอลัมน์และแถว (เช่น "A1") เรากำลังได้รับการอ้างอิงไปยังเซลล์`A1` เพื่อการดำเนินการต่อไป
## ขั้นตอนที่ 7: เพิ่มค่าให้กับเซลล์
 ต่อไปเรามาแทรกข้อความลงในเซลล์กัน โดยเราจะเขียนว่า “Hello Aspose!” ในเซลล์`A1`.
```csharp
// การเพิ่มค่าบางอย่างลงในเซลล์ "A1"
cell.PutValue("Hello Aspose!");
```
 การ`PutValue` วิธีนี้ใช้เพื่อกำหนดค่าสตริงให้กับเซลล์ คุณสามารถปรับเปลี่ยนสตริงนี้ให้เป็นค่าใดก็ได้ที่คุณต้องการให้แสดง
## ขั้นตอนที่ 8: รับรูปแบบของเซลล์
ตอนนี้เรามีข้อความในเซลล์แล้ว ถึงเวลาเข้าถึงรูปแบบเซลล์เพื่อใช้การจัดรูปแบบที่ต้องการ รวมถึงเอฟเฟกต์การขีดฆ่าด้วย
```csharp
// การได้รับสไตล์ของเซลล์
Style style = cell.GetStyle();
```
 การ`GetStyle` วิธีการดึงข้อมูลรูปแบบปัจจุบันของเซลล์ ช่วยให้คุณสามารถปรับเปลี่ยนคุณสมบัติ เช่น ชนิดของแบบอักษร ขนาด และเอฟเฟกต์ได้
## ขั้นตอนที่ 9: ตั้งค่าเอฟเฟกต์การขีดฆ่า
ลองใช้เอฟเฟ็กต์ขีดฆ่าข้อความในเซลล์ดู เราจะปรับเปลี่ยนรูปแบบฟอนต์ของเซลล์
```csharp
// ExStart: ตั้งค่าการหยุดงาน
// การตั้งค่าเอฟเฟกต์การขีดฆ่าบนแบบอักษร
style.Font.IsStrikeout = true;
// ExEnd: ตั้งค่าการขีดฆ่า
```
 โดยการตั้งค่า`IsStrikeout` หากเป็นจริง คุณกำลังสั่งให้ Excel ขีดฆ่าข้อความในเซลล์ที่เลือกโดยใช้ภาพ ซึ่งก็คล้ายกับการทำเครื่องหมายบางสิ่งบางอย่างออกจากรายการโดยใช้ภาพ
## ขั้นตอนที่ 10: นำสไตล์ไปใช้กับเซลล์
หลังจากปรับเปลี่ยนสไตล์แล้ว คุณต้องนำสไตล์นั้นกลับไปใช้กับเซลล์อีกครั้งเพื่อสะท้อนการเปลี่ยนแปลง
```csharp
// การนำรูปแบบไปใช้กับเซลล์
cell.SetStyle(style);
```
 การ`SetStyle` วิธีการนี้จะอัปเดตเซลล์ด้วยรูปแบบใหม่ ซึ่งขณะนี้รวมถึงการจัดรูปแบบการขีดฆ่าด้วย
## ขั้นตอนที่ 11: บันทึกไฟล์ Excel
 ในที่สุด ก็ถึงเวลาบันทึกเวิร์กบุ๊กของคุณไปยังไดเร็กทอรีที่ระบุ ในตัวอย่างนี้ เราจะบันทึกไฟล์โดยใช้ชื่อ`book1.out.xls`.
```csharp
// การบันทึกไฟล์ Excel
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
 การ`Save`วิธีการนี้จะเขียนเวิร์กบุ๊กลงในดิสก์ในรูปแบบ Excel 97-2003 คุณสามารถระบุรูปแบบอื่นได้หากจำเป็น
## บทสรุป
การสร้างเอฟเฟกต์ขีดฆ่าข้อความใน Excel โดยใช้ Aspose.Cells สำหรับ .NET เป็นกระบวนการที่ตรงไปตรงมาเมื่อคุณแบ่งกระบวนการออกเป็นขั้นตอนต่างๆ เมื่อปฏิบัติตามคู่มือนี้แล้ว ตอนนี้คุณจะมีทักษะในการปรับปรุงสเปรดชีตของคุณด้วยคำแนะนำทางภาพ ทำให้ข้อมูลของคุณไม่เพียงแต่ให้ข้อมูลเท่านั้น แต่ยังดึงดูดสายตาอีกด้วย
## คำถามที่พบบ่อย
### Aspose.Cells คืออะไร?
Aspose.Cells เป็นไลบรารีอันทรงพลังสำหรับการจัดการไฟล์ Excel ในแอปพลิเคชัน .NET ช่วยให้คุณสามารถสร้าง จัดการ และแปลงเอกสาร Excel ได้โดยการใช้โปรแกรม
### ฉันสามารถใช้ Aspose.Cells ได้ฟรีหรือไม่?
 ใช่ คุณสามารถใช้งานฟรีในช่วงทดลองใช้งาน สามารถทดลองใช้งานฟรีได้ที่[Aspose.Cells ทดลองใช้งานฟรี](https://releases.aspose.com/).
### ฉันจะซื้อ Aspose.Cells ได้อย่างไร?
 คุณสามารถซื้อใบอนุญาตสำหรับ Aspose.Cells ได้ผ่านทางเว็บไซต์ของพวกเขา[ซื้อ Aspose.Cells](https://purchase.aspose.com/buy).
### มีตัวอย่างการใช้ Aspose.Cells หรือไม่
 ใช่ คุณจะพบตัวอย่างและตัวอย่างโค้ดมากมายใน[เอกสารประกอบ Aspose.Cells](https://reference.aspose.com/cells/net/).
### ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Cells ได้จากที่ไหน
 คุณสามารถรับการสนับสนุนและความช่วยเหลือจากชุมชนได้จาก[ฟอรั่ม Aspose](https://forum.aspose.com/c/cells/9).