---
title: ปรับเปลี่ยนแผนภูมิวงกลม
linktitle: ปรับเปลี่ยนแผนภูมิวงกลม
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: ปลดล็อกพลังของ Aspose.Cells สำหรับ .NET เพื่อปรับเปลี่ยนแผนภูมิวงกลม Excel ของคุณได้อย่างง่ายดาย ทำตามบทช่วยสอนนี้เพื่อดูคำแนะนำทีละขั้นตอน
type: docs
weight: 16
url: /th/net/manipulating-chart-types/modify-pie-chart/
---
## การแนะนำ

คุณเคยสงสัยไหมว่าคุณจะปรับปรุงแผนภูมิวงกลมในแผ่นงาน Excel ของคุณได้อย่างไร แผนภูมิวงกลมเป็นวิธีที่ยอดเยี่ยมในการแสดงข้อมูล ทำให้ผู้ชมของคุณมีส่วนร่วมและรับทราบข้อมูล อย่างไรก็ตาม บางครั้งแผนภูมิเหล่านั้นอาจไม่สามารถบอกเล่าเรื่องราวที่คุณต้องการได้ทันที นั่นคือจุดที่ Aspose.Cells สำหรับ .NET เข้ามามีบทบาท ไลบรารีอันทรงพลังนี้ช่วยให้คุณจัดการไฟล์ Excel ได้ด้วยโปรแกรม ช่วยให้คุณมีเครื่องมือที่จำเป็นในการปรับแต่งแผนภูมิวงกลมของคุณให้ละเอียดถี่ถ้วน ในบทช่วยสอนนี้ เราจะเจาะลึกการปรับแต่งแผนภูมิวงกลมโดยใช้ Aspose.Cells ไม่ว่าจะเป็นการเปลี่ยนป้ายข้อมูลหรือปรับแต่งรูปลักษณ์ของแผนภูมิ

## ข้อกำหนดเบื้องต้น

ก่อนที่เราจะเจาะลึกถึงรายละเอียดเล็กๆ น้อยๆ ของการปรับเปลี่ยนแผนภูมิวงกลม คุณควรมีข้อกำหนดเบื้องต้นบางประการดังต่อไปนี้:

- ความรู้พื้นฐานเกี่ยวกับ C#: ความเข้าใจพื้นฐานเกี่ยวกับการเขียนโปรแกรม C# จะช่วยให้คุณทำตามได้อย่างง่ายดาย
- Aspose.Cells สำหรับ .NET: คุณจะต้องติดตั้งไลบรารี Aspose.Cells ไม่ว่าคุณจะตัดสินใจใช้เวอร์ชันเต็มหรือเลือกทดลองใช้งานฟรี โปรดตรวจสอบให้แน่ใจว่าไลบรารีพร้อมใช้งาน
- Visual Studio หรือ IDE C# ใดๆ: คุณจะต้องมีสภาพแวดล้อมในการเขียนและดำเนินการโค้ด C# ของคุณ
-  ไฟล์ตัวอย่าง Excel: สำหรับบทช่วยสอนนี้ มีไฟล์ตัวอย่าง Excel ชื่อ`sampleModifyPieChart.xlsx` จะถูกนำมาใช้.

 คุณสามารถดาวน์โหลดไลบรารี Aspose.Cells ได้[ที่นี่](https://releases.aspose.com/cells/net/).

## แพ็คเกจนำเข้า

ขั้นตอนแรกในการเดินทางของเราคือการนำเข้าแพ็คเกจที่จำเป็นเข้าสู่โครงการ C# ของเรา ซึ่งคุณสามารถทำได้ดังนี้:

## ตั้งค่าโครงการของคุณ

ในการเริ่มต้น ให้เปิด IDE C# ของคุณ (ขอแนะนำ Visual Studio อย่างยิ่ง) และสร้างโปรเจ็กต์ใหม่:

1. เปิด Visual Studio
2. เลือก "สร้างโครงการใหม่"
3. เลือกแอปพลิเคชันคอนโซล C#
4.  ตั้งชื่อโครงการของคุณ (เช่น`ModifyPieChartDemo`-
5. คลิกสร้าง

## ติดตั้ง Aspose.Cells

เมื่อโครงการของคุณพร้อมแล้ว ก็ถึงเวลาเพิ่มไลบรารี Aspose.Cells คุณสามารถติดตั้งได้โดยใช้ NuGet:

1. ใน “Solution Explorer” ให้คลิกขวาที่โครงการของคุณ
2. เลือกจัดการแพ็คเกจ NuGet
3. ไปที่แท็บเรียกดู
4. ค้นหา Aspose.Cells
5. คลิกติดตั้งและยอมรับข้อตกลงใบอนุญาตใดๆ

ตอนนี้คุณได้ติดตั้งไลบรารีแล้ว ให้เรานำเข้าเนมสเปซที่จำเป็นลงในโค้ดของคุณ

## การนำเข้าเนมสเปซ

 ที่ด้านบนของคุณ`Program.cs` ไฟล์นำเข้าเนมสเปซต่อไปนี้:

```csharp
using System;
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
using Aspose.Cells.Charts;
```

เมื่อทำเสร็จแล้ว เราก็พร้อมที่จะไปสู่โค้ดจริงแล้ว!

## ขั้นตอนที่ 1: กำหนดไดเรกทอรีอินพุตและเอาต์พุต

เริ่มต้นด้วยการกำหนดไดเรกทอรีสำหรับไฟล์อินพุตและเอาต์พุตของคุณ นี่คือตำแหน่งที่คุณระบุตำแหน่งของไฟล์ Excel และตำแหน่งที่คุณต้องการบันทึกไฟล์ที่แก้ไข

 ในของคุณ`Main` วิธีการพิมพ์รหัสดังต่อไปนี้:

```csharp
// ไดเรกทอรีผลลัพธ์
string outputDir = "Your Output Directory Path";

// ไดเรกทอรีแหล่งที่มา
string sourceDir = "Your Document Directory Path";
```

 อย่าลืมเปลี่ยน`Your Output Directory Path` และ`Your Document Directory Path` ด้วยเส้นทางจริงบนระบบของคุณ

## ขั้นตอนที่ 2: เปิดสมุดงานที่มีอยู่

 ต่อไปเราต้องเปิดไฟล์ Excel ที่มีแผนภูมิวงกลมที่คุณต้องการแก้ไข สำหรับสิ่งนี้ ให้ใช้`Workbook` ระดับ:

```csharp
// เปิดไฟล์ที่มีอยู่
Workbook workbook = new Workbook(sourceDir + "sampleModifyPieChart.xlsx");
```

 ในสไนปเป็ตนี้ เรากำลังสร้างใหม่`Workbook` วัตถุและโหลดไฟล์ Excel ของเราลงไป

## ขั้นตอนที่ 3: เข้าถึงแผ่นงาน

ตอนนี้เรามาดูแผ่นงานที่มีแผนภูมิวงกลมกัน เราจะถือว่าแผนภูมิวงกลมนั้นอยู่ในแผ่นงานที่สอง (ดัชนี 1):

```csharp
// รับแผนภูมิของผู้ออกแบบในแผ่นงานที่สอง
Worksheet sheet = workbook.Worksheets[1];
```

 โดยการเข้าถึง`Worksheets` การรวบรวม เราสามารถรับแผ่นงานเฉพาะที่เราต้องการได้

## ขั้นตอนที่ 4: รับแผนภูมิ

ตอนนี้เราพร้อมที่จะเข้าถึงแผนภูมิแล้ว โดยสมมติว่ามีแผนภูมิเพียงแผนภูมิเดียวในเวิร์กชีตนั้น เราสามารถดึงแผนภูมินั้นได้โดยตรง:

```csharp
Aspose.Cells.Charts.Chart chart = sheet.Charts[0];
```

ที่นี่ เราจะดึงแผนภูมิแรกจากเวิร์กชีตที่ระบุ

## ขั้นตอนที่ 5: เข้าถึงป้ายข้อมูล

ตอนนี้มาถึงส่วนที่น่าตื่นเต้นแล้ว นั่นคือ การแก้ไขป้ายข้อมูลบนแผนภูมิวงกลม มาดูป้ายข้อมูลของชุดข้อมูลกัน:

```csharp
// รับป้ายข้อมูลในชุดข้อมูลของจุดข้อมูลที่สาม
Aspose.Cells.Charts.DataLabels datalabels = chart.NSeries[0].Points[2].DataLabels;
```

ด้วยบรรทัดนี้ เรากำหนดเป้าหมายป้ายข้อมูลสำหรับจุดที่สามในชุดข้อมูลของเราโดยเฉพาะ 

## ขั้นตอนที่ 6: แก้ไขข้อความในฉลาก

ต่อไปก็ถึงเวลาเปลี่ยนแปลงข้อความในฉลากแล้ว สำหรับตัวอย่างของเรา เราจะอัปเดตเป็น "สหราชอาณาจักร 400K"

```csharp
// เปลี่ยนแปลงข้อความของฉลาก
datalabels.Text = "United Kingdom, 400K";
```

เพียงเท่านี้ เราก็ได้อัปเดตฉลากแล้ว! 

## ขั้นตอนที่ 7: บันทึกสมุดงาน

ตอนนี้เราได้ทำการเปลี่ยนแปลงแล้ว มาบันทึกเวิร์กบุ๊กที่แก้ไขกัน 

```csharp
// บันทึกไฟล์ Excel
workbook.Save(outputDir + "outputModifyPieChart.xlsx");
```

บรรทัดนี้จะบันทึกเวิร์กบุ๊กไปยังไดเร็กทอรีเอาท์พุตที่ระบุ 

## ขั้นตอนที่ 8: ยืนยันการดำเนินการ

สุดท้ายนี้ ให้เราส่งข้อความยืนยันเพื่อให้แน่ใจว่าทุกอย่างทำงานได้อย่างราบรื่น:

```csharp
Console.WriteLine("ModifyPieChart executed successfully.");
```

ซึ่งจะทำให้คุณสบายใจได้บ้างว่าการเปลี่ยนแปลงของคุณเกิดขึ้นตามที่คาดหวัง

# บทสรุป

เท่านี้คุณก็แก้ไขแผนภูมิวงกลมสำเร็จแล้วด้วยขั้นตอนง่ายๆ เพียงไม่กี่ขั้นตอนโดยใช้ Aspose.Cells สำหรับ .NET ไลบรารีอันทรงพลังนี้ไม่เพียงแต่ทำให้การจัดการไฟล์ Excel ง่ายขึ้นเท่านั้น แต่ยังช่วยให้คุณปรับแต่งการแสดงภาพข้อมูลของคุณให้มีประสิทธิภาพสูงสุดอีกด้วย หากคุณกำลังจัดการการนำเสนอข้อมูลในงานของคุณ การใช้เวลาเรียนรู้วิธีใช้ Aspose.Cells จะทำให้คุณได้ประโยชน์อย่างแน่นอน ลองเล่นกับแผนภูมิเหล่านี้แล้วดูว่าคุณสามารถทำให้ข้อมูลของคุณมีชีวิตชีวาได้อย่างไร!

# คำถามที่พบบ่อย

### Aspose.Cells สำหรับ .NET คืออะไร?  
Aspose.Cells สำหรับ .NET เป็นไลบรารีอันทรงพลังที่ออกแบบมาเพื่อสร้าง จัดการ และแปลงไฟล์ Excel ด้วยโปรแกรมโดยไม่ต้องใช้ Microsoft Excel

### ฉันสามารถปรับเปลี่ยนแผนภูมิอื่น ๆ นอกเหนือจากแผนภูมิวงกลมได้ไหม?  
แน่นอน! Aspose.Cells รองรับแผนภูมิประเภทต่างๆ รวมถึงแผนภูมิแท่ง แผนภูมิเส้น และแผนภูมิพื้นที่ ช่วยให้แสดงข้อมูลได้อย่างยืดหยุ่น

### มี Aspose.Cells เวอร์ชันฟรีหรือไม่  
ใช่! Aspose นำเสนอเวอร์ชันทดลองใช้งานฟรีซึ่งช่วยให้คุณทดสอบไลบรารีได้ก่อนการซื้อ

### ฉันสามารถค้นหาการสนับสนุนสำหรับ Aspose.Cells ได้ที่ไหน  
คุณสามารถค้นหาการสนับสนุนได้ในฟอรัม Aspose ซึ่งสมาชิกชุมชนและเจ้าหน้าที่ Aspose จะสามารถช่วยเหลือคุณได้

### ฉันจำเป็นต้องติดตั้ง Microsoft Excel เพื่อใช้ Aspose.Cells หรือไม่  
ไม่ Aspose.Cells ทำงานแยกจาก Microsoft Excel คุณไม่จำเป็นต้องติดตั้งโปรแกรมนี้ในระบบของคุณ