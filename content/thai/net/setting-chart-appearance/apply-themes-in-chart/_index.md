---
title: นำธีมไปใช้กับแผนภูมิ
linktitle: นำธีมไปใช้กับแผนภูมิ
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีใช้ธีมกับแผนภูมิใน Excel โดยใช้ Aspose.Cells สำหรับ .NET พร้อมคำแนะนำทีละขั้นตอนที่ทำตามได้ง่ายของเรา ปรับปรุงการนำเสนอข้อมูลของคุณ
type: docs
weight: 10
url: /th/net/setting-chart-appearance/apply-themes-in-chart/
---
## การแนะนำ

การสร้างแผนภูมิที่ดึงดูดสายตาใน Excel เป็นสิ่งสำคัญสำหรับการสื่อสารข้อมูลของคุณอย่างมีประสิทธิภาพ การใช้ธีมจะช่วยเพิ่มความสวยงามให้กับแผนภูมิ ทำให้ข้อมูลไม่เพียงเข้าถึงได้ แต่ยังน่าสนใจอีกด้วย ในคู่มือนี้ เราจะมาสำรวจวิธีใช้ธีมโดยใช้ Aspose.Cells สำหรับ .NET หยิบขนมที่คุณชอบแล้วไปดำดิ่งสู่โลกแห่งความคิดสร้างสรรค์ของแผนภูมิกันเลย!

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเข้าสู่หัวข้อการเขียนโค้ด มีข้อกำหนดเบื้องต้นบางประการที่คุณต้องมี

### ซอฟต์แวร์ที่จำเป็น

1. Visual Studio: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Visual Studio ไว้ในเครื่องของคุณแล้ว ซึ่งจะช่วยให้มีสภาพแวดล้อมที่เป็นมิตรต่อการพัฒนาแอปพลิเคชัน .NET
2. .NET Framework หรือ .NET Core: ขึ้นอยู่กับความต้องการของคุณ คุณควรมีการตั้งค่า .NET Framework หรือ .NET Core เพื่อใช้งานตามโค้ดของเรา
3.  Aspose.Cells สำหรับ .NET: คุณไม่ควรพลาดสิ่งนี้! ดาวน์โหลด Aspose.Cells สำหรับ .NET เพื่อเริ่มต้น คุณสามารถค้นหา DLL ได้[ที่นี่](https://releases.aspose.com/cells/net/).
4. ความรู้พื้นฐานเกี่ยวกับ C#: แม้ว่าเราจะพาคุณอ่านโค้ดทีละขั้นตอน แต่ความคุ้นเคยพื้นฐานเกี่ยวกับ C# จะช่วยได้อย่างแน่นอน

## แพ็คเกจนำเข้า

ในการใช้งาน Aspose.Cells สำหรับ .NET ขั้นตอนแรกคือการนำเข้าแพ็คเกจที่จำเป็น ในโปรเจ็กต์ C# ของคุณ ให้รวมเนมสเปซต่อไปนี้:

```csharp
using System;
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Charts;
```

ตอนนี้เราได้ครอบคลุมข้อกำหนดเบื้องต้นแล้ว มาแยกขั้นตอนการใช้ธีมกับแผนภูมิใน Excel ทีละขั้นตอนกัน

## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอาต์พุตและแหล่งที่มา

สิ่งแรกที่เราต้องทำคือสร้างไดเรกทอรีเอาต์พุตและไดเรกทอรีต้นทาง ที่นี่คือที่ที่คุณจะโหลดไฟล์ Excel และที่ที่ไฟล์ที่แก้ไขจะถูกบันทึก

```csharp
// ไดเรกทอรีผลลัพธ์
string outputDir = "Your Output Directory";

// ไดเรกทอรีแหล่งที่มา
string sourceDir = "Your Document Directory";
```

 ที่นี่แทนที่`Your Output Directory` และ`Your Document Directory` ด้วยเส้นทางเฉพาะของคุณ การกำหนดไดเร็กทอรีเหล่านี้ให้ชัดเจนจะช่วยให้เวิร์กโฟลว์ของคุณราบรื่นและหลีกเลี่ยงความสับสนในภายหลัง

## ขั้นตอนที่ 2: สร้างตัวอย่างสมุดงาน

 ขั้นตอนต่อไปคือเปิดไฟล์ Excel ที่มีแผนภูมิที่คุณต้องการแก้ไข เราทำได้โดยสร้างอินสแตนซ์ของแผนภูมิ`Workbook` คลาสและการโหลดไฟล์ต้นฉบับของเรา

```csharp
// สร้างอินสแตนซ์ของเวิร์กบุ๊กเพื่อเปิดไฟล์ที่มีแผนภูมิ
Workbook workbook = new Workbook(sourceDir + "sampleApplyingThemesInChart.xlsx");
```

 ให้แน่ใจว่า`sampleApplyingThemesInChart.xlsx` มีอยู่ในไดเร็กทอรีต้นทางของคุณ

## ขั้นตอนที่ 3: เข้าถึงแผ่นงาน

ตอนนี้เราได้ตั้งค่าเวิร์กบุ๊กแล้ว ขั้นตอนถัดไปคือการเข้าถึงเวิร์กชีตเฉพาะที่เก็บแผนภูมิของเราไว้ 

```csharp
// รับแผ่นงานแรก
Worksheet worksheet = workbook.Worksheets[0];
```

ในกรณีนี้ เราเพียงแค่หยิบแผ่นงานแรกซึ่งเพียงพอสำหรับตัวอย่างนี้ หากคุณมีแผ่นงานหลายแผ่น คุณสามารถระบุดัชนีหรือชื่อแผ่นงานตามความต้องการของคุณได้

## ขั้นตอนที่ 4: รับแผนภูมิ

เมื่อมีแผ่นงานอยู่ในมือ เราสามารถเข้าถึงแผนภูมิที่เราตั้งใจจะออกแบบได้

```csharp
// รับแผนภูมิแรกในแผ่นงาน
Chart chart = worksheet.Charts[0];
```

เรากำลังดึงแผนภูมิแรกมาอยู่ที่นี่ หากเวิร์กชีตของคุณมีแผนภูมิหลายรายการและคุณต้องการแผนภูมิเฉพาะหนึ่งรายการ เพียงเปลี่ยนดัชนีให้เหมาะสม

## ขั้นตอนที่ 5: ใช้วัสดุอุดแบบทึบกับซีรีส์

ก่อนที่จะใช้ธีมใด ๆ เรามาตรวจสอบให้แน่ใจก่อนว่าชุดแผนภูมิของเรามีความสมบูรณ์ ต่อไปนี้คือวิธีการตั้งค่า:

```csharp
// ระบุชนิดของ FillFormat ให้เป็น Solid Fill ของซีรีส์แรก
chart.NSeries[0].Area.FillFormat.FillType = Aspose.Cells.Drawing.FillType.Solid;
```

บรรทัดโค้ดนี้จะช่วยให้แน่ใจว่าชุดข้อมูลแรกในแผนภูมิได้รับการตั้งค่าให้ใช้การเติมแบบทึบ

## ขั้นตอนที่ 6: กำหนดค่าสี

 ตอนนี้ซีรีส์ของเราพร้อมแล้ว เราต้องปรับเปลี่ยนสี ซึ่งเกี่ยวข้องกับการสร้าง`CellsColor` วัตถุและระบุสีธีม เราจะเลือกสไตล์เน้นสำหรับตัวอย่างนี้

```csharp
// รับ CellsColor ของ SolidFill
CellsColor cc = chart.NSeries[0].Area.FillFormat.SolidFill.CellsColor;

// สร้างธีมในสไตล์ Accent
cc.ThemeColor = new ThemeColor(ThemeColorType.Accent6, 0.6);
```

นี่คือสิ่งที่เกิดขึ้น:
1. เราจะได้สีของการเติมแบบทึบ
2.  โดยใช้`ThemeColor` เราตั้งค่าสีสำหรับการเติมแบบทึบ คุณสามารถเปลี่ยนได้`Accent6` เป็นสีธีมอื่น ๆ ได้ตามที่คุณต้องการ

## ขั้นตอนที่ 7: นำธีมไปใช้กับซีรีย์

หลังจากกำหนดค่าสีแล้ว ก็ถึงเวลาที่จะนำธีมใหม่มาใช้กับซีรี่ส์ของเรา 

```csharp
// นำธีมไปปรับใช้กับซีรีย์
chart.NSeries[0].Area.FillFormat.SolidFill.CellsColor = cc;
```

เส้นนี้จะอัพเดทสีในแผนภูมิอย่างมีประสิทธิภาพ 

## ขั้นตอนที่ 8: บันทึกสมุดงาน

หลังจากทำงานหนักมาทั้งหมดแล้ว เราจะต้องบันทึกการเปลี่ยนแปลงของเราลงในไฟล์ Excel ใหม่

```csharp
// บันทึกไฟล์ Excel
workbook.Save(outputDir + "outputApplyingThemesInChart.xlsx");
```

ที่นี่ เรากำลังบันทึกสมุดงานที่แก้ไขแล้วในไดเร็กทอรีเอาต์พุตที่คุณระบุไว้ก่อนหน้านี้ 

## ขั้นตอนที่ 9: ผลลัพธ์การยืนยัน

เพื่อให้เราทราบว่ากระบวนการได้ดำเนินการสำเร็จแล้ว เราสามารถพิมพ์ข้อความยืนยันได้:

```csharp
Console.WriteLine("ApplyingThemesInChart executed successfully.");
```

บรรทัดนี้จะแสดงข้อความในคอนโซลว่างานเสร็จสมบูรณ์แล้ว

## บทสรุป

การใช้ธีมกับแผนภูมิของคุณใน Excel โดยใช้ Aspose.Cells สำหรับ .NET จะช่วยเปลี่ยนแปลงวิธีการแสดงข้อมูลของคุณได้อย่างสิ้นเชิง ไม่เพียงแต่ทำให้แผนภูมิของคุณดูสวยงามเท่านั้น แต่ยังช่วยให้สื่อสารข้อความของคุณได้อย่างมีประสิทธิภาพมากขึ้นอีกด้วย โดยทำตามขั้นตอนที่ระบุไว้ในคู่มือนี้ คุณสามารถปรับแต่งแผนภูมิของคุณได้อย่างง่ายดาย และนำเสนอข้อมูลของคุณในลักษณะที่ดึงดูดความสนใจของผู้ชม

## คำถามที่พบบ่อย

### Aspose.Cells คืออะไร?
Aspose.Cells เป็นไลบรารีอันทรงพลังสำหรับ .NET ที่ช่วยให้นักพัฒนาสามารถจัดการไฟล์ Excel ด้วยโปรแกรมได้

### ฉันสามารถทดลองใช้ Aspose.Cells ก่อนซื้อได้หรือไม่?
 ใช่ คุณสามารถดาวน์โหลดรุ่นทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).

### ฉันสามารถใช้ธีมแผนภูมิประเภทใดได้บ้าง
Aspose.Cells รองรับสีธีมต่างๆ รวมถึงสไตล์ Accent และอื่นๆ

### เป็นไปได้ไหมที่จะนำธีมไปใช้กับแผนภูมิต่างๆ มากมาย?
 แน่นอน! คุณสามารถวนซ้ำได้`worksheet.Charts` และใช้ธีมตามที่จำเป็น

### ฉันจะได้รับการสนับสนุนสำหรับ Aspose.Cells ได้จากที่ไหน
 คุณสามารถรับการสนับสนุนและมีส่วนร่วมกับชุมชนผู้ใช้[ที่นี่](https://forum.aspose.com/c/cells/9).