---
title: वर्कशीट की कागज की चौड़ाई और ऊंचाई प्राप्त करें
linktitle: वर्कशीट की कागज की चौड़ाई और ऊंचाई प्राप्त करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके स्प्रेडशीट की पेपर चौड़ाई और ऊंचाई प्राप्त करने के लिए निम्नलिखित C# स्रोत कोड को समझाने के लिए चरण दर चरण मार्गदर्शिका बनाएं।
type: docs
weight: 80
url: /hi/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके वर्कशीट की पेपर चौड़ाई और ऊंचाई प्राप्त करने के लिए निम्नलिखित C# स्रोत कोड को चरण दर चरण समझाएंगे। नीचे दिए गए चरणों का पालन करें:

## चरण 1: कार्यपुस्तिका बनाएँ
 का उपयोग करके एक नई कार्यपुस्तिका बनाकर प्रारंभ करें`Workbook` कक्षा:

```csharp
Workbook wb = new Workbook();
```

## चरण 2: पहली वर्कशीट तक पहुंचें
 इसके बाद, का उपयोग करके कार्यपुस्तिका में पहली वर्कशीट पर नेविगेट करें`Worksheet` कक्षा:

```csharp
Worksheet ws = wb.Worksheets[0];
```

## चरण 3: कागज का आकार A2 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में दिखाएं
 उपयोग`PaperSize` की संपत्ति`PageSetup` कागज़ का आकार A2 पर सेट करने के लिए ऑब्जेक्ट करें, फिर इसका उपयोग करें`PaperWidth` और`PaperHeight` क्रमशः कागज की चौड़ाई और ऊंचाई प्राप्त करने के लिए गुण। का उपयोग करके इन मानों को प्रदर्शित करें`Console.WriteLine` तरीका:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## चरण 4: अन्य कागज़ आकारों के लिए चरणों को दोहराएं
पिछले चरणों को दोहराएँ, कागज़ का आकार A3, A4 और अक्षर में बदलें, फिर प्रत्येक आकार के लिए कागज़ की चौड़ाई और ऊँचाई मान प्रदर्शित करें:

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### .NET के लिए Aspose.Cells का उपयोग करके पेपर की चौड़ाई और वर्कशीट की ऊंचाई प्राप्त करने के लिए नमूना स्रोत कोड 

```csharp
//कार्यपुस्तिका बनाएँ
Workbook wb = new Workbook();
//पहली वर्कशीट तक पहुंचें
Worksheet ws = wb.Worksheets[0];
//कागज का आकार A2 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//कागज का आकार A3 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//कागज का आकार A4 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//कागज का आकार अक्षर पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## निष्कर्ष

आपने सीखा कि स्प्रेडशीट की कागज़ की चौड़ाई और ऊंचाई प्राप्त करने के लिए .NET के लिए Aspose.Cells का उपयोग कैसे करें। यह सुविधा आपके Excel दस्तावेज़ों के कॉन्फ़िगरेशन और सटीक लेआउट के लिए उपयोगी हो सकती है।

### अक्सर पूछे जाने वाले प्रश्न (FAQ)

#### .NET के लिए Aspose.Cells क्या है?

.NET के लिए Aspose.Cells .NET अनुप्रयोगों में एक्सेल फ़ाइलों में हेरफेर और प्रसंस्करण के लिए एक शक्तिशाली लाइब्रेरी है। यह एक्सेल फ़ाइलों को बनाने, संशोधित करने, परिवर्तित करने और विश्लेषण करने के लिए कई सुविधाएँ प्रदान करता है।

#### मैं .NET के लिए Aspose.Cells के साथ स्प्रेडशीट का पेपर आकार कैसे प्राप्त कर सकता हूं?

 आप इसका उपयोग कर सकते हैं`PageSetup` की कक्षा`Worksheet` कागज़ के आकार तक पहुँचने के लिए आपत्ति। उपयोग`PaperSize` कागज़ का आकार निर्धारित करने की संपत्ति और`PaperWidth` और`PaperHeight` क्रमशः कागज की चौड़ाई और ऊंचाई प्राप्त करने के लिए गुण।

#### .NET के लिए Aspose.Cells किस आकार के कागज़ का समर्थन करता है?

.NET के लिए Aspose.Cells आमतौर पर उपयोग किए जाने वाले पेपर आकारों की एक विस्तृत श्रृंखला का समर्थन करता है, जैसे कि A2, A3, A4 और लेटर, साथ ही कई अन्य कस्टम आकार।

#### क्या मैं .NET के लिए Aspose.Cells के साथ स्प्रेडशीट के कागज़ के आकार को अनुकूलित कर सकता हूँ?

 हां, आप इसका उपयोग करके सटीक चौड़ाई और ऊंचाई आयाम निर्दिष्ट करके एक कस्टम पेपर आकार सेट कर सकते हैं`PaperWidth` और`PaperHeight` के गुण`PageSetup` कक्षा।