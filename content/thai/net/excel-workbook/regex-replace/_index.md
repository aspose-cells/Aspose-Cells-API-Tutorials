---
title: แทนที่ Regex
linktitle: แทนที่ Regex
second_title: Aspose.Cells สำหรับการอ้างอิง .NET API
description: เรียนรู้วิธีดำเนินการแทนที่ Regex ในไฟล์ Excel โดยใช้ Aspose.Cells สำหรับ .NET
type: docs
weight: 140
url: /th/net/excel-workbook/regex-replace/
---
การแทนที่ข้อความตามนิพจน์ทั่วไป (Regex) เป็นงานทั่วไปเมื่อต้องจัดการข้อมูลในไฟล์ Excel ด้วย Aspose.Cells สำหรับ .NET คุณสามารถทำการแทนที่ Regex ได้อย่างง่ายดายโดยทำตามขั้นตอนเหล่านี้:

## ขั้นตอนที่ 1: ระบุไดเร็กทอรีต้นทางและไดเร็กทอรีเอาต์พุต

ก่อนอื่น คุณต้องระบุไดเร็กทอรีต้นทางซึ่งมีไฟล์ Excel ที่มีข้อมูลที่จะแทนที่อยู่ รวมถึงไดเร็กทอรีเอาต์พุตที่คุณต้องการบันทึกไฟล์ที่แก้ไข ต่อไปนี้เป็นวิธีดำเนินการโดยใช้ Aspose.Cells:

```csharp
// ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();

// ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
```

## ขั้นตอนที่ 2: โหลดไฟล์ Excel ต้นฉบับ

ถัดไป คุณต้องโหลดไฟล์ Excel ต้นทางที่คุณต้องการดำเนินการแทนที่ Regex ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// โหลดไฟล์ Excel ต้นฉบับ
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## ขั้นตอนที่ 3: ดำเนินการเปลี่ยน Regex

หลังจากอัปโหลดไฟล์ คุณสามารถตั้งค่าตัวเลือกการแทนที่ได้ รวมถึงการพิจารณาตัวพิมพ์เล็กและตัวพิมพ์ใหญ่และการจับคู่เนื้อหาเซลล์แบบตรงทั้งหมด นี่คือโค้ดตัวอย่างเพื่อทำการแทนที่ Regex:

```csharp
// ตั้งค่าตัวเลือกการเปลี่ยน
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// กำหนดว่าคีย์การค้นหาเป็นนิพจน์ทั่วไป
replace. RegexKey = true;

// ดำเนินการแทนที่ Regex
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## ขั้นตอนที่ 4: บันทึกไฟล์ Excel เอาต์พุต

เมื่อการแทนที่ Regex เสร็จสิ้น คุณสามารถบันทึกไฟล์ Excel ที่แก้ไขแล้วลงในไดเร็กทอรีเอาต์พุตที่ระบุได้ ต่อไปนี้เป็นวิธีดำเนินการ:

```csharp
// บันทึกไฟล์ Excel เอาต์พุต
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### ตัวอย่างซอร์สโค้ดสำหรับ Regex แทนที่โดยใช้ Aspose.Cells สำหรับ .NET 
```csharp
//ไดเรกทอรีต้นทาง
string sourceDir = RunExamples.Get_SourceDirectory();
//ไดเร็กทอรีเอาต์พุต
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// ตั้งค่าเป็นจริงเพื่อระบุว่าคีย์ที่ค้นหาคือ regex
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## บทสรุป

การแทนที่ Regex เป็นเทคนิคที่มีประสิทธิภาพสำหรับการปรับเปลี่ยนข้อมูลในไฟล์ Excel แบบไดนามิก ด้วย Aspose.Cells สำหรับ .NET คุณสามารถทำการแทนที่ Regex ได้อย่างง่ายดายโดยทำตามขั้นตอนที่อธิบายไว้ข้างต้น ทดลองกับนิพจน์ทั่วไปของคุณเองและใช้ประโยชน์จากความยืดหยุ่นที่ Aspose.Cells มอบให้

### คำถามที่พบบ่อย

#### ถาม: การแทนที่ Regex คืออะไร
    
ตอบ: การแทนที่ Regex เป็นเทคนิคที่ใช้ในการแทนที่รูปแบบข้อความตามนิพจน์ทั่วไปในไฟล์ Excel ช่วยให้สามารถเปลี่ยนแปลงข้อมูลได้อย่างรวดเร็วและแม่นยำ

#### ถาม: การเปลี่ยน Regex คำนึงถึงขนาดตัวพิมพ์หรือไม่
    
ตอบ: ไม่ ด้วย Aspose.Cells คุณสามารถระบุได้ว่าการเปลี่ยน Regex ควรคำนึงถึงขนาดตัวพิมพ์หรือไม่ คุณสามารถควบคุมคุณสมบัตินี้ได้อย่างเต็มที่

#### ถาม: ฉันจะระบุเนื้อหาเซลล์ที่ตรงกันทุกประการเมื่อแทนที่ Regex ได้อย่างไร
    
ตอบ: Aspose.Cells ช่วยให้คุณกำหนดได้ว่าการแทนที่ Regex ควรตรงกับเนื้อหาของเซลล์ทุกประการหรือไม่ คุณสามารถปรับตัวเลือกนี้ได้ตามความต้องการของคุณ

#### ถาม: ฉันสามารถใช้นิพจน์ทั่วไปขั้นสูงเมื่อแทนที่ Regex ด้วย Aspose.Cells ได้หรือไม่
    
ตอบ: ได้ Aspose.Cells รองรับนิพจน์ทั่วไปขั้นสูง ซึ่งช่วยให้คุณสามารถดำเนินการแทนที่ที่ซับซ้อนและซับซ้อนในไฟล์ Excel ของคุณได้

#### ถาม: ฉันจะตรวจสอบได้อย่างไรว่าการเปลี่ยน Regex สำเร็จหรือไม่
    
ตอบ: หลังจากดำเนินการแทนที่ Regex แล้ว คุณจะตรวจสอบได้ว่าการดำเนินการสำเร็จหรือไม่โดยการตรวจสอบเอาต์พุตและตรวจสอบว่าไฟล์ Excel เอาต์พุตนั้นถูกสร้างขึ้นอย่างถูกต้อง
	