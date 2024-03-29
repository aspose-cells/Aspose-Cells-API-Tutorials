---
title: एक्सेल सभी पेज ब्रेक साफ़ करें
linktitle: एक्सेल सभी पेज ब्रेक साफ़ करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: जानें कि .NET के लिए Aspose.Cells के साथ एक्सेल में सभी पेज ब्रेक कैसे हटाएं। अपनी Excel फ़ाइलों को साफ़ करने के लिए चरण दर चरण ट्यूटोरियल।
type: docs
weight: 20
url: /hi/net/excel-page-breaks/excel-clear-all-page-breaks/
---

रिपोर्ट या स्प्रेडशीट को संभालते समय एक्सेल फ़ाइल में पेज ब्रेक हटाना एक आवश्यक कदम है। इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल फ़ाइल में सभी पेज ब्रेक को हटाने के लिए दिए गए C# स्रोत कोड को समझने और लागू करने के लिए चरण दर चरण मार्गदर्शन करेंगे।

## चरण 1: पर्यावरण तैयार करना

 शुरू करने से पहले, सुनिश्चित करें कि आपकी मशीन पर .NET के लिए Aspose.Cells स्थापित है। आप लाइब्रेरी को यहां से डाउनलोड कर सकते हैं[एस्पोज़ रिलीज़](https://releases.aspose.com/cells/net)और दिए गए निर्देशों का पालन करके इसे इंस्टॉल करें।

एक बार इंस्टॉलेशन पूरा हो जाने पर, अपने पसंदीदा एकीकृत विकास वातावरण (आईडीई) में एक नया सी# प्रोजेक्ट बनाएं और .NET के लिए Aspose.Cells लाइब्रेरी आयात करें।

## चरण 2: दस्तावेज़ निर्देशिका पथ को कॉन्फ़िगर करना

 दिए गए स्रोत कोड में, आपको उस निर्देशिका पथ को निर्दिष्ट करना होगा जहां आप जेनरेट की गई एक्सेल फ़ाइल को सहेजना चाहते हैं। संशोधित करें`dataDir` आपकी मशीन पर निर्देशिका के पूर्ण पथ के साथ "आपकी दस्तावेज़ निर्देशिका" को प्रतिस्थापित करके परिवर्तनीय।

```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## चरण 3: एक कार्यपुस्तिका ऑब्जेक्ट बनाना

आरंभ करने के लिए, हमें एक वर्कबुक ऑब्जेक्ट बनाना होगा जो हमारी एक्सेल फ़ाइल का प्रतिनिधित्व करता है। इसे Aspose.Cells द्वारा प्रदान की गई वर्कबुक क्लास का उपयोग करके प्राप्त किया जा सकता है।

```csharp
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook();
```

## चरण 4: पृष्ठ विराम हटाएँ

 अब हम अपनी एक्सेल वर्कशीट में सभी पेज ब्रेक हटाने जा रहे हैं। नमूना कोड में, हम इसका उपयोग करते हैं`Clear()` उन सभी को हटाने के लिए क्षैतिज और ऊर्ध्वाधर पृष्ठ विराम की विधियाँ।

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
```

## चरण 5: एक्सेल फ़ाइल को सहेजना

 एक बार सभी पेज ब्रेक हटा दिए जाने के बाद, हम अंतिम एक्सेल फ़ाइल को सहेज सकते हैं। उपयोग`Save()` आउटपुट फ़ाइल का पूरा पथ निर्दिष्ट करने की विधि।

```csharp
// एक्सेल फ़ाइल सहेजें.
workbook.Save(dataDir + "ClearingPageBreaks_out.xls");
```

### एक्सेल के लिए नमूना स्रोत कोड .NET के लिए Aspose.Cells का उपयोग करके सभी पेज ब्रेक साफ़ करें 

```csharp

//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook();
// सभी पृष्ठ विराम साफ़ किया जा रहा है
workbook.Worksheets[0].HorizontalPageBreaks.Clear();
workbook.Worksheets[0].VerticalPageBreaks.Clear();
// एक्सेल फ़ाइल सहेजें.
workbook.Save(dataDir + "ClearAllPageBreaks_out.xls");

```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके Excel फ़ाइल में सभी पेज ब्रेक को कैसे हटाया जाए। दिए गए चरणों का पालन करके, आप अपनी गतिशील रूप से जेनरेट की गई एक्सेल फ़ाइलों में अवांछित पेज ब्रेक को आसानी से प्रबंधित और साफ़ कर सकते हैं। अधिक उन्नत संचालन के लिए Aspose.Cells द्वारा दी जाने वाली सुविधाओं के बारे में जानने के लिए स्वतंत्र महसूस करें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: क्या .NET के लिए Aspose.Cells एक निःशुल्क लाइब्रेरी है?

उ: .NET के लिए Aspose.Cells एक व्यावसायिक लाइब्रेरी है, लेकिन यह एक निःशुल्क परीक्षण संस्करण प्रदान करता है जिसका उपयोग आप इसकी कार्यक्षमता का मूल्यांकन करने के लिए कर सकते हैं।

#### प्रश्न: क्या पृष्ठ विराम हटाने से अन्य कार्यपत्रक तत्व प्रभावित होते हैं?

उत्तर: नहीं, पेज ब्रेक को हटाने से केवल पेज ब्रेक में परिवर्तन होता है और वर्कशीट में किसी भी अन्य डेटा या फ़ॉर्मेटिंग पर कोई प्रभाव नहीं पड़ता है।

#### प्रश्न: क्या मैं एक्सेल में कुछ विशिष्ट पेज ब्रेक को चुनिंदा रूप से हटा सकता हूँ?

उत्तर: हां, Aspose.Cells के साथ आप व्यक्तिगत रूप से प्रत्येक पेज ब्रेक तक पहुंच सकते हैं और यदि आवश्यक हो तो उचित तरीकों का उपयोग करके इसे हटा सकते हैं।

#### प्रश्न: .NET के लिए Aspose.Cells द्वारा कौन से अन्य एक्सेल फ़ाइल प्रारूप समर्थित हैं?

उ: .NET के लिए Aspose.Cells विभिन्न एक्सेल फ़ाइल स्वरूपों का समर्थन करता है, जैसे XLSX, XLSM, CSV, HTML, PDF, आदि।

