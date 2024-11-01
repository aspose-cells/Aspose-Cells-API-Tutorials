---
title: Aspose.Cells में अनुक्रमिक पृष्ठ प्रस्तुत करें
linktitle: Aspose.Cells में अनुक्रमिक पृष्ठ प्रस्तुत करें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells के साथ Excel में अनुक्रमिक पृष्ठों को रेंडर करना सीखें। यह चरण-दर-चरण ट्यूटोरियल चयनित पृष्ठों को छवियों में बदलने के लिए एक विस्तृत मार्गदर्शिका प्रदान करता है।
type: docs
weight: 18
url: /hi/net/rendering-and-export/render-limited-number-of-sequential-pages/
---
## परिचय
एक्सेल वर्कबुक से विशिष्ट पृष्ठों को रेंडर करना अविश्वसनीय रूप से उपयोगी हो सकता है, खासकर तब जब आपको पूरी फ़ाइल के बिना केवल कुछ डेटा विज़ुअल की आवश्यकता होती है। .NET के लिए Aspose.Cells एक पावरहाउस लाइब्रेरी है जो .NET अनुप्रयोगों में एक्सेल दस्तावेज़ों पर सटीक नियंत्रण प्रदान करती है, जिससे चुनिंदा पृष्ठों को रेंडर करना, फ़ॉर्मेट बदलना और बहुत कुछ संभव हो जाता है। यह ट्यूटोरियल आपको विशिष्ट एक्सेल वर्कशीट पृष्ठों को छवि प्रारूपों में परिवर्तित करने के बारे में बताता है - अनुकूलित डेटा स्नैपशॉट बनाने के लिए आदर्श।
## आवश्यक शर्तें
कोड में प्रवेश करने से पहले, सुनिश्चित करें कि आपने निम्नलिखित आइटम सेट अप कर लिए हैं:
-  .NET लाइब्रेरी के लिए Aspose.Cells: आप कर सकते हैं[यहाँ पर डाउनलोड करो](https://releases.aspose.com/cells/net/).
- विकास वातावरण: कोई भी .NET समर्थित वातावरण जैसे कि Visual Studio.
- एक्सेल फ़ाइल: एकाधिक पृष्ठों वाली एक नमूना एक्सेल फ़ाइल, जो आपकी स्थानीय निर्देशिका में सहेजी गई है।
 इसके अतिरिक्त, सुनिश्चित करें कि आप निःशुल्क परीक्षण प्राप्त करें या यदि आपके पास लाइसेंस नहीं है तो उसे खरीद लें।[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) खरीदारी करने से पहले संपूर्ण सुविधाओं का पता लगाने के लिए यहां क्लिक करें।
## पैकेज आयात करें
आरंभ करने के लिए, हमें आपके .NET परिवेश में Aspose.Cells और किसी भी आवश्यक नामस्थान को आयात करना होगा।
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Rendering;
```
ये पैकेज एक्सेल फ़ाइलों को मैनिपुलेट और रेंडर करने के लिए आवश्यक सभी क्लास और मेथड प्रदान करते हैं। अब, आइए रेंडरिंग प्रक्रिया के प्रत्येक भाग को विस्तार से समझें।
## चरण 1: स्रोत और आउटपुट निर्देशिकाएँ सेट करें
सबसे पहले, हम इनपुट और आउटपुट फ़ाइलों के लिए निर्देशिकाएँ परिभाषित करते हैं, ताकि यह सुनिश्चित हो सके कि हमारा प्रोग्राम जानता है कि फ़ाइलों को कहाँ से प्राप्त और संग्रहीत करना है।
```csharp
// स्रोत निर्देशिका
string sourceDir = "Your Document Directory";
// आउटपुट निर्देशिका
string outputDir = "Your Document Directory";
```
स्रोत और आउटपुट निर्देशिकाओं को निर्दिष्ट करके, आप पढ़ने और लिखने दोनों कार्यों के लिए अपनी फ़ाइल एक्सेस को सुव्यवस्थित करते हैं। रनटाइम त्रुटियों से बचने के लिए सुनिश्चित करें कि ये निर्देशिकाएँ मौजूद हैं।
## चरण 2: नमूना एक्सेल फ़ाइल लोड करें
 इसके बाद, हम Aspose.Cells का उपयोग करके अपनी एक्सेल फ़ाइल लोड करते हैं।`Workbook` क्लास. इस फ़ाइल में वह डेटा और पेज होंगे जिन्हें हम रेंडर करना चाहते हैं.
```csharp
// नमूना एक्सेल फ़ाइल लोड करें
Workbook wb = new Workbook(sourceDir + "sampleImageOrPrintOptions_PageIndexPageCount.xlsx");
```
`Workbook`क्लास Aspose.Cells में आपके मुख्य एक्सेल हैंडलर की तरह है, जो शीट्स, स्टाइल्स और बहुत कुछ तक सीधी पहुंच प्रदान करता है।
## चरण 3: लक्ष्य वर्कशीट तक पहुंचें
अब, आइए उस विशिष्ट वर्कशीट का चयन करें जिसके साथ हम काम करना चाहते हैं। इस ट्यूटोरियल के लिए, हम पहली शीट का उपयोग करेंगे, लेकिन आप इसे अपनी ज़रूरत के अनुसार किसी भी शीट में संशोधित कर सकते हैं।
```csharp
// पहली वर्कशीट तक पहुँचें
Worksheet ws = wb.Worksheets[0];
```
प्रत्येक कार्यपुस्तिका में कई कार्यपत्रक हो सकते हैं, और सही कार्यपत्रक का चयन करना महत्वपूर्ण है। यह पंक्ति निर्दिष्ट कार्यपत्रक तक पहुँच प्रदान करती है जहाँ रेंडरिंग होगी।
## चरण 4: छवि या प्रिंट विकल्प सेट करें
हमारे पेज कैसे रेंडर किए जाएँ, इसे नियंत्रित करने के लिए हम कुछ प्रिंट विकल्प परिभाषित करेंगे। यहाँ, हम निर्दिष्ट करेंगे कि कौन से पेज रेंडर किए जाएँ, इमेज फ़ॉर्मेट और अन्य सेटिंग्स।
```csharp
// छवि या प्रिंट विकल्प निर्दिष्ट करें
ImageOrPrintOptions opts = new ImageOrPrintOptions();
opts.PageIndex = 3; // पेज 4 से शुरू करें
opts.PageCount = 4; // चार पृष्ठ प्रस्तुत करें
opts.ImageType = Drawing.ImageType.Png;
```
 साथ`ImageOrPrintOptions` , आप सेट कर सकते हैं`PageIndex` (प्रारंभिक पृष्ठ),`PageCount` (प्रस्तुत करने के लिए पृष्ठों की संख्या), और`ImageType` (आउटपुट के लिए प्रारूप)। यह सेटअप आपको रेंडरिंग प्रक्रिया पर सटीक नियंत्रण देता है।
## चरण 5: शीट रेंडर ऑब्जेक्ट बनाएँ
अब, हम एक बनाते हैं`SheetRender` ऑब्जेक्ट, जो हमारी वर्कशीट और छवि विकल्पों को लेगा और प्रत्येक निर्दिष्ट पृष्ठ को एक छवि के रूप में प्रस्तुत करेगा।
```csharp
// शीट रेंडर ऑब्जेक्ट बनाएं
SheetRender sr = new SheetRender(ws, opts);
```
`SheetRender` क्लास वर्कशीट को इमेज, पीडीएफ या अन्य फॉर्मेट में रेंडर करने के लिए ज़रूरी है। यह आउटपुट जेनरेट करने के लिए आपके द्वारा कॉन्फ़िगर किए गए वर्कशीट और विकल्पों का उपयोग करता है।
## चरण 6: प्रत्येक पृष्ठ को एक छवि के रूप में प्रस्तुत करें और सहेजें
अंत में, आइए प्रत्येक निर्दिष्ट पृष्ठ के माध्यम से लूप करें और इसे एक छवि के रूप में सहेजें। यह लूप प्रत्येक पृष्ठ को रेंडर करने और इसे एक अद्वितीय नाम के साथ सहेजने का काम करता है।
```csharp
// सभी पृष्ठों को चित्र के रूप में प्रिंट करें
for (int i = opts.PageIndex; i < sr.PageCount; i++)
{
    sr.ToImage(i, outputDir + "outputImage-" + (i + 1) + ".png");
}
```
यहां जो कुछ हो रहा है उसका विवरण दिया गया है:
- `for` लूप निर्दिष्ट सीमा में प्रत्येक पृष्ठ से गुजरता है।
- `ToImage` प्रत्येक पृष्ठ को एक छवि के रूप में प्रस्तुत करने के लिए उपयोग किया जाता है, प्रत्येक पृष्ठ को अलग पहचान देने के लिए एक कस्टम फ़ाइल नाम प्रारूप के साथ।
## चरण 7: पूर्णता की पुष्टि करें
रेंडरिंग पूरा होने के बाद एक सरल पुष्टिकरण संदेश जोड़ें। यह चरण वैकल्पिक है लेकिन सफल निष्पादन की पुष्टि के लिए उपयोगी हो सकता है।
```csharp
Console.WriteLine("RenderLimitedNoOfSequentialPages executed successfully.\r\n");
```
यह अंतिम पंक्ति पुष्टि करती है कि सब कुछ अपेक्षित रूप से काम कर रहा है। सभी पेज रेंडर और सेव हो जाने के बाद आपको यह संदेश आपके कंसोल में दिखाई देगा।
## निष्कर्ष
और अब यह हो गया! .NET के लिए Aspose.Cells के साथ Excel कार्यपुस्तिका में विशिष्ट पृष्ठों को रेंडर करना आपके डेटा आउटपुट को कस्टमाइज़ करने का एक सीधा लेकिन शक्तिशाली तरीका है। चाहे आपको मुख्य मीट्रिक या विशिष्ट डेटा विज़ुअल का स्नैपशॉट चाहिए, यह ट्यूटोरियल आपके लिए है। इन चरणों का पालन करके, अब आप अपनी Excel फ़ाइलों से किसी भी पृष्ठ या पृष्ठों की श्रेणी को सुंदर छवि प्रारूपों में रेंडर कर सकते हैं।
 अन्य विकल्पों का पता लगाने के लिए स्वतंत्र महसूस करें`ImageOrPrintOptions` और`SheetRender` और भी अधिक नियंत्रण के लिए। हैप्पी कोडिंग!
## अक्सर पूछे जाने वाले प्रश्न
### क्या मैं एक साथ कई वर्कशीट प्रस्तुत कर सकता हूँ?  
 हाँ, आप लूप के माध्यम से जा सकते हैं`Worksheets` संग्रह और प्रत्येक शीट पर व्यक्तिगत रूप से रेंडरिंग प्रक्रिया लागू करें।
### मैं PNG के अलावा अन्य किन प्रारूपों में पृष्ठ प्रस्तुत कर सकता हूँ?  
 Aspose.Cells कई प्रारूपों का समर्थन करता है, जिसमें JPEG, BMP, TIFF और GIF शामिल हैं। बस बदलें`ImageType` में`ImageOrPrintOptions`.
### मैं कई पृष्ठों वाली बड़ी एक्सेल फ़ाइलों को कैसे संभालूँ?  
बड़ी फ़ाइलों के लिए, मेमोरी उपयोग को प्रभावी ढंग से प्रबंधित करने के लिए रेंडर को छोटे-छोटे खंडों में विभाजित करने पर विचार करें।
### क्या छवि रिज़ोल्यूशन को अनुकूलित करना संभव है?  
 हाँ,`ImageOrPrintOptions` कस्टम रिज़ॉल्यूशन के लिए DPI सेट करने की अनुमति देता है`HorizontalResolution` और`VerticalResolution`.
### यदि मुझे पृष्ठ का केवल एक भाग ही प्रस्तुत करना हो तो क्या होगा?  
आप इसका उपयोग कर सकते हैं`PrintArea` संपत्ति में`PageSetup` किसी कार्यपत्रक पर प्रस्तुत करने के लिए विशिष्ट क्षेत्रों को परिभाषित करना।