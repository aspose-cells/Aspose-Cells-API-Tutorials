---
title: อ่านและเขียนการเชื่อมต่อภายนอกของไฟล์ XLSB
linktitle: อ่านและเขียนการเชื่อมต่อภายนอกของไฟล์ XLSB
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีอ่านและแก้ไขการเชื่อมต่อภายนอกของไฟล์ XLSB โดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 130
url: /th/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
การอ่านและเขียนการเชื่อมต่อภายนอกไปยังไฟล์ XLSB เป็นสิ่งจำเป็นสำหรับการจัดการข้อมูลจากแหล่งภายนอกในสมุดงาน Excel ของคุณ ด้วย Aspose.Cells สำหรับ .NET คุณสามารถอ่านและเขียนการเชื่อมต่อภายนอกได้อย่างง่ายดายโดยใช้ขั้นตอนต่อไปนี้:

## ขั้นตอนที่ 1: ระบุไดเร็กทอรีต้นทางและไดเร็กทอรีเอาต์พุต

ขั้นแรก คุณต้องระบุไดเร็กทอรีต้นทางซึ่งมีไฟล์ XLSB ที่มีการเชื่อมต่อภายนอกอยู่ รวมถึงไดเร็กทอรีเอาต์พุตที่คุณต้องการบันทึกไฟล์ที่แก้ไข ต่อไปนี้เป็นวิธีดำเนินการโดยใช้ Aspose.Cells:

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();

// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

## ขั้นตอนที่ 2: โหลดไฟล์ Excel XLSB ต้นทาง

ถัดไป คุณต้องโหลดไฟล์ Excel XLSB ต้นทางที่คุณต้องการดำเนินการอ่านและเขียนการเชื่อมต่อภายนอก นี่คือโค้ดตัวอย่าง:

```csharp
// โหลดไฟล์ Excel XLSB ต้นทาง
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## ขั้นตอนที่ 3: อ่านและแก้ไขการเชื่อมต่อภายนอก

หลังจากโหลดไฟล์แล้ว คุณสามารถเข้าถึงการเชื่อมต่อภายนอกครั้งแรกซึ่งจริงๆ แล้วเป็นการเชื่อมต่อฐานข้อมูล คุณสามารถอ่านและแก้ไขคุณสมบัติต่างๆ ของการเชื่อมต่อภายนอกได้ มีวิธีดังนี้:

```csharp
// อ่านการเชื่อมต่อภายนอกครั้งแรกซึ่งเป็นการเชื่อมต่อฐานข้อมูล
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// แสดงชื่อการเชื่อมต่อฐานข้อมูล คำสั่ง และข้อมูลการเชื่อมต่อ
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// แก้ไขชื่อของการเชื่อมต่อ
dbCon.Name = "NewCustomer";
```

## ขั้นตอนที่ 4: บันทึกไฟล์ Excel XLSB เอาต์พุต

เมื่อคุณทำการเปลี่ยนแปลงที่จำเป็นแล้ว คุณสามารถบันทึกไฟล์ Excel XLSB ที่แก้ไขแล้วลงในไดเร็กทอรีเอาต์พุตที่ระบุได้ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// บันทึกไฟล์ Excel XLSB เอาต์พุต
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### ตัวอย่างซอร์สโค้ดสำหรับการอ่านและเขียนการเชื่อมต่อภายนอกของไฟล์ XLSB โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
//ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
//โหลดไฟล์ Excel Xlsb ต้นทาง
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//อ่านการเชื่อมต่อภายนอกครั้งแรกซึ่งจริงๆ แล้วเป็นการเชื่อมต่อ DB
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//พิมพ์ชื่อ คำสั่ง และข้อมูลการเชื่อมต่อของการเชื่อมต่อ DB
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//แก้ไขชื่อการเชื่อมต่อ
dbCon.Name = "NewCust";
//บันทึกไฟล์ Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## บทสรุป

การอ่านและการเขียนการเชื่อมต่อภายนอกไปยังไฟล์ XLSB ช่วยให้คุณสามารถจัดการข้อมูลจากแหล่งภายนอกในสมุดงาน Excel ของคุณได้ ด้วย Aspose.Cells สำหรับ .NET คุณสามารถเข้าถึงการเชื่อมต่อภายนอก อ่านและแก้ไขข้อมูลการเชื่อมต่อ และบันทึกการเปลี่ยนแปลงได้อย่างง่ายดาย ทดลองกับไฟล์ XLSB ของคุณเองและควบคุมพลังของการเชื่อมต่อภายนอกในแอปพลิเคชัน Excel ของคุณ

### คำถามที่พบบ่อย

#### ถาม: การเชื่อมต่อภายนอกในไฟล์ XLSB คืออะไร
    
ตอบ: การเชื่อมต่อภายนอกในไฟล์ XLSB หมายถึงการเชื่อมต่อที่สร้างขึ้นกับแหล่งข้อมูลภายนอก เช่น ฐานข้อมูล ช่วยให้คุณสามารถนำเข้าข้อมูลจากแหล่งภายนอกนี้ไปยังสมุดงาน Excel

#### ถาม: ฉันสามารถมีการเชื่อมต่อภายนอกหลายรายการในไฟล์ XLSB ได้หรือไม่
     
ตอบ: ได้ คุณสามารถมีการเชื่อมต่อภายนอกได้หลายรายการในไฟล์ XLSB คุณสามารถจัดการทีละรายการได้โดยการเข้าถึงแต่ละออบเจ็กต์การเชื่อมต่อ

#### ถาม: ฉันจะอ่านรายละเอียดของการเชื่อมต่อภายนอกในไฟล์ XLSB ด้วย Aspose.Cells ได้อย่างไร
     
ตอบ: คุณสามารถใช้ฟังก์ชันที่ Aspose.Cells มอบให้เพื่อเข้าถึงคุณสมบัติของการเชื่อมต่อภายนอก เช่น ชื่อการเชื่อมต่อ คำสั่งที่เกี่ยวข้อง และข้อมูลการเชื่อมต่อ

#### ถาม: เป็นไปได้ไหมที่จะแก้ไขการเชื่อมต่อภายนอกในไฟล์ XLSB ด้วย Aspose.Cells
     
ตอบ: ได้ คุณสามารถแก้ไขคุณสมบัติของการเชื่อมต่อภายนอก เช่น ชื่อการเชื่อมต่อ เพื่อให้ตรงตามความต้องการเฉพาะของคุณได้ Aspose.Cells มีวิธีการในการเปลี่ยนแปลงเหล่านี้

#### ถาม: ฉันจะบันทึกการเปลี่ยนแปลงที่ทำกับการเชื่อมต่อภายนอกไปยังไฟล์ XLSB ด้วย Aspose.Cells ได้อย่างไร
     
ตอบ: เมื่อคุณได้ทำการเปลี่ยนแปลงที่จำเป็นกับการเชื่อมต่อภายนอกแล้ว คุณสามารถบันทึกไฟล์ Excel XLSB ที่แก้ไขแล้วได้โดยใช้วิธีการที่เหมาะสมที่ Aspose.Cells มอบให้