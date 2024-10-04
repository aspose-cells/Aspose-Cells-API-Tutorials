---
title: ตั้งค่าประเภทรูปร่างของป้ายข้อมูลของแผนภูมิ
linktitle: ตั้งค่าประเภทรูปร่างของป้ายข้อมูลของแผนภูมิ
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: ปรับปรุงแผนภูมิ Excel ของคุณด้วยรูปร่างป้ายข้อมูลที่กำหนดเองโดยใช้ Aspose.Cells สำหรับ .NET ปฏิบัติตามคำแนะนำทีละขั้นตอนนี้เพื่อยกระดับการนำเสนอข้อมูลของคุณ
type: docs
weight: 14
url: /th/net/advanced-chart-operations/set-shape-type-of-data-labels-of-chart/
---
## การแนะนำ

ในโลกแห่งการแสดงข้อมูล แผนภูมิเป็นวิธีการหลักในการนำเสนอข้อมูลที่ซับซ้อนในลักษณะที่เข้าถึงได้ อย่างไรก็ตาม ป้ายข้อมูลไม่ได้ถูกสร้างมาเท่าเทียมกันเสมอไป บางครั้ง คุณจำเป็นต้องทำให้ป้ายข้อมูลเหล่านี้โดดเด่น และการใช้รูปทรงที่แตกต่างกันสามารถสร้างความแตกต่างได้อย่างมาก หากคุณกำลังมองหาวิธีปรับปรุงป้ายข้อมูลในแผนภูมิ Excel ของคุณด้วยรูปทรงที่กำหนดเอง คุณมาถูกที่แล้ว คู่มือนี้จะแนะนำวิธีตั้งค่าประเภทรูปร่างของป้ายข้อมูลในแผนภูมิโดยใช้ Aspose.Cells สำหรับ .NET มาเจาะลึกกันเลย!

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเริ่มต้นเขียนโค้ด เรามาตรวจสอบก่อนว่าคุณได้ตั้งค่าทุกอย่างอย่างถูกต้องแล้ว นี่คือสิ่งที่คุณต้องการ:

1.  Aspose.Cells สำหรับ .NET: หากคุณยังไม่ได้ดาวน์โหลด ให้ดาวน์โหลดจาก[เว็บไซต์อาโพส](https://releases.aspose.com/cells/net/)ไลบรารีนี้รองรับการจัดการเอกสาร Excel ทุกประเภท
2. Visual Studio: คุณควรติดตั้งโปรแกรมนี้ไว้ในระบบของคุณเพื่อเขียนและรันแอปพลิเคชัน .NET ตรวจสอบให้แน่ใจว่าเป็นเวอร์ชันที่รองรับ .NET Framework หรือ .NET Core ตามความต้องการของโปรเจ็กต์ของคุณ
3. ความเข้าใจพื้นฐานเกี่ยวกับ C#: ความคุ้นเคยกับแนวคิดการเขียนโปรแกรมพื้นฐานและรูปแบบภาษา C# จะช่วยให้คุณเข้าใจชิ้นส่วนโค้ดได้ดีขึ้นอย่างแน่นอน
4. ไฟล์ Excel: คุณจะต้องมีเวิร์กบุ๊ก Excel ตัวอย่างเพื่อใช้ในการทำงาน คุณสามารถสร้างเวิร์กบุ๊กของคุณเองหรือใช้เวิร์กบุ๊กที่มีอยู่แล้วก็ได้

ตอนนี้เรามีข้อกำหนดเบื้องต้นแล้ว มาเริ่มกันเลย!

## แพ็คเกจนำเข้า

ก่อนที่คุณจะเริ่มเขียนโค้ด คุณต้องนำเข้าเนมสเปซ Aspose.Cells ที่เกี่ยวข้องเสียก่อน ซึ่งจะทำให้คุณเข้าถึงฟังก์ชันต่างๆ มากมายที่ไลบรารีนี้เสนอให้ วิธีดำเนินการมีดังนี้

### นำเข้า Aspose.Cells

เปิดโครงการ Visual Studio ของคุณ และเพิ่มคำสั่ง using directive ต่อไปนี้ที่ด้านบนของไฟล์ C# ของคุณ:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Charts;
using Aspose.Cells.Drawing;
```

เนมสเปซเหล่านี้จะช่วยให้คุณสร้างและจัดการเวิร์กบุ๊ก เวิร์กชีต และแผนภูมิได้อย่างง่ายดาย

ตอนนี้เราพร้อมแล้ว เรามาเริ่มเขียนโค้ดกันเลย! เราจะอธิบายทีละขั้นตอนเพื่อความชัดเจน

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีของคุณ

ขั้นตอนแรกสุดคือต้องกำหนดก่อนว่าไฟล์ของคุณอยู่ที่ไหน ทั้งไฟล์ต้นฉบับและโฟลเดอร์ปลายทางที่คุณต้องการบันทึกไฟล์ที่แก้ไข

```csharp
// ไดเรกทอรีแหล่งที่มา
string sourceDir = "Your Document Directory";

// ไดเรกทอรีผลลัพธ์
string outputDir = "Your Output Directory";
```

 แทนที่`"Your Document Directory"` และ`"Your Output Directory"` ด้วยเส้นทางจริงบนเครื่องของคุณ

## ขั้นตอนที่ 2: โหลดไฟล์ Excel ต้นฉบับ

ขั้นต่อไป คุณจะต้องโหลดไฟล์ Excel ที่คุณต้องการใช้งาน นี่คือจุดที่ความมหัศจรรย์เริ่มต้นขึ้น!

```csharp
// โหลดไฟล์ Excel ต้นฉบับ
Workbook wb = new Workbook(sourceDir + "sampleSetShapeTypeOfDataLabelsOfChart.xlsx");
```

 เส้นนี้จะสร้างสิ่งใหม่`Workbook` วัตถุและชี้ไปที่ไฟล์ที่มีอยู่ของคุณ ตรวจสอบให้แน่ใจว่าเส้นทางของไฟล์ถูกต้อง!

## ขั้นตอนที่ 3: เข้าถึงเวิร์กชีตแรก

ตอนนี้เรามีเวิร์กบุ๊กแล้ว เราต้องเข้าถึงเวิร์กชีตที่มีแผนภูมิที่คุณต้องการปรับแต่ง

```csharp
// เข้าถึงแผ่นงานแรก
Worksheet ws = wb.Worksheets[0];
```

 ที่นี่เรากำลังเข้าถึงแผ่นงานแรก (ดัชนี`0`) ปรับดัชนีถ้าแผนภูมิของคุณอยู่ในแผ่นงานอื่น

## ขั้นตอนที่ 4: เข้าถึงแผนภูมิแรก

เมื่อคุณมีเวิร์กชีตแล้ว ก็ถึงเวลาเข้าถึงแผนภูมิ เวิร์กชีตแต่ละแผ่นสามารถมีแผนภูมิได้หลายรายการ แต่เพื่อความเรียบง่าย เราจะยึดตามแผนภูมิแรกที่นี่

```csharp
// เข้าถึงแผนภูมิแรก
Chart ch = ws.Charts[0];
```

อีกครั้ง หากแผนภูมิที่คุณต้องการไม่ใช่แผนภูมิแรก เพียงเปลี่ยนดัชนีให้เหมาะสม

## ขั้นตอนที่ 5: เข้าถึงชุดแผนภูมิ

เมื่อเข้าถึงแผนภูมิได้แล้ว คุณจะต้องเจาะลึกมากขึ้นเพื่อปรับเปลี่ยนป้ายข้อมูล ชุดข้อมูลจะแสดงจุดข้อมูลในแผนภูมิของคุณ

```csharp
// เข้าถึงซีรีย์แรก
Series srs = ch.NSeries[0];
```

เรากำลังกำหนดเป้าหมายไปที่ซีรีส์แรกที่นี่ ซึ่งโดยทั่วไปจะมีป้ายกำกับที่คุณอาจต้องการปรับเปลี่ยน

## ขั้นตอนที่ 6: ตั้งค่าประเภทรูปร่างของป้ายข้อมูล

ตอนนี้มาถึงส่วนสำคัญ! มาตั้งค่าประเภทรูปร่างของป้ายข้อมูลกัน Aspose.Cells รองรับรูปร่างต่างๆ และสำหรับตัวอย่างนี้ เราจะเลือกรูปวงรีในกรอบคำพูดเพื่อเพิ่มความสนุกสนาน

```csharp
// ตั้งค่าชนิดรูปร่างของป้ายข้อมูล เช่น Speech Bubble Oval
srs.DataLabels.ShapeType = DataLabelShapeType.WedgeEllipseCallout;
```

 รู้สึกอิสระที่จะทดลองกับรูปร่างประเภทต่างๆ โดยการเปลี่ยนแปลง`DataLabelShapeType.WedgeEllipseCallout` สู่ตัวเลือกอื่นที่มีให้เลือก!

## ขั้นตอนที่ 7: บันทึกไฟล์ Excel เอาท์พุต

คุณได้ทำการยกของหนักเสร็จแล้ว และตอนนี้ถึงเวลาบันทึกงานของคุณแล้ว มาใส่รูปร่างป้ายข้อมูลที่แก้ไขแล้วกลับเข้าไปในไฟล์ Excel กัน

```csharp
// บันทึกไฟล์ Excel เอาท์พุต
wb.Save(outputDir + "outputSetShapeTypeOfDataLabelsOfChart.xlsx");
```

การกระทำนี้จะบันทึกสมุดงานที่แก้ไขแล้วในไดเร็กทอรีเอาต์พุตที่คุณระบุ

## ขั้นตอนที่ 8: ดำเนินการและยืนยัน

ในที่สุด ก็ถึงเวลาที่จะรันโปรแกรมของคุณแล้ว หลังจากรันแล้ว คุณควรเห็นข้อความยืนยันว่าทุกอย่างดำเนินไปอย่างราบรื่น!

```csharp
Console.WriteLine("SetShapeTypeOfDataLabelsOfChart executed successfully.");
```

เมื่อคุณเห็นข้อความดังกล่าว ให้ไปที่ไดเร็กทอรีเอาต์พุตเพื่อตรวจสอบไฟล์ Excel ใหม่ เปิดไฟล์และปลดปล่อยความคิดสร้างสรรค์ของคุณด้วยป้ายข้อมูลที่มีรูปร่างใหม่!

## บทสรุป

และนี่คือแนวทางง่ายๆ ในการปรับปรุงป้ายข้อมูลในแผนภูมิ Excel โดยใช้ Aspose.Cells สำหรับ .NET การปรับแต่งประเภทรูปร่างไม่เพียงแต่ทำให้แผนภูมิของคุณดูน่าสนใจยิ่งขึ้นเท่านั้น แต่ยังช่วยแสดงเรื่องราวของข้อมูลของคุณได้อย่างมีประสิทธิภาพมากขึ้นด้วย โปรดจำไว้ว่าการแสดงภาพข้อมูลนั้นเกี่ยวกับความชัดเจนและการมีส่วนร่วม ดังนั้น อย่าลังเลที่จะลองใช้รูปร่างและรูปแบบต่างๆ เพราะท้ายที่สุดแล้ว ข้อมูลของคุณสมควรได้รับการนำเสนอที่ดีที่สุด

## คำถามที่พบบ่อย

### Aspose.Cells คืออะไร?  
Aspose.Cells เป็นไลบรารี .NET อันทรงพลังที่ช่วยให้นักพัฒนาสามารถจัดการไฟล์ Excel ด้วยโปรแกรมได้

### ฉันสามารถเปลี่ยนแปลงลักษณะต่างๆ ของแผนภูมิ Excel โดยใช้ Aspose ได้หรือไม่  
แน่นอน! Aspose.Cells มีฟังก์ชันมากมายในการปรับเปลี่ยนแผนภูมิ รวมถึงชุดข้อมูล ป้ายกำกับ สไตล์ และอื่นๆ อีกมากมาย

### ฉันสามารถใช้ภาษาการเขียนโปรแกรมอะไรได้บ้างกับ Aspose.Cells?  
แม้ว่าบทความนี้จะเน้นที่ .NET แต่ Aspose.Cells ยังรองรับ Java, PHP, Python และอื่นๆ ผ่าน REST API อีกด้วย

### ฉันจำเป็นต้องจ่ายเงินสำหรับ Aspose.Cells หรือไม่?  
Aspose.Cells เป็นผลิตภัณฑ์เชิงพาณิชย์ แต่มีการทดลองใช้ฟรี ซึ่งคุณสามารถค้นหาได้[ที่นี่](https://releases.aspose.com/).

### ฉันจะได้รับความช่วยเหลือได้ที่ไหนหากประสบปัญหาเกี่ยวกับ Aspose.Cells?  
 หากคุณพบปัญหาใด ๆ[ฟอรั่มสนับสนุน](https://forum.aspose.com/c/cells/9) เป็นแหล่งข้อมูลที่ดีในการขอความช่วยเหลือจากผู้เชี่ยวชาญ