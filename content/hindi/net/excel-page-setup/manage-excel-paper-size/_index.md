---
title: एक्सेल पेपर का आकार प्रबंधित करें
linktitle: एक्सेल पेपर का आकार प्रबंधित करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ एक्सेल में पेपर आकार को प्रबंधित करना सीखें। C# में स्रोत कोड के साथ चरण दर चरण ट्यूटोरियल।
type: docs
weight: 70
url: /hi/net/excel-page-setup/manage-excel-paper-size/
---
इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके एक्सेल दस्तावेज़ में पेपर आकार को प्रबंधित करने के तरीके के बारे में चरण दर चरण मार्गदर्शन करेंगे। हम आपको दिखाएंगे कि C# स्रोत कोड का उपयोग करके पेपर आकार को कैसे कॉन्फ़िगर करें।

## चरण 1: वातावरण स्थापित करना

सुनिश्चित करें कि आपकी मशीन पर .NET के लिए Aspose.Cells स्थापित है। अपने पसंदीदा विकास परिवेश में एक नया प्रोजेक्ट भी बनाएं।

## चरण 2: आवश्यक पुस्तकालय आयात करें

अपनी कोड फ़ाइल में, Aspose.Cells के साथ काम करने के लिए आवश्यक लाइब्रेरी आयात करें। यहाँ संबंधित कोड है:

```csharp
using Aspose.Cells;
```

## चरण 3: दस्तावेज़ निर्देशिका सेट करें

वह निर्देशिका सेट करें जहां आप जिस एक्सेल दस्तावेज़ के साथ काम करना चाहते हैं वह स्थित है। निर्देशिका सेट करने के लिए निम्नलिखित कोड का उपयोग करें:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

संपूर्ण निर्देशिका पथ निर्दिष्ट करना सुनिश्चित करें.

## चरण 4: एक कार्यपुस्तिका ऑब्जेक्ट बनाना

वर्कबुक ऑब्जेक्ट उस एक्सेल दस्तावेज़ का प्रतिनिधित्व करता है जिसके साथ आप काम करेंगे। आप इसे निम्नलिखित कोड का उपयोग करके बना सकते हैं:

```csharp
Workbook workbook = new Workbook();
```

यह एक नई खाली वर्कबुक ऑब्जेक्ट बनाता है।

## चरण 5: पहली वर्कशीट तक पहुंच

एक्सेल दस्तावेज़ की पहली स्प्रेडशीट तक पहुंचने के लिए, निम्नलिखित कोड का उपयोग करें:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

यह आपको कार्यपुस्तिका में पहली वर्कशीट के साथ काम करने की अनुमति देगा।

## चरण 6: कागज़ का आकार सेटअप

पेपर का आकार सेट करने के लिए वर्कशीट ऑब्जेक्ट की PageSetup.PaperSize प्रॉपर्टी का उपयोग करें। इस उदाहरण में, हम कागज़ का आकार A4 पर सेट करेंगे। यहाँ संबंधित कोड है:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

यह स्प्रेडशीट पेपर का आकार A4 पर सेट करता है।

## चरण 7: कार्यपुस्तिका सहेजना

कार्यपुस्तिका में परिवर्तन सहेजने के लिए, कार्यपुस्तिका ऑब्जेक्ट की सेव() विधि का उपयोग करें। यहाँ संबंधित कोड है:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

यह कार्यपुस्तिका को निर्दिष्ट निर्देशिका में परिवर्तन के साथ सहेज लेगा।

### .NET के लिए Aspose.Cells का उपयोग करके एक्सेल पेपर साइज़ प्रबंधित करने के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook();
// एक्सेल फ़ाइल में पहली वर्कशीट तक पहुँचना
Worksheet worksheet = workbook.Worksheets[0];
// कागज़ का आकार A4 पर सेट करना
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// कार्यपुस्तिका सहेजें.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## निष्कर्ष

अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल दस्तावेज़ में कागज़ के आकार को कैसे प्रबंधित किया जाए। इस ट्यूटोरियल ने आपको पर्यावरण की स्थापना से लेकर परिवर्तनों को सहेजने तक प्रक्रिया के हर चरण के बारे में बताया। अब आप इस ज्ञान का उपयोग अपने एक्सेल दस्तावेज़ों के कागज़ के आकार को अनुकूलित करने के लिए कर सकते हैं।

### अक्सर पूछे जाने वाले प्रश्न

#### Q1: क्या मैं A4 के अलावा कोई अन्य कस्टम पेपर आकार सेट कर सकता हूँ?

A1: हां, Aspose.Cells विभिन्न प्रकार के पूर्वनिर्धारित पेपर आकारों के साथ-साथ वांछित आयामों को निर्दिष्ट करके कस्टम पेपर आकार सेट करने की क्षमता का समर्थन करता है।

#### Q2: मैं Excel दस्तावेज़ में वर्तमान कागज़ का आकार कैसे जान सकता हूँ?

 A2: आप इसका उपयोग कर सकते हैं`PageSetup.PaperSize` की संपत्ति`Worksheet` वर्तमान में निर्धारित पेपर आकार प्राप्त करने के लिए ऑब्जेक्ट करें।

#### Q3: क्या पेपर साइज के साथ अतिरिक्त पेज मार्जिन सेट करना संभव है?

 A3: हाँ, आप उपयोग कर सकते हैं`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` और`PageSetup.BottomMargin` कागज़ के आकार के अलावा अतिरिक्त पेज मार्जिन सेट करने के लिए गुण।

#### Q4: क्या यह विधि सभी Excel फ़ाइल स्वरूपों, जैसे .xls और .xlsx, के लिए काम करती है?

A4: हां, यह विधि .xls और .xlsx दोनों फ़ाइल स्वरूपों के लिए काम करती है।

#### Q5: क्या मैं एक ही कार्यपुस्तिका में अलग-अलग कार्यपत्रकों पर अलग-अलग आकार के कागज़ लागू कर सकता हूँ?

 A5: हाँ, आप इसका उपयोग करके एक ही कार्यपुस्तिका में अलग-अलग कार्यपत्रकों पर अलग-अलग आकार के कागज़ लागू कर सकते हैं`PageSetup.PaperSize` प्रत्येक वर्कशीट की संपत्ति.