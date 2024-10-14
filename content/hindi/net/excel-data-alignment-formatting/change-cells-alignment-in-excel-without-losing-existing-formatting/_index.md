---
title: स्वरूपण खोए बिना एक्सेल सेल संरेखण बदलें
linktitle: स्वरूपण खोए बिना एक्सेल सेल संरेखण बदलें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके बिना फ़ॉर्मेटिंग खोए Excel सेल संरेखण को बदलने का तरीका जानें। निर्बाध नियंत्रण के लिए हमारे व्यापक चरण-दर-चरण मार्गदर्शिका का पालन करें।
type: docs
weight: 10
url: /hi/net/excel-data-alignment-formatting/change-cells-alignment-in-excel-without-losing-existing-formatting/
---
## परिचय

एक्सेल फ़ाइलों को मैनेज करना कभी-कभी भूलभुलैया में भटकने जैसा लगता है, खासकर तब जब सेल अलाइनमेंट बदलने जैसे ज़रूरी एडजस्टमेंट करते हुए फ़ॉर्मेटिंग को बनाए रखने की बात आती है। अगर आपने कभी एक्सेल में सेल के अलाइनमेंट को बदलने की कोशिश की है और पाया है कि फ़ॉर्मेटिंग गड़बड़ा जाती है, तो आप अकेले नहीं हैं! इस ट्यूटोरियल में, हम .NET के लिए Aspose.Cells का उपयोग करके, बिना किसी फ़ॉर्मेटिंग को खोए एक्सेल सेल के अलाइनमेंट को बदलने के तरीके के बारे में विस्तार से जानेंगे। चलिए अपनी आस्तीन ऊपर चढ़ाते हैं और शुरू करते हैं!

## आवश्यक शर्तें

इससे पहले कि हम वास्तविक कोडिंग में उतरें, यह सुनिश्चित करना ज़रूरी है कि आपने सब कुछ सही तरीके से सेट किया है। आपको ये चीज़ें चाहिए होंगी:

1. विज़ुअल स्टूडियो: सुनिश्चित करें कि आपके कंप्यूटर पर विज़ुअल स्टूडियो (कोई भी संस्करण जो .NET का समर्थन करता है) स्थापित है।
2.  .NET के लिए Aspose.Cells: Aspose.Cells लाइब्रेरी को यहां से डाउनलोड और इंस्टॉल करें[Aspose की साइट](https://releases.aspose.com/cells/net/).
3. C# का मूलभूत ज्ञान: C# प्रोग्रामिंग से थोड़ी परिचितता उपयोगी होगी क्योंकि हम C# संदर्भ में काम करेंगे।
4. नमूना एक्सेल फ़ाइल: प्रदर्शन के लिए, एक नमूना एक्सेल फ़ाइल तैयार करें (उदाहरण के लिए,`sampleChangeCellsAlignmentAndKeepExistingFormatting.xlsx`) जिसमें कुछ प्रारंभिक सेल स्वरूपण शामिल है।

## पैकेज आयात करें

.NET के लिए Aspose.Cells का उपयोग करने का पहला चरण आपके प्रोजेक्ट में आवश्यक नामस्थान शामिल करना है। यहाँ बताया गया है कि कैसे:

### अपना प्रोजेक्ट खोलें

विजुअल स्टूडियो खोलें और एक नया C# प्रोजेक्ट बनाएं (कंसोल एप्लिकेशन ठीक काम करेगा)।

### Aspose.Cells में संदर्भ जोड़ें

- समाधान एक्सप्लोरर में अपने प्रोजेक्ट पर राइट-क्लिक करें।
- "NuGet पैकेज प्रबंधित करें" चुनें.
-  निम्न को खोजें`Aspose.Cells` और इसे स्थापित करें.

### आवश्यक नामस्थान आयात करें

अपनी C# फ़ाइल के शीर्ष पर निम्नलिखित using निर्देश जोड़ें:

```csharp
using Aspose.Cells;
using Aspose.Cells.Drawing;
using Aspose.Cells.Tables;
```

यह आपको Aspose.Cells लाइब्रेरी द्वारा प्रदान की गई कक्षाओं और विधियों का निर्बाध रूप से उपयोग करने की अनुमति देगा।

अब जबकि हमने अपनी पूर्वावश्यकताओं को व्यवस्थित कर लिया है और पैकेजों को आयात कर लिया है, तो आइए कोशिकाओं के संरेखण को बदलने की प्रक्रिया को चरण दर चरण समझें।

## चरण 1: अपना स्रोत और आउटपुट निर्देशिका सेट करें

आरंभ करने के लिए, आपको यह निर्धारित करना होगा कि आपकी एक्सेल फ़ाइल कहाँ संग्रहीत है और प्रसंस्करण के बाद आप उसे कहाँ सहेजना चाहते हैं।

```csharp
// स्रोत निर्देशिका
string sourceDir = "Your Document Directory\\"; // अपनी वास्तविक निर्देशिका से प्रतिस्थापित करें

// आउटपुट निर्देशिका
string outputDir = "Your Document Directory\\"; // अपनी वास्तविक निर्देशिका से प्रतिस्थापित करें
```

 यह कोड इनपुट और आउटपुट फ़ाइलों के लिए पथ सेट करता है।`"Your Document Directory\\"` आपके कंप्यूटर पर वास्तविक पथ के साथ.

## चरण 2: नमूना एक्सेल फ़ाइल लोड करें

इसके बाद, आप अपने नमूना एक्सेल फ़ाइल को एप्लिकेशन में लोड करना चाहेंगे।

```csharp
// स्वरूपण वाले कक्षों वाली नमूना एक्सेल फ़ाइल लोड करें.
Workbook wb = new Workbook(sourceDir + "sampleChangeCellsAlignmentAndKeepExistingFormatting.xlsx");
```

कोड की यह पंक्ति आपकी मौजूदा एक्सेल फ़ाइल को लोड करने के लिए वर्कबुक क्लास का उपयोग करती है ताकि हम इसकी सामग्री में बदलाव कर सकें।

## चरण 3: इच्छित वर्कशीट तक पहुंचें

वर्कबुक लोड करने के बाद, उस वर्कशीट तक पहुँचें जिसे आप मैनिपुलेट करना चाहते हैं। एक्सेल फ़ाइलों में कई शीट हो सकती हैं, इसलिए सुनिश्चित करें कि आप सही शीट को लक्षित कर रहे हैं।

```csharp
// प्रथम कार्यपत्रक तक पहुँचें.
Worksheet ws = wb.Worksheets[0];
```

यह उदाहरण पहली वर्कशीट तक पहुँचता है। यदि आपका डेटा किसी दूसरी शीट पर है, तो इंडेक्स को उसके अनुसार समायोजित करें।

## चरण 4: कोशिकाओं की एक श्रेणी बनाएँ

एक रेंज बनाकर निर्धारित करें कि आप किन सेल को बदलना चाहते हैं। यह चयन एक निर्दिष्ट रेंज पर ध्यान केंद्रित करेगा, जैसे कि “B2:D7”।

```csharp
// कोशिकाओं की श्रेणी बनाएँ.
Range rng = ws.Cells.CreateRange("B2:D7");
```

यह रेंज हमें नई संरेखण सेटिंग्स को सीधे उन कोशिकाओं पर लागू करने की अनुमति देगी।

## चरण 5: स्टाइल ऑब्जेक्ट बनाएं और उसे कस्टमाइज़ करें

अब, हमें उन संरेखण शैलियों को परिभाषित करने की आवश्यकता है जिन्हें हम लागू करना चाहते हैं।

```csharp
// शैली ऑब्जेक्ट बनाएँ.
Style st = wb.CreateStyle();

// क्षैतिज और ऊर्ध्वाधर संरेखण को केंद्र पर सेट करें।
st.HorizontalAlignment = TextAlignmentType.Center;
st.VerticalAlignment = TextAlignmentType.Center;
```

यहाँ, एक नया स्टाइल ऑब्जेक्ट बनाया गया है, और हम क्षैतिज और ऊर्ध्वाधर संरेखण दोनों को केंद्र में सेट करते हैं। यह वही है जो चुने गए सेल के भीतर टेक्स्ट को सटीक रूप से संरेखित करने में मदद करेगा।

## चरण 6: स्टाइल फ़्लैग सेट करें

स्टाइल फ़्लैग सेट करना यह सुनिश्चित करने में महत्वपूर्ण भूमिका निभाता है कि आपके स्टाइल परिवर्तन लागू हों। 

```csharp
// स्टाइल फ्लैग ऑब्जेक्ट बनाएं.
StyleFlag flag = new StyleFlag();

// स्टाइल फ्लैग संरेखण को सत्य पर सेट करें। यह एक महत्वपूर्ण कथन है।
flag.Alignments = true;
```

 सेट करके`Alignments` स्टाइलफ़्लैग की संपत्ति`true`, आप Aspose.Cells को संरेखण शैलियों को ठीक से लागू करने के लिए कहते हैं।

## चरण 7: सेल रेंज पर स्टाइल लागू करें

अपनी शैलियों और झंडों को सही स्थान पर स्थापित करने के बाद, अब उन शैलियों को कक्षों की श्रेणी पर लागू करने का समय है:

```csharp
// कक्षों की श्रेणी पर शैली लागू करें.
rng.ApplyStyle(st, flag);
```

यह चरण किसी भी मौजूदा स्वरूपण को संरक्षित करते हुए उस सीमा के भीतर सभी कोशिकाओं के संरेखण को प्रभावी ढंग से बदल देता है।

## चरण 8: कार्यपुस्तिका सहेजें

अंत में, आप अपने परिवर्तनों को एक नई फ़ाइल में सहेजना चाहेंगे ताकि मूल फ़ाइल यथावत बनी रहे।

```csharp
// कार्यपुस्तिका को XLSX प्रारूप में सहेजें.
wb.Save(outputDir + "outputChangeCellsAlignmentAndKeepExistingFormatting.xlsx", SaveFormat.Xlsx);
```

यह पंक्ति संरेखण परिवर्तनों सहित कार्यपुस्तिका को पहले निर्दिष्ट आउटपुट निर्देशिका में सहेजती है।

## चरण 9: सफलता की सूचना दें

फ़ाइल को सेव करने के बाद, यह फीडबैक देना अच्छा लगता है कि सब कुछ अपेक्षा के अनुरूप काम कर रहा है!

```csharp
Console.WriteLine("ChangeCellsAlignmentAndKeepExistingFormatting executed successfully.");
```

यदि आपका ऑपरेशन बिना किसी समस्या के पूरा हो जाता है तो यह संदेश कंसोल में दिखाई देता है।

## निष्कर्ष

मौजूदा स्वरूपण को बरकरार रखते हुए Excel में सेल संरेखण बदलना Aspose.Cells for .NET के साथ एक सहज प्रक्रिया है। इन चरणों का पालन करके, आप अपने अनुप्रयोगों में Excel हेरफेर को सरल बना सकते हैं और मूल्यवान स्वरूपण खोने के सिरदर्द से बच सकते हैं। चाहे आप रिपोर्ट तैयार कर रहे हों या डेटा फ़ीड प्रबंधित कर रहे हों, इस कौशल में महारत हासिल करना एक गेम-चेंजर हो सकता है!

## अक्सर पूछे जाने वाले प्रश्न

### क्या Aspose.Cells बड़ी Excel फ़ाइलों को संभाल सकता है?
बिल्कुल! यह प्रदर्शन के लिए अनुकूलित है और बड़ी फ़ाइलों को कुशलतापूर्वक संसाधित कर सकता है।

### क्या Aspose.Cells के लिए कोई परीक्षण संस्करण उपलब्ध है?
 हाँ! आप साइट से निःशुल्क परीक्षण डाउनलोड कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).

### Aspose.Cells कौन सी प्रोग्रामिंग भाषाओं का समर्थन करता है?
Aspose.Cells मुख्य रूप से संबंधित लाइब्रेरीज़ के माध्यम से .NET, Java और कई अन्य भाषाओं का समर्थन करता है।

### मैं Aspose.Cells के लिए समर्थन कैसे प्राप्त कर सकता हूं?
 किसी भी प्रश्न या समर्थन-संबंधी समस्या के लिए, यहां जाएं[सहयता मंच](https://forum.aspose.com/c/cells/9).

### क्या मैं एक साथ कई शैलियाँ लागू कर सकता हूँ?
हां, आप एकाधिक स्टाइल ऑब्जेक्ट बना सकते हैं और आवश्यकतानुसार उन्हें क्रमिक रूप से या सशर्त रूप से लागू कर सकते हैं।