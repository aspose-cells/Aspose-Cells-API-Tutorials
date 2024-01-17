---
title: पृष्ठ आयाम प्राप्त करें
linktitle: पृष्ठ आयाम प्राप्त करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके Excel में पृष्ठ आयाम पुनर्प्राप्त करना सीखें। C# में स्रोत कोड के साथ चरण दर चरण मार्गदर्शिका।
type: docs
weight: 40
url: /hi/net/excel-page-setup/get-page-dimensions/
---
.NET के लिए Aspose.Cells एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को Microsoft Excel फ़ाइलों के साथ प्रोग्रामेटिक रूप से काम करने की अनुमति देती है। यह एक्सेल दस्तावेज़ों में हेरफेर करने के लिए सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है, जिसमें पृष्ठ आयाम प्राप्त करने की क्षमता भी शामिल है। इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके पृष्ठ आयाम पुनर्प्राप्त करने के चरणों के बारे में बताएंगे।

## चरण 1: कार्यपुस्तिका वर्ग का एक उदाहरण बनाएं

आरंभ करने के लिए, हमें वर्कबुक क्लास का एक उदाहरण बनाना होगा, जो एक्सेल वर्कबुक का प्रतिनिधित्व करता है। इसे निम्नलिखित कोड का उपयोग करके प्राप्त किया जा सकता है:

```csharp
Workbook book = new Workbook();
```

## चरण 2: स्प्रेडशीट तक पहुँचना

इसके बाद, हमें कार्यपुस्तिका में कार्यपत्रक पर नेविगेट करना होगा जहां हम पृष्ठ आयाम सेट करना चाहते हैं। इस उदाहरण में, मान लीजिए हम पहली वर्कशीट के साथ काम करना चाहते हैं। हम निम्नलिखित कोड का उपयोग करके इसे एक्सेस कर सकते हैं:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## चरण 3: कागज का आकार A2 पर सेट करें और चौड़ाई और ऊंचाई इंच में प्रिंट करें

अब हम पेपर का आकार A2 पर सेट करेंगे और पेज की चौड़ाई और ऊंचाई इंच में प्रिंट करेंगे। इसे निम्नलिखित कोड का उपयोग करके प्राप्त किया जा सकता है:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## चरण 4: कागज का आकार A3 पर सेट करें और चौड़ाई और ऊंचाई इंच में प्रिंट करें

इसके बाद, हम कागज़ का आकार A3 पर सेट करेंगे और पृष्ठ की चौड़ाई और ऊंचाई इंच में प्रिंट करेंगे। यहाँ संबंधित कोड है:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## चरण 5: कागज का आकार A4 पर सेट करें और चौड़ाई और ऊंचाई इंच में प्रिंट करें

अब हम कागज़ का आकार A4 पर सेट करेंगे और पृष्ठ की चौड़ाई और ऊंचाई इंच में प्रिंट करेंगे। यहाँ कोड है:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## चरण 6: कागज़ का आकार लेटर पर सेट करें और चौड़ाई और ऊंचाई इंच में प्रिंट करें

अंत में, हम कागज़ का आकार लेटर पर सेट करेंगे और पृष्ठ की चौड़ाई और ऊंचाई इंच में प्रिंट करेंगे। यहाँ कोड है:

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### .NET के लिए Aspose.Cells का उपयोग करके पृष्ठ आयाम प्राप्त करने के लिए नमूना स्रोत कोड 
```csharp
// वर्कबुक क्लास का एक उदाहरण बनाएं
Workbook book = new Workbook();
// पहली वर्कशीट तक पहुंचें
Worksheet sheet = book.Worksheets[0];
// कागज का आकार A2 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// कागज का आकार A3 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// कागज का आकार A4 पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
// कागज का आकार अक्षर पर सेट करें और कागज की चौड़ाई और ऊंचाई इंच में प्रिंट करें
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## निष्कर्ष

बधाई हो! आपने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके पृष्ठ आयाम कैसे प्राप्त करें। यह सुविधा तब उपयोगी हो सकती है जब आपको अपनी Excel फ़ाइलों में पृष्ठ आयामों के आधार पर विशिष्ट संचालन करने की आवश्यकता होती है।

इसके द्वारा प्रदान की जाने वाली सभी शक्तिशाली सुविधाओं को खोजने के लिए Aspose.Cells के दस्तावेज़ीकरण को और अधिक जांचना न भूलें।

### अक्सर पूछे जाने वाले प्रश्न

#### 1. .NET के लिए Aspose.Cells अन्य कौन से आकार के कागज़ का समर्थन करता है?

.NET के लिए Aspose.Cells A1, A5, B4, B5, कार्यकारी, कानूनी, पत्र और कई अन्य सहित विभिन्न प्रकार के पेपर आकारों का समर्थन करता है। आप समर्थित पेपर आकारों की पूरी सूची के लिए दस्तावेज़ की जांच कर सकते हैं।

#### 2. क्या मैं .NET के लिए Aspose.Cells के साथ कस्टम पेज आयाम सेट कर सकता हूँ?

हां, आप वांछित चौड़ाई और ऊंचाई निर्दिष्ट करके कस्टम पेज आयाम सेट कर सकते हैं। Aspose.Cells आपकी आवश्यकताओं के अनुसार पृष्ठ आयामों को अनुकूलित करने के लिए पूर्ण लचीलापन प्रदान करता है।

#### 3. क्या मुझे इंच के अलावा अन्य इकाइयों में पृष्ठ आयाम मिल सकते हैं?

हाँ, .NET के लिए Aspose.Cells आपको इंच, सेंटीमीटर, मिलीमीटर और पॉइंट सहित विभिन्न इकाइयों में पृष्ठ आयाम प्राप्त करने की अनुमति देता है।

#### 4. क्या .NET के लिए Aspose.Cells अन्य पेज सेटिंग्स संपादन सुविधाओं का समर्थन करता है?

हां, Aspose.Cells पेज सेटिंग्स को संपादित करने के लिए सुविधाओं की एक पूरी श्रृंखला प्रदान करता है, जिसमें मार्जिन, ओरिएंटेशन, हेडर और फ़ुटर इत्यादि सेट करना शामिल है।