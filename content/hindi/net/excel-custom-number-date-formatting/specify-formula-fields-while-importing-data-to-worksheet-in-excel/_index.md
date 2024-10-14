---
title: एक्सेल शीट में डेटा आयात करते समय फ़ॉर्मूला फ़ील्ड निर्दिष्ट करें
linktitle: एक्सेल शीट में डेटा आयात करते समय फ़ॉर्मूला फ़ील्ड निर्दिष्ट करें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: इस विस्तृत ट्यूटोरियल में जानें कि .NET के लिए Aspose.Cells का उपयोग करके निर्दिष्ट सूत्र फ़ील्ड के साथ Excel शीट में डेटा कैसे आयात करें।
type: docs
weight: 11
url: /hi/net/excel-custom-number-date-formatting/specify-formula-fields-while-importing-data-to-worksheet-in-excel/
---
## परिचय

जब एक्सेल फ़ाइलों को प्रोग्रामेटिक रूप से संभालने की बात आती है, तो Aspose.Cells for .NET एक अमूल्य उपकरण है। यह एक्सेल स्प्रेडशीट को आसानी से बनाने, संशोधित करने और हेरफेर करने के लिए मजबूत कार्यक्षमता प्रदान करता है। इसकी एक दिलचस्प विशेषता यह है कि यह एक्सेल शीट में डेटा आयात करते समय फ़ॉर्मूला फ़ील्ड निर्दिष्ट करने की क्षमता प्रदान करता है। कल्पना करें कि आप एक वित्तीय रिपोर्ट पर काम कर रहे हैं और उपयोगकर्ता इनपुट के आधार पर कुल योग की स्वचालित गणना करने की आवश्यकता है। यह ट्यूटोरियल आपको एक साफ और सरल दृष्टिकोण के साथ बस इसे प्राप्त करने में चरण-दर-चरण मार्गदर्शन करेगा।

## आवश्यक शर्तें

कोड में गोता लगाने से पहले, आइए सुनिश्चित करें कि आपके पास वह सब कुछ है जो आपको चाहिए। 

1. विज़ुअल स्टूडियो या कोई भी .NET एकीकृत विकास वातावरण (IDE): सुनिश्चित करें कि आपके पास अपना C# कोड लिखने और चलाने के लिए उपयुक्त IDE है।
2. .NET के लिए Aspose.Cells: आपको अपने प्रोजेक्ट में Aspose.Cells लाइब्रेरी को डाउनलोड करके संदर्भित करना होगा। आप इसे यहाँ से डाउनलोड कर सकते हैं[एस्पोज रिलीज](https://releases.aspose.com/cells/net/).
3. बुनियादी C# ज्ञान: C# और ऑब्जेक्ट-ओरिएंटेड प्रोग्रामिंग अवधारणाओं से परिचित होने से आपको उदाहरणों को बेहतर ढंग से समझने में मदद मिलेगी।
4. .NET फ्रेमवर्क: यह ट्यूटोरियल मानता है कि आप .NET फ्रेमवर्क 4.5 या उच्चतर संस्करण का उपयोग कर रहे हैं।

एक बार जब आप आवश्यक शर्तें तय कर लें, तो चलिए निर्दिष्ट सूत्र फ़ील्ड के साथ एक्सेल शीट में कुछ डेटा आयात करने के लिए आगे बढ़ते हैं।

## पैकेज आयात करें

अपना कोड लिखना शुरू करने से पहले, आपको आवश्यक Aspose.Cells नामस्थान आयात करना होगा। यह आमतौर पर आपकी C# फ़ाइल के शीर्ष पर किया जाता है:

```csharp
using Aspose.Cells;
using System;
using System.Collections.Generic;
```

यह आपको Aspose.Cells लाइब्रेरी द्वारा प्रदान की गई कक्षाओं और विधियों का उपयोग करने की अनुमति देता है, बिना उन्हें हर बार नामस्थान के साथ उपसर्ग करने की आवश्यकता के।

आइये पूरी प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें:

## चरण 1: आउटपुट निर्देशिका निर्धारित करें

सबसे पहले, आपको यह तय करना होगा कि आप अपनी एक्सेल फ़ाइल को कहाँ सेव करना चाहते हैं। आप यह कैसे कर सकते हैं:

```csharp
static string outputDir = "Your Document Directory"; // अपनी दस्तावेज़ निर्देशिका यहाँ निर्दिष्ट करें
```

 प्रतिस्थापित करें`"Your Document Directory"` अपने वास्तविक फ़ाइल पथ के साथ। यह वह जगह है जहाँ जेनरेट की गई एक्सेल फ़ाइल सहेजी जाएगी।

## चरण 2: डेटा आइटम के लिए उपयोगकर्ता-परिभाषित क्लास बनाएँ

इसके बाद, हम उस डेटा को संरचित करने के लिए एक क्लास परिभाषित करेंगे जिसे हम आयात करने की योजना बना रहे हैं।

```csharp
class DataItems
{
    public int Number1 { get; set; }
    public int Number2 { get; set; }
    public string Formula1 { get; set; }
    public string Formula2 { get; set; }
}
```

 यह`DataItems` क्लास में कच्चे पूर्णांक और सूत्र होंगे जिन्हें हम एक्सेल शीट में लिखेंगे। 

## चरण 3: डेटा आइटम रखने के लिए सूची आरंभ करें

 हम अपने कई उदाहरणों को रखने के लिए एक सूची का उपयोग करेंगे`DataItems` कक्षा।

```csharp
List<DataItems> dis = new List<DataItems>();
```

## चरण 4: सूची में डेटा आइटम जोड़ें

अब, आइए अपनी सूची में कुछ प्रविष्टियाँ जोड़ें। प्रत्येक प्रविष्टि में दो संख्याएँ और दो सूत्र होंगे।

```csharp
// प्रत्येक डेटा आइटम को परिभाषित करें और जोड़ें
DataItems di = new DataItems();
di.Number1 = 2002;
di.Number2 = 3502;
di.Formula1 = "=SUM(A2,B2)";
di.Formula2 = "=HYPERLINK(\"https://www.aspose.com\",\"Aspose वेबसाइट\")";
dis.Add(di);

// अतिरिक्त डेटा आइटम के लिए दोहराएँ
```

 प्रत्येक को अनुकूलित करना सुनिश्चित करें`DataItems` अद्वितीय मान और सूत्रों के साथ उदाहरण.

## चरण 5: कार्यपुस्तिका और एक्सेस वर्कशीट बनाएँ

इसके बाद, कार्यपुस्तिका बनाएं और पहली कार्यपत्रक तक पहुंचें जहां हम अंततः डेटा आयात करेंगे।

```csharp
Workbook wb = new Workbook(); // एक नई कार्यपुस्तिका बनाएँ
Worksheet ws = wb.Worksheets[0]; // पहली वर्कशीट तक पहुँचें
```

## चरण 6: आयात तालिका विकल्प निर्दिष्ट करें

यहीं पर जादू होता है। आपको यह निर्दिष्ट करना होगा कि आपके डेटा में कौन से फ़ील्ड फ़ार्मुलों से मेल खाते हैं। 

```csharp
ImportTableOptions opts = new ImportTableOptions();
opts.IsFormulas = new bool[] { false, false, true, true };
```

 इस उदाहरण में, अंतिम दो फ़ील्ड में सूत्र हैं, जिन्हें इस प्रकार दर्शाया गया है`true` , जबकि पहले दो फ़ील्ड पर सेट हैं`false`.

## चरण 7: कस्टम ऑब्जेक्ट आयात करें

अब जब सब कुछ सेट हो गया है, तो आइए डेटा आइटम की अपनी सूची को वर्कशीट में आयात करें।

```csharp
ws.Cells.ImportCustomObjects(dis, 0, 0, opts);
```

यह पंक्ति सेल A1 से शुरू होने वाले डेटा को प्रभावी रूप से आयात करती है।

## चरण 8: सूत्रों की गणना करें

चूंकि हमने कुछ सूत्र आयात किए हैं, इसलिए उनकी गणना करना महत्वपूर्ण है।

```csharp
wb.CalculateFormula();
```

यह विधि सुनिश्चित करती है कि आपके सूत्रों का मूल्यांकन उनकी निर्भरता के आधार पर किया जाए।

## चरण 9: कॉलम स्वचालित रूप से फ़िट करें

यह सुनिश्चित करने के लिए कि आपका डेटा प्रदर्शन-अनुकूल है, आप सामग्री के आधार पर कॉलम को स्वचालित रूप से फ़िट कर सकते हैं।

```csharp
ws.AutoFitColumns();
```

यह चरण Excel फ़ाइल के लेआउट को अनुकूलित करता है। 

## चरण 10: अपनी एक्सेल फ़ाइल सहेजें

अंत में, आपकी नई बनाई गई एक्सेल फ़ाइल को सेव करने का समय आ गया है। 

```csharp
wb.Save(outputDir + "outputSpecifyFormulaFieldsWhileImportingDataToWorksheet.xlsx");
```

सुनिश्चित करें कि आपका आउटपुट फ़ाइल नाम प्रासंगिक और वर्णनात्मक है!

## चरण 11: निष्पादन की जाँच करना

यह पुष्टि करने के लिए कि सब कुछ सही ढंग से हुआ है, आप एक संदेश प्रिंट करना चाह सकते हैं।

```csharp
Console.WriteLine("SpecifyFormulaFieldsWhileImportingDataToWorksheet executed successfully.");
```

इससे आपको तुरंत फीडबैक मिल जाता है कि कोड बिना किसी समस्या के काम कर रहा है।

## निष्कर्ष

और अब यह हो गया! आपने .NET के लिए Aspose.Cells का उपयोग करके और निर्दिष्ट फ़ॉर्मूला फ़ील्ड का उपयोग करके Excel शीट में डेटा को सफलतापूर्वक आयात कर लिया है। इन चरणों का पालन करके, आप अपनी ज़रूरतों के अनुसार डेटा प्रोसेसिंग कार्यों को स्वचालित करने के लिए समान तकनीकों को लागू कर सकते हैं। चाहे आप रिपोर्ट के लिए संख्याओं को क्रंच कर रहे हों या केवल डेटा को बनाए रख रहे हों, Aspose के साथ Excel हेरफेर की कला में महारत हासिल करना एक कौशल है।

## अक्सर पूछे जाने वाले प्रश्न

### Aspose.Cells क्या है?
Aspose.Cells एक .NET लाइब्रेरी है जिसे प्रोग्रामेटिक रूप से Excel फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने के लिए डिज़ाइन किया गया है।

### मैं .NET के लिए Aspose.Cells कैसे स्थापित करूं?
 आप इसे यहाँ से डाउनलोड कर सकते हैं[एस्पोज रिलीज](https://releases.aspose.com/cells/net/)और इसे अपने प्रोजेक्ट में संदर्भित करें.

### क्या मैं Aspose.Cells का निःशुल्क उपयोग कर सकता हूँ?
 हाँ, Aspose एक निःशुल्क परीक्षण उपलब्ध कराता है[इस लिंक](https://releases.aspose.com/).

### मैं और अधिक उदाहरण कहां पा सकता हूं?
 अतिरिक्त उदाहरण और दस्तावेज यहां देखे जा सकते हैं[Aspose दस्तावेज़ीकरण पृष्ठ](https://reference.aspose.com/cells/net/).

### यदि मुझे Aspose का उपयोग करते समय कोई समस्या आती है तो क्या होगा?
 आप Aspose सहायता फ़ोरम से सहायता ले सकते हैं[यहाँ](https://forum.aspose.com/c/cells/9).
 