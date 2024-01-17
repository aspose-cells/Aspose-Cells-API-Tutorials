---
title: सामग्री प्रकार गुणों के साथ कार्य करना
linktitle: सामग्री प्रकार गुणों के साथ कार्य करना
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके सामग्री प्रकार गुणों के साथ काम करना सीखें।
type: docs
weight: 180
url: /hi/net/excel-workbook/working-with-content-type-properties/
---
सामग्री प्रकार गुण .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल फ़ाइलों को प्रबंधित और हेरफेर करने में महत्वपूर्ण भूमिका निभाते हैं। ये गुण आपको एक्सेल फ़ाइलों के लिए अतिरिक्त मेटाडेटा परिभाषित करने की अनुमति देते हैं, जिससे डेटा को व्यवस्थित करना और ढूंढना आसान हो जाता है। इस ट्यूटोरियल में, हम आपको नमूना C# कोड का उपयोग करके सामग्री प्रकार गुणों को समझने और उनके साथ काम करने के लिए चरण-दर-चरण ले जाएंगे।

## आवश्यक शर्तें

शुरू करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित हैं:

- आपकी विकास मशीन पर .NET के लिए Aspose.Cells स्थापित हैं।
- C# के साथ संगत एक एकीकृत विकास वातावरण (IDE), जैसे विज़ुअल स्टूडियो।

## चरण 1: वातावरण स्थापित करना

इससे पहले कि आप सामग्री प्रकार गुणों के साथ काम करना शुरू करें, सुनिश्चित करें कि आपने .NET के लिए Aspose.Cells के साथ अपना विकास वातावरण स्थापित कर लिया है। आप अपने प्रोजेक्ट में Aspose.Cells लाइब्रेरी का संदर्भ जोड़ सकते हैं और आवश्यक नेमस्पेस को अपनी कक्षा में आयात कर सकते हैं।

```csharp
using Aspose.Cells;
```

## चरण 2: एक नई एक्सेल वर्कबुक बनाना

 सबसे पहले, हम इसका उपयोग करके एक नई एक्सेल वर्कबुक बनाएंगे`Workbook`Aspose.Cells द्वारा प्रदान की गई कक्षा। निम्नलिखित कोड दिखाता है कि एक नई एक्सेल वर्कबुक कैसे बनाएं और इसे एक निर्दिष्ट आउटपुट निर्देशिका में कैसे संग्रहीत करें।

```csharp
// गन्तव्य निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();

// एक नई एक्सेल वर्कबुक बनाएं
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## चरण 3: सामग्री प्रकार गुण जोड़ना

 अब जब हमारे पास हमारी एक्सेल वर्कबुक है, तो हम इसका उपयोग करके सामग्री प्रकार के गुण जोड़ सकते हैं`Add` की विधि`ContentTypeProperties` का संग्रह`Workbook` कक्षा। प्रत्येक संपत्ति को एक नाम और एक मूल्य द्वारा दर्शाया जाता है। आप

  आप संपत्ति का डेटा प्रकार भी निर्दिष्ट कर सकते हैं।

```csharp
// पहली सामग्री प्रकार संपत्ति जोड़ें
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

// दूसरी सामग्री प्रकार संपत्ति जोड़ें
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## चरण 4: एक्सेल वर्कबुक को सेव करना

 सामग्री प्रकार गुणों को जोड़ने के बाद, हम एक्सेल वर्कबुक को परिवर्तनों के साथ सहेज सकते हैं। उपयोग`Save` की विधि`Workbook` आउटपुट निर्देशिका और फ़ाइल नाम निर्दिष्ट करने के लिए क्लास।

```csharp
// एक्सेल वर्कबुक को सेव करें
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### .NET के लिए Aspose.Cells का उपयोग करके सामग्री प्रकार गुणों के साथ काम करने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## निष्कर्ष

बधाई हो! आपने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके सामग्री प्रकार के गुणों के साथ कैसे काम किया जाए। अब आप अपनी एक्सेल फाइलों में कस्टम मेटाडेटा जोड़ सकते हैं और उन्हें अधिक कुशलता से प्रबंधित कर सकते हैं।

### पूछे जाने वाले प्रश्न

#### प्रश्न: क्या सामग्री प्रकार गुण एक्सेल के सभी संस्करणों के साथ संगत हैं?

उ: हाँ, सामग्री प्रकार गुण Excel के सभी संस्करणों में बनाई गई Excel फ़ाइलों के साथ संगत हैं।

#### प्रश्न: क्या मैं सामग्री प्रकार गुणों को Excel कार्यपुस्तिका में जोड़ने के बाद संपादित कर सकता हूँ?

 उत्तर: हां, आप किसी भी समय सामग्री प्रकार के गुणों को यहां जाकर बदल सकते हैं`ContentTypeProperties` का संग्रह`Workbook` क्लास और और पी विधियों का उपयोग करके उपयुक्त गुण।

#### प्रश्न: क्या पीडीएफ में सहेजते समय सामग्री प्रकार के गुण समर्थित हैं?

उत्तर: नहीं, पीडीएफ में सहेजते समय सामग्री प्रकार के गुण समर्थित नहीं हैं। वे Excel फ़ाइलों के लिए विशिष्ट हैं.