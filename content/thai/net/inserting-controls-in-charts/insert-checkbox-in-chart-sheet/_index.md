---
title: แทรกช่องกาเครื่องหมายในแผ่นงานแผนภูมิ
linktitle: แทรกช่องกาเครื่องหมายในแผ่นงานแผนภูมิ
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีแทรกช่องกาเครื่องหมายในแผ่นงานแผนภูมิ Excel ได้อย่างง่ายดายโดยใช้ Aspose.Cells สำหรับ .NET ด้วยบทช่วยสอนทีละขั้นตอนนี้
type: docs
weight: 13
url: /th/net/inserting-controls-in-charts/insert-checkbox-in-chart-sheet/
---
## การแนะนำ

หากคุณเคยสร้างแผนภูมิใน Excel คุณจะทราบดีว่า Excel เป็นเครื่องมือที่มีประสิทธิภาพอย่างเหลือเชื่อในการแสดงข้อมูล แต่จะเป็นอย่างไรหากคุณสามารถปรับปรุงการโต้ตอบนั้นให้ดียิ่งขึ้นโดยการเพิ่มช่องกาเครื่องหมายลงในแผนภูมิ แม้ว่าจะฟังดูซับซ้อนเล็กน้อย แต่จริงๆ แล้วสามารถทำได้ง่ายมากด้วยไลบรารี Aspose.Cells สำหรับ .NET ในบทช่วยสอนนี้ ฉันจะแนะนำคุณตลอดกระบวนการทีละขั้นตอน ทำให้ง่ายและปฏิบัติตามได้ง่าย

## ข้อกำหนดเบื้องต้น

ก่อนจะเริ่มลงมือปฏิบัติจริง เรามาตรวจสอบกันก่อนว่าคุณได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว นี่คือสิ่งที่คุณต้องการ:

### ติดตั้ง Visual Studio แล้ว
- สิ่งสำคัญอันดับแรกคือคุณต้องมี Visual Studio หากคุณยังไม่ได้ติดตั้ง คุณสามารถดาวน์โหลดได้จากเว็บไซต์ของ Microsoft

### ห้องสมุดเซลล์ Aspose
- เครื่องมือสำคัญถัดไปคือไลบรารี Aspose.Cells สำหรับ .NET คุณสามารถรับได้อย่างง่ายดายจาก[เว็บไซต์อาโพส](https://releases.aspose.com/cells/net/) สำหรับการดาวน์โหลด หากคุณต้องการทดสอบก่อนซื้อ ก็มี[มีให้ทดลองใช้งานฟรี](https://releases.aspose.com/).

### ความเข้าใจพื้นฐานเกี่ยวกับ C#
- เนื่องจากเราจะเขียนโค้ดบางส่วน ความเข้าใจพื้นฐานเกี่ยวกับ C# จึงจะเป็นประโยชน์ ไม่ต้องกังวล ฉันจะอธิบายสิ่งต่างๆ ให้เราฟังไปเรื่อยๆ!

### ไดเรกทอรีผลลัพธ์
- คุณจะต้องมีไดเรกทอรีที่จะบันทึกไฟล์ Excel เอาต์พุตของคุณ โปรดเตรียมสิ่งนี้ไว้ให้พร้อม

เมื่อตรวจสอบข้อกำหนดเบื้องต้นเหล่านี้ออกจากรายการของคุณแล้ว เราก็พร้อมที่จะเริ่มดำเนินการได้เลย!

## แพ็คเกจนำเข้า

ในการเริ่มต้น ให้ตั้งค่าโปรเจ็กต์ใน Visual Studio และนำเข้าแพ็คเกจที่จำเป็น นี่คือคำแนะนำทีละขั้นตอนแบบตรงไปตรงมา:

### สร้างโครงการใหม่

เปิด Visual Studio และสร้างโปรเจ็กต์แอปพลิเคชันคอนโซลใหม่ เพียงทำตามขั้นตอนง่ายๆ เหล่านี้:
- คลิกที่ “สร้างโครงการใหม่”
- เลือก “แอปคอนโซล (.NET Framework)” จากตัวเลือก
- ตั้งชื่อโครงการของคุณเป็น "CheckboxInChart"

### ติดตั้ง Aspose.Cells ผ่าน NuGet

เมื่อตั้งค่าโครงการของคุณเรียบร้อยแล้ว ก็ถึงเวลาเพิ่มไลบรารี Aspose.Cells คุณสามารถทำได้ผ่านตัวจัดการแพ็กเกจ NuGet:
- คลิกขวาที่โครงการของคุณใน Solution Explorer และเลือก “จัดการแพ็คเกจ NuGet”
- ค้นหา “Aspose.Cells” แล้วคลิก “ติดตั้ง”
- นี่จะดึงสิ่งที่ต้องมีทั้งหมดที่คุณต้องการ ทำให้การเริ่มใช้ไลบรารีเป็นเรื่องง่าย

### เพิ่มสิ่งที่จำเป็นโดยใช้คำสั่ง

 ที่ด้านบนของคุณ`Program.cs` ไฟล์ เพิ่มคำสั่งต่อไปนี้เพื่อทำให้ฟังก์ชัน Aspose.Cells พร้อมใช้งาน:
```csharp
using Aspose.Cells.Charts;
using System;
using Aspose.Cells.Drawing;
```

ตอนนี้คุณได้ติดตั้งเสร็จเรียบร้อยแล้ว! เหมือนกับการวางรากฐานให้มั่นคงก่อนสร้างบ้าน ซึ่งถือเป็นสิ่งสำคัญสำหรับโครงสร้างที่มั่นคง

ตอนนี้เราตั้งค่าทุกอย่างเรียบร้อยแล้ว เรามาเริ่มลงมือเขียนโค้ดกันเลย ต่อไปนี้คือรายละเอียดการแทรกช่องกาเครื่องหมายลงในแผ่นงานแผนภูมิโดยใช้ Aspose.Cells

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีผลลัพธ์ของคุณ

ก่อนที่เราจะไปถึงส่วนที่น่าตื่นเต้นนี้ เราต้องกำหนดก่อนว่าเราต้องการบันทึกไฟล์ไว้ที่ใด คุณจะต้องระบุเส้นทางไดเรกทอรีเอาต์พุต
```csharp
string outputDir = "C:\\YourOutputDirectory\\"; //เปลี่ยนเป็นไดเร็กทอรีที่คุณระบุ
```
 อย่าลืมเปลี่ยน`"C:\\YourOutputDirectory\\"` ด้วยเส้นทางที่คุณต้องการบันทึกไฟล์ของคุณ ให้คิดว่านี่เป็นการตั้งค่าพื้นที่ทำงานของคุณ คุณต้องรู้ว่าคุณกำลังวางเครื่องมือของคุณไว้ที่ไหน (หรือในกรณีนี้คือไฟล์ Excel ของคุณ)

## ขั้นตอนที่ 2: การสร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก

 ถัดไปเราจะสร้างอินสแตนซ์ของ`Workbook` ชั้นเรียน นี่คือที่ที่งานทั้งหมดของเราจะเกิดขึ้น
```csharp
Workbook workbook = new Workbook();
```
โค้ดบรรทัดนี้เปรียบเสมือนการเปิดผ้าใบเปล่า คุณพร้อมที่จะเริ่มวาดภาพแล้ว (หรือในกรณีของเราคือการเขียนโค้ด)!

## ขั้นตอนที่ 3: การเพิ่มแผนภูมิลงในเวิร์กชีต

ตอนนี้ถึงเวลาเพิ่มแผนภูมิลงในสมุดงานของคุณแล้ว วิธีดำเนินการมีดังนี้
```csharp
int index = workbook.Worksheets.Add(SheetType.Chart);
Worksheet sheet = workbook.Worksheets[index];
sheet.Charts.AddFloatingChart(ChartType.Column, 0, 0, 1024, 960);
```
ในโค้ดนี้คุณจะ:
- การเพิ่มแผ่นงานแผนภูมิใหม่ลงในสมุดงาน
- เลือกประเภทแผนภูมิ ในที่นี้เราจะใช้แผนภูมิคอลัมน์แบบง่าย
- การระบุขนาดของแผนภูมิของคุณ

พิจารณาขั้นตอนนี้เป็นการเลือกประเภทของกรอบรูปที่คุณต้องการก่อนที่จะวางงานศิลปะของคุณลงไป

## ขั้นตอนที่ 4: การเพิ่มชุดข้อมูลลงในแผนภูมิของคุณ

ในขั้นตอนนี้ เรามาเพิ่มชุดข้อมูลลงในแผนภูมิกันก่อน หากต้องการเพิ่มข้อมูลตัวอย่าง ให้ทำดังนี้:
```csharp
sheet.Charts[0].NSeries.Add("{1,2,3}", false);
```
เส้นนี้มีความสำคัญมาก! เหมือนกับการลงสีบนผืนผ้าใบ ตัวเลขแสดงจุดข้อมูลตัวอย่างสำหรับแผนภูมิของคุณ

## ขั้นตอนที่ 5: การเพิ่มช่องกาเครื่องหมายลงในแผนภูมิ

ตอนนี้เรามาถึงส่วนสนุก ๆ แล้ว นั่นคือการเพิ่มช่องกาเครื่องหมายลงในแผนภูมิของเรา โดยทำได้ดังนี้:
```csharp
sheet.Charts[0].Shapes.AddShapeInChart(MsoDrawingType.CheckBox, PlacementType.Move, 400, 400, 1000, 600);
sheet.Charts[0].Shapes[0].Text = "CheckBox 1";
```
ในโค้ดนี้:
- เราระบุประเภทของรูปร่างที่เราต้องการเพิ่ม — ในกรณีนี้คือช่องกาเครื่องหมาย
- `PlacementType.Move` หมายความว่าหากแผนภูมิเคลื่อนไหว ช่องกาเครื่องหมายก็จะเคลื่อนไหวด้วย
- เรายังกำหนดตำแหน่งและขนาดของกล่องกาเครื่องหมายภายในพื้นที่แผนภูมิ และในที่สุด เรายังตั้งค่าป้ายข้อความของกล่องกาเครื่องหมายอีกด้วย

การเพิ่มช่องกาเครื่องหมายเปรียบเสมือนการใส่เชอร์รีไว้บนซันเดย์ของคุณ ซึ่งจะช่วยเสริมให้การนำเสนอทั้งหมดดูดีขึ้น!

## ขั้นตอนที่ 6: การบันทึกไฟล์ Excel

สุดท้ายนี้ เรามาบันทึกงานของเราไว้ นี่คือชิ้นส่วนสุดท้ายของปริศนา:
```csharp
workbook.Save(outputDir + "InsertCheckboxInChartSheet_out.xlsx");
```
บรรทัดนี้จะบันทึกไฟล์ Excel ที่คุณเพิ่งสร้างใหม่พร้อมช่องทำเครื่องหมายในไดเร็กทอรีเอาต์พุตที่กำหนดไว้ เหมือนกับการปิดผนึกงานศิลปะของคุณในกล่องป้องกัน!

## บทสรุป

และแล้วคุณก็ทำได้สำเร็จ! คุณได้เพิ่มช่องกาเครื่องหมายลงในแผ่นงานแผนภูมิในไฟล์ Excel สำเร็จแล้วโดยใช้ Aspose.Cells สำหรับ .NET เมื่อทำตามขั้นตอนเหล่านี้ คุณก็สามารถสร้างแผ่นงาน Excel แบบโต้ตอบและแบบไดนามิกที่มีฟังก์ชันการทำงานที่ยอดเยี่ยม ทำให้การแสดงภาพข้อมูลของคุณน่าสนใจยิ่งขึ้น

## คำถามที่พบบ่อย

### Aspose.Cells คืออะไร?  
Aspose.Cells เป็นไลบรารีอันทรงพลังสำหรับการสร้างและจัดการไฟล์ Excel ในแอปพลิเคชัน .NET

### ฉันสามารถใช้ Aspose.Cells ได้ฟรีหรือไม่?  
 ใช่ Aspose เสนอรุ่นทดลองใช้งานฟรี คุณสามารถเริ่มต้นด้วยรุ่นทดลองใช้ที่มีจำหน่าย[ที่นี่](https://releases.aspose.com/).

### การเพิ่มช่องกาเครื่องหมายลงในแผ่นงานแผนภูมิเป็นเรื่องซับซ้อนหรือไม่?  
ไม่เลย! ตามที่สาธิตไว้ในบทช่วยสอนนี้ สามารถทำได้ด้วยโค้ดเพียงไม่กี่บรรทัด

### ฉันสามารถซื้อ Aspose.Cells ได้ที่ไหน?  
คุณสามารถซื้อ Aspose.Cells ได้จาก[ลิงค์ซื้อ](https://purchase.aspose.com/buy).

### ฉันจะได้รับการสนับสนุนได้อย่างไรหากประสบปัญหา?  
 Aspose มีฟอรัมสนับสนุนซึ่งคุณสามารถถามคำถามและค้นหาวิธีแก้ไขได้ ลองดู[หน้าสนับสนุน](https://forum.aspose.com/c/cells/9).