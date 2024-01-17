---
title: अन्य वर्कशीट से पेज सेटअप सेटिंग्स कॉपी करें
linktitle: अन्य वर्कशीट से पेज सेटअप सेटिंग्स कॉपी करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके पेज कॉन्फ़िगरेशन सेटिंग्स को एक स्प्रेडशीट से दूसरे में कॉपी करना सीखें। इस लाइब्रेरी के उपयोग को अनुकूलित करने के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 10
url: /hi/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
इस लेख में, हम आपको निम्नलिखित C# स्रोत कोड को चरण दर चरण समझाएंगे: .NET के लिए Aspose.Cells का उपयोग करके किसी अन्य स्प्रेडशीट से पेज कॉन्फ़िगरेशन सेटिंग्स की प्रतिलिपि बनाएँ। इस ऑपरेशन को करने के लिए हम .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करेंगे। यदि आप पेज सेटअप सेटिंग्स को एक वर्कशीट से दूसरे वर्कशीट में कॉपी करना चाहते हैं, तो नीचे दिए गए चरणों का पालन करें।

## चरण 1: कार्यपुस्तिका बनाना
पहला कदम एक कार्यपुस्तिका बनाना है। हमारे मामले में, हम Aspose.Cells लाइब्रेरी द्वारा प्रदान की गई वर्कबुक क्लास का उपयोग करेंगे। कार्यपुस्तिका बनाने के लिए कोड यहां दिया गया है:

```csharp
Workbook wb = new Workbook();
```

## चरण 2: परीक्षण कार्यपत्रक जोड़ना
वर्कबुक बनाने के बाद हमें टेस्ट वर्कशीट जोड़ने की जरूरत है। इस उदाहरण में, हम दो वर्कशीट जोड़ेंगे। दो वर्कशीट जोड़ने के लिए कोड यहां दिया गया है:

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## चरण 3: वर्कशीट तक पहुँचना
अब जब हमने कार्यपत्रक जोड़ दिए हैं, तो हमें उनकी सेटिंग्स बदलने में सक्षम होने के लिए उन तक पहुंचने की आवश्यकता है। हम "टेस्टशीट1" और "टेस्टशीट2" वर्कशीट को उनके नामों का उपयोग करके एक्सेस करेंगे। इसे एक्सेस करने के लिए कोड यहां दिया गया है:

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## चरण 4: कागज़ का आकार निर्धारित करना
 इस चरण में, हम "टेस्टशीट1" वर्कशीट का पेपर आकार निर्धारित करेंगे। हम उपयोग करेंगे`PageSetup.PaperSize` कागज का आकार निर्धारित करने की संपत्ति। उदाहरण के लिए, हम कागज़ का आकार "पेपरए3एक्स्ट्राट्रांसवर्स" पर सेट करेंगे। यहाँ उसके लिए कोड है:

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## चरण 5: पृष्ठ सेटअप सेटिंग्स की प्रतिलिपि बनाना
अब हम पेज कॉन्फ़िगरेशन सेटिंग्स को "टेस्टशीट1" वर्कशीट से "टेस्टशीट2" में कॉपी करेंगे। हम उपयोग करेंगे`PageSetup.Copy` इस ऑपरेशन को करने की विधि. यहाँ उसके लिए कोड है:

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## चरण 6: कागज़ के आकार की छपाई
 पेज सेटअप सेटिंग्स को कॉपी करने के बाद, हम दो वर्कशीट के पेपर साइज को प्रिंट करेंगे। हम इस्तेमाल करेंगे`Console.WriteLine` कागज़ का आकार प्रदर्शित करने के लिए. यहाँ उसके लिए कोड है:

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### .NET के लिए Aspose.Cells का उपयोग करके अन्य वर्कशीट से पेज सेटअप सेटिंग्स कॉपी करने के लिए नमूना स्रोत कोड 
```csharp
//कार्यपुस्तिका बनाएँ
Workbook wb = new Workbook();
//दो परीक्षण कार्यपत्रक जोड़ें
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//दोनों वर्कशीट को TestSheet1 और TestSheet2 के रूप में एक्सेस करें
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//TestSheet1 के पेपर का आकार पेपरA3ExtraTransvers पर सेट करें
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//दोनों वर्कशीट का पेपर साइज प्रिंट करें
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//पेजसेटअप को TestSheet1 से TestSheet2 में कॉपी करें
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//दोनों वर्कशीट का पेपर साइज प्रिंट करें
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## निष्कर्ष
इस लेख में, हमने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके पेज कॉन्फ़िगरेशन सेटिंग्स को एक वर्कशीट से दूसरे में कैसे कॉपी किया जाए। हम निम्नलिखित चरणों से गुजरे: कार्यपुस्तिका बनाना, परीक्षण कार्यपत्रक जोड़ना, कार्यपत्रकों तक पहुंचना, कागज का आकार निर्धारित करना, पृष्ठ सेटअप सेटिंग्स की प्रतिलिपि बनाना, और कागज के आकार को प्रिंट करना। अब आप इस ज्ञान का उपयोग पेज कॉन्फ़िगरेशन सेटिंग्स को अपने प्रोजेक्ट में कॉपी करने के लिए कर सकते हैं।

### पूछे जाने वाले प्रश्न

#### प्रश्न: क्या मैं विभिन्न कार्यपुस्तिका उदाहरणों के बीच पृष्ठ कॉन्फ़िगरेशन सेटिंग्स की प्रतिलिपि बना सकता हूँ?

 उ: हाँ, आप इसका उपयोग करके विभिन्न कार्यपुस्तिका उदाहरणों के बीच पृष्ठ सेटअप सेटिंग्स की प्रतिलिपि बना सकते हैं`PageSetup.Copy` Aspose.Cells लाइब्रेरी की विधि।

#### प्रश्न: क्या मैं ओरिएंटेशन या मार्जिन जैसी अन्य पेज सेटअप सेटिंग्स कॉपी कर सकता हूं?

 उ: हां, आप इसका उपयोग करके अन्य पेज सेटअप सेटिंग्स कॉपी कर सकते हैं`PageSetup.Copy` उचित विकल्पों के साथ विधि. उदाहरण के लिए, आप ओरिएंटेशन का उपयोग करके कॉपी कर सकते हैं`CopyOptions.Orientation` और मार्जिन का उपयोग कर रहे हैं`CopyOptions.Margins`.

#### प्रश्न: मुझे कैसे पता चलेगा कि कागज़ के आकार के लिए कौन से विकल्प उपलब्ध हैं?

उ: आप कागज़ के आकार के लिए उपलब्ध विकल्पों के लिए Aspose.Cells लाइब्रेरी API संदर्भ की जांच कर सकते हैं। वहाँ एक enum कहा जाता है`PaperSizeType` जो विभिन्न समर्थित पेपर आकारों को सूचीबद्ध करता है।

#### प्रश्न: मैं .NET के लिए Aspose.Cells लाइब्रेरी कैसे डाउनलोड कर सकता हूं?

 उत्तर: आप .NET के लिए Aspose.Cells लाइब्रेरी डाउनलोड कर सकते हैं[एस्पोज़ रिलीज़](https://releases.aspose.com/cells/net). नि:शुल्क परीक्षण संस्करण उपलब्ध हैं, साथ ही व्यावसायिक उपयोग के लिए सशुल्क लाइसेंस भी उपलब्ध हैं।

#### प्रश्न: क्या Aspose.Cells लाइब्रेरी अन्य प्रोग्रामिंग भाषाओं का समर्थन करती है?

उत्तर: हाँ, Aspose.Cells लाइब्रेरी C#, Java, Python और कई अन्य सहित कई प्रोग्रामिंग भाषाओं का समर्थन करती है।