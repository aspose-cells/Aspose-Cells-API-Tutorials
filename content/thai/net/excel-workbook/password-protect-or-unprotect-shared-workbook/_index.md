---
title: รหัสผ่านป้องกันหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกัน
linktitle: รหัสผ่านป้องกันหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกัน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีการป้องกันด้วยรหัสผ่านหรือเลิกป้องกันสมุดงานที่ใช้ร่วมกันโดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 120
url: /th/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
การปกป้องเวิร์กบุ๊กที่ใช้ร่วมกันด้วยรหัสผ่านเป็นสิ่งสำคัญในการรับรองความเป็นส่วนตัวของข้อมูล ด้วย Aspose.Cells สำหรับ .NET คุณสามารถป้องกันหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกันได้อย่างง่ายดายโดยใช้รหัสผ่าน ทำตามขั้นตอนด้านล่างเพื่อให้ได้ผลลัพธ์ที่ต้องการ:

## ขั้นตอนที่ 1: ระบุไดเรกทอรีผลลัพธ์

ขั้นแรก คุณต้องระบุไดเร็กทอรีเอาต์พุตที่จะบันทึกไฟล์ Excel ที่ได้รับการป้องกัน ต่อไปนี้เป็นวิธีดำเนินการโดยใช้ Aspose.Cells:

```csharp
// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

## ขั้นตอนที่ 2: สร้างไฟล์ Excel เปล่า

จากนั้นคุณสามารถสร้างไฟล์ Excel ว่างที่คุณต้องการใช้การป้องกันหรือการป้องกัน นี่คือโค้ดตัวอย่าง:

```csharp
// สร้างสมุดงาน Excel เปล่า
Workbook wb = new Workbook();
```

## ขั้นตอนที่ 3: ป้องกันหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกัน

หลังจากสร้างสมุดงานแล้ว คุณสามารถป้องกันหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกันได้โดยการระบุรหัสผ่านที่เหมาะสม มีวิธีดังนี้:

```csharp
// ป้องกันสมุดงานที่ใช้ร่วมกันด้วยรหัสผ่าน
wb.ProtectSharedWorkbook("1234");

// ยกเลิกหมายเหตุบรรทัดนี้เพื่อยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกัน
// wb.UnprotectSharedWorkbook("1234");
```

## ขั้นตอนที่ 4: บันทึกไฟล์ Excel เอาต์พุต

เมื่อคุณใช้การป้องกันหรือไม่มีการป้องกัน คุณสามารถบันทึกไฟล์ Excel ที่ได้รับการป้องกันไปยังไดเร็กทอรีเอาต์พุตที่ระบุได้ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// บันทึกไฟล์ Excel เอาต์พุต
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### ตัวอย่างซอร์สโค้ดสำหรับการป้องกันด้วยรหัสผ่านหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกันโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
//สร้างไฟล์ Excel เปล่า
Workbook wb = new Workbook();
//ป้องกันสมุดงานที่ใช้ร่วมกันด้วยรหัสผ่าน
wb.ProtectSharedWorkbook("1234");
//ยกเลิกหมายเหตุบรรทัดนี้เพื่อยกเลิกการปกป้องสมุดงานที่ใช้ร่วมกัน
//wb.UnprotectSharedWorkbook("1234");
//บันทึกไฟล์ Excel เอาต์พุต
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## บทสรุป

การป้องกันหรือยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกันด้วยรหัสผ่านถือเป็นสิ่งสำคัญเพื่อให้มั่นใจในความปลอดภัยของข้อมูล ด้วย Aspose.Cells สำหรับ .NET คุณสามารถเพิ่มฟังก์ชันนี้ลงในไฟล์ Excel ของคุณได้อย่างง่ายดาย ด้วยการทำตามขั้นตอนในคู่มือนี้ คุณสามารถป้องกันหรือยกเลิกการป้องกันเวิร์กบุ๊กที่แชร์ของคุณโดยใช้รหัสผ่านได้อย่างมีประสิทธิภาพ ทดลองกับไฟล์ Excel ของคุณเอง และอย่าลืมรักษาความปลอดภัยของข้อมูลที่ละเอียดอ่อนของคุณ

### คำถามที่พบบ่อย

#### ถาม: การป้องกันประเภทใดที่ฉันใช้กับเวิร์กบุ๊กที่แชร์กับ Aspose.Cells ได้
    
ตอบ: ด้วย Aspose.Cells คุณสามารถปกป้องสมุดงานที่ใช้ร่วมกันได้โดยการระบุรหัสผ่านเพื่อป้องกันการเข้าถึง การแก้ไข หรือการลบข้อมูลโดยไม่ได้รับอนุญาต

#### ถาม: ฉันสามารถป้องกันเวิร์กบุ๊กที่แชร์โดยไม่ต้องระบุรหัสผ่านได้หรือไม่
    
ตอบ: ได้ คุณสามารถป้องกันเวิร์กบุ๊กที่ใช้ร่วมกันได้โดยไม่ต้องระบุรหัสผ่าน อย่างไรก็ตาม ขอแนะนำให้ใช้รหัสผ่านที่รัดกุมเพื่อความปลอดภัยที่ดีขึ้น

#### ถาม: ฉันจะยกเลิกการป้องกันเวิร์กบุ๊กที่แชร์กับ Aspose.Cells ได้อย่างไร
    
ตอบ: เมื่อต้องการยกเลิกการป้องกันสมุดงานที่ใช้ร่วมกัน คุณต้องระบุรหัสผ่านเดียวกันกับที่ใช้เมื่อปกป้องสมุดงาน ซึ่งช่วยให้สามารถลบการป้องกันออกและเข้าถึงข้อมูลได้อย่างอิสระ

#### ถาม: การปกป้องเวิร์กบุ๊กที่แชร์ส่งผลต่อฟีเจอร์และสูตรในเวิร์กบุ๊กหรือไม่
    
ตอบ: เมื่อคุณป้องกันเวิร์กบุ๊กที่ใช้ร่วมกัน ผู้ใช้ยังคงสามารถเข้าถึงฟีเจอร์และสูตรที่มีอยู่ในเวิร์กบุ๊กได้ การป้องกันส่งผลต่อการเปลี่ยนแปลงโครงสร้างสมุดงานเท่านั้น