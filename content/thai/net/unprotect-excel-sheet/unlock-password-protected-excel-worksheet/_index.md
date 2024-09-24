---
title: ปลดล็อกแผ่นงาน Excel ที่ป้องกันด้วยรหัสผ่าน
linktitle: ปลดล็อกแผ่นงาน Excel ที่ป้องกันด้วยรหัสผ่าน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีปลดล็อกสเปรดชีต Excel ที่ป้องกันด้วยรหัสผ่านโดยใช้ Aspose.Cells สำหรับ .NET บทช่วยสอนทีละขั้นตอนใน C#
type: docs
weight: 10
url: /th/net/unprotect-excel-sheet/unlock-password-protected-excel-worksheet/
---
การป้องกันด้วยรหัสผ่านของสเปรดชีต Excel มักใช้เพื่อรักษาความปลอดภัยข้อมูลที่ละเอียดอ่อน ในบทช่วยสอนนี้ เราจะแนะนำคุณทีละขั้นตอนเพื่อทำความเข้าใจและใช้งานซอร์สโค้ด C# ที่ให้มาเพื่อปลดล็อกสเปรดชีต Excel ที่ป้องกันด้วยรหัสผ่านโดยใช้ไลบรารี Aspose.Cells สำหรับ .NET

## ขั้นตอนที่ 1: การเตรียมสภาพแวดล้อม

ก่อนที่คุณจะเริ่มต้น ตรวจสอบให้แน่ใจว่าคุณได้ติดตั้ง Aspose.Cells สำหรับ .NET บนเครื่องของคุณแล้ว คุณสามารถดาวน์โหลดไลบรารีได้จากเว็บไซต์อย่างเป็นทางการของ Aspose และติดตั้งโดยทำตามคำแนะนำที่ให้ไว้

เมื่อการติดตั้งเสร็จสมบูรณ์ ให้สร้างโปรเจ็กต์ C# ใหม่ในสภาพแวดล้อมการพัฒนาแบบรวม (IDE) ที่คุณต้องการ และนำเข้าไลบรารี Aspose.Cells สำหรับ .NET

## ขั้นตอนที่ 2: การกำหนดค่าเส้นทางไดเรกทอรีเอกสาร

 ในซอร์สโค้ดที่ให้มา คุณต้องระบุเส้นทางไดเร็กทอรีซึ่งมีไฟล์ Excel ที่คุณต้องการปลดล็อกอยู่ ปรับเปลี่ยน`dataDir` ตัวแปรโดยการแทนที่ "ไดเรกทอรีเอกสารของคุณ" ด้วยเส้นทางที่แน่นอนของไดเรกทอรีบนเครื่องของคุณ

```csharp
//เส้นทางไปยังไดเร็กทอรีเอกสาร
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## ขั้นตอนที่ 3: การสร้างวัตถุสมุดงาน

ในการเริ่มต้น เราต้องสร้างวัตถุสมุดงานที่แสดงถึงไฟล์ Excel ของเรา ใช้ตัวสร้างคลาสสมุดงานและระบุเส้นทางแบบเต็มของไฟล์ Excel ที่จะเปิด

```csharp
// การสร้างอินสแตนซ์วัตถุสมุดงาน
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## ขั้นตอนที่ 4: การเข้าถึงสเปรดชีต

 ต่อไปเราต้องไปที่แผ่นงานแรกในไฟล์ Excel ใช้`Worksheets` คุณสมบัติของวัตถุสมุดงานเพื่อเข้าถึงคอลเลกชันของแผ่นงานจากนั้นใช้`[0]` ดัชนีเพื่อเข้าถึงแผ่นงานแรก

```csharp
// การเข้าถึงแผ่นงานแรกในไฟล์ Excel
Worksheet worksheet = workbook.Worksheets[0];
```

## ขั้นตอนที่ 5: ปลดล็อกสเปรดชีต

 ตอนนี้เราจะปลดล็อกแผ่นงานโดยใช้`Unprotect()` วิธีการของวัตถุแผ่นงาน ปล่อยให้สตริงรหัสผ่านว่างไว้ (`""`) หากสเปรดชีตไม่มีการป้องกันด้วยรหัสผ่าน

```csharp
// ยกเลิกการป้องกันแผ่นงานด้วยรหัสผ่าน
worksheet.Unprotect("");
```

## ขั้นตอนที่ 6: บันทึกไฟล์ Excel ที่ปลดล็อค

เมื่อปลดล็อคสเปรดชีตแล้ว เราก็สามารถบันทึกไฟล์ Excel สุดท้ายได้ ใช้`Save()` วิธีการระบุเส้นทางแบบเต็มของไฟล์ที่ส่งออก

.

```csharp
// บันทึกสมุดงาน
workbook.Save(dataDir + "output.out.xls");
```

### ตัวอย่างซอร์สโค้ดสำหรับแผ่นงาน Excel ที่ป้องกันด้วยรหัสผ่านโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
try
{
    //เส้นทางไปยังไดเร็กทอรีเอกสาร
    string dataDir = "YOUR DOCUMENT DIRECTORY";
    // การสร้างอินสแตนซ์วัตถุสมุดงาน
    Workbook workbook = new Workbook(dataDir + "book1.xls");
    // การเข้าถึงแผ่นงานแรกในไฟล์ Excel
    Worksheet worksheet = workbook.Worksheets[0];
    // ยกเลิกการป้องกันแผ่นงานด้วยรหัสผ่าน
    worksheet.Unprotect("");
    // บันทึกสมุดงาน
    workbook.Save(dataDir + "output.out.xls");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## บทสรุป

ขอแสดงความยินดี! ตอนนี้ คุณได้ทราบวิธีใช้ Aspose.Cells สำหรับ .NET เพื่อปลดล็อกสเปรดชีต Excel ที่ป้องกันด้วยรหัสผ่านโดยใช้ซอร์สโค้ด C# ด้วยการทำตามขั้นตอนในบทช่วยสอนนี้ คุณจะสามารถใช้ฟังก์ชันนี้กับโปรเจ็กต์ของคุณเองและทำงานกับไฟล์ Excel ได้อย่างมีประสิทธิภาพและปลอดภัย

สำรวจคุณสมบัติเพิ่มเติมที่ Aspose.Cells นำเสนอเพิ่มเติมได้ตามสบายเพื่อการทำงานขั้นสูงยิ่งขึ้น

### คำถามที่พบบ่อย

#### ถาม: จะเกิดอะไรขึ้นหากสเปรดชีตมีการป้องกันด้วยรหัสผ่าน

 ตอบ: หากสเปรดชีตมีการป้องกันด้วยรหัสผ่าน คุณต้องระบุรหัสผ่านที่เหมาะสมใน`Unprotect()` วิธีการที่จะปลดล็อคมันได้

#### ถาม: มีข้อจำกัดหรือข้อควรระวังในการปลดล็อกสเปรดชีต Excel ที่ได้รับการป้องกันหรือไม่

ตอบ: ใช่ ตรวจสอบให้แน่ใจว่าคุณมีสิทธิ์ที่จำเป็นในการปลดล็อคสเปรดชีต นอกจากนี้ อย่าลืมปฏิบัติตามนโยบายความปลอดภัยขององค์กรของคุณเมื่อใช้ฟีเจอร์นี้