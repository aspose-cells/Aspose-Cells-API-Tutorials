---
title: एक्सेल मार्जिन सेट करें
linktitle: एक्सेल मार्जिन सेट करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: जानें कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल में मार्जिन कैसे सेट करें। C# में चरण दर चरण ट्यूटोरियल।
type: docs
weight: 110
url: /hi/net/excel-page-setup/set-excel-margins/
---
इस ट्यूटोरियल में, हम आपको चरण दर चरण बताएंगे कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल में मार्जिन कैसे सेट करें। हम प्रक्रिया को स्पष्ट करने के लिए C# स्रोत कोड का उपयोग करेंगे।

## चरण 1: वातावरण स्थापित करना

सुनिश्चित करें कि आपकी मशीन पर .NET के लिए Aspose.Cells स्थापित है। अपने पसंदीदा विकास परिवेश में एक नया प्रोजेक्ट भी बनाएं।

## चरण 2: आवश्यक पुस्तकालय आयात करें

अपनी कोड फ़ाइल में, Aspose.Cells के साथ काम करने के लिए आवश्यक लाइब्रेरी आयात करें। यहाँ संबंधित कोड है:

```csharp
using Aspose.Cells;
```

## चरण 3: डेटा निर्देशिका सेट करें

वह डेटा निर्देशिका सेट करें जहां आप संशोधित एक्सेल फ़ाइल को सहेजना चाहते हैं। निम्नलिखित कोड का प्रयोग करें:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

संपूर्ण निर्देशिका पथ निर्दिष्ट करना सुनिश्चित करें.

## चरण 4: कार्यपुस्तिका और कार्यपत्रक बनाना

एक नई वर्कबुक ऑब्जेक्ट बनाएं और निम्नलिखित कोड का उपयोग करके वर्कबुक में पहली वर्कशीट पर नेविगेट करें:

```csharp
Workbook workbook = new Workbook();
WorksheetCollection worksheets = workbook. Worksheets;
Worksheet worksheet = worksheets[0];
```

यह एक वर्कशीट के साथ एक खाली वर्कबुक बनाएगा और उस वर्कशीट तक पहुंच प्रदान करेगा।

## चरण 5: मार्जिन सेट करना

वर्कशीट के पेजसेटअप ऑब्जेक्ट तक पहुंचें और बॉटममार्जिन, लेफ्टमार्जिन, राइटमार्जिन और टॉपमार्जिन गुणों का उपयोग करके मार्जिन सेट करें। यहाँ एक नमूना कोड है:

```csharp
PageSetup pageSetup = worksheet.PageSetup;
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
```

यह वर्कशीट के क्रमशः नीचे, बाएँ, दाएँ और शीर्ष हाशिये को सेट करेगा।

## चरण 6: संशोधित कार्यपुस्तिका को सहेजना

निम्नलिखित कोड का उपयोग करके संशोधित कार्यपुस्तिका सहेजें:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

यह संशोधित कार्यपुस्तिका को निर्दिष्ट डेटा निर्देशिका में सहेज लेगा।

### .NET के लिए Aspose.Cells का उपयोग करके एक्सेल मार्जिन सेट करने के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// एक कार्यपुस्तिका ऑब्जेक्ट बनाएं
Workbook workbook = new Workbook();
// कार्यपुस्तिका में कार्यपत्रक प्राप्त करें
WorksheetCollection worksheets = workbook.Worksheets;
// पहली (डिफ़ॉल्ट) वर्कशीट प्राप्त करें
Worksheet worksheet = worksheets[0];
// पेजसेटअप ऑब्जेक्ट प्राप्त करें
PageSetup pageSetup = worksheet.PageSetup;
// नीचे, बाएँ, दाएँ और शीर्ष पृष्ठ मार्जिन सेट करें
pageSetup.BottomMargin = 2;
pageSetup.LeftMargin = 1;
pageSetup.RightMargin = 1;
pageSetup.TopMargin = 3;
// कार्यपुस्तिका सहेजें.
workbook.Save(dataDir + "SetMargins_out.xls");
```

## निष्कर्ष

अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके Excel में मार्जिन कैसे सेट करें। इस ट्यूटोरियल ने आपको पर्यावरण की स्थापना से लेकर संशोधित कार्यपुस्तिका को सहेजने तक प्रक्रिया के हर चरण के बारे में बताया। अपनी Excel फ़ाइलों में और अधिक हेरफेर करने के लिए Aspose.Cells की विशेषताओं को और अधिक जानने के लिए स्वतंत्र महसूस करें।

### अक्सर पूछे जाने वाले प्रश्न (अक्सर पूछे जाने वाले प्रश्न)

#### 1. मैं अपनी स्प्रैडशीट के लिए कस्टम मार्जिन कैसे निर्दिष्ट कर सकता हूं?

 आप का उपयोग करके कस्टम मार्जिन निर्दिष्ट कर सकते हैं`BottomMargin`, `LeftMargin`, `RightMargin` , और`TopMargin` के गुण`PageSetup` वस्तु। आवश्यकतानुसार मार्जिन को समायोजित करने के लिए बस प्रत्येक संपत्ति के लिए वांछित मान निर्धारित करें।

#### 2. क्या मैं एक ही कार्यपुस्तिका में विभिन्न कार्यपत्रकों के लिए अलग-अलग मार्जिन सेट कर सकता हूँ?

 हां, आप एक ही कार्यपुस्तिका में प्रत्येक कार्यपत्रक के लिए अलग-अलग मार्जिन सेट कर सकते हैं। बस पहुंचें`PageSetup` प्रत्येक वर्कशीट का ऑब्जेक्ट अलग-अलग बनाएं और प्रत्येक के लिए विशिष्ट मार्जिन सेट करें।

#### 3. क्या परिभाषित मार्जिन कार्यपुस्तिका की छपाई पर भी लागू होते हैं?

हां, Aspose.Cells का उपयोग करके सेट किए गए मार्जिन कार्यपुस्तिका को प्रिंट करते समय भी लागू होते हैं। कार्यपुस्तिका का मुद्रित आउटपुट तैयार करते समय निर्दिष्ट मार्जिन को ध्यान में रखा जाएगा।

#### 4. क्या मैं Aspose.Cells का उपयोग करके मौजूदा Excel फ़ाइल का मार्जिन बदल सकता हूँ?

 हां, आप Aspose.Cells के साथ फ़ाइल लोड करके, प्रत्येक वर्कशीट तक पहुंच कर मौजूदा एक्सेल फ़ाइल के मार्जिन को बदल सकते हैं`PageSetup` ऑब्जेक्ट, और मार्जिन गुणों के मान को बदलना। फिर नए मार्जिन लागू करने के लिए संशोधित फ़ाइल को सहेजें।

#### 5. मैं स्प्रेडशीट से मार्जिन कैसे हटाऊं?

 वर्कशीट से मार्जिन हटाने के लिए, आप बस इसके मान सेट कर सकते हैं`BottomMargin`, `LeftMargin`, `RightMargin` और`TopMargin` गुण शून्य पर. यह मार्जिन को उनके डिफ़ॉल्ट (आमतौर पर शून्य) पर रीसेट कर देगा।