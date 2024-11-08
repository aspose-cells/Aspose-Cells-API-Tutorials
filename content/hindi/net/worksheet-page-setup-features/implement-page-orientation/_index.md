---
title: वर्कशीट में पेज ओरिएंटेशन लागू करें
linktitle: वर्कशीट में पेज ओरिएंटेशन लागू करें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके Excel वर्कशीट में पेज ओरिएंटेशन सेट करना सीखें। बेहतर दस्तावेज़ प्रस्तुति के लिए सरल चरण-दर-चरण मार्गदर्शिका।
type: docs
weight: 18
url: /hi/net/worksheet-page-setup-features/implement-page-orientation/
---
## परिचय
जब स्प्रेडशीट को फ़ॉर्मेट करने की बात आती है, तो एक महत्वपूर्ण पहलू जिसे अक्सर अनदेखा कर दिया जाता है वह है पेज ओरिएंटेशन। स्प्रेडशीट बनाते या प्रस्तुत करते समय आप इसके बारे में ज़्यादा नहीं सोचते होंगे, लेकिन आपकी सामग्री का संरेखण इसकी पठनीयता और समग्र सौंदर्य को महत्वपूर्ण रूप से प्रभावित कर सकता है। इस गाइड में, हम .NET के लिए Aspose.Cells का उपयोग करके वर्कशीट में पेज ओरिएंटेशन को लागू करने के तरीके के बारे में विस्तार से जानेंगे।
## आवश्यक शर्तें
इससे पहले कि हम बारीकियों में उतरें, आइए सुनिश्चित करें कि आपके पास .NET के लिए Aspose.Cells के साथ कुशलतापूर्वक काम करने के लिए सब कुछ सेट है।
### जिसकी आपको जरूरत है:
1.  विजुअल स्टूडियो: यह लेख मानता है कि आपके पास यह स्थापित है; यदि नहीं, तो आप इसे यहाँ से प्राप्त कर सकते हैं[विज़ुअल स्टूडियो डाउनलोड](https://visualstudio.microsoft.com/vs/).
2.  Aspose.Cells for .NET: आपको लाइब्रेरी डाउनलोड करके इंस्टॉल करनी होगी। आप इसे यहाँ से प्राप्त कर सकते हैं[Aspose डाउनलोड पृष्ठ](https://releases.aspose.com/cells/net/) वैकल्पिक रूप से, यदि आप अधिक व्यावहारिक दृष्टिकोण पसंद करते हैं, तो आप हमेशा से शुरुआत कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/).
3. C# का बुनियादी ज्ञान: C# प्रोग्रामिंग से परिचित होना उपयोगी होगा, क्योंकि हमारे उदाहरण इसी भाषा में कोडित किए जाएंगे।
अब जबकि हमने एक ठोस आधार स्थापित कर लिया है, तो आइए आवश्यक पैकेजों को आयात करें ताकि यह सुनिश्चित हो सके कि हम आगे बढ़ने के लिए तैयार हैं।
## पैकेज आयात करें
अपनी कोडिंग यात्रा शुरू करने के लिए, हमें अपने प्रोजेक्ट में Aspose.Cells लाइब्रेरी को आयात करना होगा। इन चरणों का पालन करें:
## विज़ुअल स्टूडियो खोलें 
Visual Studio लॉन्च करें और एक नया C# प्रोजेक्ट बनाएँ। आप अपनी पसंद के अनुसार कंसोल एप्लीकेशन या Windows Forms एप्लीकेशन चुन सकते हैं।
## संदर्भ जोड़ें
सॉल्यूशन एक्सप्लोरर पर जाएँ। अपने प्रोजेक्ट पर राइट-क्लिक करें, मैनेज नुगेट पैकेज चुनें, और Aspose.Cells लाइब्रेरी खोजें। यह सुनिश्चित करने के लिए इसे इंस्टॉल करें कि सभी कार्यक्षमताएँ आपके निपटान में हैं।
## लाइब्रेरी आयात करें 
 आपकी मुख्य प्रोग्राम फ़ाइल में (आमतौर पर`Program.cs`), शीर्ष पर निम्नलिखित निर्देश शामिल करना सुनिश्चित करें:
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
यह चरण आपको Aspose.Cells लाइब्रेरी द्वारा प्रदान की गई सभी कक्षाओं और विधियों तक पहुंच प्रदान करेगा।
अब, आइए .NET के लिए Aspose.Cells का उपयोग करके Excel वर्कशीट में पृष्ठ ओरिएंटेशन को पोर्ट्रेट में बदलने की प्रक्रिया पर चलते हैं।
## चरण 1: दस्तावेज़ निर्देशिका निर्धारित करें
आरंभ करने के लिए, हमें अपनी एक्सेल फ़ाइल को संग्रहीत करने के लिए पथ निर्दिष्ट करना होगा। यहीं पर हम अपनी हेरफेर की गई स्प्रेडशीट को सहेजेंगे।
```csharp
string dataDir = "Your Document Directory";
```
 प्रतिस्थापित करना सुनिश्चित करें`"Your Document Directory"` जैसे एक वास्तविक पथ के साथ`"C:\\Documents\\"` जहाँ आप आउटपुट एक्सेल फ़ाइल को सहेजना चाहते हैं।
## चरण 2: वर्कबुक ऑब्जेक्ट को इंस्टैंसिएट करें
इसके बाद, हमें एक नई वर्कबुक इंस्टेंस बनाने की आवश्यकता है। यह ऑब्जेक्ट अनिवार्य रूप से स्प्रेडशीट में हेरफेर करने के लिए हमारा प्लेग्राउंड है।
```csharp
Workbook workbook = new Workbook();
```
 तत्कालीकरण करके`Workbook`, हमने मेमोरी में एक नई एक्सेल फ़ाइल बनाई है जिस पर हम काम कर सकते हैं।
## चरण 3: पहली वर्कशीट तक पहुँचें
अब जब हमारे पास कार्यपुस्तिका है, तो आइए पहले कार्यपत्रक पर जाएं जहां हम पृष्ठ अभिविन्यास निर्धारित करेंगे। 
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
यहां, हम कार्यपुस्तिका में पहली कार्यपत्रिका तक पहुंच रहे हैं (कार्यपत्रिकाएं शून्य-अनुक्रमित हैं)। 
## चरण 4: ओरिएंटेशन को पोर्ट्रेट पर सेट करें
हमारी वर्कशीट तैयार होने के बाद, अब पेज ओरिएंटेशन सेट करने का समय है। हम कोड की एक सरल लाइन का उपयोग करके आसानी से ओरिएंटेशन बदल सकते हैं:
```csharp
worksheet.PageSetup.Orientation = PageOrientationType.Portrait;
```
बस हो गया! आपने अपनी वर्कशीट को पोर्ट्रेट ओरिएंटेशन पर सफलतापूर्वक सेट कर लिया है। इस चरण की कल्पना करें कि आप अपनी नोटबुक को लैंडस्केप से पोर्ट्रेट में बदल रहे हैं, जिससे आपकी सामग्री ऊपर से नीचे तक अच्छी तरह से प्रवाहित हो रही है।
## चरण 5: कार्यपुस्तिका सहेजें
अंत में, अब समय है कि हम अपने बदलावों को एक्सेल फ़ाइल में सेव करें। यह बहुत ज़रूरी है; अन्यथा, हमारी सारी मेहनत बेकार चली जाएगी!
```csharp
workbook.Save(dataDir + "PageOrientation_out.xls");
```
 यहाँ, हम कार्यपुस्तिका को इस नाम से सहेज रहे हैं`PageOrientation_out.xls` निर्दिष्ट निर्देशिका में.
## निष्कर्ष
और बस इसी तरह, आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके वर्कशीट में पेज ओरिएंटेशन कैसे लागू किया जाता है! जब आप इसे चरण दर चरण तोड़ते हैं तो यह वास्तव में काफी सरल है, है न? अब, आप न केवल अपनी स्प्रेडशीट को बेहतर ढंग से फ़ॉर्मेट कर सकते हैं, बल्कि उन्हें अधिक पठनीय और पेशेवर दिखने वाला भी बना सकते हैं।
रिमोट वर्क और स्क्रीन शेयरिंग में वृद्धि के साथ, अच्छी तरह से फ़ॉर्मेट किए गए दस्तावेज़ वास्तव में बहुत फ़र्क डाल सकते हैं, ख़ास तौर पर प्रेजेंटेशन के दौरान। तो, क्यों न इसे अपने प्रोजेक्ट में आज़माया जाए? 
## अक्सर पूछे जाने वाले प्रश्न
### क्या Aspose.Cells निःशुल्क है?
 Aspose.Cells एक सशुल्क लाइब्रेरी है, लेकिन आप एक से शुरू कर सकते हैं[मुफ्त परीक्षण](https://releases.aspose.com/)जो आपको इसकी विशेषताओं का पता लगाने देता है।
### क्या मैं पृष्ठ ओरिएंटेशन को लैंडस्केप में भी बदल सकता हूँ?
 बिलकुल! बस बदलें`PageOrientationType.Portrait` साथ`PageOrientationType.Landscape` अपने कोड में.
### Aspose.Cells .NET के किस संस्करण का समर्थन करता है?
Aspose.Cells .NET के कई संस्करणों का समर्थन करता है, जिसमें .NET Framework, .NET Core और .NET Standard शामिल हैं।
### यदि मुझे कोई समस्या आती है तो मैं आगे की सहायता कैसे प्राप्त कर सकता हूँ?
 सहायता के लिए आप यहां जा सकते हैं[Aspose समर्थन मंच](https://forum.aspose.com/c/cells/9) जहां समुदाय और टीम आपकी मदद कर सकती है।
### मुझे सम्पूर्ण दस्तावेज कहां मिल सकते हैं?
 आप Aspose.Cells के लिए व्यापक दस्तावेज़ पा सकते हैं[यहाँ](https://reference.aspose.com/cells/net/).