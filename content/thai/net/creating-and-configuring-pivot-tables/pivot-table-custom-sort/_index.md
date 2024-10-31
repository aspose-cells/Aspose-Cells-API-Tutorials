---
title: การเรียงลำดับตารางสรุปข้อมูลแบบกำหนดเองด้วยโปรแกรมใน .NET
linktitle: การเรียงลำดับตารางสรุปข้อมูลแบบกำหนดเองด้วยโปรแกรมใน .NET
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีการเรียงลำดับตารางสรุปข้อมูลใน .NET โดยใช้ Aspose.Cells คำแนะนำทีละขั้นตอนที่ครอบคลุมถึงการตั้งค่า การกำหนดค่า การเรียงลำดับ และการบันทึกผลลัพธ์เป็นไฟล์ Excel และ PDF
type: docs
weight: 29
url: /th/net/creating-and-configuring-pivot-tables/pivot-table-custom-sort/
---
## การแนะนำ
เมื่อต้องทำงานกับ Excel ในสภาพแวดล้อม .NET ไลบรารี่หนึ่งที่โดดเด่นกว่าไลบรารี่อื่นๆ นั่นก็คือ Aspose.Cells คุณคงชอบที่เครื่องมือนี้ช่วยให้คุณจัดการสเปรดชีตด้วยโปรแกรมใช่ไหม นั่นคือสิ่งที่ Aspose.Cells ทำได้ ในบทช่วยสอนของวันนี้ เราจะเจาะลึกเข้าไปในโลกของ Pivot Table และแสดงให้คุณเห็นถึงวิธีการนำการเรียงลำดับแบบกำหนดเองไปใช้ในโปรแกรมโดยใช้ไลบรารี่เอนกประสงค์นี้
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มลงมือเขียนโค้ด โปรดตรวจสอบให้แน่ใจว่าคุณมีบางสิ่งบางอย่างพร้อมแล้ว:
1. Visual Studio: คุณต้องมี Visual Studio เวอร์ชันที่ใช้งานได้จริง ซึ่งเป็นสนามเด็กเล่นที่ทำให้เกิดความมหัศจรรย์ทั้งหมด
2. .NET Framework: ความคุ้นเคยกับการเขียนโปรแกรม .NET ถือเป็นสิ่งสำคัญ ไม่ว่าคุณจะเป็นผู้ที่ชื่นชอบ .NET Core หรือ .NET Framework คุณก็พร้อมแล้ว
3.  ไลบรารี Aspose.Cells: คุณต้องติดตั้งไลบรารี Aspose.Cells คุณสามารถรับได้จาก[ลิงค์ดาวน์โหลด](https://releases.aspose.com/cells/net/) และเพิ่มมันลงในโครงการของคุณ
4. ความเข้าใจพื้นฐานเกี่ยวกับ Pivot Table: แม้ว่าคุณไม่จำเป็นต้องเป็นผู้เชี่ยวชาญ ความรู้เพียงเล็กน้อยเกี่ยวกับวิธีการทำงานของ Pivot Table จะเป็นประโยชน์เมื่อเราทำตามบทช่วยสอนนี้
5.  ตัวอย่างไฟล์ Excel: มีไฟล์ Excel ตัวอย่างชื่อ`SamplePivotSort.xlsx` พร้อมอยู่ในไดเร็กทอรีการทำงานของคุณสำหรับการทดสอบ
## แพ็คเกจนำเข้า
เมื่อคุณจัดเตรียมข้อกำหนดเบื้องต้นทั้งหมดเรียบร้อยแล้ว ขั้นตอนแรกคือการนำเข้าแพ็คเกจที่จำเป็น โดยให้รวมบรรทัดต่อไปนี้ไว้ที่ด้านบนของโค้ดของคุณ:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells;
using Aspose.Cells.Pivot;
```
แพ็คเกจนี้ประกอบด้วยฟังก์ชันทั้งหมดที่คุณต้องการในการจัดการไฟล์ Excel โดยใช้ Aspose.Cells

เอาล่ะ มาเริ่มกันที่ส่วนสนุก ๆ กันเลย เราจะมาแบ่งกระบวนการสร้าง Pivot Table และการใช้การเรียงลำดับแบบกำหนดเองออกเป็นขั้นตอนที่สามารถจัดการได้
## ขั้นตอนที่ 1: ตั้งค่าเวิร์กบุ๊ก
ในการเริ่มต้น เราจะต้องตั้งค่าเวิร์กบุ๊กของเราก่อน โดยทำได้ดังนี้:
```csharp
string sourceDir = "Your Document Directory";
string outputDir = "Your Document Directory";
Workbook wb = new Workbook(sourceDir + "SamplePivotSort.xlsx");
```
 ในขั้นตอนนี้เราจะเริ่มต้นใหม่`Workbook` อินสแตนซ์ที่มีเส้นทางไปยังไฟล์ Excel ของเรา ซึ่งทำหน้าที่เป็นพื้นที่ที่ตารางสรุปข้อมูลของเราจะทำงานได้
## ขั้นตอนที่ 2: เข้าถึงแผ่นงาน
ต่อไปเราต้องเข้าถึงเวิร์กชีตที่เราจะเพิ่มตารางสรุปข้อมูล
```csharp
Worksheet sheet = wb.Worksheets[0];
PivotTableCollection pivotTables = sheet.PivotTables;
```
 ที่นี่ เราคว้าแผ่นงานแรกในสมุดงานของเราและเรียกใช้`PivotTableCollection`คอลเลกชันนี้ช่วยให้เราจัดการตารางสรุปข้อมูลทั้งหมดบนเวิร์กชีตนี้ได้
## ขั้นตอนที่ 3: สร้างตารางสรุปข้อมูลแรกของคุณ
ตอนนี้ถึงเวลาสร้าง Pivot Table ของเราแล้ว
```csharp
int index = pivotTables.Add("=Sheet1!A1:C10", "E3", "PivotTable1");
PivotTable pivotTable = pivotTables[index];
```
เราเพิ่ม Pivot Table ใหม่ลงในเวิร์กชีตโดยระบุช่วงข้อมูลและตำแหน่งของช่วงข้อมูล "E3" ระบุตำแหน่งที่เราต้องการให้ Pivot Table เริ่มต้น จากนั้นจึงอ้างอิง Pivot Table ใหม่นี้โดยใช้ดัชนี
## ขั้นตอนที่ 4: กำหนดค่าการตั้งค่าตารางสรุปข้อมูล
มาตั้งค่า Pivot Table ของเรากันเถอะ! ซึ่งหมายถึงการควบคุมด้านต่างๆ เช่น ยอดรวมและการจัดเรียงข้อมูลในฟิลด์
```csharp
pivotTable.RowGrand = false;
pivotTable.ColumnGrand = false;
pivotTable.AddFieldToArea(PivotFieldType.Row,1);
PivotField rowField = pivotTable.RowFields[0];
rowField.IsAutoSort = true;
rowField.IsAscendSort = true;
```
เราตรวจสอบให้แน่ใจว่าผลรวมทั้งหมดของแถวและคอลัมน์จะไม่ปรากฏ ซึ่งอาจทำให้ข้อมูลดูสะอาดขึ้น จากนั้นเราจะเพิ่มฟิลด์แรกลงในพื้นที่แถว เปิดใช้งานการเรียงลำดับอัตโนมัติและการเรียงลำดับแบบเรียงจากน้อยไปมาก
## ขั้นตอนที่ 5: เพิ่มคอลัมน์และฟิลด์ข้อมูล
เมื่อกำหนดแถวแล้ว ให้เราเพิ่มคอลัมน์และฟิลด์ข้อมูล
```csharp
pivotTable.AddFieldToArea(PivotFieldType.Column,0);
PivotField colField = pivotTable.ColumnFields[0];
colField.NumberFormat = "dd/mm/yyyy";
colField.IsAutoSort = true;
colField.IsAscendSort = true;
```
เราเพิ่มฟิลด์ที่สองเป็นคอลัมน์และจัดรูปแบบเป็นวันที่ อีกครั้ง เราเปิดใช้งานการเรียงลำดับอัตโนมัติและการเรียงลำดับจากน้อยไปมากเพื่อให้ทุกอย่างเป็นระเบียบ ในที่สุด เราต้องเพิ่มฟิลด์ที่สามลงในพื้นที่ข้อมูลของเรา:
```csharp
pivotTable.AddFieldToArea(PivotFieldType.Data,2);
```
## ขั้นตอนที่ 6: รีเฟรชและคำนวณตารางสรุปข้อมูล
หลังจากเพิ่มฟิลด์ที่จำเป็นทั้งหมดแล้ว มาตรวจสอบให้แน่ใจว่า Pivot Table ของเราสดใหม่และพร้อมใช้งาน
```csharp
pivotTable.RefreshData();
pivotTable.CalculateData();
```
วิธีการเหล่านี้จะรีเฟรชข้อมูลและคำนวณใหม่ โดยให้แน่ใจว่าทุกอย่างเป็นปัจจุบันและแสดงอย่างถูกต้องในตารางสรุปของเรา
## ขั้นตอนที่ 7: การเรียงลำดับแบบกำหนดเองตามค่าของฟิลด์แถว
มาเพิ่มความเก๋ไก๋สักหน่อยโดยการเรียงลำดับตารางสรุปข้อมูลตามค่าเฉพาะ เช่น "อาหารทะเล"
```csharp
index = pivotTables.Add("=Sheet1!A1:C10", "E10", "PivotTable2");
pivotTable = pivotTables[index];
```
เรากำลังทำซ้ำขั้นตอนโดยสร้างตารางสรุปข้อมูลอีกตารางหนึ่งและตั้งค่าให้คล้ายกับตารางแรก ตอนนี้เราสามารถปรับแต่งเพิ่มเติมได้ดังนี้:
```csharp
pivotTable.AddFieldToArea(PivotFieldType.Row,1);
rowField = pivotTable.RowFields[0];
rowField.IsAutoSort = true;
rowField.IsAscendSort = true;
```
## ขั้นตอนที่ 8: การปรับแต่งการเรียงลำดับเพิ่มเติม ลองใช้วิธีการเรียงลำดับอื่นตามวันที่ที่ระบุ:
```csharp
// การเพิ่มตารางสรุปข้อมูลอีกตารางหนึ่งสำหรับการเรียงลำดับตามวันที่
index = pivotTables.Add("=Sheet1!A1:C10", "E18", "PivotTable3");
pivotTable = pivotTables[index];
// ทำซ้ำการตั้งค่าแถวและคอลัมน์ที่คล้ายกับขั้นตอนก่อนหน้า
```
คุณเพียงแค่ทำซ้ำกระบวนการเดียวกัน โดยสร้างตารางสรุปข้อมูลที่สามที่มีเกณฑ์การเรียงลำดับที่เหมาะกับความต้องการของคุณ
## ขั้นตอนที่ 9: บันทึกสมุดงานถึงเวลาบันทึกงานหนักที่เราได้ใส่ลงไป!
```csharp
wb.Save(outputDir + "out.xlsx");
PdfSaveOptions options = new PdfSaveOptions();
options.OnePagePerSheet = true;
wb.Save(outputDir + "out.pdf", options);
```
 ที่นี่ คุณสามารถบันทึกสมุดงานเป็นไฟล์ Excel และ PDF`PdfSaveOptions` ช่วยให้จัดรูปแบบได้ดีขึ้น โดยแน่ใจว่าแต่ละแผ่นงานจะปรากฏในหน้าแยกกันเมื่อแปลง
## ขั้นตอนที่ 10: เสร็จสิ้น สรุปทุกอย่างโดยแจ้งให้ผู้ใช้ทราบว่าทุกอย่างเรียบร้อยดี
```csharp
Console.WriteLine("PivotTableCustomSort executed successfully.");
```
## บทสรุป
ตอนนี้ คุณได้เรียนรู้วิธีใช้พลังของ Aspose.Cells เพื่อสร้างและปรับแต่ง Pivot Table ในแอปพลิเคชัน .NET ของคุณแล้ว ตั้งแต่การตั้งค่าเริ่มต้นไปจนถึงการเรียงลำดับแบบกำหนดเอง แต่ละขั้นตอนจะรวมกันเพื่อมอบประสบการณ์ที่ราบรื่น ไม่ว่าคุณจะต้องนำเสนอข้อมูลยอดขายประจำปีหรือติดตามสถิติสินค้าคงคลัง ทักษะเหล่านี้จะเป็นประโยชน์กับคุณมาก!
## คำถามที่พบบ่อย
### Pivot Table คืออะไร?
Pivot Table เป็นเครื่องมือประมวลผลข้อมูลใน Excel ที่ช่วยให้คุณสรุปและวิเคราะห์ข้อมูลได้ อีกทั้งยังมีวิธีการที่ยืดหยุ่นในการดึงข้อมูลเชิงลึกได้อย่างง่ายดาย
### ฉันจะติดตั้ง Aspose.Cells ได้อย่างไร?
 คุณสามารถติดตั้งได้ผ่าน NuGet ใน Visual Studio หรือดาวน์โหลดโดยตรงจาก[ลิงค์ดาวน์โหลด](https://releases.aspose.com/cells/net/).
### มี Aspose.Cells เวอร์ชันทดลองใช้หรือไม่
 ใช่! คุณสามารถลองใช้งานฟรีได้โดยเข้าไปที่[ลิงค์ทดลองใช้ฟรี](https://releases.aspose.com/).
### ฉันสามารถเรียงลำดับฟิลด์หลายฟิลด์ในตารางสรุปข้อมูลได้หรือไม่
แน่นอน! คุณสามารถเพิ่มและเรียงลำดับฟิลด์ต่างๆ ได้ตามความต้องการของคุณ
### ฉันสามารถค้นหาการสนับสนุนสำหรับ Aspose.Cells ได้ที่ไหน
 ชุมชนมีความกระตือรือร้นมาก และคุณสามารถถามคำถามในฟอรัมของพวกเขาได้[ที่นี่](https://forum.aspose.com/c/cells/9).