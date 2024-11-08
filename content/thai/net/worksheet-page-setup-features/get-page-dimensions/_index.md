---
title: รับขนาดหน้าของเวิร์กชีต
linktitle: รับขนาดหน้าของเวิร์กชีต
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีการรับขนาดหน้ากระดาษในเวิร์กชีต Excel ด้วย Aspose.Cells สำหรับ .NET คำแนะนำทีละขั้นตอนในการปรับแต่งขนาดกระดาษ A2, A3, A4 และ Letter
type: docs
weight: 13
url: /th/net/worksheet-page-setup-features/get-page-dimensions/
---
## การแนะนำ
หากคุณกำลังทำงานกับไฟล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET ในการเขียนโปรแกรม อาจมีบางครั้งที่คุณต้องเข้าถึงและตั้งค่าขนาดหน้าของเวิร์กชีต การทราบขนาดจะช่วยให้สามารถจัดเค้าโครง การพิมพ์ และปรับแต่งแผ่นงาน Excel เพื่อวัตถุประสงค์เฉพาะได้ ในบทความนี้ เราจะมาสำรวจวิธีการเรียกค้นและแสดงขนาดหน้าต่างๆ ใน Excel โดยใช้ Aspose.Cells สำหรับ .NET เราจะอธิบายแบบทีละขั้นตอนเพื่อให้แน่ใจว่าคุณมีรายละเอียดทั้งหมดเพื่อเริ่มต้นใช้งานอย่างมั่นใจ
## ข้อกำหนดเบื้องต้น
ก่อนจะเริ่มดำเนินการ ให้แน่ใจว่าคุณมีทุกสิ่งที่จำเป็นในการปฏิบัติตามบทช่วยสอนนี้
1.  Aspose.Cells สำหรับ .NET: ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET แล้ว คุณสามารถ[ดาวน์โหลดห้องสมุดได้ที่นี่](https://releases.aspose.com/cells/net/) หรือติดตั้งผ่าน NuGet ในโครงการ .NET ของคุณ
2. สภาพแวดล้อม .NET: สภาพแวดล้อมการพัฒนา .NET ที่เข้ากันได้ (เช่น Visual Studio)
3.  การตั้งค่าใบอนุญาต: สำหรับฟังก์ชันการทำงานเต็มรูปแบบของ Aspose.Cells ให้ใช้ใบอนุญาต คุณสามารถ[ขอใบอนุญาตชั่วคราวฟรี](https://purchase.aspose.com/temporary-license/) เพื่อวัตถุประสงค์ในการประเมินผล
เริ่มต้นด้วยเวอร์ชันทดลองใช้งานฟรีของ Aspose.Cells หากคุณกำลังประเมินเป็นครั้งแรก
## แพ็คเกจนำเข้า
ก่อนที่จะเริ่มเขียนโค้ด คุณจะต้องนำเข้าเนมสเปซ Aspose.Cells เข้าสู่โปรเจ็กต์ของคุณเพื่อเข้าถึงคลาสและวิธีการที่จำเป็นทั้งหมด
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
มาแบ่งขั้นตอนออกเป็นขั้นตอนง่ายๆ กัน ในที่นี้ เราจะเข้าถึงขนาดกระดาษต่างๆ นำไปใช้กับเวิร์กชีต และพิมพ์ขนาดของกระดาษแต่ละขนาด
## ขั้นตอนที่ 1: สร้างอินสแตนซ์เวิร์กบุ๊ก
 ขั้นตอนแรกคือการสร้างอินสแตนซ์ของ`Workbook` คลาส วัตถุนี้จะทำหน้าที่เป็นเวิร์กบุ๊กหลักของเราซึ่งประกอบด้วยเวิร์กชีตที่เราสามารถจัดการได้
```csharp
Workbook book = new Workbook();
```
 คิดถึง`Workbook` เป็นคอนเทนเนอร์หลักสำหรับไฟล์ Excel ของคุณ เราจำเป็นต้องใช้เพื่อเข้าถึงและควบคุมเวิร์กชีตแต่ละรายการ
## ขั้นตอนที่ 2: เข้าถึงแผ่นงานแรก
 ต่อไปเรามาเข้าถึงเวิร์กชีตแรกในเวิร์กบุ๊กกัน ตามค่าเริ่มต้น เวิร์กบุ๊กใหม่จะมีชีตหนึ่งแผ่น ดังนั้นเราจึงสามารถอ้างอิงโดยตรงได้โดยใช้ดัชนีของ`0`.
```csharp
Worksheet sheet = book.Worksheets[0];
```
 การ`Worksheets` คอลเลกชันใน`Workbook` ช่วยให้เราเข้าถึงเวิร์กชีตแต่ละแผ่นได้โดยใช้ดัชนี ที่นี่ เราจะเลือกชีตแรกเพื่อเริ่มตั้งค่าขนาดหน้า
## ขั้นตอนที่ 3: ตั้งขนาดกระดาษเป็น A2 และแสดงขนาด
ตอนนี้เราเข้าถึงเวิร์กชีตได้แล้ว เรามาตั้งค่าขนาดกระดาษเป็น A2 กันดีกว่า การตั้งค่าขนาดกระดาษมีประโยชน์สำหรับการจัดรูปแบบหน้ากระดาษก่อนพิมพ์หรือส่งออก เมื่อเราตั้งค่าขนาดกระดาษแล้ว เราจะพิมพ์ขนาดหน้ากระดาษเป็นนิ้ว
```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```
 ที่นี่เราจะเปลี่ยน`PaperSize` ทรัพย์สินที่จะ`PaperA2` . หลังจากตั้งค่าขนาดแล้ว`PageSetup.PaperWidth` และ`PageSetup.PaperHeight` ดึงข้อมูลความกว้างและความสูงของแผ่นงานเป็นนิ้ว วิธีนี้ช่วยให้เราเห็นภาพรวมของขนาดหน้าได้อย่างรวดเร็ว
## ขั้นตอนที่ 4: ตั้งขนาดกระดาษเป็น A3 และแสดงขนาด
ทำตามขั้นตอนเดียวกันกับข้างต้น แล้วปรับขนาดหน้ากระดาษเป็นขนาด A3 การเปลี่ยนแปลงนี้มีประโยชน์สำหรับการพิมพ์ขนาดใหญ่ขึ้นเล็กน้อย หรือสำหรับใส่เนื้อหาเพิ่มเติมในหน้าเดียว
```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```
ขนาด A3 มีขนาดใหญ่เป็นสองเท่าของ A4 จึงเหมาะสำหรับใช้เขียนตารางขนาดใหญ่หรือแผนภูมิที่มีรายละเอียด การเปลี่ยนขนาดกระดาษจะช่วยให้เค้าโครงของเวิร์กชีตเหมาะสม
## ขั้นตอนที่ 5: ตั้งขนาดกระดาษเป็น A4 และแสดงขนาด
ต่อไปเรามาตั้งค่าขนาดกระดาษเป็น A4 กัน ซึ่งเป็นขนาดกระดาษที่นิยมใช้ในการพิมพ์เอกสาร เราจะแสดงขนาดที่อัปเดตในภายหลัง
```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```
หากเป้าหมายของคุณคือรูปแบบเอกสารมาตรฐาน ขนาด A4 มักจะเหมาะสมที่สุด การทราบขนาดจะช่วยในการปรับเค้าโครงเนื้อหาเพื่อหลีกเลี่ยงปัญหาการพิมพ์
## ขั้นตอนที่ 6: ตั้งค่าขนาดกระดาษเป็น Letter และแสดงขนาด
สุดท้ายนี้ เราจะกำหนดขนาดกระดาษเป็นรูปแบบ Letter ซึ่งนิยมใช้ในอเมริกาเหนือ มาพิมพ์ขนาดกันอีกครั้งเป็นครั้งสุดท้าย
```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```
ขนาด Letter ถูกใช้กันอย่างแพร่หลายสำหรับเอกสารในอเมริกาเหนือ ดังนั้น การตั้งค่าขนาดนี้จึงช่วยในการทำงานร่วมกันกับทีมงานหรือลูกค้าที่อยู่ในที่นั่น
## บทสรุป
ในบทช่วยสอนนี้ เราจะแนะนำวิธีตั้งค่าและเรียกค้นขนาดหน้ากระดาษสำหรับกระดาษขนาดต่างๆ โดยใช้ Aspose.Cells สำหรับ .NET คุณสามารถจัดรูปแบบเวิร์กชีต Excel ให้เหมาะกับความต้องการในการพิมพ์และเค้าโครงเฉพาะต่างๆ ได้ด้วยการกำหนดค่าขนาดหน้ากระดาษ เช่น A2, A3, A4 และ Letter การควบคุมขนาดหน้ากระดาษนี้มีประโยชน์อย่างยิ่งสำหรับการรายงานและการนำเสนอแบบมืออาชีพ เนื่องจากช่วยให้แน่ใจว่าเนื้อหาของคุณพอดีกับขนาดหน้ากระดาษแต่ละขนาด
## คำถามที่พบบ่อย
### ฉันจะเปลี่ยนทิศทางของหน้าใน Aspose.Cells ได้อย่างไร  
 คุณสามารถเปลี่ยนทิศทางได้โดยใช้`PageSetup.Orientation` ทรัพย์สิน โดยตั้งค่าให้เป็นอย่างใดอย่างหนึ่ง`PageOrientationType.Portrait` หรือ`PageOrientationType.Landscape`.
### ฉันสามารถตั้งค่าขนาดหน้าแบบกำหนดเองใน Aspose.Cells ได้หรือไม่  
 ใช่ คุณสามารถตั้งค่าขนาดหน้าแบบกำหนดเองได้โดยการปรับระยะขอบและตัวเลือกการปรับขนาดภายใต้`PageSetup` เพื่อการควบคุมที่มากขึ้น
### ขนาดกระดาษเริ่มต้นใน Aspose.Cells คืออะไร  
ขนาดกระดาษเริ่มต้นโดยทั่วไปคือ A4 อย่างไรก็ตาม ขนาดดังกล่าวอาจขึ้นอยู่กับการตั้งค่าในแต่ละภูมิภาคและสามารถปรับเปลี่ยนได้ตามต้องการ
### สามารถดูตัวอย่างเค้าโครงหน้าใน Aspose.Cells ได้หรือไม่  
แม้ว่า Aspose.Cells จะไม่มีการแสดงตัวอย่างแบบกราฟิก แต่คุณสามารถตั้งค่าเค้าโครงและใช้การแสดงตัวอย่างก่อนพิมพ์ใน Excel ได้โดยผ่านโปรแกรม
### ฉันจะติดตั้ง Aspose.Cells สำหรับ .NET ได้อย่างไร?  
 คุณสามารถติดตั้ง Aspose.Cells โดยใช้ตัวจัดการแพ็กเกจ NuGet ใน Visual Studio หรือดาวน์โหลด DLL จาก[หน้าดาวน์โหลด Aspose.Cells](https://releases.aspose.com/cells/net/).