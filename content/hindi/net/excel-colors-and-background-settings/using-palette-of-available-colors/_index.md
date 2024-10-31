---
title: एक्सेल में उपलब्ध रंगों के पैलेट का उपयोग करना
linktitle: एक्सेल में उपलब्ध रंगों के पैलेट का उपयोग करना
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: जानें कि कस्टम कलर पैलेट कैसे बनाएं और उन्हें .NET के लिए Aspose.Cells का उपयोग करके अपने एक्सेल स्प्रेडशीट पर कैसे लागू करें। जीवंत रंगों और फ़ॉर्मेटिंग विकल्पों के साथ अपने डेटा की दृश्य अपील को बढ़ाएँ।
type: docs
weight: 11
url: /hi/net/excel-colors-and-background-settings/using-palette-of-available-colors/
---
## परिचय
क्या आपने कभी किसी नीरस, मोनोक्रोम स्प्रेडशीट को देखा है और उसमें रंग भरने की इच्छा की है? .NET के लिए Aspose.Cells बचाव के लिए आता है, जो आपको कस्टम रंग पैलेट की शक्ति का उपयोग करने और अपनी स्प्रेडशीट को देखने में आश्चर्यजनक मास्टरपीस में बदलने की शक्ति देता है। इस व्यापक गाइड में, हम Aspose.Cells का उपयोग करके Excel में रंग अनुकूलन के रहस्यों को अनलॉक करने के लिए चरण-दर-चरण यात्रा शुरू करेंगे। 

## आवश्यक शर्तें

- Aspose.Cells for .NET लाइब्रेरी: वेबसाइट से नवीनतम संस्करण डाउनलोड करें ([https://releases.aspose.com/ Cells/net/](https://releases.aspose.com/cells/net/)) प्रारंभ करना। 
- टेक्स्ट एडिटर या IDE: अपनी पसंद का हथियार चुनें, जैसे विजुअल स्टूडियो या कोई अन्य .NET विकास वातावरण। 
- बुनियादी प्रोग्रामिंग ज्ञान: यह मार्गदर्शिका मानती है कि आपको C# की बुनियादी समझ है और .NET परियोजनाओं में लाइब्रेरीज़ के साथ काम करने की जानकारी है।

## पैकेज आयात करें

 इसके अतिरिक्त, आपको कुछ सिस्टम नेमस्पेस आयात करने की आवश्यकता होगी जैसे`System.IO` फ़ाइल हेरफेर के लिए. 

```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```

रंगीन स्प्रेडशीट तैयार करना: एक चरण-दर-चरण मार्गदर्शिका

अब, आइए कोड में गोता लगाएँ और देखें कि कस्टम कलर पैलेट कैसे बनाएँ और इसे एक्सेल सेल पर कैसे लागू करें। कल्पना करें कि आप अपनी स्प्रेडशीट को जीवंत "ऑर्किड" रंग से रंग रहे हैं!

## चरण 1: निर्देशिका सेट अप करना:

```csharp
// अपने दस्तावेज़ निर्देशिका का पथ निर्धारित करें
string dataDir = "Your Document Directory";

// यदि निर्देशिका मौजूद नहीं है तो उसे बनाएँ
bool isExists = System.IO.Directory.Exists(dataDir);
if (!isExists)
{
   System.IO.Directory.CreateDirectory(dataDir);
}
```

यह कोड स्निपेट वह निर्देशिका स्थापित करता है जहाँ आप अपनी अंतिम एक्सेल फ़ाइल को सहेजना चाहते हैं। "आपकी दस्तावेज़ निर्देशिका" को अपने सिस्टम पर वास्तविक पथ से बदलना याद रखें।

## चरण 2: वर्कबुक ऑब्जेक्ट को इंस्टैंशिएट करना:

```csharp
// एक नया वर्कबुक ऑब्जेक्ट बनाएँ
Workbook workbook = new Workbook();
```

 के बारे में सोचो`Workbook` ऑब्जेक्ट को खाली कैनवास के रूप में चुनें जहाँ आप अपनी रंगीन मास्टरपीस को पेंट करेंगे। यह लाइन एक नई वर्कबुक इंस्टेंस बनाती है, जो डेटा और फ़ॉर्मेटिंग से भरने के लिए तैयार है।

## चरण 3: पैलेट में कस्टम रंग जोड़ना:

```csharp
// पैलेट में इंडेक्स 55 पर ऑर्किड रंग जोड़ें
workbook.ChangePalette(Color.Orchid, 55);
```

यहाँ जादू होता है! यह लाइन एक्सेल कलर पैलेट में एक कस्टम रंग, इस मामले में "ऑर्किड" जोड़ती है।`ChangePalette` विधि दो तर्क लेती है: वांछित रंग और पैलेट के भीतर सूचकांक (0 से 55 तक) जहां आप इसे रखना चाहते हैं। 

महत्वपूर्ण नोट: एक्सेल में सीमित डिफ़ॉल्ट रंग पैलेट है। यदि आप डिफ़ॉल्ट सेट में मौजूद नहीं किसी रंग का उपयोग करने का प्रयास करते हैं, तो आपको इसे अपनी स्प्रेडशीट में किसी भी तत्व पर लागू करने से पहले इस विधि का उपयोग करके पैलेट में जोड़ना होगा।

## चरण 4: नई वर्कशीट बनाना:

```csharp
// कार्यपुस्तिका में एक नई कार्यपत्रिका जोड़ें
int i = workbook.Worksheets.Add();

// नए जोड़े गए वर्कशीट का संदर्भ प्राप्त करें
Worksheet worksheet = workbook.Worksheets[i];
```

हाथ में खाली कैनवास (वर्कबुक) के साथ, अपने कलात्मक प्रयासों के लिए एक शीट बनाने का समय आ गया है। यह कोड स्निपेट वर्कबुक में एक नई वर्कशीट जोड़ता है और इसके इंडेक्स का उपयोग करके इसका संदर्भ प्राप्त करता है।

## चरण 5: लक्ष्य सेल तक पहुंचना:

```csharp
// "A1" स्थिति पर स्थित सेल तक पहुँचें
Cell cell = worksheet.Cells["A1"];
```

अपनी स्प्रेडशीट को एक विशाल ग्रिड के रूप में कल्पना करें। प्रत्येक सेल का एक अनूठा पता होता है, जिसे कॉलम अक्षर (A, B, C...) और पंक्ति संख्या (1, 2, 3...) के संयोजन से पहचाना जाता है। यह पंक्ति नई बनाई गई वर्कशीट के भीतर "A1" पर स्थित सेल का संदर्भ प्राप्त करती है।

## चरण 6: सेल में सामग्री जोड़ना:

```csharp
// सेल A1 में कुछ टेक्स्ट जोड़ें
cell.PutValue("Hello Aspose!");
```

अब जब आपके पास अपना पेंटब्रश (सेल संदर्भ) है, तो कैनवास पर कुछ सामग्री जोड़ने का समय आ गया है। यह पंक्ति पाठ सम्मिलित करती है "

## चरण 7: कस्टम रंग लागू करना

```csharp
// एक नया स्टाइल ऑब्जेक्ट बनाएं
Style styleObject = workbook.CreateStyle();

// फ़ॉन्ट पर ऑर्किड रंग सेट करें
styleObject.Font.Color = Color.Orchid;

// सेल पर शैली लागू करें
cell.SetStyle(styleObject);
```

 इस चरण में, हम एक नया बना रहे हैं`Style` हमारे पाठ के लिए स्वरूपण को परिभाषित करने के लिए ऑब्जेक्ट।`styleObject.Font.Color` प्रॉपर्टी को "ऑर्किड" रंग पर सेट किया गया है जिसे हमने पहले पैलेट में जोड़ा था। अंत में,`cell.SetStyle` विधि "A1" पर पहले से चयनित सेल पर शैली लागू करती है।

## चरण 8: कार्यपुस्तिका को सहेजना

```csharp
// कार्यपुस्तिका सहेजें
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Auto);
```

यह अंतिम पंक्ति कार्यपुस्तिका को उसके सभी स्वरूपण परिवर्तनों के साथ निर्दिष्ट निर्देशिका में सहेज देती है।`SaveFormat.Auto` तर्क स्वचालित रूप से फ़ाइल एक्सटेंशन के आधार पर उपयुक्त फ़ाइल प्रारूप निर्धारित करता है।

## निष्कर्ष

इन चरणों का पालन करके, आपने .NET के लिए Aspose.Cells का उपयोग करके Excel में रंग पैलेट को सफलतापूर्वक अनुकूलित कर लिया है। अब आप अपनी रचनात्मकता को उजागर कर सकते हैं और आकर्षक स्प्रेडशीट बना सकते हैं जो भीड़ से अलग दिखाई देती हैं। 

## अक्सर पूछे जाने वाले प्रश्न

### क्या मैं Color.Orchid के अलावा अन्य रंग प्रारूपों का उपयोग कर सकता हूँ?
 बिल्कुल! आप किसी भी रंग का उपयोग कर सकते हैं`Color` गणना या कस्टम रंग परिभाषित का उपयोग कर`Color` संरचना।

### मैं एकाधिक कक्षों पर कस्टम रंग कैसे लागू करूँ?
 आप एक बना सकते हैं`Style` ऑब्जेक्ट को चुनें और लूप या रेंज का उपयोग करके इसे एकाधिक कक्षों पर लागू करें।

### क्या मैं कस्टम रंग ग्रेडिएंट बना सकता हूँ?
हां, Aspose.Cells आपको सेल या आकृतियों के लिए कस्टम रंग ग्रेडिएंट बनाने की अनुमति देता है। अधिक जानकारी के लिए दस्तावेज़ देखें।

### क्या किसी सेल का पृष्ठभूमि रंग बदलना संभव है?
ज़रूर! आप इसे संशोधित कर सकते हैं`Style` वस्तु का`BackgroundColor` पृष्ठभूमि का रंग बदलने के लिए संपत्ति.

### मैं और अधिक उदाहरण और दस्तावेज कहां पा सकता हूं?
.NET दस्तावेज़ के लिए Aspose.Cells पर जाएँ ([https://reference.aspose.com/ Cells/net/](https://reference.aspose.com/cells/net/)) विस्तृत जानकारी और कोड उदाहरणों के लिए देखें।