---
title: .NET में प्रोग्रामेटिक रूप से CSV को JSON में परिवर्तित करना
linktitle: .NET में प्रोग्रामेटिक रूप से CSV को JSON में परिवर्तित करना
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: Aspose.Cells का उपयोग करके .NET में CSV को JSON में बदलने का तरीका जानें। आसानी से समझ में आने वाले कोड उदाहरणों के साथ डेटा रूपांतरण के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 10
url: /hi/net/converting-excel-files-to-other-formats/converting-csv-to-json/
---
## परिचय
इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके CSV फ़ाइल को JSON फ़ॉर्मेट में बदलने की प्रक्रिया से अवगत कराएँगे। हम सब कुछ आसान चरणों में विभाजित करेंगे ताकि आप इस कार्यक्षमता को अपने प्रोजेक्ट में जल्दी से एकीकृत कर सकें।
## आवश्यक शर्तें
कोड में आगे बढ़ने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
1.  .NET के लिए Aspose.Cells: आपको अपने प्रोजेक्ट में Aspose.Cells इंस्टॉल करना होगा। अगर आपने पहले से ऐसा नहीं किया है, तो आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cells/net/).
2. .NET फ्रेमवर्क या .NET कोर: सुनिश्चित करें कि आपके पास .NET का संगत संस्करण स्थापित है।
3. CSV फ़ाइल: एक नमूना CSV फ़ाइल जिसे आप JSON में बदलना चाहते हैं.
## पैकेज आयात करें
कोडिंग शुरू करने से पहले, Aspose.Cells से आवश्यक नेमस्पेस आयात करना महत्वपूर्ण है। ये आपको अलग-अलग फ़ॉर्मेट में डेटा लोड करने, हेरफेर करने और निर्यात करने की अनुमति देंगे।
```csharp
using Aspose.Cells.Utility;
using System;
using System.IO;
```
आइये इसे चरण दर चरण समझें, ताकि आपको पता चल सके कि यह प्रक्रिया किस प्रकार काम करती है।
## चरण 1: CSV फ़ाइल लोड करें
 पहला चरण आपकी CSV फ़ाइल को एक में लोड करना है`Workbook` ऑब्जेक्ट। यहीं पर Aspose.Cells चमकता है। यह CSV फ़ाइलों को किसी भी अन्य स्प्रेडशीट की तरह व्यवहार करता है, जिससे आपको डेटा में हेरफेर करने की सुविधा मिलती है।
### चरण 1.1: स्रोत निर्देशिका को परिभाषित करें
आपको यह बताना होगा कि आपकी CSV फ़ाइल कहाँ स्थित है। फ़ाइल लोड करने के लिए इस निर्देशिका का उपयोग किया जाएगा।
```csharp
string sourceDir = "Your Document Directory";
```
यह सरल स्ट्रिंग असाइनमेंट उस फ़ोल्डर की ओर इशारा करता है जहां आपकी CSV फ़ाइल स्थित है।
### चरण 1.2: CSV प्रारूप के लिए लोड विकल्प सेट करें
 इसके बाद, हम परिभाषित करते हैं कि Aspose.Cells को फ़ाइल प्रारूप का किस तरह से उपयोग करना चाहिए। CSV फ़ाइलें एक विशिष्ट प्रकार की टेक्स्ट फ़ाइल होती हैं, इसलिए हम सेट करते हैं`LoadFormat` को`Csv` का उपयोग करते हुए`LoadOptions`.
```csharp
LoadOptions loadOptions = new LoadOptions(LoadFormat.Csv);
```
इससे यह सुनिश्चित होता है कि जब हम फ़ाइल लोड करते हैं, तो Aspose.Cells इसे पारंपरिक एक्सेल स्प्रेडशीट के बजाय CSV के रूप में मानता है।
### चरण 1.3: CSV फ़ाइल को कार्यपुस्तिका में लोड करें
 अब, CSV फ़ाइल को लोड करें`Workbook`ऑब्जेक्ट। कार्यपुस्तिका को अपने डेटा कंटेनर के रूप में सोचें, जिसमें CSV फ़ाइल की सामग्री है।
```csharp
Workbook workbook = new Workbook(sourceDir + "SampleCsv.csv", loadOptions);
```
कार्यपुस्तिका अब हेरफेर के लिए तैयार है, जिसमें आपकी CSV से पंक्तियाँ और कॉलम शामिल हैं।
## चरण 2: वर्कशीट में अंतिम सेल की पहचान करें
डेटा को JSON में बदलने के लिए, आपको यह जानना होगा कि CSV में कितना डेटा है। ऐसा करने के लिए, हमें वर्कशीट में आखिरी पॉप्युलेटेड सेल का पता लगाना होगा।
```csharp
Cell lastCell = workbook.Worksheets[0].Cells.LastCell;
```
यह आपकी CSV-लोडेड कार्यपुस्तिका की पहली वर्कशीट में डेटा वाले अंतिम सेल की पहचान करता है।
## चरण 3: निर्यात करने के लिए डेटा रेंज निर्धारित करें
आपको Aspose.Cells को यह बताना होगा कि डेटा की कौन सी रेंज एक्सपोर्ट करनी है। इस मामले में, आप पहले सेल से लेकर पहले पहचाने गए आखिरी सेल तक की पूरी डेटा रेंज का चयन करेंगे।
### चरण 3.1: JSON के लिए निर्यात विकल्प सेट करें
 हम उपयोग करते हैं`ExportRangeToJsonOptions` यह निर्दिष्ट करने के लिए कि हम डेटा को किस तरह निर्यात करना चाहते हैं। यदि आवश्यक हो तो आप इसे और भी कस्टमाइज़ कर सकते हैं, लेकिन अभी के लिए, हम डिफ़ॉल्ट विकल्पों के साथ ही रहेंगे।
```csharp
ExportRangeToJsonOptions options = new ExportRangeToJsonOptions();
```
### चरण 3.2: डेटा की रेंज बनाएं
डेटा की सीमा को प्रारंभिक पंक्ति और स्तंभ (दोनों 0) तथा अंतिम पंक्ति और स्तंभ को अंतिम सेल की स्थिति के आधार पर निर्दिष्ट करके परिभाषित किया जाता है।
```csharp
Range range = workbook.Worksheets[0].Cells.CreateRange(0, 0, lastCell.Row + 1, lastCell.Column + 1);
```
यह श्रेणी निर्यात के लिए तैयार सम्पूर्ण CSV डेटा को कवर करती है।
## चरण 4: रेंज को JSON में बदलें
 डेटा श्रेणी निर्धारित होने के बाद, अगला चरण इस श्रेणी को JSON में परिवर्तित करना है`JsonUtility.ExportRangeToJson()` तरीका।
```csharp
string data = JsonUtility.ExportRangeToJson(range, options);
```
यह फ़ंक्शन निर्दिष्ट श्रेणी से डेटा निकालेगा और उसे JSON स्ट्रिंग में परिवर्तित करेगा।
## चरण 5: JSON डेटा आउटपुट करें
अंत में, आप आवश्यकतानुसार JSON डेटा को प्रिंट या आगे भी संशोधित कर सकते हैं। सरलता के लिए, हम JSON डेटा को कंसोल पर आउटपुट करेंगे।
```csharp
Console.WriteLine(data);
```
## निष्कर्ष
Aspose.Cells का उपयोग करके .NET में CSV फ़ाइल को JSON में बदलना एक सीधी प्रक्रिया है। Aspose.Cells की शक्तिशाली डेटा हेरफेर क्षमताओं का लाभ उठाकर, आप आसानी से CSV जैसे जटिल डेटा प्रारूपों को JSON जैसे अधिक वेब-अनुकूल प्रारूपों में निर्यात कर सकते हैं। यह वेब सेवाओं, API एकीकरण या किसी भी परिदृश्य के लिए एकदम सही है जहाँ JSON डेटा को प्राथमिकता दी जाती है।
## अक्सर पूछे जाने वाले प्रश्न
### क्या Aspose.Cells JSON में रूपांतरण के लिए बड़ी CSV फ़ाइलों को संभाल सकता है?  
हां, Aspose.Cells प्रदर्शन के लिए अनुकूलित है और बड़े डेटासेट को कुशलतापूर्वक संभाल सकता है। आप प्रदर्शन संबंधी समस्याओं में भागे बिना हजारों पंक्तियों वाली CSV फ़ाइलों के साथ काम कर सकते हैं।
### क्या JSON आउटपुट को किसी विशिष्ट तरीके से प्रारूपित करना संभव है?  
 हां`ExportRangeToJsonOptions` क्लास आपको JSON डेटा की संरचना को अनुकूलित करने की अनुमति देता है, जिससे आपको हेडर, फ़ॉर्मेटिंग और अन्य चीज़ों पर नियंत्रण मिलता है।
### क्या मुझे इस रूपांतरण के लिए Aspose.Cells का उपयोग करने के लिए लाइसेंस की आवश्यकता है?  
 आप Aspose.Cells को आज़मा सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/) या आवेदन करें[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) यदि आप इसे खरीदे बिना इसकी पूरी क्षमताएं जानना चाहते हैं।
### क्या मैं इसी पद्धति का उपयोग करके एक्सेल जैसे अन्य प्रारूपों को JSON में परिवर्तित कर सकता हूँ?  
बिल्कुल! Aspose.Cells एक्सेल (XLSX, XLS) सहित विभिन्न प्रारूपों का समर्थन करता है, और आप उन्हें JSON में बदलने के लिए एक समान प्रक्रिया का उपयोग कर सकते हैं।
### क्या Aspose.Cells JSON से CSV या Excel में डेटा परिवर्तित करने का समर्थन करता है?  
हां, Aspose.Cells न केवल JSON में निर्यात करने के लिए बल्कि JSON से डेटा आयात करने के लिए भी पूर्ण लचीलापन प्रदान करता है, जिससे आप आसानी से प्रारूपों के बीच डेटा को बदल सकते हैं।