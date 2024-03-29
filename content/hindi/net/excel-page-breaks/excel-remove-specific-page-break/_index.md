---
title: एक्सेल विशिष्ट पृष्ठ विराम हटाएँ
linktitle: एक्सेल विशिष्ट पृष्ठ विराम हटाएँ
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ एक्सेल में एक विशिष्ट पेज ब्रेक को हटाने का तरीका जानें। सटीक संचालन के लिए चरण-दर-चरण ट्यूटोरियल।
type: docs
weight: 30
url: /hi/net/excel-page-breaks/excel-remove-specific-page-break/
---
रिपोर्ट या स्प्रेडशीट के साथ काम करते समय एक्सेल फ़ाइल में विशिष्ट पेज ब्रेक हटाना एक सामान्य कार्य है। इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल फ़ाइल में एक विशिष्ट पेज ब्रेक को हटाने के लिए दिए गए C# स्रोत कोड को समझने और लागू करने के लिए चरण दर चरण मार्गदर्शन करेंगे।

## चरण 1: पर्यावरण तैयार करना

शुरू करने से पहले, सुनिश्चित करें कि आपकी मशीन पर .NET के लिए Aspose.Cells स्थापित है। आप Aspose की आधिकारिक वेबसाइट से लाइब्रेरी डाउनलोड कर सकते हैं और दिए गए निर्देशों का पालन करके इसे इंस्टॉल कर सकते हैं।

एक बार इंस्टॉलेशन पूरा हो जाने पर, अपने पसंदीदा एकीकृत विकास वातावरण (आईडीई) में एक नया सी# प्रोजेक्ट बनाएं और .NET के लिए Aspose.Cells लाइब्रेरी आयात करें।

## चरण 2: दस्तावेज़ निर्देशिका पथ को कॉन्फ़िगर करना

 दिए गए स्रोत कोड में, आपको उस निर्देशिका पथ को निर्दिष्ट करना होगा जहां वह एक्सेल फ़ाइल स्थित है जिसमें वह पेज ब्रेक है जिसे आप हटाना चाहते हैं। संशोधित करें`dataDir` आपकी मशीन पर निर्देशिका के पूर्ण पथ के साथ "आपकी दस्तावेज़ निर्देशिका" को प्रतिस्थापित करके परिवर्तनीय।

```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## चरण 3: एक कार्यपुस्तिका ऑब्जेक्ट बनाना

आरंभ करने के लिए, हमें एक वर्कबुक ऑब्जेक्ट बनाना होगा जो हमारी एक्सेल फ़ाइल का प्रतिनिधित्व करता है। वर्कबुक क्लास कंस्ट्रक्टर का उपयोग करें और खोलने के लिए एक्सेल फ़ाइल का पूरा पथ निर्दिष्ट करें।

```csharp
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook(dataDir + "PageBreaks.xls");
```

## चरण 4: विशिष्ट पृष्ठ विराम हटाएँ

 अब हम अपनी एक्सेल वर्कशीट में विशिष्ट पेज ब्रेक को हटाने जा रहे हैं। नमूना कोड में, हम इसका उपयोग करते हैं`RemoveAt()` पहले क्षैतिज और ऊर्ध्वाधर पृष्ठ विराम को हटाने की विधियाँ।

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.RemoveAt(0);
workbook.Worksheets[0].VerticalPageBreaks.RemoveAt(0);
```

## चरण 5: एक्सेल फ़ाइल को सहेजना

 एक बार जब विशिष्ट पृष्ठ विराम हटा दिया जाता है, तो हम अंतिम एक्सेल फ़ाइल को सहेज सकते हैं। उपयोग`Save()` आउटपुट फ़ाइल का पूरा पथ निर्दिष्ट करने की विधि।

```csharp
// एक्सेल फ़ाइल सहेजें.
workbook.Save(dataDir + "RemoveSpecificPageBreak_out.xls");
```

### एक्सेल के लिए नमूना स्रोत कोड .NET के लिए Aspose.Cells का उपयोग करके विशिष्ट पेज ब्रेक निकालें 
```csharp

//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook(dataDir + "PageBreaks.xls");
// एक विशिष्ट पृष्ठ विराम हटा रहा है
workbook.Worksheets[0].HorizontalPageBreaks.RemoveAt(0);
workbook.Worksheets[0].VerticalPageBreaks.RemoveAt(0);
// एक्सेल फ़ाइल सहेजें.
workbook.Save(dataDir + "RemoveSpecificPageBreak_out.xls");

```

## निष्कर्ष

इस ट्यूटोरियल में, हमने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल फ़ाइल में एक विशिष्ट पेज ब्रेक को कैसे हटाया जाए। दिए गए चरणों का पालन करके, आप अपनी गतिशील रूप से जेनरेट की गई एक्सेल फ़ाइलों में अवांछित पेज ब्रेक को आसानी से प्रबंधित और हटा सकते हैं। वह मत करो

कृपया अधिक उन्नत संचालन के लिए Aspose.Cells द्वारा दी जाने वाली सुविधाओं के बारे में और जानने के लिए स्वतंत्र महसूस करें।


### पूछे जाने वाले प्रश्न

#### प्रश्न: क्या किसी विशिष्ट पेज ब्रेक को हटाने से एक्सेल फ़ाइल में अन्य पेज ब्रेक प्रभावित होते हैं?
 
उ: नहीं, किसी विशिष्ट पेज ब्रेक को हटाने से एक्सेल वर्कशीट में मौजूद अन्य पेज ब्रेक प्रभावित नहीं होते हैं।

#### प्रश्न: क्या मैं एक साथ अनेक विशिष्ट पृष्ठ विराम हटा सकता हूँ?

 उत्तर: हाँ, आप इसका उपयोग कर सकते हैं`RemoveAt()` की विधि`HorizontalPageBreaks` और`VerticalPageBreaks` एक ऑपरेशन में कई विशिष्ट पेज ब्रेक को हटाने के लिए क्लास।

#### प्रश्न: .NET के लिए Aspose.Cells द्वारा कौन से अन्य एक्सेल फ़ाइल प्रारूप समर्थित हैं?

उ: .NET के लिए Aspose.Cells विभिन्न एक्सेल फ़ाइल स्वरूपों का समर्थन करता है, जैसे XLSX, XLSM, CSV, HTML, PDF, आदि।

#### प्रश्न: क्या मैं विशिष्ट पृष्ठ विराम को हटाने के बाद एक्सेल फ़ाइल को किसी अन्य प्रारूप में सहेज सकता हूँ?

उत्तर: हाँ, .NET के लिए Aspose.Cells आपको अपनी आवश्यकताओं के अनुसार Excel फ़ाइल को विभिन्न स्वरूपों में सहेजने की अनुमति देता है।