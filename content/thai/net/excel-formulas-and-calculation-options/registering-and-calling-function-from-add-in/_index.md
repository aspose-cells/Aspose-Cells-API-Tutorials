---
title: การลงทะเบียนและการเรียกใช้ฟังก์ชันจาก Add-In ใน Excel
linktitle: การลงทะเบียนและการเรียกใช้ฟังก์ชันจาก Add-In ใน Excel
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: ค้นพบวิธีการลงทะเบียนและเรียกใช้ฟังก์ชันจากส่วนเสริมใน Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยบทช่วยสอนทีละขั้นตอนง่ายๆ ของเรา
type: docs
weight: 20
url: /th/net/excel-formulas-and-calculation-options/registering-and-calling-function-from-add-in/
---
## การแนะนำ
คุณต้องการปรับปรุงประสบการณ์ใช้งาน Excel ของคุณโดยเรียกใช้ฟังก์ชันจาก Add-in หรือไม่ ถ้าใช่ คุณมาถูกที่แล้ว! Add-in ของ Excel เปรียบเสมือนแม่ทูนหัวของสเปรดชีต พวกมันขยายฟังก์ชันการทำงานอย่างน่าอัศจรรย์ ช่วยให้คุณมีเครื่องมือใหม่ๆ มากมายอยู่ในมือ และด้วย Aspose.Cells สำหรับ .NET ทำให้การลงทะเบียนและใช้ฟังก์ชัน Add-in เหล่านี้ง่ายกว่าที่เคย 
ในคู่มือนี้ ฉันจะแนะนำคุณเกี่ยวกับขั้นตอนการลงทะเบียนและเรียกใช้ฟังก์ชันจากโปรแกรมเสริมของ Excel โดยใช้ Aspose.Cells สำหรับ .NET เราจะอธิบายทุกอย่างทีละขั้นตอนเพื่อให้คุณรู้สึกเหมือนเป็นผู้เชี่ยวชาญในเวลาไม่นาน!
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเจาะลึกเรื่องการเขียนโค้ด มาดูสิ่งที่คุณต้องมีกันก่อน:
1. Visual Studio: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Visual Studio ไว้ในเครื่องของคุณแล้ว นี่คือที่ที่เราจะเขียนและรันโค้ดของเรา
2.  ไลบรารี Aspose.Cells: คุณจะต้องติดตั้งไลบรารี Aspose.Cells คุณสามารถดาวน์โหลดจาก[หน้าดาวน์โหลด](https://releases.aspose.com/cells/net/).
3. ความรู้พื้นฐานเกี่ยวกับ C#: ความเข้าใจ C# เพียงเล็กน้อยก็จะเป็นประโยชน์และช่วยให้คุณสามารถติดตามได้อย่างราบรื่น
4.  Add-Ins ของ Excel: คุณควรมีไฟล์ Add-in (เช่น`.xlam`) ที่มีฟังก์ชั่นที่คุณต้องการลงทะเบียนและใช้งาน
5.  ตัวอย่าง Add-In ของ Excel: สำหรับบทช่วยสอนนี้ เราจะใช้ Add-In ของ Excel ชื่อ`TESTUDF.xlam`ดังนั้นให้แน่ใจว่าคุณมีสิ่งนี้ไว้ใช้งาน!
ตอนนี้คุณก็ตั้งค่าทุกอย่างเรียบร้อยแล้ว มาเริ่มเขียนโค้ดกันเลย!
## การนำเข้าแพ็คเกจ
ในการเริ่มต้น คุณจะต้องนำเข้าเนมสเปซที่จำเป็นบางส่วนไว้ที่ด้านบนของไฟล์ C# นี่คือสิ่งที่คุณต้องรวมไว้:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
เนมสเปซเหล่านี้จะช่วยให้คุณสามารถเข้าถึงคลาสและวิธีการที่เราจะใช้ในบทช่วยสอนนี้
มาแบ่งขั้นตอนเหล่านี้ออกเป็นขั้นตอนที่จัดการได้ เมื่ออ่านคู่มือนี้จบ คุณจะเข้าใจอย่างถ่องแท้ว่าต้องลงทะเบียนฟังก์ชัน Add-in และใช้งานฟังก์ชันเหล่านี้ในเวิร์กบุ๊ก Excel อย่างไร
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีต้นทางและปลายทาง
ก่อนที่คุณจะลงทะเบียน Add-in ของคุณได้ คุณต้องกำหนดก่อนว่า Add-in และไฟล์เอาท์พุตของคุณจะอยู่ที่ใด
```csharp
// ไดเรกทอรีแหล่งที่มา
string sourceDir = "Your Document Directory";
// ไดเรกทอรีผลลัพธ์
string outputDir = "Your Document Directory";
```
 แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงที่คุณ`.xlam` ไฟล์และไฟล์เอาต์พุตจะถูกบันทึกไว้ ซึ่งก็เหมือนกับการเตรียมฉากก่อนการแสดงจะเริ่มต้น
## ขั้นตอนที่ 2: สร้างสมุดงานว่างเปล่า
ต่อไปคุณจะต้องการสร้างเวิร์กบุ๊กเปล่าซึ่งเราสามารถทดลองใช้ฟังก์ชันเพิ่มเติมได้
```csharp
// สร้างสมุดงานเปล่า
Workbook workbook = new Workbook();
```
โค้ดบรรทัดนี้จะสร้างเวิร์กบุ๊กใหม่ที่จะทำหน้าที่เป็นสนามเด็กเล่นของเรา ลองนึกถึงมันว่าเป็นผืนผ้าใบใหม่ที่พร้อมให้คุณสร้างสรรค์ผลงาน
## ขั้นตอนที่ 3: ลงทะเบียนฟังก์ชัน Add-In
ตอนนี้เรามาเริ่มที่หัวใจของเรื่องนี้กันเลย ถึงเวลาลงทะเบียนฟังก์ชัน Add-in ของคุณแล้ว วิธีดำเนินการมีดังนี้:
```csharp
// ลงทะเบียน Add-in ที่เปิดใช้งานแมโครพร้อมกับชื่อฟังก์ชัน
int id = workbook.Worksheets.RegisterAddInFunction(sourceDir + @"TESTUDF.xlam", "TEST_UDF", false);
```
 บรรทัดนี้จะลงทะเบียนฟังก์ชัน Add-in ที่ชื่อ`TEST_UDF` พบใน`TESTUDF.xlam` ไฟล์เสริม`false`พารามิเตอร์หมายถึง Add-in ไม่ได้โหลดในโหมด 'แยก' 
## ขั้นตอนที่ 4: ลงทะเบียนฟังก์ชั่นเพิ่มเติม (ถ้ามี)
หากคุณมีฟังก์ชันอื่นๆ ที่ลงทะเบียนไว้ในไฟล์ Add-in เดียวกัน คุณสามารถลงทะเบียนฟังก์ชันเหล่านั้นได้เช่นกัน!
```csharp
// ลงทะเบียนฟังก์ชั่นเพิ่มเติมในไฟล์ (ถ้ามี)
workbook.Worksheets.RegisterAddInFunction(id, "TEST_UDF1");
```
ที่นี่ คุณจะเห็นได้ว่าการเพิ่มฟังก์ชันต่างๆ จาก Add-in เดียวกันนั้นง่ายเพียงใด เพียงแค่วางซ้อนกันเหมือนบล็อกตัวต่อ!
## ขั้นตอนที่ 5: เข้าถึงแผ่นงาน
ต่อไปเรามาเข้าถึงเวิร์กชีตที่เราจะใช้ฟังก์ชันของเรากัน 
```csharp
// เข้าถึงแผ่นงานแรก
Worksheet worksheet = workbook.Worksheets[0];
```
เรากำลังเข้าถึงเวิร์กชีตแรกในเวิร์กบุ๊กเพื่อวางสูตรของเรา มันเหมือนกับการเปิดประตูสู่ห้องที่ความสนุกสนานเกิดขึ้น
## ขั้นตอนที่ 6: เข้าถึงเซลล์เฉพาะ
ถัดไปเราต้องเลือกเซลล์ที่เราต้องการใช้สำหรับสูตรของเรา 
```csharp
// เข้าถึงเซลล์แรก
var cell = worksheet.Cells["A1"];
```
ที่นี่เราชี้ไปที่เซลล์ A1 นี่คือจุดที่เราจะละทิ้งสูตรวิเศษของเรา คุณอาจคิดว่ามันเป็นการปักหมุดเป้าหมายไว้บนแผนที่ขุมทรัพย์ของคุณ!
## ขั้นตอนที่ 7: ตั้งค่าสูตร
ตอนนี้ถึงเวลาเปิดตัวครั้งยิ่งใหญ่แล้ว มากำหนดสูตรที่เรียกใช้ฟังก์ชันที่ลงทะเบียนไว้กัน
```csharp
// ตั้งชื่อสูตรที่มีอยู่ใน Add-in
cell.Formula = "=TEST_UDF()";
```
ด้วยบรรทัดนี้ เรากำลังบอกให้ Excel ใช้ฟังก์ชันของเราภายในเซลล์ A1 เหมือนกับการให้คำสั่ง Excel แล้วบอกว่า "เฮ้ ทำแบบนี้สิ!"
## ขั้นตอนที่ 8: บันทึกสมุดงาน
สุดท้ายแต่ไม่ท้ายสุด ก็ถึงเวลาที่จะกอบกู้ผลงานชิ้นเอกของเรา
```csharp
// บันทึกสมุดงานเป็นเอาท์พุตรูปแบบ XLSX
workbook.Save(outputDir + @"test_udf.xlsx", Aspose.Cells.SaveFormat.Xlsx);
```
ที่นี่ เรากำลังบันทึกสมุดงานของเราเป็นไฟล์ XLSX ขั้นตอนสุดท้ายนี้เหมือนกับการใส่ภาพวาดของคุณไว้ในกรอบและเตรียมพร้อมที่จะจัดแสดง!
## ขั้นตอนที่ 9: ยืนยันการดำเนินการ
สุดท้ายเรามาสรุปทั้งหมดนี้โดยการพิมพ์ข้อความแสดงความสำเร็จไปยังคอนโซล
```csharp
Console.WriteLine("RegisterAndCallFuncFromAddIn executed successfully.");
```
เส้นนี้เปรียบเสมือนธงแห่งชัยชนะของเรา เป็นสิ่งเล็กๆ น้อยๆ ที่ช่วยยืนยันว่าทุกอย่างดำเนินไปอย่างราบรื่น
## บทสรุป 
และแล้วคุณก็จะได้มัน! คุณไม่เพียงแต่เรียนรู้วิธีการลงทะเบียนและเรียกใช้ฟังก์ชันจากโปรแกรมเสริมของ Excel โดยใช้ Aspose.Cells สำหรับ .NET เท่านั้น แต่คุณยังได้รับความเข้าใจที่ลึกซึ้งยิ่งขึ้นในแต่ละขั้นตอนที่เกี่ยวข้องอีกด้วย ชีวิตง่ายขึ้นเล็กน้อยแล้วใช่ไหม? ทำไมไม่ลองด้วยตัวคุณเองล่ะ? เจาะลึกลงไปในโปรแกรมเสริมของ Excel เหล่านั้นและยกระดับการโต้ตอบและการใช้งานให้กับสเปรดชีตของคุณ
## คำถามที่พบบ่อย
### Add-In ของ Excel คืออะไร?  
Add-In ของ Excel คือโปรแกรมที่เพิ่มคุณลักษณะ ฟังก์ชัน หรือคำสั่งที่กำหนดเองให้กับ Excel ช่วยให้ผู้ใช้สามารถขยายความสามารถได้
### ฉันสามารถใช้ Aspose.Cells ได้โดยไม่ต้องติดตั้งในเครื่องหรือไม่?  
ไม่ คุณต้องติดตั้งไลบรารี Aspose.Cells เพื่อใช้ในแอพพลิเคชั่น .NET ของคุณ
### ฉันจะได้รับใบอนุญาตชั่วคราวสำหรับ Aspose.Cells ได้อย่างไร  
 คุณสามารถเยี่ยมชมพวกเขาได้[หน้าใบอนุญาตชั่วคราว](https://purchase.aspose.com/temporary-license/) สำหรับข้อมูลเพิ่มเติม
### สามารถเรียกหลายฟังก์ชันจาก Add-in เดียวได้หรือไม่  
 ใช่! คุณสามารถลงทะเบียนฟังก์ชันต่างๆ มากมายจากไฟล์ Add-in เดียวกันได้โดยใช้`RegisterAddInFunction` วิธี.
### ฉันสามารถหาเอกสารเพิ่มเติมเกี่ยวกับ Aspose.Cells ได้จากที่ใด  
 คุณสามารถสำรวจเอกสารประกอบที่ครอบคลุมของพวกเขาได้บนเว็บไซต์[ที่นี่](https://reference.aspose.com/cells/net/).