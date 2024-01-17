---
title: กรองชื่อที่กำหนดขณะโหลดสมุดงาน
linktitle: กรองชื่อที่กำหนดขณะโหลดสมุดงาน
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีกรองชื่อที่กำหนดเมื่อโหลดสมุดงาน Excel ด้วย Aspose.Cells สำหรับ .NET
type: docs
weight: 100
url: /th/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
เมื่อทำงานกับสมุดงาน Excel ในแอปพลิเคชัน .NET มักจำเป็นต้องกรองข้อมูลตามโหลด Aspose.Cells for .NET เป็นไลบรารีที่มีประสิทธิภาพในการจัดการสมุดงาน Excel ได้อย่างง่ายดาย ในคู่มือนี้ เราจะแสดงวิธีกรองชื่อที่กำหนดเมื่อโหลดเวิร์กบุ๊กโดยใช้ Aspose.Cells สำหรับ .NET ทำตามขั้นตอนง่ายๆ เหล่านี้เพื่อให้ได้ผลลัพธ์ที่ต้องการ:

## ขั้นตอนที่ 1: ระบุตัวเลือกการโหลด

ขั้นแรก คุณต้องระบุตัวเลือกการโหลดเพื่อกำหนดลักษณะการโหลดของสมุดงาน ในกรณีของเรา เราต้องการละเว้นชื่อที่ตั้งไว้เมื่อโหลด ต่อไปนี้เป็นวิธีดำเนินการโดยใช้ Aspose.Cells:

```csharp
// ระบุตัวเลือกการโหลด
LoadOptions opts = new LoadOptions();

// อย่าโหลดชื่อที่กำหนด
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## ขั้นตอนที่ 2: โหลดสมุดงาน

เมื่อกำหนดค่าตัวเลือกการโหลดแล้ว คุณสามารถโหลดสมุดงาน Excel จากไฟล์ต้นฉบับได้ อย่าลืมระบุเส้นทางไฟล์ที่ถูกต้อง นี่คือโค้ดตัวอย่าง:

```csharp
// โหลดสมุดงาน
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## ขั้นตอนที่ 3: บันทึกสมุดงานที่ถูกกรอง

หลังจากโหลดสมุดงานแล้ว คุณสามารถดำเนินการอื่นๆ หรือแก้ไขได้ตามต้องการ จากนั้นคุณสามารถบันทึกเวิร์กบุ๊กที่กรองแล้วลงในไฟล์เอาต์พุตได้ มีวิธีดังนี้:

```csharp
// บันทึกสมุดงาน Excel ที่กรองแล้ว
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### ตัวอย่างซอร์สโค้ดสำหรับชื่อที่กำหนดโดยตัวกรองขณะโหลดสมุดงานโดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ระบุตัวเลือกการโหลด
LoadOptions opts = new LoadOptions();
//เราไม่ต้องการโหลดชื่อที่กำหนด
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//โหลดสมุดงาน
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//บันทึกไฟล์ Excel เอาต์พุต มันจะทำลายสูตรใน C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## บทสรุป

การกรองชื่อที่กำหนดเมื่อโหลดสมุดงาน Excel อาจมีความสำคัญสำหรับหลายแอปพลิเคชัน Aspose.Cells สำหรับ .NET ช่วยให้งานนี้ง่ายขึ้นโดยมีตัวเลือกที่ยืดหยุ่นสำหรับการโหลดและการกรองข้อมูล เมื่อทำตามขั้นตอนในคู่มือนี้ คุณจะสามารถกรองชื่อที่กำหนดออกได้อย่างมีประสิทธิภาพ และบรรลุผลลัพธ์ที่ต้องการในสมุดงาน Excel ของคุณ


### คำถามที่พบบ่อย

#### ถาม: Aspose.Cells รองรับภาษาการเขียนโปรแกรมอื่นๆ นอกเหนือจาก C# หรือไม่
    
ตอบ: ใช่ Aspose.Cells เป็นไลบรารีข้ามแพลตฟอร์มที่รองรับภาษาการเขียนโปรแกรมมากมาย เช่น Java, Python, C++และอื่น ๆ อีกมากมาย.

#### ถาม: ฉันสามารถกรองข้อมูลประเภทอื่นเมื่อโหลดเวิร์กบุ๊กด้วย Aspose.Cells ได้หรือไม่
    
ตอบ: ใช่ Aspose.Cells มีตัวเลือกการกรองข้อมูลมากมาย รวมถึงสูตร สไตล์ มาโคร ฯลฯ

#### ถาม: Aspose.Cells ยังคงรักษาการจัดรูปแบบและคุณสมบัติของเวิร์กบุ๊กต้นฉบับไว้หรือไม่
    
ตอบ: ใช่ Aspose.Cells ยังคงรักษาการจัดรูปแบบ สไตล์ สูตร และคุณสมบัติอื่นๆ ของเวิร์กบุ๊กต้นฉบับเมื่อทำงานกับไฟล์ Excel