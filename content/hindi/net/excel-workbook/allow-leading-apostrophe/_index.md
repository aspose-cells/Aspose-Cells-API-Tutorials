---
title: अग्रणी एपोस्ट्रोफ की अनुमति दें
linktitle: अग्रणी एपोस्ट्रोफ की अनुमति दें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ Excel कार्यपुस्तिकाओं में अग्रणी एपोस्ट्रोफ़ की अनुमति दें।
type: docs
weight: 60
url: /hi/net/excel-workbook/allow-leading-apostrophe/
---
इस चरण-दर-चरण ट्यूटोरियल में, हम दिए गए C# स्रोत कोड की व्याख्या करेंगे जो आपको .NET के लिए Aspose.Cells का उपयोग करके Excel कार्यपुस्तिका में एक अग्रणी एपोस्ट्रोफ़ के उपयोग की अनुमति देगा। इस ऑपरेशन को करने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: स्रोत और आउटपुट निर्देशिका सेट करें

```csharp
// स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
// उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
```

इस पहले चरण में, हम एक्सेल फ़ाइलों के लिए स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करते हैं।

## चरण 2: वर्कबुकडिज़ाइनर ऑब्जेक्ट को इंस्टेंट करें

```csharp
// वर्कबुकडिज़ाइनर ऑब्जेक्ट को इंस्टेंट करें
WorkbookDesigner designer = new WorkbookDesigner();
```

 हम इसका एक उदाहरण बनाते हैं`WorkbookDesigner` Aspose.Cells से कक्षा।

## चरण 3: एक्सेल वर्कबुक लोड करें

```csharp
// एक्सेल वर्कबुक लोड करें
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

हम एक्सेल वर्कबुक को निर्दिष्ट फ़ाइल से लोड करते हैं और प्रारंभिक एपोस्ट्रोफ के स्वचालित रूपांतरण को टेक्स्ट शैली में अक्षम कर देते हैं।

## चरण 4: डेटा स्रोत सेट करें

```csharp
// डिज़ाइनर कार्यपुस्तिका के लिए डेटा स्रोत को परिभाषित करें
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 हम डेटा ऑब्जेक्ट की एक सूची परिभाषित करते हैं और इसका उपयोग करते हैं`SetDataSource` डिज़ाइनर कार्यपुस्तिका के लिए डेटा स्रोत सेट करने की विधि।

## चरण 5: स्मार्ट मार्करों की प्रक्रिया करें

```csharp
// स्मार्ट मार्करों की प्रक्रिया करें
designer. Process();
```

 हम उपयोग करते हैं`Process` डिज़ाइनर कार्यपुस्तिका में स्मार्ट मार्करों को संसाधित करने की विधि।

## चरण 6: संशोधित एक्सेल कार्यपुस्तिका सहेजें

```csharp
// संशोधित Excel कार्यपुस्तिका सहेजें
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

हम संशोधित एक्सेल वर्कबुक को किए गए परिवर्तनों के साथ सहेजते हैं।

### .NET के लिए Aspose.Cells का उपयोग करके लीडिंग एपोस्ट्रोफ को अनुमति देने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// वर्कबुकडिज़ाइनर ऑब्जेक्ट को इंस्टेंट करना
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// स्मार्ट मार्कर युक्त एक डिज़ाइनर स्प्रेडशीट खोलें
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// डिज़ाइनर स्प्रेडशीट के लिए डेटा स्रोत सेट करें
designer.SetDataSource("sampleData", list);
// स्मार्ट मार्करों को संसाधित करें
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## निष्कर्ष

बधाई हो! आपने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके Excel कार्यपुस्तिका में अग्रणी एपोस्ट्रोफ़ के उपयोग की अनुमति कैसे दी जाए। अपनी Excel कार्यपुस्तिकाओं को और अधिक अनुकूलित करने के लिए अपने स्वयं के डेटा के साथ प्रयोग करें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: एक्सेल वर्कबुक में लीडिंग एपॉस्ट्रॉफी अनुमति क्या है?

ए: एक्सेल वर्कबुक में प्रारंभिक एपोस्ट्रोफ की अनुमति देने से एपोस्ट्रोफ से शुरू होने वाले डेटा को टेक्स्ट शैली में परिवर्तित किए बिना सही ढंग से प्रदर्शित किया जा सकता है। यह तब उपयोगी होता है जब आप एपोस्ट्रोफ को डेटा के हिस्से के रूप में रखना चाहते हैं।

#### प्रश्न: मुझे आरंभिक एपोस्ट्रोफ़ के स्वचालित रूपांतरण को बंद करने की आवश्यकता क्यों है?

उ: प्रमुख उद्धरणों के स्वचालित रूपांतरण को अक्षम करके, आप उनके उपयोग को वैसे ही सुरक्षित रख सकते हैं जैसे यह आपके डेटा में है। यह Excel कार्यपुस्तिका को खोलते या उसमें हेरफेर करते समय डेटा के किसी भी अनपेक्षित संशोधन से बचाता है।

#### प्रश्न: डिज़ाइनर वर्कबुक में डेटासोर्स कैसे सेट करें?

 उ: डिज़ाइनर कार्यपुस्तिका में डेटा स्रोत सेट करने के लिए, आप इसका उपयोग कर सकते हैं`SetDataSource` डेटा स्रोत का नाम और संबंधित डेटा ऑब्जेक्ट की सूची निर्दिष्ट करने वाली विधि।

#### प्रश्न: क्या अग्रणी एपोस्ट्रोफ की अनुमति एक्सेल वर्कबुक में अन्य डेटा को प्रभावित करती है?

उत्तर: नहीं, अग्रणी एपॉस्ट्रॉफ़ी की अनुमति केवल एपॉस्ट्रॉफ़ी से शुरू होने वाले डेटा को प्रभावित करती है। एक्सेल वर्कबुक में अन्य डेटा अपरिवर्तित रहता है।

#### प्रश्न: क्या मैं इस सुविधा का उपयोग अन्य एक्सेल फ़ाइल स्वरूपों के साथ कर सकता हूँ?

उ: हां, आप इस सुविधा का उपयोग Aspose.Cells द्वारा समर्थित अन्य एक्सेल फ़ाइल स्वरूपों, जैसे .xls, .xlsm, आदि के साथ कर सकते हैं।