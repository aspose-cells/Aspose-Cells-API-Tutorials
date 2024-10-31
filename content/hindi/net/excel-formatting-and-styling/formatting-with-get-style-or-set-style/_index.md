---
title: एक्सेल में गेट स्टाइल या सेट स्टाइल के साथ फ़ॉर्मेटिंग
linktitle: एक्सेल में गेट स्टाइल या सेट स्टाइल के साथ फ़ॉर्मेटिंग
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: इस आसान गाइड में .NET के लिए Aspose.Cells का उपयोग करके Excel सेल को फ़ॉर्मेट करना सीखें। सटीक डेटा प्रस्तुति के लिए स्टाइल और बॉर्डर मास्टर करें।
type: docs
weight: 12
url: /hi/net/excel-formatting-and-styling/formatting-with-get-style-or-set-style/
---
## परिचय
जब डेटा प्रबंधन की बात आती है तो एक्सेल एक पावरहाउस है, और .NET के लिए Aspose.Cells अपने सीधे API के साथ इसे और भी अधिक शक्तिशाली बनाता है जो डेवलपर्स को एक्सेल फ़ाइलों में हेरफेर करने की अनुमति देता है। चाहे आप व्यावसायिक रिपोर्टिंग या व्यक्तिगत परियोजनाओं के लिए स्प्रेडशीट को फ़ॉर्मेट कर रहे हों, एक्सेल में शैलियों को अनुकूलित करना जानना आवश्यक है। इस गाइड में, हम आपके एक्सेल सेल में विभिन्न शैलियों को लागू करने के लिए .NET में Aspose.Cells लाइब्रेरी का उपयोग करने की अनिवार्यताओं में गोता लगाएँगे।
## आवश्यक शर्तें
इससे पहले कि हम आपकी एक्सेल फाइलों को स्टाइल करने की बारीकियों में उतरें, यहां कुछ आवश्यक बातें बताई गई हैं जो आपके पास होनी चाहिए:
1. .NET वातावरण: सुनिश्चित करें कि आपके पास .NET विकास वातावरण सेट अप है। आप Visual Studio का उपयोग कर सकते हैं, जो आपके प्रोजेक्ट बनाना और प्रबंधित करना आसान बनाता है।
2.  Aspose.Cells लाइब्रेरी: आपको .NET लाइब्रेरी के लिए Aspose.Cells की आवश्यकता होगी। आप इसे यहाँ से डाउनलोड कर सकते हैं।[पेज](https://releases.aspose.com/cells/net/) , या आप एक का विकल्प चुन सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).
3. बुनियादी C# ज्ञान: C# से परिचित होने से आपको कोड स्निपेट को बेहतर ढंग से समझने में मदद मिलेगी।
4. नामस्थानों के संदर्भ: सुनिश्चित करें कि आपके प्रोजेक्ट में आवश्यक नामस्थान शामिल हैं, ताकि आप अपनी आवश्यकतानुसार कक्षाओं तक पहुंच सकें।
## पैकेज आयात करें
आरंभ करने के लिए, आपको उचित नामस्थान आयात करने की आवश्यकता होगी। यहां बताया गया है कि आप इसे कैसे करते हैं:
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```
यह स्निपेट कार्यपुस्तिका में हेरफेर और स्टाइलिंग सहित एक्सेल फ़ाइलों को संभालने के लिए आवश्यक क्लासेस को आयात करता है।
अब, आइये इस प्रक्रिया को विस्तृत चरणों में विभाजित करें ताकि आप आसानी से उसका अनुसरण कर सकें।
## चरण 1: दस्तावेज़ निर्देशिका सेट करें
अपनी परियोजना की दस्तावेज़ निर्देशिका बनाएँ और परिभाषित करें
सबसे पहले, हमें एक डायरेक्टरी सेट करनी होगी जहाँ हमारी एक्सेल फाइलें स्टोर की जाएँगी। यह वह जगह है जहाँ Aspose.Cells फ़ॉर्मेटेड एक्सेल फ़ाइल को सेव करेगा।
```csharp
string dataDir = "Your Document Directory";
// यदि निर्देशिका पहले से मौजूद नहीं है तो उसे बनाएं।
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
इस चरण में, हम जाँचते हैं कि निर्दिष्ट निर्देशिका मौजूद है या नहीं। यदि नहीं है, तो हम इसे बनाते हैं। इससे आपकी फ़ाइलें व्यवस्थित और सुलभ रहती हैं।
## चरण 2: वर्कबुक ऑब्जेक्ट को इंस्टैंसिएट करें
एक्सेल वर्कबुक बनाएं
इसके बाद, हमें एक नई कार्यपुस्तिका बनानी होगी जहां हम अपना सारा फ़ॉर्मेटिंग कार्य करेंगे।
```csharp
Workbook workbook = new Workbook();
```
यह पंक्ति एक नई वर्कबुक ऑब्जेक्ट को आरंभ करती है, जो अनिवार्यतः एक नई एक्सेल फ़ाइल बनाती है।
## चरण 3: वर्कशीट का संदर्भ प्राप्त करें
प्रथम वर्कशीट तक पहुँचना
एक बार वर्कबुक बन जाने के बाद, हमें इसकी वर्कशीट तक पहुंचने की जरूरत होती है। प्रत्येक वर्कबुक में कई वर्कशीट हो सकती हैं।
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
यहां, हम अपनी नव निर्मित कार्यपुस्तिका की पहली वर्कशीट (इंडेक्स 0) तक पहुंच रहे हैं।
## चरण 4: किसी सेल तक पहुँचें
एक विशिष्ट सेल का चयन करें
अब, आइए उस सेल को निर्दिष्ट करें जिसे हम फ़ॉर्मेट करना चाहते हैं। इस मामले में, हम सेल A1 के साथ काम करने जा रहे हैं।
```csharp
Cell cell = worksheet.Cells["A1"];
```
यह चरण हमें एक विशिष्ट सेल को लक्षित करने की अनुमति देता है जहां हम अपनी स्टाइलिंग लागू करेंगे।
## चरण 5: सेल में डेटा इनपुट करें
सेल में मूल्य जोड़ना
अब, आइए अपने चुने हुए सेल में कुछ टेक्स्ट डालें।
```csharp
cell.PutValue("Hello Aspose!");
```
 यहाँ, हम उपयोग करते हैं`PutValue` टेक्स्ट को "Hello Aspose!" पर सेट करने की विधि। अपने टेक्स्ट को Excel में देखना हमेशा रोमांचक होता है!
## चरण 6: स्टाइल ऑब्जेक्ट परिभाषित करें
फ़ॉर्मेटिंग के लिए स्टाइल ऑब्जेक्ट बनाना
शैलियाँ लागू करने के लिए, हमें पहले एक स्टाइल ऑब्जेक्ट बनाना होगा।
```csharp
Aspose.Cells.Style style;
style = cell.GetStyle();
```
यह पंक्ति सेल A1 की वर्तमान शैली को पुनः प्राप्त करती है, जिससे हम इसे संशोधित कर सकते हैं।
## चरण 7: ऊर्ध्वाधर और क्षैतिज संरेखण सेट करें
अपने पाठ को केन्द्रित करना
आइए सेल के भीतर पाठ के संरेखण को समायोजित करें ताकि इसे दृश्य रूप से आकर्षक बनाया जा सके।
```csharp
style.VerticalAlignment = TextAlignmentType.Center;
style.HorizontalAlignment = TextAlignmentType.Center;
```
इन गुणों को सेट करने के बाद, पाठ अब सेल A1 में ऊर्ध्वाधर और क्षैतिज दोनों तरह से केंद्रित हो जाएगा।
## चरण 8: फ़ॉन्ट का रंग बदलें
अपने पाठ को अलग बनाएं
रंग का एक स्पलैश आपके डेटा को आकर्षक बना सकता है। चलिए फ़ॉन्ट का रंग बदलकर हरा कर देते हैं।
```csharp
style.Font.Color = Color.Green;
```
यह रंगीन परिवर्तन न केवल पठनीयता को बढ़ाता है, बल्कि आपकी स्प्रेडशीट में व्यक्तित्व भी जोड़ता है!
## चरण 9: फिट करने के लिए टेक्स्ट को छोटा करें
यह सुनिश्चित करना कि पाठ साफ और सुव्यवस्थित हो
इसके बाद, हम यह सुनिश्चित करना चाहते हैं कि पाठ सेल के भीतर अच्छी तरह से फिट हो जाए, खासकर यदि हमारे पास एक लंबी स्ट्रिंग है।
```csharp
style.ShrinkToFit = true;
```
इस सेटिंग के साथ, फ़ॉन्ट का आकार स्वचालित रूप से सेल आयामों के अनुरूप समायोजित हो जाएगा।
## चरण 10: सीमाएं निर्धारित करें
निचला बॉर्डर जोड़ना
एक ठोस बॉर्डर आपकी सेल परिभाषाओं को स्पष्ट बना सकता है। आइए सेल के निचले भाग पर बॉर्डर लगाएं।
```csharp
style.Borders[BorderType.BottomBorder].Color = Color.Red;
style.Borders[BorderType.BottomBorder].LineStyle = CellBorderType.Medium;
```
यहां, हम निचली सीमा के लिए रंग और रेखा शैली निर्दिष्ट करते हैं, जिससे हमारे सेल को एक परिभाषित बंदोबस्त मिलता है।
## चरण 11: सेल पर स्टाइल लागू करें
अपनी शैली में परिवर्तन को अंतिम रूप देना
अब, हमारे द्वारा परिभाषित सभी सुंदर शैलियों को हमारे सेल पर लागू करने का समय आ गया है।
```csharp
cell.SetStyle(style);
```
यह कमांड संचित शैली गुणों को लागू करके हमारे स्वरूपण को अंतिम रूप देता है।
## चरण 12: कार्यपुस्तिका सहेजें
अपना कार्य सहेजना
अंत में, हमें अपनी नई स्वरूपित एक्सेल फ़ाइल को सेव करना होगा।
```csharp
workbook.Save(dataDir + "book1.out.xls");
```
यह पंक्ति कुशलतापूर्वक सब कुछ निर्दिष्ट निर्देशिका में सहेज लेती है, स्वरूपण और सब कुछ!
## निष्कर्ष
और वाह! अब आपने .NET के लिए Aspose.Cells का उपयोग करके एक Excel सेल को सफलतापूर्वक फ़ॉर्मेट कर लिया है। पहली नज़र में यह बहुत ज़्यादा लग सकता है, लेकिन एक बार जब आप चरणों से परिचित हो जाते हैं, तो यह एक सहज प्रक्रिया है जो आपके स्प्रेडशीट हेरफेर को बढ़ा सकती है। शैलियों को अनुकूलित करके, आप अपने डेटा प्रस्तुति की स्पष्टता और सौंदर्य को बढ़ाते हैं। तो, आप आगे क्या फ़ॉर्मेट करने जा रहे हैं?
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.Cells क्या है?
Aspose.Cells एक मजबूत लाइब्रेरी है जो आपको .NET अनुप्रयोगों का उपयोग करके Excel फ़ाइलें बनाने, उनमें हेरफेर करने और आयात करने की अनुमति देती है।
### क्या मैं Aspose.Cells का परीक्षण संस्करण डाउनलोड कर सकता हूँ?
 हां, आप एक निःशुल्क परीक्षण डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).
### Aspose.Cells कौन सी प्रोग्रामिंग भाषाओं का समर्थन करता है?
Aspose.Cells मुख्य रूप से फ़ाइल हेरफेर के लिए .NET, Java और कई अन्य प्रोग्रामिंग भाषाओं का समर्थन करता है।
### मैं एक साथ कई सेलों को कैसे फ़ॉर्मेट कर सकता हूँ?
आप एक साथ कई कक्षों पर शैलियाँ लागू करने के लिए कक्ष संग्रहों के माध्यम से लूप कर सकते हैं।
### मैं Aspose.Cells पर आगे का दस्तावेज़ कहां पा सकता हूं?
 अतिरिक्त संसाधन और दस्तावेज़ यहां पाए जा सकते हैं[यहाँ](https://reference.aspose.com/cells/net/).