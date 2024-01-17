---
title: एक्सेल पेज ऑर्डर सेट करें
linktitle: एक्सेल पेज ऑर्डर सेट करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके एक्सेल में पेज ऑर्डर सेट करने के लिए चरण-दर-चरण मार्गदर्शिका। विस्तृत निर्देश और स्रोत कोड शामिल हैं।
type: docs
weight: 120
url: /hi/net/excel-page-setup/set-excel-page-order/
---
इस लेख में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके एक्सेल पेज ऑर्डर सेट करने के लिए निम्नलिखित C# स्रोत कोड को समझाने के लिए चरण दर चरण मार्गदर्शन करेंगे। हम आपको दिखाएंगे कि दस्तावेज़ निर्देशिका कैसे सेट करें, वर्कबुक ऑब्जेक्ट को तुरंत चालू करें, पेजसेटअप संदर्भ प्राप्त करें, पेज प्रिंट ऑर्डर सेट करें और वर्कबुक को सहेजें।

## चरण 1: दस्तावेज़ निर्देशिका सेटअप

 शुरू करने से पहले, आपको दस्तावेज़ निर्देशिका को कॉन्फ़िगर करना होगा जहां आप एक्सेल फ़ाइल को सहेजना चाहते हैं। आप के मान को प्रतिस्थापित करके निर्देशिका पथ निर्दिष्ट कर सकते हैं`dataDir` अपने पथ के साथ परिवर्तनशील।

```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## चरण 2: किसी कार्यपुस्तिका ऑब्जेक्ट को इंस्टेंट करना

पहला कदम वर्कबुक ऑब्जेक्ट को इंस्टेंट करना है। यह उस एक्सेल वर्कबुक का प्रतिनिधित्व करता है जिसके साथ हम काम करेंगे।

```csharp
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करें
Workbook workbook = new Workbook();
```

## चरण 3: पेजसेटअप संदर्भ प्राप्त करना

इसके बाद, हमें उस वर्कशीट का पेजसेटअप ऑब्जेक्ट संदर्भ प्राप्त करना होगा जिस पर हम पेज ऑर्डर सेट करना चाहते हैं।

```csharp
// वर्कशीट का पेजसेटअप संदर्भ प्राप्त करें
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## चरण 4: पेजों का प्रिंट ऑर्डर सेट करना

अब हम पृष्ठों का मुद्रण क्रम निर्धारित कर सकते हैं। इस उदाहरण में, हम "OverThenDown" विकल्प का उपयोग कर रहे हैं, जिसका अर्थ है कि पेज बाएं से दाएं, फिर ऊपर से नीचे मुद्रित होंगे।

```csharp
// पेज प्रिंट ऑर्डर को "OverThenDown" पर सेट करें
pageSetup.Order = PrintOrderType.OverThenDown;
```

## चरण 5: कार्यपुस्तिका सहेजना

अंत में, हम एक्सेल वर्कबुक को पेज ऑर्डर परिवर्तन के साथ सहेजते हैं।

```csharp
// कार्यपुस्तिका सहेजें
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### .NET के लिए Aspose.Cells का उपयोग करके एक्सेल पेज ऑर्डर सेट करने के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook();
// वर्कशीट के पेजसेटअप का संदर्भ प्राप्त करना
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// पृष्ठों के मुद्रण क्रम को ऊपर से नीचे पर सेट करना
pageSetup.Order = PrintOrderType.OverThenDown;
// कार्यपुस्तिका सहेजें.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने समझाया कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल फ़ाइल में पेज ऑर्डर कैसे सेट करें। दिए गए चरणों का पालन करके, आप आसानी से दस्तावेज़ निर्देशिका को कॉन्फ़िगर कर सकते हैं, वर्कबुक ऑब्जेक्ट को तुरंत चालू कर सकते हैं, पेजसेटअप संदर्भ प्राप्त कर सकते हैं, पेज प्रिंट ऑर्डर सेट कर सकते हैं और वर्कबुक को सहेज सकते हैं।

### अक्सर पूछे जाने वाले प्रश्न

#### Q1: एक्सेल फ़ाइल में पेज ऑर्डर सेट करना क्यों महत्वपूर्ण है?

एक्सेल फ़ाइल में पृष्ठों के क्रम को परिभाषित करना महत्वपूर्ण है क्योंकि यह निर्धारित करता है कि पेज कैसे मुद्रित या प्रदर्शित किए जाएंगे। एक विशिष्ट क्रम निर्दिष्ट करके, आप डेटा को तार्किक रूप से व्यवस्थित कर सकते हैं और फ़ाइल को पढ़ने या प्रिंट करने में आसान बना सकते हैं।

#### Q2: क्या मैं .NET के लिए Aspose.Cells के साथ अन्य पेज प्रिंट ऑर्डर का उपयोग कर सकता हूँ?

हां, .NET के लिए Aspose.Cells कई पेज प्रिंट ऑर्डर का समर्थन करता है जैसे "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", आदि। आप वह चुन सकते हैं जो आपकी आवश्यकताओं के लिए सबसे उपयुक्त हो।

#### Q3: क्या मैं .NET के लिए Aspose.Cells के साथ पृष्ठों को प्रिंट करने के लिए अतिरिक्त विकल्प सेट कर सकता हूँ?

हां, आप .NET के लिए Aspose.Cells में पेजसेटअप ऑब्जेक्ट के गुणों का उपयोग करके विभिन्न पेज प्रिंटिंग विकल्प जैसे स्केल, ओरिएंटेशन, मार्जिन इत्यादि सेट कर सकते हैं।

#### Q4: क्या .NET के लिए Aspose.Cells अन्य Excel फ़ाइल स्वरूपों का समर्थन करता है?

हां, .NET के लिए Aspose.Cells XLSX, XLS, CSV, HTML, PDF इत्यादि जैसे एक्सेल फ़ाइल स्वरूपों की एक विस्तृत श्रृंखला का समर्थन करता है। आप लाइब्रेरी द्वारा प्रदान की गई सुविधाओं का उपयोग करके इन प्रारूपों के बीच आसानी से कनवर्ट कर सकते हैं।