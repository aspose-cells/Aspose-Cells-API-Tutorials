---
title: एक्सेल में प्रोग्रामेटिक रूप से बॉर्डर सेट करना
linktitle: एक्सेल में प्रोग्रामेटिक रूप से बॉर्डर सेट करना
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके Excel में प्रोग्रामेटिक रूप से बॉर्डर सेट करना सीखें। समय बचाएँ और अपने Excel कार्यों को स्वचालित करें।
type: docs
weight: 10
url: /hi/net/excel-borders-and-formatting-options/setting-border/
---
## परिचय

क्या आप अपनी एक्सेल शीट में मैन्युअल रूप से बॉर्डर सेट करने से थक गए हैं? आप अकेले नहीं हैं! बॉर्डर सेट करना एक थकाऊ काम हो सकता है, खासकर जब आप बड़े डेटासेट से निपट रहे हों। लेकिन डरो मत! .NET के लिए Aspose.Cells के साथ, आप इस प्रक्रिया को स्वचालित कर सकते हैं, जिससे आपका समय और प्रयास बचता है। इस ट्यूटोरियल में, हम एक्सेल वर्कबुक में प्रोग्रामेटिक रूप से बॉर्डर सेट करने की बारीकियों पर चर्चा करेंगे। चाहे आप एक अनुभवी डेवलपर हों या अभी शुरुआत कर रहे हों, आपको यह गाइड अनुसरण करने में आसान और मददगार जानकारी से भरपूर लगेगी।

तो, क्या आप अपने एक्सेल ऑटोमेशन कौशल को बढ़ाने के लिए तैयार हैं? चलिए शुरू करते हैं!

## आवश्यक शर्तें

आरंभ करने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ हैं:

1.  विज़ुअल स्टूडियो: आपके मशीन पर विज़ुअल स्टूडियो इंस्टॉल होना चाहिए। अगर नहीं है, तो इसे यहाँ से डाउनलोड करें[यहाँ](https://visualstudio.microsoft.com/downloads/).
2.  .NET के लिए Aspose.Cells: आपके पास Aspose.Cells लाइब्रेरी होनी चाहिए। आप इसे DLL डाउनलोड करके प्राप्त कर सकते हैं[इस लिंक](https://releases.aspose.com/cells/net/) या अपने प्रोजेक्ट में NuGet का उपयोग करके:
```bash
Install-Package Aspose.Cells
```
3. बुनियादी C# ज्ञान: C# प्रोग्रामिंग से परिचित होने से आपको कोड को बेहतर ढंग से समझने में मदद मिलेगी।
4. विकास वातावरण: एक कंसोल अनुप्रयोग या कोई भी प्रोजेक्ट प्रकार सेट करें जहां आप C# कोड चला सकें।

एक बार जब आप सब कुछ सेट कर लें, तो हम मज़ेदार भाग की ओर बढ़ सकते हैं: कोडिंग!

## पैकेज आयात करें

अब जब हमारे पास सब कुछ है, तो चलिए अपनी C# फ़ाइल में आवश्यक नेमस्पेस आयात करते हैं। अपनी कोड फ़ाइल के शीर्ष पर, निम्न जोड़ें:

```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```

ये नामस्थान आपको Aspose.Cells की कार्यात्मकताओं और System.Drawing नामस्थान की रंग कार्यात्मकताओं तक पहुंच प्रदान करते हैं।

## चरण 1: अपनी दस्तावेज़ निर्देशिका निर्धारित करें

सबसे पहले, हमें यह निर्दिष्ट करना होगा कि हमारी एक्सेल फ़ाइल कहाँ सहेजी जाएगी। अपने दस्तावेज़ निर्देशिका का पथ परिभाषित करें:

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
```

 प्रतिस्थापित करें`"Your Document Directory"` उस वास्तविक पथ के साथ जहां आप अपनी एक्सेल फ़ाइल को सहेजना चाहते हैं। 

## चरण 2: वर्कबुक ऑब्जेक्ट बनाएँ

 इसके बाद, आइए इसका एक उदाहरण बनाएं`Workbook` क्लास. यह हमारी एक्सेल वर्कबुक का प्रतिनिधित्व करेगा.

```csharp
// वर्कबुक ऑब्जेक्ट को इंस्टैंशिएट करना
Workbook workbook = new Workbook();
Worksheet sheet = workbook.Worksheets[0];
```

यहाँ, हम अपनी कार्यपुस्तिका में पहली वर्कशीट तक भी पहुँच रहे हैं। बहुत आसान!

## चरण 3: सशर्त स्वरूपण जोड़ें

अब हम कुछ सशर्त स्वरूपण जोड़ेंगे। यह हमें यह निर्दिष्ट करने की अनुमति देता है कि किन कोशिकाओं में कुछ शर्तों के आधार पर सीमाएँ होंगी। 

```csharp
// एक रिक्त सशर्त स्वरूपण जोड़ता है
int index = sheet.ConditionalFormattings.Add();
FormatConditionCollection fcs = sheet.ConditionalFormattings[index];
```

## चरण 4: सशर्त प्रारूप सीमा निर्धारित करें

आइए उन कक्षों की श्रेणी निर्धारित करें जिन पर हम सशर्त स्वरूपण लागू करना चाहते हैं। इस मामले में, हम एक ऐसी श्रेणी के साथ काम कर रहे हैं जो पंक्तियों 0 से 5 और स्तंभ 0 से 3 को कवर करती है:

```csharp
// सशर्त प्रारूप सीमा निर्धारित करता है.
CellArea ca = new CellArea();
ca.StartRow = 0;
ca.EndRow = 5;
ca.StartColumn = 0;
ca.EndColumn = 3;
fcs.AddArea(ca);
```

## चरण 5: एक शर्त जोड़ें

अब, हम अपने फ़ॉर्मेटिंग में एक शर्त जोड़ेंगे। इस उदाहरण में, हम फ़ॉर्मेटिंग को उन कक्षों पर लागू करेंगे जिनमें 50 और 100 के बीच मान हैं:

```csharp
// शर्त जोड़ता है.
int conditionIndex = fcs.AddCondition(FormatConditionType.CellValue, OperatorType.Between, "50", "100");
```

## चरण 6: बॉर्डर शैलियाँ अनुकूलित करें

हमारी शर्त सेट होने के बाद, अब हम बॉर्डर स्टाइल को कस्टमाइज़ कर सकते हैं। यहाँ बताया गया है कि हम सभी चार बॉर्डर को डैश्ड कैसे सेट कर सकते हैं:

```csharp
// पृष्ठभूमि का रंग सेट करता है.
FormatCondition fc = fcs[conditionIndex];
fc.Style.Borders[BorderType.LeftBorder].LineStyle = CellBorderType.Dashed;
fc.Style.Borders[BorderType.RightBorder].LineStyle = CellBorderType.Dashed;
fc.Style.Borders[BorderType.TopBorder].LineStyle = CellBorderType.Dashed;
fc.Style.Borders[BorderType.BottomBorder].LineStyle = CellBorderType.Dashed;
```

## चरण 7: बॉर्डर रंग सेट करें

हम प्रत्येक बॉर्डर के लिए रंग भी सेट कर सकते हैं। आइए बाएं, दाएं और ऊपरी बॉर्डर को सियान रंग दें और नीचे के बॉर्डर को पीला रंग दें:

```csharp
fc.Style.Borders[BorderType.LeftBorder].Color = Color.FromArgb(0, 255, 255);
fc.Style.Borders[BorderType.RightBorder].Color = Color.FromArgb(0, 255, 255);
fc.Style.Borders[BorderType.TopBorder].Color = Color.FromArgb(0, 255, 255);
fc.Style.Borders[BorderType.BottomBorder].Color = Color.FromArgb(255, 255, 0);
```

## चरण 8: अपनी कार्यपुस्तिका सहेजें

अंत में, आइए अपनी कार्यपुस्तिका को सेव करें। परिवर्तनों को सेव करने के लिए निम्न कोड का उपयोग करें:

```csharp
workbook.Save(dataDir + "output.xlsx");
```

 यह आपकी एक्सेल फ़ाइल को इस रूप में सहेज देगा`output.xlsx` निर्दिष्ट निर्देशिका में. 

## निष्कर्ष

और अब यह हो गया! आपने .NET के लिए Aspose.Cells का उपयोग करके Excel फ़ाइल में सफलतापूर्वक बॉर्डर सेट कर लिए हैं। इस प्रक्रिया को स्वचालित करके, आप अनगिनत घंटे बचा सकते हैं, खासकर जब बड़े डेटासेट से निपटना हो। कल्पना करें कि बिना उंगली उठाए अपनी रिपोर्ट को कस्टमाइज़ करने में सक्षम होना—अब यही दक्षता है।

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं Excel के अलावा अन्य फ़ाइल स्वरूपों के लिए Aspose.Cells का उपयोग कर सकता हूँ?  
हां, Aspose.Cells मुख्य रूप से एक्सेल पर केंद्रित है, लेकिन यह आपको एक्सेल फाइलों को पीडीएफ और HTML जैसे विभिन्न प्रारूपों में परिवर्तित करने की भी अनुमति देता है।

### क्या मुझे Aspose.Cells का उपयोग करने के लिए लाइसेंस की आवश्यकता है?  
 आप इसकी कार्यक्षमताओं का परीक्षण करने के लिए एक निःशुल्क परीक्षण का उपयोग कर सकते हैं। दीर्घकालिक उपयोग के लिए, आपको लाइसेंस खरीदना होगा, जिसे आप पा सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### मैं Aspose.Cells कैसे स्थापित करूँ?  
आप NuGet के माध्यम से या साइट से DLL डाउनलोड करके Aspose.Cells को स्थापित कर सकते हैं।

### क्या कोई दस्तावेज उपलब्ध है?  
 बिल्कुल! आप विस्तृत दस्तावेज़ तक पहुँच सकते हैं[यहाँ](https://reference.aspose.com/cells/net/).

### यदि मुझे कोई समस्या आती है तो मुझे सहायता कहां से मिल सकती है?  
 आप किसी भी प्रश्न या समस्या के लिए Aspose सहायता फोरम पर जा सकते हैं:[एस्पोज फोरम](https://forum.aspose.com/c/cells/9).