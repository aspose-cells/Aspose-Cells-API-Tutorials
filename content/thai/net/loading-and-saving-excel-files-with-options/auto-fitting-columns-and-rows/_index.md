---
title: ปรับคอลัมน์และแถวให้พอดีอัตโนมัติขณะโหลด HTML ในเวิร์กบุ๊ก
linktitle: ปรับคอลัมน์และแถวให้พอดีอัตโนมัติขณะโหลด HTML ในเวิร์กบุ๊ก
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีการปรับคอลัมน์และแถวให้พอดีโดยอัตโนมัติขณะโหลด HTML ลงใน Excel โดยใช้ Aspose.Cells สำหรับ .NET มีคู่มือทีละขั้นตอนรวมอยู่ด้วย
type: docs
weight: 10
url: /th/net/loading-and-saving-excel-files-with-options/auto-fitting-columns-and-rows/
---
## การแนะนำ
เคยสงสัยไหมว่าจะปรับขนาดคอลัมน์และแถวโดยอัตโนมัติขณะโหลดเนื้อหา HTML ลงในเวิร์กบุ๊ก Excel โดยใช้ Aspose.Cells สำหรับ .NET ได้อย่างไร? คุณมาถูกที่แล้ว! ในบทช่วยสอนนี้ เราจะเจาะลึกว่าคุณสามารถโหลดตาราง HTML ลงในเวิร์กบุ๊กได้อย่างไร และตรวจสอบให้แน่ใจว่าคอลัมน์และแถวได้รับการปรับให้พอดีโดยอัตโนมัติเพื่อให้ตรงกับเนื้อหา หากคุณทำงานกับข้อมูลแบบไดนามิกที่เปลี่ยนแปลงบ่อยครั้ง คู่มือนี้จะเป็นแนวทางของคุณในการสร้างแผ่นงาน Excel ที่มีรูปแบบที่ดีจาก HTML
### ข้อกำหนดเบื้องต้น
ก่อนที่จะเริ่มเขียนโค้ด มีบางสิ่งที่คุณจำเป็นต้องตั้งค่าในระบบของคุณ ไม่ต้องกังวล เพราะมันง่ายและตรงไปตรงมา!
1. ติดตั้ง Visual Studio: คุณจะต้องมี Visual Studio หรือสภาพแวดล้อมการพัฒนา .NET อื่น ๆ
2.  Aspose.Cells สำหรับ .NET: คุณสามารถทำได้[ดาวน์โหลดเวอร์ชั่นล่าสุด](https://releases.aspose.com/cells/net/)หรือใช้ตัวจัดการแพ็กเกจ NuGet เพื่อติดตั้ง
3. .NET Framework: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง .NET Framework 4.0 ขึ้นไป
4. ความเข้าใจพื้นฐานเกี่ยวกับ C#: การมีความรู้เกี่ยวกับ C# จะทำให้บทช่วยสอนนี้ราบรื่นยิ่งขึ้นสำหรับคุณ
5. ข้อมูลตาราง HTML: เตรียมเนื้อหา HTML บางส่วน (แม้กระทั่งตารางพื้นฐาน) ที่คุณต้องการโหลดลงใน Excel
## แพ็คเกจนำเข้า
อันดับแรก เรามาเริ่มด้วยการนำเข้าเนมสเปซที่จำเป็นกันก่อน นี่คือรายการง่ายๆ ของสิ่งที่คุณต้องนำเข้า:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.IO;
```
แพ็คเกจเหล่านี้ช่วยให้คุณจัดการเวิร์กบุ๊ก จัดการข้อมูล HTML และโหลดเข้าสู่ Excel ได้อย่างราบรื่น
มาแบ่งกระบวนการนี้ออกเป็นส่วนๆ ที่จัดการได้เพื่อให้คุณทำตามได้ง่าย เมื่อสิ้นสุดขั้นตอนนี้ คุณจะมีตัวอย่างการใช้งานของการปรับคอลัมน์และแถวให้พอดีโดยอัตโนมัติขณะโหลด HTML ลงในเวิร์กบุ๊กโดยใช้ Aspose.Cells สำหรับ .NET
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีเอกสาร
เพื่อบันทึกและเรียกค้นไฟล์ได้อย่างง่ายดาย เราจะระบุเส้นทางที่จะจัดเก็บเอกสารของคุณ คุณสามารถแทนที่เส้นทางไดเรกทอรีด้วยตำแหน่งโฟลเดอร์ของคุณเองได้
```csharp
string dataDir = "Your Document Directory";
```
บรรทัดนี้จะกำหนดไดเรกทอรีที่จะบันทึกไฟล์ Excel ของคุณ เป็นเรื่องสำคัญที่จะต้องจัดระเบียบไฟล์ของคุณอย่างเหมาะสมเมื่อทำงานกับหลายโครงการ ลองนึกภาพว่านี่คือตู้เก็บเอกสารของโครงการของคุณสิ!
## ขั้นตอนที่ 2: สร้างข้อมูล HTML เป็นสตริง
ต่อไปเราจะกำหนดเนื้อหา HTML พื้นฐาน สำหรับตัวอย่างนี้ เราจะใช้ตาราง HTML ง่ายๆ คุณสามารถปรับแต่งได้ตามความต้องการของโครงการของคุณ
```csharp
string sampleHtml = "<html><body><table><tr><td>This is sample text.</td><td>Some text.</td></tr><tr><td>This is another sample text.</td><td>Some text.</td></tr></table></body></html>";
```
เราจะกำหนดสตริง HTML พื้นฐานที่นี่ ซึ่งประกอบด้วยตารางที่มีแถวและคอลัมน์สองสามคอลัมน์ คุณสามารถเพิ่มแถวหรือคอลัมน์เพิ่มเติมได้ตามความต้องการ ลองนึกภาพว่าคุณกำลังเตรียมส่วนผสมก่อนทำอาหาร!
## ขั้นตอนที่ 3: โหลดสตริง HTML ลงใน MemoryStream
 ตอนนี้เรามีเนื้อหา HTML พร้อมแล้ว ขั้นตอนต่อไปคือการโหลดเข้าสู่หน่วยความจำโดยใช้`MemoryStream`วิธีนี้ช่วยให้เราจัดการเนื้อหา HTML ในหน่วยความจำได้โดยไม่ต้องบันทึกลงในดิสก์ก่อน
```csharp
MemoryStream ms = new MemoryStream(Encoding.UTF8.GetBytes(sampleHtml));
```
 โดยการแปลงสตริง HTML ลงในอาร์เรย์ไบต์และป้อนเข้าใน`MemoryStream`เราสามารถทำงานกับข้อมูล HTML ในหน่วยความจำได้ ลองนึกภาพขั้นตอนนี้ว่าเป็นการเตรียมอาหารในหม้อก่อนจะนำเข้าเตาอบ!
## ขั้นตอนที่ 4: โหลด MemoryStream ลงในเวิร์กบุ๊ก (โดยไม่ต้องปรับอัตโนมัติ)
 เมื่อเรามีเนื้อหา HTML ในหน่วยความจำแล้ว เราจะโหลดมันเข้าใน Aspose`Workbook`ในขณะนี้ เราไม่ได้ปรับคอลัมน์และแถวให้พอดีโดยอัตโนมัติ นี่เป็นสถานการณ์จำลอง "ก่อน" ของเรา เพื่อเปรียบเทียบกับเวอร์ชันที่ปรับให้พอดีโดยอัตโนมัติในภายหลัง
```csharp
Workbook wb = new Workbook(ms);
wb.Save(dataDir + "outputWithout_AutoFitColsAndRows.xlsx");
```
เวิร์กบุ๊กโหลดเนื้อหา HTML แล้ว แต่คอลัมน์และแถวยังไม่ปรับให้พอดีกับข้อความโดยอัตโนมัติ ลองนึกภาพว่ากำลังอบเค้กแต่ลืมตรวจสอบอุณหภูมิดู—วิธีนี้ได้ผลแต่ก็อาจไม่สมบูรณ์แบบ!
## ขั้นตอนที่ 5: ระบุตัวเลือกการโหลด HTML พร้อมเปิดใช้งานการปรับพอดีอัตโนมัติ
 ตอนนี้มาถึงจุดมหัศจรรย์แล้ว! เราสร้างอินสแตนซ์ของ`HtmlLoadOptions` และเปิดใช้งาน`AutoFitColsAndRows` คุณสมบัตินี้จะช่วยให้มั่นใจได้ว่าเมื่อโหลดเนื้อหา HTML แล้ว คอลัมน์และแถวจะปรับให้พอดีกับเนื้อหาภายใน
```csharp
HtmlLoadOptions opts = new HtmlLoadOptions();
opts.AutoFitColsAndRows = true;
```
การตั้งค่าตัวเลือกนี้จะทำให้ Aspose.Cells ปรับขนาดแถวและคอลัมน์โดยอัตโนมัติ ลองนึกภาพว่าการตั้งเตาอบให้มีอุณหภูมิที่เหมาะสมเพื่อให้เค้กขึ้นฟูพอดี!
## ขั้นตอนที่ 6: โหลด HTML ลงในเวิร์กบุ๊กโดยเปิดใช้งานการปรับอัตโนมัติ
 ตอนนี้เราโหลดเนื้อหา HTML อีกครั้ง แต่คราวนี้ด้วย`AutoFitColsAndRows` เปิดใช้งานตัวเลือกนี้แล้ว ซึ่งจะปรับความกว้างของคอลัมน์และความสูงของแถวตามเนื้อหาภายใน
```csharp
wb = new Workbook(ms, opts);
wb.Save(dataDir + "outputWith_AutoFitColsAndRows.xlsx");
```
ขั้นตอนนี้จะโหลดเนื้อหา HTML ลงในเวิร์กบุ๊กใหม่และบันทึกเป็นไฟล์ Excel แต่ตอนนี้คอลัมน์และแถวจะถูกปรับให้พอดีโดยอัตโนมัติ ลองนึกภาพว่านี่เป็นเค้กที่อบอย่างสมบูรณ์แบบ โดยที่ทุกอย่างมีขนาดที่พอเหมาะพอดี
## บทสรุป
หากทำตามขั้นตอนง่ายๆ เหล่านี้ คุณจะได้เรียนรู้วิธีโหลดเนื้อหา HTML ลงในเวิร์กบุ๊กโดยใช้ Aspose.Cells สำหรับ .NET และปรับคอลัมน์และแถวให้พอดีโดยอัตโนมัติ วิธีนี้จะช่วยให้แผ่นงาน Excel ของคุณดูเรียบร้อยอยู่เสมอ ไม่ว่าเนื้อหาจะเปลี่ยนแปลงไปอย่างไร ฟีเจอร์นี้ใช้งานง่ายแต่ทรงพลังซึ่งจะช่วยประหยัดเวลาในการจัดรูปแบบและจัดระเบียบข้อมูล Excel ของคุณได้มาก
ตอนนี้คุณได้รับความรู้เหล่านี้แล้ว คุณสามารถทดลองใช้เนื้อหา HTML ที่ซับซ้อนยิ่งขึ้น เพิ่มรูปแบบ และแม้แต่สร้างเวิร์กบุ๊ก Excel ทั้งหมดจากหน้าเว็บได้!
## คำถามที่พบบ่อย
### ฉันสามารถใช้วิธีนี้เพื่อโหลดตาราง HTML ขนาดใหญ่ได้หรือไม่
ใช่ Aspose.Cells จัดการตาราง HTML ขนาดใหญ่ได้อย่างมีประสิทธิภาพ แต่เพื่อประสิทธิภาพที่ดีที่สุด ควรทดสอบด้วยขนาดข้อมูลของคุณ
### ฉันสามารถใช้ความกว้างของคอลัมน์และความสูงของแถวที่เจาะจงได้ด้วยตนเองหลังจากการปรับอัตโนมัติหรือไม่
แน่นอน! คุณยังสามารถปรับแต่งคอลัมน์และแถวแต่ละรายการได้แม้จะใช้คุณลักษณะปรับพอดีอัตโนมัติแล้วก็ตาม
### ฉันจะกำหนดรูปแบบตารางหลังจากโหลด HTML ได้อย่างไร?
คุณสามารถใช้รูปแบบได้โดยใช้ตัวเลือกรูปแบบอันครอบคลุมของ Aspose.Cells หลังจากโหลด HTML
### Aspose.Cells สำหรับ .NET เข้ากันได้กับ .NET Framework เวอร์ชันเก่ากว่าหรือไม่
ใช่ Aspose.Cells สำหรับ .NET รองรับ .NET Framework 4.0 และรุ่นใหม่กว่า
### ฉันสามารถโหลดเนื้อหาประเภทอื่นนอกจาก HTML ลงใน Excel โดยใช้ Aspose.Cells ได้หรือไม่
ใช่ Aspose.Cells รองรับการโหลดรูปแบบต่างๆ เช่น CSV, JSON และ XML ลงใน Excel