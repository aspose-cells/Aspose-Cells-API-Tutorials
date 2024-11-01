---
title: การจัดกลุ่มแถวและคอลัมน์ใน Excel ด้วย Aspose.Cells
linktitle: การจัดกลุ่มแถวและคอลัมน์ใน Excel ด้วย Aspose.Cells
second_title: API การประมวลผล Excel ของ Aspose.Cells .NET
description: เรียนรู้วิธีการจัดกลุ่มแถวและคอลัมน์ใน Excel โดยใช้ Aspose.Cells สำหรับ .NET ด้วยคู่มือทีละขั้นตอนนี้
type: docs
weight: 12
url: /th/net/row-and-column-management/grouping-rows-and-columns/
---
## การแนะนำ
หากคุณทำงานกับแผ่นงาน Excel ขนาดใหญ่ คุณคงทราบดีว่าการจัดระเบียบทุกอย่างให้ดีและเป็นมิตรต่อผู้ใช้นั้นมีความสำคัญเพียงใด การจัดกลุ่มแถวและคอลัมน์ช่วยให้คุณสร้างส่วนต่างๆ ได้ ทำให้การนำทางข้อมูลราบรื่นยิ่งขึ้น ด้วย Aspose.Cells สำหรับ .NET คุณสามารถจัดกลุ่มแถวและคอลัมน์ใน Excel ได้อย่างง่ายดายตามโปรแกรม ทำให้คุณควบคุมเค้าโครงของไฟล์ได้อย่างเต็มที่
ในบทช่วยสอนนี้ เราจะแนะนำทุกสิ่งที่คุณจำเป็นต้องรู้ในการตั้งค่า จัดกลุ่ม และซ่อนแถวและคอลัมน์ในแผ่นงาน Excel ด้วย Aspose.Cells สำหรับ .NET เมื่อจบบทช่วยสอนนี้ คุณจะสามารถจัดการไฟล์ Excel ได้อย่างมืออาชีพโดยที่ไม่ต้องเปิด Excel ขึ้นมาเองด้วยซ้ำ พร้อมที่จะเริ่มใช้งานหรือยัง
## ข้อกำหนดเบื้องต้น
ก่อนที่เราจะเริ่มต้นเขียนโค้ด เรามาตรวจสอบกันก่อนว่าคุณได้ตั้งค่าทุกอย่างเรียบร้อยแล้ว:
1.  Aspose.Cells สำหรับไลบรารี .NET: คุณจะต้องมีไลบรารีนี้เพื่อทำงานกับไฟล์ Excel คุณสามารถดาวน์โหลดได้[ที่นี่](https://releases.aspose.com/cells/net/).
2. Visual Studio: บทช่วยสอนนี้ใช้ Visual Studio สำหรับตัวอย่างโค้ด
3. ความรู้พื้นฐานเกี่ยวกับ C#: ความคุ้นเคยกับ C# และ .NET จะเป็นประโยชน์
4. ใบอนุญาต Aspose: จำเป็นต้องมีใบอนุญาตแบบชำระเงินหรือชั่วคราวเพื่อหลีกเลี่ยงข้อจำกัดในการประเมิน รับใบอนุญาตชั่วคราว[ที่นี่](https://purchase.aspose.com/temporary-license/).
## แพ็คเกจนำเข้า
ในการเริ่มต้น ให้ทำการนำเข้าเนมสเปซ Aspose.Cells ที่จำเป็น พร้อมด้วยไลบรารี .NET ที่จำเป็นสำหรับการจัดการไฟล์ 
```csharp
using System.IO;
using Aspose.Cells;
```
มาแยกส่วนแต่ละส่วนของโค้ดออกเพื่อให้คุณตามและเข้าใจได้ง่ายขึ้น
## ขั้นตอนที่ 1: ตั้งค่าไดเรกทอรีข้อมูลของคุณ
ขั้นแรก เราต้องกำหนดเส้นทางไปยังไฟล์ Excel ที่จะใช้งาน โดยปกติแล้วเส้นทางนี้จะเป็นเส้นทางภายในเครื่อง แต่ก็อาจเป็นเส้นทางบนเครือข่ายก็ได้
```csharp
// เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "Your Document Directory";
```
 ที่นี่แทนที่`"Your Document Directory"` ด้วยเส้นทางจริงไปยังไฟล์ Excel ของคุณ การตั้งค่านี้จะช่วยให้โค้ดของคุณค้นหาไฟล์ที่ต้องการใช้งาน
## ขั้นตอนที่ 2: สร้างสตรีมไฟล์เพื่อเข้าถึงไฟล์ Excel
Aspose.Cells ต้องการให้คุณเปิดไฟล์ผ่านสตรีมไฟล์ สตรีมนี้จะอ่านและโหลดเนื้อหาของไฟล์เพื่อประมวลผล
```csharp
// การสร้างสตรีมไฟล์ที่มีไฟล์ Excel ที่จะเปิด
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```
 โค้ดด้านบนจะเปิดขึ้นมา`book1.xls` จากไดเร็กทอรีที่คุณระบุ หากไม่มีไฟล์ โปรดสร้างใหม่หรือเปลี่ยนชื่อไฟล์
## ขั้นตอนที่ 3: โหลดเวิร์กบุ๊กด้วย Aspose.Cells
ตอนนี้เรามาเริ่มต้นเวิร์กบุ๊กผ่าน Aspose.Cells กัน ขั้นตอนนี้ทำให้เราเข้าถึงไฟล์ Excel ได้ ทำให้จัดการได้ง่าย
```csharp
// การเปิดไฟล์ Excel ผ่านทางสตรีมไฟล์
Workbook workbook = new Workbook(fstream);
```
 หลังจากบรรทัดนี้แล้ว`workbook` วัตถุจะประกอบด้วยข้อมูลและโครงสร้างทั้งหมดจากไฟล์ Excel ของคุณ ลองนึกภาพว่าคุณกำลังโหลดสเปรดชีตทั้งหมดลงในหน่วยความจำ
## ขั้นตอนที่ 4: เข้าถึงแผ่นงานที่คุณต้องการแก้ไข
Aspose.Cells จะจัดเก็บเวิร์กชีตแต่ละแผ่นในเวิร์กบุ๊กเป็นอ็อบเจ็กต์แยกกัน ในที่นี้ เราจะเลือกเวิร์กชีตแรก
```csharp
// การเข้าถึงเวิร์กชีตแรกในไฟล์ Excel
Worksheet worksheet = workbook.Worksheets[0];
```
หากคุณต้องการเวิร์กชีตเฉพาะ คุณสามารถปรับเปลี่ยนบรรทัดนี้เพื่อเข้าถึงตามชื่อหรือดัชนีได้
## ขั้นตอนที่ 5: จัดกลุ่มแถวในเวิร์กชีต
ตอนนี้ถึงเวลาสำหรับส่วนสนุก ๆ แล้ว—การจัดกลุ่มแถว! มาจัดกลุ่มแถวแรกหกแถวและซ่อนไว้กัน
```csharp
// การจัดกลุ่มหกแถวแรก (ตั้งแต่ 0 ถึง 5) และซ่อนไว้โดยส่งผ่านค่า true
worksheet.Cells.GroupRows(0, 5, true);
```
นี่คือสิ่งที่แต่ละพารามิเตอร์ทำ:
- 0, 5: ดัชนีเริ่มต้นและสิ้นสุดสำหรับแถวที่คุณต้องการจัดกลุ่ม ใน Excel ดัชนีแถวจะเริ่มต้นที่ 0
- จริง: การตั้งค่านี้เป็นจริงจะซ่อนแถวที่ถูกจัดกลุ่ม
เมื่อดำเนินการแล้ว แถวตั้งแต่ 0 ถึง 5 จะถูกจัดกลุ่มและซ่อนจากมุมมอง
## ขั้นตอนที่ 6: การจัดกลุ่มคอลัมน์ในเวิร์กชีต
เช่นเดียวกับแถว คุณสามารถจัดกลุ่มคอลัมน์เพื่อสร้างเค้าโครงที่สะอาดตาและเป็นระเบียบมากขึ้น ต่อไปนี้เป็นวิธีการจัดกลุ่มสามคอลัมน์แรก
```csharp
// การจัดกลุ่มสามคอลัมน์แรก (ตั้งแต่ 0 ถึง 2) และซ่อนไว้โดยส่งค่า true
worksheet.Cells.GroupColumns(0, 2, true);
```
พารามิเตอร์สำหรับฟังก์ชั่นนี้คือ:
- 0, 2: ช่วงของคอลัมน์ที่จะจัดกลุ่ม โดยที่การสร้างดัชนีเริ่มที่ 0
- จริง: พารามิเตอร์นี้จะซ่อนคอลัมน์ที่ถูกจัดกลุ่ม
คอลัมน์ที่คุณเลือก (0 ถึง 2) จะปรากฏเป็นกลุ่มและซ่อนอยู่ในไฟล์ Excel
## ขั้นตอนที่ 7: บันทึกไฟล์ Excel ที่ปรับเปลี่ยนแล้ว
หลังจากทำการเปลี่ยนแปลงแล้ว ให้เราบันทึกไฟล์ด้วยชื่อใหม่เพื่อหลีกเลี่ยงการเขียนทับไฟล์ต้นฉบับ
```csharp
// การบันทึกไฟล์ Excel ที่แก้ไขแล้ว
workbook.Save(dataDir + "output.xls");
```
 ตอนนี้คุณได้บันทึกแถวและคอลัมน์ที่จัดกลุ่มไว้เรียบร้อยแล้ว`output.xls`คุณสามารถปรับเปลี่ยนชื่อไฟล์ได้ตามต้องการ
## ขั้นตอนที่ 8: ปิดสตรีมไฟล์ไปยังทรัพยากรฟรี
สุดท้าย ให้ปิดสตรีมไฟล์เพื่อปล่อยทรัพยากรใดๆ หากไม่ทำเช่นนี้ อาจทำให้เกิดปัญหาได้หากคุณจำเป็นต้องเข้าถึงหรือแก้ไขไฟล์อีกครั้ง
```csharp
// การปิดสตรีมไฟล์เพื่อปลดปล่อยทรัพยากรทั้งหมด
fstream.Close();
```
เพียงเท่านี้ คุณก็จัดกลุ่มแถวและคอลัมน์ในไฟล์ Excel ได้แล้วโดยใช้ Aspose.Cells สำหรับ .NET
## บทสรุป
การจัดกลุ่มแถวและคอลัมน์ใน Excel ด้วย Aspose.Cells สำหรับ .NET เป็นกระบวนการที่ตรงไปตรงมาซึ่งจะทำให้สเปรดชีตของคุณเป็นมิตรต่อผู้ใช้และเป็นระเบียบมากขึ้น ด้วยโค้ดเพียงไม่กี่บรรทัด คุณก็เรียนรู้ฟีเจอร์อันทรงพลังที่ต้องใช้ขั้นตอนมากขึ้นหากทำด้วยตนเองใน Excel นอกจากนี้ คุณยังสามารถทำให้กระบวนการนี้เป็นแบบอัตโนมัติกับไฟล์ต่างๆ ได้มากมาย ช่วยประหยัดเวลาและลดข้อผิดพลาด คู่มือนี้จะแสดงขั้นตอนทั้งหมดที่คุณต้องใช้เพื่อควบคุมไฟล์ Excel ของคุณโดยใช้โปรแกรม
## คำถามที่พบบ่อย
### ฉันสามารถจัดกลุ่มแถวและคอลัมน์โดยไม่ต้องซ่อนได้หรือไม่  
 ใช่ครับ เพียงผ่าน`false` เป็นพารามิเตอร์ที่สามใน`GroupRows` หรือ`GroupColumns` วิธี.
### หากฉันต้องการยกเลิกการจัดกลุ่มแถวหรือคอลัมน์จะทำอย่างไร  
 ใช้`worksheet.Cells.UngroupRows(startRow, endRow)` หรือ`worksheet.Cells.UngroupColumns(startColumn, endColumn)` เพื่อยกเลิกการจัดกลุ่มพวกเขา
### ฉันสามารถจัดกลุ่มช่วงต่างๆ หลายช่วงภายในเวิร์กชีตเดียวกันได้หรือไม่  
 แน่นอนครับ โทรหา`GroupRows` หรือ`GroupColumns`วิธีการในแต่ละช่วงที่คุณต้องการจัดกลุ่ม
### ฉันต้องมีใบอนุญาตเพื่อใช้ Aspose.Cells สำหรับ .NET หรือไม่?  
 ใช่ แม้ว่าจะมีเวอร์ชันทดลองใช้งาน แต่คุณจะต้องมีใบอนุญาตเพื่อปลดล็อกฟังก์ชันทั้งหมด คุณสามารถรับใบอนุญาตชั่วคราวได้[ที่นี่](https://purchase.aspose.com/temporary-license/).
### ฉันสามารถจัดกลุ่มแถวและคอลัมน์ด้วยตรรกะเงื่อนไขได้หรือไม่  
ใช่! คุณสามารถสร้างการจัดกลุ่มแบบมีเงื่อนไขได้โดยการผสานตรรกะเข้ากับโค้ดของคุณก่อนการจัดกลุ่ม โดยขึ้นอยู่กับข้อมูลในแต่ละแถวหรือคอลัมน์