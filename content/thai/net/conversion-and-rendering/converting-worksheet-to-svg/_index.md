---
title: การแปลงเวิร์กชีตเป็น SVG ใน .NET
linktitle: การแปลงเวิร์กชีตเป็น SVG ใน .NET
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีแปลงเวิร์กชีต Excel เป็น SVG โดยใช้ Aspose.Cells สำหรับ .NET ด้วยคู่มือทีละขั้นตอนนี้ เหมาะสำหรับนักพัฒนา .NET ที่ต้องการเรนเดอร์ Excel เป็น SVG
type: docs
weight: 11
url: /th/net/conversion-and-rendering/converting-worksheet-to-svg/
---
## การแนะนำ

หากคุณต้องการแปลงเวิร์กชีต Excel เป็นรูปแบบ SVG คุณมาถูกที่แล้ว! Aspose.Cells สำหรับ .NET เป็นเครื่องมืออันทรงพลังที่ช่วยให้ผู้พัฒนาสามารถจัดการไฟล์ Excel และแปลงเป็นรูปแบบต่างๆ ได้ รวมถึง SVG (Scalable Vector Graphics) ที่ได้รับการสนับสนุนอย่างกว้างขวาง บทช่วยสอนนี้จะแนะนำคุณตลอดกระบวนการแปลงเวิร์กชีตเป็น SVG ใน .NET โดยแบ่งขั้นตอนทีละขั้นตอนเพื่อให้แม้แต่ผู้เริ่มต้นก็สามารถทำตามได้อย่างง่ายดาย

## ข้อกำหนดเบื้องต้น

ก่อนที่จะเจาะลึกโค้ด เรามาตรวจสอบกันก่อนว่าคุณมีทุกสิ่งที่คุณต้องการ:

1.  Aspose.Cells สำหรับ .NET: ดาวน์โหลดและติดตั้ง Aspose.Cells เวอร์ชันล่าสุดสำหรับ .NET จาก[Aspose.Cells สำหรับ .NET](https://releases.aspose.com/cells/net/).
2. สภาพแวดล้อมการพัฒนา .NET: คุณจะต้องติดตั้ง Visual Studio หรือ IDE .NET อื่น ๆ
3. ความรู้พื้นฐานเกี่ยวกับ C#: ต้องมีความคุ้นเคยกับ C# แต่ไม่ต้องกังวล เราจะอธิบายทุกอย่างอย่างชัดเจน
4. ไฟล์ Excel: เตรียมไฟล์ Excel ที่คุณต้องการแปลงเป็นรูปแบบ SVG ไว้

## การนำเข้าแพ็คเกจที่จำเป็น

ก่อนจะเริ่มเขียนโค้ด อย่าลืมรวมเนมสเปซที่จำเป็นไว้ที่ด้านบนของไฟล์ C#

```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Rendering;
```

แพ็คเกจเหล่านี้จำเป็นสำหรับการทำงานกับ Aspose.Cells และการจัดการตัวเลือกการเรนเดอร์เช่นการส่งออก SVG

ตอนนี้เมื่อครอบคลุมพื้นฐานแล้ว มาดูขั้นตอนจริงในการแปลงเวิร์กชีต Excel เป็นภาพ SVG กัน

## ขั้นตอนที่ 1: ตั้งค่าเส้นทางไปยังไดเร็กทอรีเอกสารของคุณ

สิ่งแรกที่เราต้องทำคือกำหนดเส้นทางไปยังโฟลเดอร์ที่ไฟล์ Excel ของคุณตั้งอยู่ ซึ่งเป็นสิ่งสำคัญมาก เนื่องจากโค้ดของคุณจะอ้างอิงถึงไดเรกทอรีเพื่อโหลดและบันทึกไฟล์

```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```

 อย่าลืมเปลี่ยน`"Your Document Directory"`ด้วยเส้นทางจริงที่ไฟล์ Excel ของคุณอยู่

##  ขั้นตอนที่ 2: โหลดไฟล์ Excel โดยใช้`Workbook`

 ถัดไป เราต้องโหลดไฟล์ Excel ลงในอินสแตนซ์ของ`Workbook` ชั้นเรียน.`Workbook` คลาสแสดงถึงไฟล์ Excel ทั้งหมด รวมถึงเวิร์กชีตทั้งหมดภายในนั้น

```csharp
string filePath = dataDir + "Template.xlsx";
Workbook book = new Workbook(filePath);
```

 ที่นี่,`"Template.xlsx"` คือชื่อไฟล์ Excel ที่คุณใช้งานอยู่ ตรวจสอบว่าไฟล์นี้มีอยู่ในไดเร็กทอรีที่ระบุ มิฉะนั้นคุณจะพบข้อผิดพลาด

## ขั้นตอนที่ 3: ตั้งค่าตัวเลือกภาพหรือการพิมพ์สำหรับการแปลง SVG

 ก่อนที่เราจะแปลงแผ่นงานเป็นรูปแบบ SVG เราจะต้องระบุตัวเลือกรูปภาพ`ImageOrPrintOptions` คลาสนี้ช่วยให้คุณควบคุมวิธีการแปลงเวิร์กชีตได้ โดยเฉพาะอย่างยิ่ง เราต้องตั้งค่า`SaveFormat` ถึง`SVG` และให้แน่ใจว่าแผ่นงานแต่ละแผ่นจะถูกแปลงเป็นหน้าเดียว

```csharp
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
imgOptions.SaveFormat = SaveFormat.Svg;
imgOptions.OnePagePerSheet = true;
```

 การ`SaveFormat.Svg` ตัวเลือกนี้ช่วยให้แน่ใจว่ารูปแบบเอาต์พุตจะเป็น SVG ในขณะที่`OnePagePerSheet` รับประกันว่าแต่ละแผ่นงานจะถูกแสดงบนหน้าเดียว

## ขั้นตอนที่ 4: ทำซ้ำผ่านแต่ละเวิร์กชีตในเวิร์กบุ๊ก

ตอนนี้เราต้องวนซ้ำเวิร์กชีตทั้งหมดในไฟล์ Excel เวิร์กชีตแต่ละแผ่นจะถูกแปลงทีละแผ่น

```csharp
foreach (Worksheet sheet in book.Worksheets)
{
    // เราจะประมวลผลแผ่นงานแต่ละแผ่นทีละแผ่น
}
```

ลูปนี้จะทำให้แน่ใจว่าไม่ว่าจะมีเวิร์กชีตอยู่ในเวิร์กบุ๊กของคุณกี่แผ่นก็ตาม ทุกแผ่นก็จะได้รับการจัดการ

##  ขั้นตอนที่ 5: สร้าง`SheetRender` Object for Rendering

 สำหรับแต่ละแผ่นงานเราจะสร้าง`SheetRender` วัตถุ วัตถุนี้รับผิดชอบในการแปลงเวิร์กชีตเป็นรูปแบบภาพที่ต้องการ ซึ่งในกรณีนี้คือ SVG

```csharp
SheetRender sr = new SheetRender(sheet, imgOptions);
```

 การ`SheetRender` วัตถุใช้สองอาร์กิวเมนต์: เวิร์กชีตที่คุณกำลังแปลงและตัวเลือกภาพที่คุณกำหนดไว้ก่อนหน้านี้

## ขั้นตอนที่ 6: แปลงเวิร์กชีตเป็น SVG

 ในที่สุด เราจะแปลงเวิร์กชีตแต่ละแผ่นเป็นรูปแบบ SVG ภายในลูป เราใช้ลูปซ้อนเพื่อวนซ้ำผ่านหน้าต่างๆ (แม้ว่าในกรณีนี้ จะมีเพียงหนึ่งหน้าต่อเวิร์กชีตเท่านั้น เนื่องจาก`OnePagePerSheet` ตัวเลือก).

```csharp
for (int i = 0; i < sr.PageCount; i++)
{
    // ส่งออกแผ่นงานเป็นรูปแบบภาพ SVG
    sr.ToImage(i, filePath + sheet.Name + i + ".out.svg");
}
```

โค้ดนี้จะบันทึกเวิร์กชีตเป็นไฟล์ SVG ในไดเร็กทอรีเดียวกับไฟล์ Excel ไฟล์ SVG แต่ละไฟล์จะได้รับการตั้งชื่อตามชื่อเวิร์กชีตและหมายเลขดัชนีเพื่อหลีกเลี่ยงการขัดแย้งในการตั้งชื่อ

## บทสรุป

และแล้วเสร็จ! คุณได้แปลงเวิร์กชีต Excel เป็นรูปแบบ SVG สำเร็จแล้วโดยใช้ Aspose.Cells สำหรับ .NET ขั้นตอนนี้ช่วยให้คุณสามารถคงเค้าโครงและการออกแบบของเวิร์กชีตไว้ได้ พร้อมทั้งทำให้สามารถดูได้ในเบราว์เซอร์หรืออุปกรณ์ใดๆ ที่รองรับ SVG ซึ่งก็คือแทบทั้งหมด ไม่ว่าคุณจะทำงานกับไฟล์ Excel ที่ซับซ้อนหรือเพียงแค่ตารางธรรมดา วิธีนี้จะช่วยให้มั่นใจว่าข้อมูลของคุณจะถูกแสดงอย่างสวยงามในรูปแบบที่เป็นมิตรกับเว็บ

## คำถามที่พบบ่อย

### SVG คืออะไร และทำไมฉันจึงควรใช้มัน?
SVG (Scalable Vector Graphics) เป็นรูปแบบที่ใช้งานได้บนเว็บ ซึ่งสามารถปรับขนาดได้ไม่จำกัดโดยไม่สูญเสียคุณภาพ เหมาะอย่างยิ่งสำหรับแผนภูมิ ไดอะแกรม และรูปภาพที่ต้องแสดงในขนาดต่างๆ

### Aspose.Cells จัดการกับไฟล์ Excel ขนาดใหญ่เพื่อการแปลงได้หรือไม่
ใช่ Aspose.Cells สามารถจัดการไฟล์ Excel ขนาดใหญ่ได้อย่างมีประสิทธิภาพ และแปลงไฟล์เหล่านั้นเป็น SVG โดยไม่เกิดปัญหาประสิทธิภาพการทำงานอย่างมีนัยสำคัญ

### จำนวนเวิร์กชีตที่สามารถแปลงเป็น SVG มีจำกัดหรือไม่
ไม่ มีข้อจำกัดโดยธรรมชาติใน Aspose.Cells สำหรับการแปลงเวิร์กชีตหลายแผ่น ข้อจำกัดเพียงอย่างเดียวคือหน่วยความจำและประสิทธิภาพของระบบของคุณ

### ฉันต้องมีใบอนุญาตเพื่อใช้ Aspose.Cells หรือไม่?
 ใช่ Aspose.Cells ต้องมีใบอนุญาตสำหรับการใช้งานจริง คุณสามารถขอรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/) หรือสำรวจ[ทดลองใช้งานฟรี](https://releases.aspose.com/).

### ฉันสามารถปรับแต่งเอาท์พุต SVG ได้หรือไม่
 ใช่ คุณสามารถปรับเปลี่ยนได้`ImageOrPrintOptions` เพื่อปรับแต่งด้านต่างๆ ของเอาต์พุต SVG เช่น ความละเอียดและการปรับขนาด