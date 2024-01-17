---
title: อัปเดตรายการสูตร Power Query
linktitle: อัปเดตรายการสูตร Power Query
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีอัปเดตองค์ประกอบสูตร Power Query ในไฟล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 160
url: /th/net/excel-workbook/update-power-query-formula-item/
---
การอัปเดตรายการสูตร Power Query เป็นการดำเนินการทั่วไปเมื่อทำงานกับข้อมูลในไฟล์ Excel ด้วย Aspose.Cells สำหรับ .NET คุณสามารถอัปเดตรายการสูตร Power Query ได้อย่างง่ายดายโดยทำตามขั้นตอนเหล่านี้:

## ขั้นตอนที่ 1: ระบุไดเร็กทอรีต้นทางและเอาต์พุต

ขั้นแรก คุณต้องระบุไดเรกทอรีต้นทางซึ่งมีไฟล์ Excel ที่มีสูตร Power Query ที่จะอัปเดต รวมถึงไดเรกทอรีผลลัพธ์ที่คุณต้องการบันทึกไฟล์ที่แก้ไข ต่อไปนี้เป็นวิธีดำเนินการโดยใช้ Aspose.Cells:

```csharp
// ไดเรกทอรีต้นทาง
string SourceDir = RunExamples.Get_SourceDirectory();

// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

## ขั้นตอนที่ 2: โหลดเวิร์กบุ๊ก Excel ต้นฉบับ

ถัดไป คุณต้องโหลดเวิร์กบุ๊ก Excel ต้นทางที่คุณต้องการอัปเดตรายการสูตร Power Query ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// โหลดสมุดงาน Excel ต้นฉบับ
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## ขั้นตอนที่ 3: เรียกดูและอัปเดตรายการสูตร Power Query

หลังจากโหลดเวิร์กบุ๊กแล้ว คุณสามารถนำทางไปยังคอลเลกชันสูตร Power Query และเรียกดูแต่ละสูตรและองค์ประกอบต่างๆ ได้ ในตัวอย่างนี้ เรากำลังมองหารายการสูตรที่มีชื่อว่า "แหล่งที่มา" และอัปเดตค่าของมัน นี่คือโค้ดตัวอย่างในการอัปเดตรายการสูตร Power Query:

```csharp
// เข้าถึงคอลเลกชันสูตร Power Query
DataMashup mashupData = workbook.DataMashup;

// วนซ้ำสูตร Power Query และองค์ประกอบต่างๆ
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## ขั้นตอนที่ 4: บันทึกเวิร์กบุ๊ก Excel เอาท์พุต

เมื่อคุณอัปเดตรายการสูตร Power Query แล้ว คุณสามารถบันทึกเวิร์กบุ๊ก Excel ที่แก้ไขลงในไดเร็กทอรีเอาต์พุตที่ระบุได้ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// บันทึกเวิร์กบุ๊ก Excel เอาท์พุต
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### ซอร์สโค้ดตัวอย่างสำหรับอัปเดตรายการสูตร Power Query โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
// ไดเร็กทอรีการทำงาน
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// บันทึกสมุดงานผลลัพธ์
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## บทสรุป

การอัปเดตองค์ประกอบสูตร Power Query เป็นการดำเนินการที่สำคัญเมื่อใช้ Aspose.Cells เพื่อจัดการและประมวลผลข้อมูลในไฟล์ Excel เมื่อทำตามขั้นตอนข้างต้น คุณจะอัปเดตองค์ประกอบสูตรได้อย่างง่ายดาย

### คำถามที่พบบ่อย

#### ถาม: Power Query ใน Excel คืออะไร
     
ตอบ: Power Query เป็นฟีเจอร์ใน Excel ที่ช่วยรวบรวม แปลง และโหลดข้อมูลจากแหล่งต่างๆ มีเครื่องมืออันทรงพลังในการล้าง รวม และจัดรูปแบบข้อมูลใหม่ก่อนที่จะนำเข้าไปยัง Excel

#### ถาม: ฉันจะรู้ได้อย่างไรว่ารายการสูตร Power Query ได้รับการอัปเดตสำเร็จแล้ว
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### ถาม: ฉันสามารถอัปเดตรายการสูตร Power Query หลายรายการพร้อมกันได้หรือไม่
    
ตอบ: ได้ คุณสามารถวนซ้ำคอลเลกชันรายการสูตร Power Query และอัปเดตหลายรายการในการวนรอบเดียวได้ ขึ้นอยู่กับความต้องการเฉพาะของคุณ

#### ถาม: มีการดำเนินการอื่นๆ ที่ฉันสามารถทำได้บนสูตร Power Query ด้วย Aspose.Cells หรือไม่
    
ตอบ: ใช่ Aspose.Cells มีฟีเจอร์ครบครันสำหรับการทำงานกับสูตร Power Query รวมถึงการสร้าง การลบ การคัดลอก และการค้นหาสูตรในเวิร์กบุ๊ก Excel