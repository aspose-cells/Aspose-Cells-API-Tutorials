---
title: वर्कशीट के पंक्ति कॉलम हेडर प्रदर्शित करें और छुपाएं
linktitle: वर्कशीट के पंक्ति कॉलम हेडर प्रदर्शित करें और छुपाएं
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके एक्सेल वर्कशीट में पंक्ति और कॉलम हेडर प्रदर्शित करें या छिपाएँ।
type: docs
weight: 40
url: /hi/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
इस ट्यूटोरियल में, हम आपको दिखाएंगे कि .NET के लिए Aspose.Cells के साथ C# सोर्स कोड का उपयोग करके एक्सेल वर्कशीट की पंक्ति और कॉलम हेडर को कैसे प्रदर्शित या छिपाया जाए। वांछित परिणाम प्राप्त करने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: आवश्यक पुस्तकालय आयात करें

सुनिश्चित करें कि आपने .NET के लिए Aspose.Cells लाइब्रेरी स्थापित की है और आवश्यक लाइब्रेरी को अपने C# प्रोजेक्ट में आयात करें।

```csharp
using Aspose.Cells;
using System.IO;
```

## चरण 2: निर्देशिका पथ सेट करें और एक्सेल फ़ाइल खोलें

 अपनी Excel फ़ाइल वाली निर्देशिका के लिए पथ सेट करें, फिर फ़ाइल स्ट्रीम बनाकर और इंस्टेंटिएट करके फ़ाइल खोलें`Workbook` वस्तु।

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## चरण 3: पहली वर्कशीट पर जाएं और पंक्ति और कॉलम हेडर छिपाएं

 का उपयोग करके एक्सेल फ़ाइल में पहली वर्कशीट तक पहुंचें`Worksheets` की संपत्ति`Workbook` वस्तु। फिर उपयोग करें`IsRowColumnHeadersVisible` की संपत्ति`Worksheet` पंक्ति और स्तंभ शीर्षलेखों को छिपाने के लिए ऑब्जेक्ट।

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## चरण 4: परिवर्तन सहेजें

 एक बार जब आप आवश्यक परिवर्तन कर लें, तो संशोधित एक्सेल फ़ाइल को का उपयोग करके सहेजें`Save` की विधि`Workbook` वस्तु।

```csharp
workbook.Save(dataDir + "output.xls");
```

### .NET के लिए Aspose.Cells का उपयोग करके वर्कशीट के पंक्ति कॉलम हेडर को प्रदर्शित करने और छिपाने के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// एक फ़ाइल स्ट्रीम बनाना जिसमें एक्सेल फ़ाइल खोली जानी है
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
// फ़ाइल स्ट्रीम के माध्यम से एक्सेल फ़ाइल खोलना
Workbook workbook = new Workbook(fstream);
// एक्सेल फ़ाइल में पहली वर्कशीट तक पहुँचना
Worksheet worksheet = workbook.Worksheets[0];
// पंक्तियों और स्तंभों के शीर्षकों को छिपाना
worksheet.IsRowColumnHeadersVisible = false;
// संशोधित एक्सेल फ़ाइल सहेजा जा रहा है
workbook.Save(dataDir + "output.xls");
// सभी संसाधनों को मुक्त करने के लिए फ़ाइल स्ट्रीम को बंद करना
fstream.Close(); 
```

## निष्कर्ष

इस चरण-दर-चरण मार्गदर्शिका ने आपको दिखाया कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल स्प्रेडशीट में पंक्ति और कॉलम हेडर को कैसे प्रदर्शित या छिपाया जाए। दिए गए C# स्रोत कोड का उपयोग करके, आप अपनी Excel फ़ाइलों में हेडर के प्रदर्शन को आसानी से अनुकूलित कर सकते हैं।

### अक्सर पूछे जाने वाले प्रश्न (FAQ)

#### .NET के लिए Aspose.Cells क्या है?

.NET के लिए Aspose.Cells .NET अनुप्रयोगों में एक्सेल फ़ाइलों में हेरफेर करने के लिए एक शक्तिशाली लाइब्रेरी है।

#### मैं .NET के लिए Aspose.Cells कैसे स्थापित कर सकता हूँ?

 .NET के लिए Aspose.Cells स्थापित करने के लिए, आपको संबंधित पैकेज डाउनलोड करना होगा[एस्पोज़ रिलीज़](https://releases/aspose.com/cells/net/) और इसे अपने .NET प्रोजेक्ट में जोड़ें।

#### मैं .NET के लिए Aspose.Cells के साथ एक्सेल स्प्रेडशीट की पंक्ति और कॉलम हेडर को कैसे दिखा या छिपा सकता हूँ?

 आप इसका उपयोग कर सकते हैं`IsRowColumnHeadersVisible` की संपत्ति`Worksheet`पंक्ति और स्तंभ शीर्षलेखों को प्रदर्शित करने या छिपाने के लिए ऑब्जेक्ट। इसे सेट करें`true` उन्हें दिखाने के लिए और करने के लिए`false` उन्हें छुपाने के लिए.

#### .NET के लिए Aspose.Cells द्वारा कौन से अन्य Excel फ़ाइल स्वरूप समर्थित हैं?

.NET के लिए Aspose.Cells विभिन्न Excel फ़ाइल स्वरूपों, जैसे XLS, XLSX, CSV, HTML, PDF और कई अन्य का समर्थन करता है।
