---
title: कार्यपुस्तिका मुद्रण पूर्वावलोकन
linktitle: कार्यपुस्तिका मुद्रण पूर्वावलोकन
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: जानें कि .NET के लिए Aspose.Cells का उपयोग करके किसी कार्यपुस्तिका का प्रिंट पूर्वावलोकन कैसे तैयार किया जाए।
type: docs
weight: 170
url: /hi/net/excel-workbook/workbook-print-preview/
---
.NET के लिए Aspose.Cells के साथ एक्सेल फ़ाइलों के साथ काम करते समय वर्कबुक का प्रिंट पूर्वावलोकन एक आवश्यक सुविधा है। आप इन चरणों का पालन करके आसानी से एक प्रिंट पूर्वावलोकन तैयार कर सकते हैं:

## चरण 1: स्रोत निर्देशिका निर्दिष्ट करें

सबसे पहले, आपको उस स्रोत निर्देशिका को निर्दिष्ट करना होगा जहां आप जिस एक्सेल फ़ाइल का पूर्वावलोकन करना चाहते हैं वह स्थित है। इसे करने का तरीका यहां बताया गया है:

```csharp
// स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
```

## चरण 2: कार्यपुस्तिका लोड करें

फिर आपको वर्कबुक वर्कबुक को निर्दिष्ट एक्सेल फ़ाइल से लोड करना होगा। इसे करने का तरीका यहां बताया गया है:

```csharp
// कार्यपुस्तिका कार्यपुस्तिका लोड करें
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## चरण 3: छवि और प्रिंट विकल्प कॉन्फ़िगर करें

प्रिंट पूर्वावलोकन तैयार करने से पहले, आप आवश्यकतानुसार छवि और प्रिंट विकल्पों को कॉन्फ़िगर कर सकते हैं। इस उदाहरण में, हम डिफ़ॉल्ट विकल्पों का उपयोग कर रहे हैं। इसे करने का तरीका यहां बताया गया है:

```csharp
// छवि और प्रिंट विकल्प
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## चरण 4: कार्यपुस्तिका का प्रिंट पूर्वावलोकन तैयार करें

अब आप WorkbookPrintingPreview क्लास का उपयोग करके वर्कबुक वर्कबुक का प्रिंट पूर्वावलोकन तैयार कर सकते हैं। इसे करने का तरीका यहां बताया गया है:

```csharp
// कार्यपुस्तिका का पूर्वावलोकन प्रिंट करें
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## चरण 5: वर्कशीट का प्रिंट पूर्वावलोकन तैयार करें

यदि आप किसी विशिष्ट वर्कशीट का प्रिंट पूर्वावलोकन तैयार करना चाहते हैं, तो आप शीटप्रिंटिंगप्रीव्यू क्लास का उपयोग कर सकते हैं। यहाँ एक उदाहरण है :

```csharp
// वर्कशीट का पूर्वावलोकन प्रिंट करें
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### .NET के लिए Aspose.Cells का उपयोग करके कार्यपुस्तिका प्रिंट पूर्वावलोकन के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## निष्कर्ष

किसी कार्यपुस्तिका का प्रिंट पूर्वावलोकन तैयार करना .NET के लिए Aspose.Cells द्वारा पेश की गई एक शक्तिशाली सुविधा है। ऊपर दिए गए चरणों का पालन करके, आप आसानी से अपनी एक्सेल वर्कबुक का पूर्वावलोकन कर सकते हैं और प्रिंट करने के लिए पृष्ठों की संख्या के बारे में जानकारी प्राप्त कर सकते हैं।

### पूछे जाने वाले प्रश्न

#### प्रश्न: मैं अपनी कार्यपुस्तिका को लोड करने के लिए एक अलग स्रोत निर्देशिका कैसे निर्दिष्ट कर सकता हूं?
    
 उत्तर: आप इसका उपयोग कर सकते हैं`Set_SourceDirectory` एक अलग स्रोत निर्देशिका निर्दिष्ट करने की विधि। उदाहरण के लिए:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### प्रश्न: क्या मैं प्रिंट पूर्वावलोकन बनाते समय छवि और प्रिंट विकल्पों को अनुकूलित कर सकता हूं?
    
 उ: हां, आप गुणों को बदलकर छवि और प्रिंट विकल्पों को अनुकूलित कर सकते हैं`ImageOrPrintOptions` वस्तु। उदाहरण के लिए, आप छवि रिज़ॉल्यूशन, आउटपुट फ़ाइल स्वरूप आदि सेट कर सकते हैं।

#### प्रश्न: क्या किसी कार्यपुस्तिका में एकाधिक कार्यपत्रकों के लिए प्रिंट पूर्वावलोकन तैयार करना संभव है?
    
उ: हाँ, आप कार्यपुस्तिका में विभिन्न कार्यपत्रकों पर पुनरावृति कर सकते हैं और इसका उपयोग करके प्रत्येक पत्रक के लिए एक प्रिंट पूर्वावलोकन तैयार कर सकते हैं।`SheetPrintingPreview` कक्षा।

#### प्रश्न: मैं प्रिंट पूर्वावलोकन को छवि या पीडीएफ फ़ाइल के रूप में कैसे सहेजूं?
    
 उत्तर: आप उपयोग कर सकते हैं`ToImage` या`ToPdf` उसकि विधि`WorkbookPrintingPreview` या`SheetPrintingPreview` प्रिंट पूर्वावलोकन को छवि या पीडीएफ फ़ाइल के रूप में सहेजने के लिए ऑब्जेक्ट।

#### प्रश्न: एक बार प्रिंट पूर्वावलोकन तैयार हो जाने पर मैं उसके साथ क्या कर सकता हूं?
    
उ: एक बार जब आप प्रिंट पूर्वावलोकन तैयार कर लेते हैं, तो आप इसे स्क्रीन पर देख सकते हैं, इसे एक छवि या पीडीएफ फ़ाइल के रूप में सहेज सकते हैं, या इसे अन्य कार्यों जैसे ईमेल या प्रिंट द्वारा भेजने के लिए उपयोग कर सकते हैं।
	