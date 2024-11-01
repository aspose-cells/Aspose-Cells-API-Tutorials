---
title: ตั้งค่าความสูงของแถวใน Excel ด้วย Aspose.Cells
linktitle: ตั้งค่าความสูงของแถวใน Excel ด้วย Aspose.Cells
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้การตั้งค่าความสูงของแถวใน Excel ได้อย่างง่ายดายโดยใช้ Aspose.Cells สำหรับ .NET ด้วยคู่มือทีละขั้นตอนนี้
type: docs
weight: 14
url: /th/net/size-and-spacing-customization/setting-height-of-row/
---
## การแนะนำ
หากคุณเคยลองเล่นกับสเปรดชีต Excel คุณจะรู้ว่าการนำเสนอมีความสำคัญเพียงใด ไม่ว่าคุณจะกำลังเตรียมรายงานสำหรับงาน สร้างแผ่นงานงบประมาณ หรือจัดวางข้อมูลสำหรับการวิเคราะห์ ความสูงของแถวสามารถสร้างความแตกต่างอย่างมากในวิธีที่ข้อมูลของคุณถูกรับรู้ แล้วจะเป็นอย่างไรหากฉันบอกคุณว่าคุณสามารถควบคุมด้านนั้นด้วยโปรแกรมได้ ลองใช้ Aspose.Cells สำหรับ .NET ซึ่งเป็นไลบรารีที่มีประสิทธิภาพที่ให้คุณจัดการไฟล์ Excel ได้อย่างง่ายดาย ในบทช่วยสอนนี้ เราจะมาสำรวจวิธีการตั้งค่าความสูงของแถวในแผ่นงาน Excel โดยใช้ Aspose.Cells
เอาล่ะ มาเริ่มกันเลยดีกว่า?
## ข้อกำหนดเบื้องต้น
ก่อนที่จะเข้าสู่ขั้นตอนการเขียนโปรแกรม สิ่งสำคัญคือต้องแน่ใจว่าทุกอย่างพร้อมแล้ว 
1. ติดตั้ง .NET Framework: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง .NET Framework ไว้ในเครื่องของคุณแล้ว หากคุณใช้ Visual Studio การดำเนินการนี้ก็น่าจะง่ายดาย
2.  Aspose.Cells สำหรับ .NET: คุณจะต้องดาวน์โหลดและติดตั้ง Aspose.Cells สำหรับ .NET คุณสามารถค้นหาแพ็คเกจได้[ที่นี่](https://releases.aspose.com/cells/net/).
3. IDE: คุณจะต้องมี Integrated Development Environment (IDE) เพื่อเขียนโค้ดของคุณ Visual Studio เป็นตัวเลือกที่ดีหากคุณทำงานในสภาพแวดล้อม Windows
4. ความรู้พื้นฐานเกี่ยวกับ C#: แม้ว่าฉันจะแนะนำคุณในแต่ละขั้นตอน แต่การเข้าใจ C# ขั้นพื้นฐานจะทำให้สิ่งต่างๆ ชัดเจนยิ่งขึ้น
ตอนนี้คุณได้จัดเตรียมข้อกำหนดเบื้องต้นเรียบร้อยแล้ว มาเริ่มเขียนโค้ดกันเลย!
## แพ็คเกจนำเข้า
ก่อนที่เราจะทำอะไรได้ เราต้องนำเข้าแพ็คเกจที่ทำให้ Aspose.Cells ทำงานได้ วิธีดำเนินการมีดังนี้:
### สร้างโครงการใหม่
เปิด Visual Studio และสร้างโปรเจ็กต์ C# ใหม่ เลือกแอปพลิเคชันคอนโซลเพื่อความเรียบง่าย 
### ติดตั้ง Aspose.Cells ผ่าน NuGet
 ในโครงการของคุณ ไปที่`Tools` -`NuGet Package Manager` -`Manage NuGet Packages for Solution`ค้นหา Aspose.Cells และกดติดตั้ง เท่านี้คุณก็สามารถเข้าถึงคุณสมบัติพิเศษทั้งหมดที่ Aspose.Cells มอบให้ได้
### เพิ่มการใช้คำสั่ง
 ที่ด้านบนของคุณ`Program.cs`ไฟล์ คุณต้องรวมสิ่งต่อไปนี้โดยใช้คำสั่ง:
```csharp
using System.IO;
using Aspose.Cells;
```
เมื่อตั้งค่าเสร็จแล้ว เรามาแบ่งโค้ดออกเป็นขั้นตอนที่ชัดเจนและเข้าใจได้

## ขั้นตอนที่ 1: กำหนดเส้นทางไดเร็กทอรีของคุณ
สิ่งแรกที่เราต้องการคือเส้นทางสำหรับไฟล์ Excel ของเรา 
```csharp
string dataDir = "Your Document Directory";
```
 แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงบนระบบของคุณที่ไฟล์ Excel อยู่ นี่คือที่ที่โปรแกรมของเราจะค้นหาไฟล์ ตรวจสอบให้แน่ใจว่าได้รับการออกแบบอย่างสมบูรณ์แบบเหมือนแผนที่ที่นำทางเราไปสู่ขุมทรัพย์!
## ขั้นตอนที่ 2: สร้างสตรีมไฟล์
ตอนนี้เราเปิดไฟล์ Excel โดยใช้ FileStream 
```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```
 โดยใช้`FileMode.Open` แจ้งให้แอปพลิเคชันทราบว่าเราต้องการเปิดไฟล์ที่มีอยู่แล้ว เหมือนกับการบอกว่า “เฮ้ ฉันต้องการดูบางอย่างที่นี่แล้ว!”
## ขั้นตอนที่ 3: สร้างอินสแตนซ์ของวัตถุเวิร์กบุ๊ก
 ถัดไปเราจะสร้างตัวอย่าง`Workbook` วัตถุ วัตถุนี้แสดงถึงไฟล์ Excel ทั้งหมด 
```csharp
Workbook workbook = new Workbook(fstream);
```
บรรทัดนี้จะสร้างสะพานเชื่อมระหว่างโค้ดของคุณกับไฟล์ Excel 
## ขั้นตอนที่ 4: เข้าถึงแผ่นงาน
เมื่อคุณมีเวิร์กบุ๊กแล้ว คุณสามารถเข้าถึงเวิร์กชีตแต่ละแผ่นได้ ไฟล์ Excel ส่วนใหญ่จะเริ่มต้นด้วยชีตเริ่มต้น (คล้ายกับผืนผ้าใบเปล่า!) 
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
 ที่นี่,`Worksheets[0]` อ้างอิงแผ่นงานแรกในสมุดงาน 
## ขั้นตอนที่ 5: ตั้งค่าความสูงของแถว
ตอนนี้มาถึงส่วนสนุก ๆ แล้ว: การกำหนดความสูงของแถว! 
```csharp
worksheet.Cells.SetRowHeight(1, 13);
```
บรรทัดนี้บอกให้ Oracle กำหนดความสูงของแถวที่ 2 เป็น 13 พิกเซล ทำไมถึงเป็น 13 พิกเซล นั่นก็ขึ้นอยู่กับความชอบในการออกแบบของคุณเลย! เหมือนกับการเลือกขนาดฟอนต์ที่เหมาะสมสำหรับงานนำเสนอของคุณ
## ขั้นตอนที่ 6: บันทึกไฟล์ Excel ที่ปรับเปลี่ยนแล้ว
หลังจากทำการเปลี่ยนแปลงแล้ว เราจำเป็นต้องบันทึกไฟล์ คุณคงไม่อยากสูญเสียงานหนักทั้งหมดไปหรอกใช่ไหม!
```csharp
workbook.Save(dataDir + "output.out.xls");
```
บรรทัดนี้จะบันทึกไฟล์ที่คุณแก้ไขไว้ในไดเร็กทอรีเดียวกันโดยมีชื่อที่แตกต่างกัน ดังนั้นไฟล์ต้นฉบับจะยังไม่ถูกแตะต้อง เช่นเดียวกับแผนสำรอง!
## ขั้นตอนที่ 7: ปิดสตรีมไฟล์
สุดท้ายนี้ จำเป็นต้องปิดสตรีมไฟล์เพื่อปลดปล่อยทรัพยากรระบบ 
```csharp
fstream.Close();
```
วิธีนี้จะช่วยให้แน่ใจว่าทุกอย่างจะจบลงอย่างสวยงาม และไม่มีกระบวนการตกค้างอยู่เบื้องหลัง
## บทสรุป
และแล้วคุณก็ทำได้! คุณได้เขียนโปรแกรมเพื่อตั้งค่าความสูงของแถวใน Excel โดยใช้ Aspose.Cells สำหรับ .NET แล้ว ซึ่งเป็นกระบวนการตรงไปตรงมาที่เปิดโอกาสให้มีการโต้ตอบที่ซับซ้อนมากขึ้นกับไฟล์ Excel
ใครจะไปรู้ว่าการเขียนโค้ดเพียงเล็กน้อยสามารถเปลี่ยนวิธีการจัดการสเปรดชีตของคุณได้ ตอนนี้ คุณสามารถสร้างเอกสารที่สวยงามและมีโครงสร้างที่ดีได้ในเวลาไม่นาน ด้วยการใช้ Aspose.Cells คุณสามารถจัดการไม่เพียงแค่ความสูงของแถวเท่านั้น แต่ยังรวมถึงฟีเจอร์อื่นๆ อีกมากมายที่จะทำให้ข้อมูลของคุณโดดเด่น
## คำถามที่พบบ่อย
### Aspose.Cells รองรับ .NET เวอร์ชันใดบ้าง
Aspose.Cells สำหรับ .NET เข้ากันได้กับ .NET Framework หลายเวอร์ชัน รวมถึง .NET Core
### ฉันสามารถทดลองใช้ Aspose.Cells ฟรีได้หรือไม่?
 ใช่! คุณสามารถดาวน์โหลด Aspose.Cells รุ่นทดลองใช้งานฟรีได้[ที่นี่](https://releases.aspose.com/).
### Aspose.Cells สามารถจัดการรูปแบบ Excel ประเภทใดได้บ้าง
Aspose.Cells รองรับรูปแบบต่างๆ มากมาย เช่น XLSX, XLS, CSV และอื่นๆ
### Aspose.Cells เหมาะสำหรับแอพพลิเคชันด้านเซิร์ฟเวอร์หรือไม่
แน่นอน! Aspose.Cells ได้รับการออกแบบมาเพื่อจัดการกับแอปพลิเคชันที่หลากหลาย รวมถึงการประมวลผลด้านเซิร์ฟเวอร์
### ฉันสามารถหาเอกสารเพิ่มเติมได้ที่ไหน
 คุณสามารถตรวจสอบเอกสารรายละเอียดสำหรับ Aspose.Cells ได้[ที่นี่](https://reference.aspose.com/cells/net/).