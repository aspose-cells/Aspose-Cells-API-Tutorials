---
title: एक्सेल में सुदूर पूर्व और लैटिन फ़ॉन्ट निर्दिष्ट करें
linktitle: एक्सेल में सुदूर पूर्व और लैटिन फ़ॉन्ट निर्दिष्ट करें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: इस व्यापक और आसान ट्यूटोरियल में .NET के लिए Aspose.Cells का उपयोग करके Excel में सुदूर पूर्व और लैटिन फ़ॉन्ट निर्दिष्ट करना सीखें।
type: docs
weight: 17
url: /hi/net/excel-shape-text-modifications/specify-far-east-latin-font-excel/
---
## परिचय
क्या आप अपनी एक्सेल रिपोर्ट या दस्तावेजों को विशिष्ट फ़ॉन्ट आवश्यकताओं के साथ बेहतर बनाना चाहते हैं? चाहे आप कई भाषाओं से निपट रहे हों या अपनी स्प्रेडशीट में एक अद्वितीय सौंदर्य के लिए प्रयास कर रहे हों, एक्सेल में सुदूर पूर्व और लैटिन फ़ॉन्ट को निर्दिष्ट करना समझना एक महत्वपूर्ण कौशल है। आपके लिए सौभाग्य की बात है कि हमारे पास इसका समाधान है! इस ट्यूटोरियल में, हम इस सुविधा को सहजता से लागू करने के लिए .NET के लिए Aspose.Cells का उपयोग करने का तरीका तलाशते हैं। आइए शुरू करते हैं!
## आवश्यक शर्तें
इससे पहले कि हम बारीकियों में जाएं, कुछ चीजें हैं जिन्हें आपको Aspose.Cells के साथ आरंभ करने से पहले सेट अप करना होगा:
### .NET फ्रेमवर्क या .NET कोर
सुनिश्चित करें कि आपके मशीन पर .NET Framework या .NET Core इंस्टॉल है। यह लाइब्रेरी दोनों के साथ अच्छी तरह से काम करती है।
### Aspose.Cells की स्थापना
आपको Aspose.Cells लाइब्रेरी डाउनलोड करनी होगी।[इसे यहाँ से डाउनलोड करें](https://releases.aspose.com/cells/net/) यदि आप NuGet पैकेज स्थापित करने से परिचित नहीं हैं, तो अनुसरण करें[यह गाइड](https://www.nuget.org/).
### एकीकृत विकास वातावरण (आईडीई)
विजुअल स्टूडियो या जेटब्रेन्स राइडर जैसे IDE से कोडिंग, डिबगिंग और आपके प्रोजेक्ट को चलाना सरल हो सकता है।
### C# का बुनियादी ज्ञान
इस ट्यूटोरियल का अनुसरण करने के लिए C# प्रोग्रामिंग से परिचित होना बहुत फायदेमंद होगा।
## पैकेज आयात करें
Aspose.Cells के साथ काम करने से पहले, हमें अपने प्रोजेक्ट में आवश्यक पैकेज आयात करने की आवश्यकता है। यहाँ बताया गया है कि आप ऐसा कैसे कर सकते हैं:
### एक नया प्रोजेक्ट बनाएं
1. अपना IDE खोलें और एक नया कंसोल एप्लिकेशन प्रोजेक्ट बनाएं।
2.  अपनी परियोजना का नाम कुछ वर्णनात्मक रखें, जैसे`FontSpecifyingApp`.
### Aspose.Cells NuGet पैकेज जोड़ें
1. समाधान एक्सप्लोरर में अपने प्रोजेक्ट पर राइट-क्लिक करें।
2.  चुनना`Manage NuGet Packages...`.
3.  निम्न को खोजें`Aspose.Cells` और इसे स्थापित करें.
इन चरणों के अंत तक, आपके पास कोडिंग शुरू करने के लिए सब कुछ तैयार हो जाएगा!
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
सेटअप पूरा होने के बाद, अब समय है कि आप अपनी आस्तीन ऊपर चढ़ाएं और कोडिंग शुरू करें। विशेष रूप से, हम एक नई एक्सेल वर्कबुक बनाएंगे और टेक्स्ट बॉक्स के लिए सुदूर पूर्व और लैटिन दोनों फ़ॉन्ट निर्दिष्ट करेंगे। इसे चरण दर चरण कैसे करें, यहाँ बताया गया है:
## चरण 1: आउटपुट निर्देशिका सेट करें
हम सबसे पहले यह निर्दिष्ट करते हैं कि हम अपनी एक्सेल फ़ाइल को कहाँ सहेजना चाहते हैं। यह महत्वपूर्ण है क्योंकि हम यह सुनिश्चित करना चाहते हैं कि हमारी आउटपुट फ़ाइल ऐसी जगह पर संग्रहीत हो जहाँ आसानी से पहुँचा जा सके।
```csharp
// आउटपुट निर्देशिका
string outputDir = "Your Document Directory";
```
## चरण 2: एक खाली कार्यपुस्तिका बनाएँ
अब जब हमने अपनी डायरेक्टरी सेट कर ली है, तो चलिए एक नई वर्कबुक बनाते हैं जहाँ हम अपनी सामग्री जोड़ेंगे। यह पेंटिंग से पहले एक नए कैनवास से शुरुआत करने जैसा है।
```csharp
// रिक्त कार्यपुस्तिका बनाएँ.
Workbook wb = new Workbook();
```
## चरण 3: पहली वर्कशीट तक पहुँचें
इसके बाद, हम अपनी वर्कबुक से वर्कशीट के साथ काम करना चाहते हैं। वर्कशीट को अपनी किताब के एक पन्ने की तरह समझें जहाँ सारा जादू होता है।
```csharp
// प्रथम कार्यपत्रक तक पहुंचें.
Worksheet ws = wb.Worksheets[0];
```
## चरण 4: एक टेक्स्टबॉक्स जोड़ें
अब, हम अपनी वर्कशीट में एक टेक्स्टबॉक्स जोड़ेंगे। यहीं पर हम अपना टेक्स्ट टाइप करेंगे। इसे एक प्रेजेंटेशन की स्लाइड के भीतर एक टेक्स्टबॉक्स बनाने के रूप में कल्पना करें।
```csharp
// वर्कशीट के अंदर टेक्स्टबॉक्स जोड़ें.
int idx = ws.TextBoxes.Add(5, 5, 50, 200);
Aspose.Cells.Drawing.TextBox tb = ws.TextBoxes[idx];
```
## चरण 5: टेक्स्टबॉक्स का टेक्स्ट सेट करें
चलिए कुछ टेक्स्ट टाइप करते हैं। इस उदाहरण में, हम फ़ार ईस्ट फ़ॉन्ट को प्रदर्शित करने के लिए जापानी अक्षर इनपुट करने जा रहे हैं। यह आपके कंप्यूटर पर टेक्स्टबॉक्स में लिखने जितना ही सरल है!
```csharp
// टेक्स्टबॉक्स का टेक्स्ट सेट करें.
tb.Text = "こんにちは世界"; //जापानी में इसका अर्थ है "हैलो वर्ल्ड"।
```
## चरण 6: फ़ॉन्ट निर्दिष्ट करें
अब आता है रोमांचक हिस्सा! हम टेक्स्ट के लिए लैटिन और फार ईस्ट दोनों फॉन्ट सेट करेंगे। यह एक फैंसी शादी के निमंत्रण के लिए एकदम सही फॉन्ट चुनने जैसा है!
```csharp
// फ़ॉन्ट का सुदूर पूर्व और लैटिन नाम निर्दिष्ट करें.
tb.TextOptions.LatinName = "Comic Sans MS"; // यह हमारा चुना हुआ लैटिन फ़ॉन्ट है।
tb.TextOptions.FarEastName = "KaiTi"; // यह हमारा वांछित सुदूर पूर्व फ़ॉन्ट है।
```
## चरण 7: आउटपुट एक्सेल फ़ाइल को सेव करें
अंत में, चलिए अपनी कार्यपुस्तिका को सेव करते हैं! यह चरण हमारे कार्य को पूरा करता है और यह सुनिश्चित करता है कि हमने जो भी कड़ी मेहनत की है वह ठीक से सेव हो गई है। 
```csharp
// आउटपुट एक्सेल फ़ाइल को सहेजें.
wb.Save(outputDir + "outputSpecifyFarEastAndLatinNameOfFontInTextOptionsOfShape.xlsx", SaveFormat.Xlsx);
```
## चरण 8: पुष्टिकरण संदेश
यह बताने के लिए कि सब कुछ सफलतापूर्वक निष्पादित हो गया है, हम कंसोल पर एक पुष्टिकरण संदेश प्रिंट करेंगे:
```csharp
Console.WriteLine("SpecifyFarEastAndLatinNameOfFontInTextOptionsOfShape executed successfully.");
```
## निष्कर्ष
और अब आप समझ गए! आपने .NET के लिए Aspose.Cells का उपयोग करके Excel कार्यपुस्तिका में फ़ार ईस्ट और लैटिन फ़ॉन्ट को सफलतापूर्वक निर्दिष्ट किया है। यह कौशल न केवल आपके दस्तावेज़ों को एक पेशेवर स्पर्श देता है, बल्कि विभिन्न भाषाओं के उपयोगकर्ताओं के लिए पढ़ने के अनुभव को भी समृद्ध करता है।
अपनी विशिष्ट आवश्यकताओं के अनुरूप संयोजन खोजने के लिए अलग-अलग फ़ॉन्ट और शैलियों के साथ प्रयोग करने में संकोच न करें। हैप्पी कोडिंग!
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.Cells क्या है?
Aspose.Cells एक .NET लाइब्रेरी है जो आपके मशीन पर Microsoft Excel स्थापित किए बिना Excel स्प्रेडशीट बनाने और प्रबंधित करने के लिए है। 
### क्या मैं वेब अनुप्रयोगों के लिए Aspose.Cells का उपयोग कर सकता हूँ?
हाँ! Aspose.Cells का उपयोग डेस्कटॉप अनुप्रयोगों और .NET के साथ निर्मित वेब अनुप्रयोगों दोनों के लिए किया जा सकता है।
### क्या Aspose.Cells का कोई निःशुल्क संस्करण उपलब्ध है?
 हां, Aspose एक निःशुल्क परीक्षण प्रदान करता है। आप ऐसा कर सकते हैं[यहाँ पर डाउनलोड करो](https://releases.aspose.com/).
### मैं Aspose.Cells के लिए समर्थन कैसे प्राप्त करूं?
 आप सहायता मांग सकते हैं और मूल्यवान संसाधन पा सकते हैं[Aspose फ़ोरम](https://forum.aspose.com/c/cells/9).
### मैं Aspose.Cells कहां से खरीद सकता हूं?
 आप Aspose.Cells को सीधे से खरीद सकते हैं[Aspose वेबसाइट](https://purchase.aspose.com/buy).