---
title: पावर क्वेरी फॉर्मूला आइटम अपडेट करें
linktitle: पावर क्वेरी फॉर्मूला आइटम अपडेट करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके एक्सेल फ़ाइलों में पावर क्वेरी फॉर्मूला तत्वों को अपडेट करना सीखें।
type: docs
weight: 160
url: /hi/net/excel-workbook/update-power-query-formula-item/
---
एक्सेल फ़ाइलों में डेटा के साथ काम करते समय पावर क्वेरी फॉर्मूला आइटम को अपडेट करना एक सामान्य ऑपरेशन है। .NET के लिए Aspose.Cells के साथ, आप इन चरणों का पालन करके आसानी से पावर क्वेरी फॉर्मूला आइटम को अपडेट कर सकते हैं:

## चरण 1: स्रोत और आउटपुट निर्देशिका निर्दिष्ट करें

सबसे पहले, आपको स्रोत निर्देशिका निर्दिष्ट करने की आवश्यकता है जहां अद्यतन करने के लिए पावर क्वेरी फ़ार्मुलों वाली एक्सेल फ़ाइल स्थित है, साथ ही आउटपुट निर्देशिका जहां आप संशोधित फ़ाइल को सहेजना चाहते हैं। Aspose.Cells का उपयोग करके इसे कैसे करें यहां बताया गया है:

```csharp
// स्रोत निर्देशिका
string SourceDir = RunExamples.Get_SourceDirectory();

// उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
```

## चरण 2: स्रोत एक्सेल कार्यपुस्तिका लोड करें

इसके बाद, आपको स्रोत एक्सेल वर्कबुक को लोड करना होगा जिस पर आप पावर क्वेरी फॉर्मूला आइटम को अपडेट करना चाहते हैं। इसे करने का तरीका यहां बताया गया है:

```csharp
// स्रोत एक्सेल कार्यपुस्तिका लोड करें
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## चरण 3: पावर क्वेरी फॉर्मूला आइटम ब्राउज़ करें और अपडेट करें

कार्यपुस्तिका लोड करने के बाद, आप पावर क्वेरी फॉर्मूला संग्रह पर नेविगेट कर सकते हैं और प्रत्येक सूत्र और उसके तत्वों को ब्राउज़ कर सकते हैं। इस उदाहरण में, हम "स्रोत" नाम से सूत्र आइटम ढूंढ रहे हैं और उसका मान अपडेट कर रहे हैं। पावर क्वेरी फॉर्मूला आइटम को अपडेट करने के लिए यहां नमूना कोड दिया गया है:

```csharp
// पावर क्वेरी फॉर्मूला संग्रह तक पहुंचें
DataMashup mashupData = workbook.DataMashup;

// पावर क्वेरी फ़ार्मुलों और उनके तत्वों के माध्यम से लूप करें
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

## चरण 4: आउटपुट एक्सेल वर्कबुक सहेजें

एक बार जब आप पावर क्वेरी फॉर्मूला आइटम को अपडेट कर लेते हैं, तो आप संशोधित एक्सेल वर्कबुक को निर्दिष्ट आउटपुट निर्देशिका में सहेज सकते हैं। इसे करने का तरीका यहां बताया गया है:

```csharp
// आउटपुट एक्सेल वर्कबुक को सेव करें
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### .NET के लिए Aspose.Cells का उपयोग करके अपडेट पावर क्वेरी फॉर्मूला आइटम के लिए नमूना स्रोत कोड 
```csharp
// कार्यशील निर्देशिकाएँ
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
// आउटपुट वर्कबुक सहेजें.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## निष्कर्ष

एक्सेल फ़ाइलों में डेटा में हेरफेर और प्रसंस्करण के लिए Aspose.Cells का उपयोग करते समय पावर क्वेरी फॉर्मूला तत्वों को अपडेट करना एक आवश्यक ऑपरेशन है। ऊपर दिए गए चरणों का पालन करके आप फॉर्मूला तत्वों को आसानी से अपडेट कर सकते हैं

### पूछे जाने वाले प्रश्न

#### प्रश्न: एक्सेल में पावर क्वेरी क्या है?
     
उ: पावर क्वेरी एक्सेल में एक सुविधा है जो विभिन्न स्रोतों से डेटा एकत्र करने, बदलने और लोड करने में मदद करती है। यह एक्सेल में आयात करने से पहले डेटा को साफ करने, संयोजित करने और दोबारा आकार देने के लिए शक्तिशाली उपकरण प्रदान करता है।

#### प्रश्न: मुझे कैसे पता चलेगा कि पावर क्वेरी फॉर्मूला आइटम सफलतापूर्वक अपडेट किया गया था?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### प्रश्न: क्या मैं एक साथ कई पावर क्वेरी फॉर्मूला आइटम अपडेट कर सकता हूं?
    
उ: हां, आप अपनी विशिष्ट आवश्यकताओं के आधार पर, पावर क्वेरी फॉर्मूला आइटम संग्रह के माध्यम से लूप कर सकते हैं और एक ही लूप में कई आइटम अपडेट कर सकते हैं।

#### प्रश्न: क्या ऐसे अन्य ऑपरेशन हैं जो मैं Aspose.Cells के साथ पावर क्वेरी फ़ार्मुलों पर कर सकता हूँ?
    
उ: हां, Aspose.Cells पावर क्वेरी फ़ार्मुलों के साथ काम करने के लिए सुविधाओं की एक पूरी श्रृंखला प्रदान करता है, जिसमें एक्सेल वर्कबुक में फ़ॉर्मूले बनाना, हटाना, कॉपी करना और खोजना शामिल है।