---
title: एक्सेल में टेक्स्टबॉक्स में टैग को टेक्स्ट से बदलें
linktitle: एक्सेल में टेक्स्टबॉक्स में टैग को टेक्स्ट से बदलें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके अपने Excel शीट में टेक्स्ट बॉक्स में टेक्स्ट को आसानी से बदलें। Excel स्वचालन के लिए चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 11
url: /hi/net/excel-shape-text-modifications/replace-tag-text-textbox-excel/
---
## परिचय
इस लेख में, हम एक विशिष्ट कार्य पर चर्चा करेंगे: Aspose.Cells का उपयोग करके Excel शीट में टेक्स्ट बॉक्स के अंदर टैग को टेक्स्ट से बदलना। हम आपको पूरी प्रक्रिया के माध्यम से चरण-दर-चरण मार्गदर्शन करेंगे, यह सुनिश्चित करते हुए कि आप हर विवरण को समझ सकें। इस ट्यूटोरियल के अंत तक, आप न केवल Aspose.Cells की अपनी समझ को बढ़ाएँगे बल्कि अपने Excel-संबंधित कार्यों को भी सुव्यवस्थित करेंगे!
## आवश्यक शर्तें
आरंभ करने से पहले आपको कुछ चीजें तैयार रखनी होंगी:
1. विज़ुअल स्टूडियो: सुनिश्चित करें कि आपके पास विज़ुअल स्टूडियो इंस्टॉल है। यह एक लचीला IDE है जो C# में कोडिंग को आसान बनाता है।
2.  Aspose.Cells लाइब्रेरी: यदि आपने अभी तक ऐसा नहीं किया है, तो .NET के लिए Aspose.Cells लाइब्रेरी को यहाँ से डाउनलोड करें।[पेज](https://releases.aspose.com/cells/net/)आप इसकी विशेषताओं को देखने के लिए इसका निःशुल्क परीक्षण संस्करण भी प्राप्त कर सकते हैं।
3. C# का बुनियादी ज्ञान: C# प्रोग्रामिंग की बुनियादी समझ आपको इस गाइड का आसानी से पालन करने में काफी मदद करेगी।
अब जब आप पूरी तरह तैयार हैं, तो चलिए मज़ेदार भाग की ओर बढ़ते हैं - कोड लिखना!
## पैकेज आयात करें
सबसे पहले सबसे पहले - आइए आवश्यक पैकेज आयात करें। यह महत्वपूर्ण है क्योंकि सही आयात के बिना, आपका कोड उन क्लासेस और विधियों को नहीं पहचान पाएगा जिनका हम उपयोग करेंगे।
## अपना C# प्रोजेक्ट शुरू करें
विजुअल स्टूडियो खोलें और एक नया C# प्रोजेक्ट बनाएं, अधिमानतः एक कंसोल एप्लीकेशन, क्योंकि इससे आप आसानी से आउटपुट देख पाएंगे।
## Aspose.Cells संदर्भ जोड़ें
- सॉल्यूशन एक्सप्लोरर में अपने प्रोजेक्ट पर राइट क्लिक करें।
- “जोड़ें” > “संदर्भ” चुनें।
- उस स्थान पर ब्राउज़ करें जहां से आपने Aspose.Cells लाइब्रेरी डाउनलोड की थी और उसे अपने प्रोजेक्ट में शामिल करें।
## आवश्यक नामस्थान आयात करें
 एक बार संदर्भ जोड़ लेने के बाद, निम्नलिखित जोड़ें`using` अपनी मुख्य फ़ाइल के शीर्ष पर निर्देश:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Drawing;
```
यह आपको Aspose.Cells नामस्थान के भीतर कक्षाओं तक पहुंच प्रदान करता है।
अब जब हमने अपना एनवायरनमेंट सेट कर लिया है, तो चलिए सबसे रोचक भाग में आते हैं - कोडिंग! हमारा लक्ष्य एक्सेल फ़ाइल के भीतर टेक्स्ट बॉक्स में विशिष्ट टैग ढूँढ़ना और उन्हें दिए गए टेक्स्ट से बदलना है।
## चरण 1: स्रोत और आउटपुट निर्देशिका को परिभाषित करें
सबसे पहले, हमें यह निर्दिष्ट करना होगा कि हमारी स्रोत एक्सेल फ़ाइल कहाँ स्थित है और हम संशोधित संस्करण को कहाँ सहेजना चाहते हैं।
```csharp
// स्रोत और आउटपुट निर्देशिका
string sourceDir = "Your Document Directory"; // अपनी निर्देशिका में परिवर्तन करें
string outputDir = "Your Document Directory"; // अपनी निर्देशिका में परिवर्तन करें
```
## चरण 2: कार्यपुस्तिका लोड करें
यहीं पर हम अपनी एक्सेल वर्कबुक लोड करेंगे। अगर फ़ाइल मौजूद नहीं है, तो यह एक त्रुटि उत्पन्न करती है। इसलिए, सुनिश्चित करें कि आपकी फ़ाइल का पथ सही है!
```csharp
Workbook wb = new Workbook(sourceDir + "sampleReplaceTagWithText.xlsx");
```
 यहाँ, हम एक मौजूदा एक्सेल फ़ाइल लोड कर रहे हैं जिसका नाम है`sampleReplaceTagWithText.xlsx`.
## चरण 3: टैग और प्रतिस्थापन पाठ परिभाषित करें
इसके बाद, हमें उन टैगों को परिभाषित करना होगा जिन्हें हम ढूंढ रहे हैं और हम उन्हें किसके साथ बदलना चाहते हैं।
```csharp
string tag = "TAG_2$TAG_1";
string replace = "1$ys";
```
 इस उदाहरण में, टैग को विभाजित किया गया है`$`आप इसे अपनी पसंद के किसी भी सीमांकक से बदल सकते हैं।
## चरण 4: टैग पर लूप करें और बदलें
हम प्रत्येक टैग से गुजरने के लिए एक लूप बनाएंगे जिसे हम बदलना चाहते हैं। यहाँ जादू होता है!
```csharp
for (int i = 0; i < tag.Split('$').Length; i++)
{
    sheetReplace(wb, "<" + tag.Split('$')[i] + ">", replace.Split('$')[i]);
}
```
## चरण 5: कार्यपुस्तिका सहेजें
अब जबकि हमने अपने प्रतिस्थापन कर लिए हैं, अब संशोधित कार्यपुस्तिका को वांछित प्रारूप में सहेजने का समय है। यहाँ बताया गया है कि हम इसे PDF में कैसे परिवर्तित करते हैं।
```csharp
PdfSaveOptions opts = new PdfSaveOptions();
wb.Save(outputDir + "outputReplaceTagWithText.pdf", opts);
```
आप इसे XLSX सहित विभिन्न अन्य प्रारूपों में भी सहेज सकते हैं।
## चरण 6: प्रतिस्थापन तर्क को लागू करें
 यहीं पर हमारी कार्यक्षमता का हृदय स्थित है।`sheetReplace` विधि एक्सेल वर्कशीट में वास्तविक प्रतिस्थापन को संभालेगी।
```csharp
public static void sheetReplace(Workbook workbook, string sFind, string sReplace)
{
    string finding = sFind;
    foreach (Worksheet sheet in workbook.Worksheets)
    {
        sheet.Replace(finding, sReplace);
        for (int j = 0; j < 3; j++)
        {
            if (sheet.PageSetup.GetHeader(j) != null)
                sheet.PageSetup.SetHeader(j, sheet.PageSetup.GetHeader(j).Replace(finding, sReplace));
                
            if (sheet.PageSetup.GetFooter(j) != null)
                sheet.PageSetup.SetFooter(j, sheet.PageSetup.GetFooter(j).Replace(finding, sReplace));
        }
    }
    foreach (Worksheet sheet in workbook.Worksheets)
    {
        sFind = sFind.Replace("<", "&lt;");
        sFind = sFind.Replace(">", "&gt;");
        foreach (Aspose.Cells.Drawing.TextBox mytextbox in sheet.TextBoxes)
        {
            if (mytextbox.HtmlText != null)
            {
                if (mytextbox.HtmlText.IndexOf(sFind) >= 0)
                {
                    mytextbox.HtmlText = mytextbox.HtmlText.Replace(sFind, sReplace);
                }
            }
        }
    }
}
```
- सबसे पहले, हम कार्यपुस्तिका में प्रत्येक वर्कशीट पर लूप करते हैं।
- हम मुख्य टैग को न केवल सेल सामग्री में बल्कि हेडर और फ़ुटर (यदि वे मौजूद हैं) में भी बदलते हैं।
- अंत में, हम शीट में प्रत्येक टेक्स्ट बॉक्स को जांचते हैं और उनके भीतर के टेक्स्ट को, उस टैग के आधार पर प्रतिस्थापित करते हैं जिसे हम खोज रहे हैं।
## निष्कर्ष
और वाह! अब आप सीख चुके हैं कि .NET के लिए Aspose.Cells का उपयोग करके अपने Excel दस्तावेज़ों में टेक्स्ट बॉक्स में टैग को टेक्स्ट से कैसे बदला जाए। यह वास्तव में समय बचाने वाला हो सकता है, खासकर जब स्प्रेडशीट में दोहराए जाने वाले कार्यों से निपटना हो।
## अक्सर पूछे जाने वाले प्रश्न
### क्या मैं एक साथ अनेक एक्सेल फाइलों में टैग बदल सकता हूँ?
हां, फ़ाइलों की सूची के माध्यम से लूपिंग करके, आप एक ही तर्क को कई एक्सेल फ़ाइलों पर लागू कर सकते हैं।
### क्या मुझे Aspose.Cells का उपयोग करने के लिए सशुल्क लाइसेंस की आवश्यकता है?
 आप निःशुल्क परीक्षण के साथ शुरुआत कर सकते हैं, लेकिन पूर्ण कार्यक्षमता के लिए, आपको लाइसेंस खरीदना होगा।[Aspose के खरीद विकल्प](https://purchase.aspose.com/buy).
### क्या मैं Aspose.Cells का उपयोग करके टेक्स्ट बॉक्स में छवियों को बदल सकता हूँ?
Aspose.Cells मुख्य रूप से टेक्स्ट से संबंधित है। हालाँकि, यदि आवश्यक हो तो आप छवियों को अलग से भी जोड़ सकते हैं।
### मैं अपनी संशोधित एक्सेल फ़ाइल को किस प्रारूप में सहेज सकता हूँ?
आप इसे XLSX, PDF, CSV आदि सहित विभिन्न प्रारूपों में सहेज सकते हैं।
### मैं Aspose.Cells के लिए समर्थन कहां पा सकता हूं?
 आप सहायता पा सकते हैं और प्रश्न पूछ सकते हैं[एस्पोज फोरम](https://forum.aspose.com/c/cells/9).