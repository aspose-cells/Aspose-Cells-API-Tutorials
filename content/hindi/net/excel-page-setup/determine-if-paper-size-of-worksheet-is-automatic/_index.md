---
title: निर्धारित करें कि वर्कशीट का पेपर आकार स्वचालित है या नहीं
linktitle: निर्धारित करें कि वर्कशीट का पेपर आकार स्वचालित है या नहीं
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: जानें कि .NET के लिए Aspose.Cells के साथ यह कैसे निर्धारित किया जाए कि स्प्रेडशीट का पेपर आकार स्वचालित है।
type: docs
weight: 20
url: /hi/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
इस लेख में, हम आपको निम्नलिखित C# स्रोत कोड को चरण दर चरण समझाएंगे: .NET के लिए Aspose.Cells का उपयोग करके निर्धारित करें कि वर्कशीट का पेपर आकार स्वचालित है या नहीं। इस ऑपरेशन को करने के लिए हम .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करेंगे। यह निर्धारित करने के लिए कि वर्कशीट का पेपर आकार स्वचालित है या नहीं, नीचे दिए गए चरणों का पालन करें।

## चरण 1: कार्यपुस्तिकाएँ लोड हो रही हैं
पहला कदम कार्यपुस्तिकाओं को लोड करना है। हमारे पास दो कार्यपुस्तिकाएँ होंगी: एक स्वचालित पेपर आकार अक्षम के साथ और दूसरी स्वचालित पेपर आकार सक्षम के साथ। कार्यपुस्तिकाएँ लोड करने के लिए कोड यहां दिया गया है:

```csharp
// स्रोत निर्देशिका
string sourceDir = "YOUR_SOURCE_DIR";
// उत्पादन निर्देशिका
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// स्वचालित पेपर आकार अक्षम के साथ पहली कार्यपुस्तिका लोड करें
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// स्वचालित पेपर आकार सक्षम करके दूसरी कार्यपुस्तिका लोड करें
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## चरण 2: स्प्रेडशीट तक पहुँचना
अब जब हमने कार्यपुस्तिकाएं लोड कर ली हैं, तो हमें कार्यपत्रकों तक पहुंचने की आवश्यकता है ताकि हम स्वचालित पेपर आकार की जांच कर सकें। हम दोनों वर्कबुक की पहली वर्कशीट पर जाएंगे। इसे एक्सेस करने के लिए कोड यहां दिया गया है:

```csharp
//पहली वर्कबुक की पहली वर्कशीट पर जाएँ
Worksheet ws11 = wb1.Worksheets[0];

// दूसरी वर्कबुक की पहली वर्कशीट पर जाएँ
Worksheet ws12 = wb2.Worksheets[0];
```

## चरण 3: स्वचालित पेपर आकार की जाँच करें
 इस चरण में, हम जांचेंगे कि वर्कशीट पेपर का आकार स्वचालित है या नहीं। हम उपयोग करेंगे`PageSetup.IsAutomaticPaperSize` यह जानकारी प्राप्त करने के लिए संपत्ति. फिर हम परिणाम प्रदर्शित करेंगे. यहाँ उसके लिए कोड है:

```csharp
// पहली वर्कबुक में पहली वर्कशीट की IsAutomaticPaperSize प्रॉपर्टी प्रदर्शित करें
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// पहली वर्कशीट की IsAutomaticPaperSize प्रॉपर्टी को दूसरी वर्कबुक में प्रदर्शित करें
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### .NET के लिए Aspose.Cells का उपयोग करके निर्धारित करें कि वर्कशीट का पेपर आकार स्वचालित है या नहीं, इसके लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//उत्पादन निर्देशिका
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//स्वचालित पेपर आकार वाली पहली कार्यपुस्तिका को गलत लोड करें
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//स्वचालित कागज़ का आकार सही होने पर दूसरी कार्यपुस्तिका लोड करें
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//दोनों कार्यपुस्तिकाओं की पहली वर्कशीट तक पहुँचें
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//दोनों वर्कशीट की PageSetup.IsAutomaticPaperSize प्रॉपर्टी प्रिंट करें
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## निष्कर्ष
इस लेख में, हमने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके यह कैसे निर्धारित किया जाए कि वर्कशीट का पेपर आकार स्वचालित है। हमने निम्नलिखित चरणों का पालन किया: कार्यपुस्तिकाएँ लोड करना,

स्प्रेडशीट और स्वचालित पेपर आकार की जाँच तक पहुंच। अब आप इस ज्ञान का उपयोग यह निर्धारित करने के लिए कर सकते हैं कि आपकी स्प्रैडशीट का पेपर आकार स्वचालित है या नहीं।

### पूछे जाने वाले प्रश्न

#### प्रश्न: मैं .NET के लिए Aspose.Cells के साथ कार्यपुस्तिकाएँ कैसे लोड कर सकता हूँ?

उ: आप Aspose.Cells लाइब्रेरी से वर्कबुक क्लास का उपयोग करके वर्कबुक लोड कर सकते हैं। किसी फ़ाइल से कार्यपुस्तिका लोड करने के लिए Workbook.Load विधि का उपयोग करें।

#### प्रश्न: क्या मैं अन्य स्प्रेडशीट के लिए स्वचालित पेपर आकार की जांच कर सकता हूं?

उ: हां, आप संबंधित वर्कशीट ऑब्जेक्ट की PageSetup.IsAutomaticPaperSize प्रॉपर्टी तक पहुंच कर किसी भी वर्कशीट के लिए स्वचालित पेपर आकार की जांच कर सकते हैं।

#### प्रश्न: मैं स्प्रेडशीट के स्वचालित पेपर आकार को कैसे बदल सकता हूँ?

उ: किसी वर्कशीट के स्वचालित पेपर आकार को बदलने के लिए, आप PageSetup.IsAutomaticPaperSize प्रॉपर्टी का उपयोग कर सकते हैं और इसे वांछित मान (सही या गलत) पर सेट कर सकते हैं।

#### प्रश्न: .NET के लिए Aspose.Cells अन्य कौन सी सुविधाएँ प्रदान करता है?

उ: .NET के लिए Aspose.Cells स्प्रेडशीट के साथ काम करने के लिए कई सुविधाएँ प्रदान करता है, जैसे कार्यपुस्तिकाएँ बनाना, संशोधित करना और परिवर्तित करना, साथ ही डेटा, सूत्रों और स्वरूपण में हेरफेर करना।