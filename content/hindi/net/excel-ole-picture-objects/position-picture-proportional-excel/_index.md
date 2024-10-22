---
title: एक्सेल में चित्र की स्थिति (आनुपातिक)
linktitle: एक्सेल में चित्र की स्थिति (आनुपातिक)
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके Excel में छवियों को आनुपातिक रूप से रखना सीखें। अपनी स्प्रेडशीट को अधिक आकर्षक बनाएँ।
type: docs
weight: 14
url: /hi/net/excel-ole-picture-objects/position-picture-proportional-excel/
---
## परिचय
क्या आप उन पिक्सेलयुक्त छवियों से थक चुके हैं जो आपकी एक्सेल स्प्रेडशीट में कभी भी ठीक से फिट नहीं होती हैं? कल्पना करें: आपके पास एक सुंदर लोगो है जिसे आपकी एक्सेल शीट में प्रमुखता से प्रदर्शित करने की आवश्यकता है, लेकिन यह सिकुड़ जाता है, खिंच जाता है या गलत तरीके से रखा जाता है। कोई भी ऐसा नहीं चाहता! खैर, अपनी सीटों पर बैठें क्योंकि आज आप सीखेंगे कि .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल में छवियों को आनुपातिक रूप से कैसे रखा जाए। यह शक्तिशाली लाइब्रेरी एक्सेल फ़ाइलों में हेरफेर करना आसान बनाती है, चाहे वह रिपोर्टिंग के लिए हो, डेटा विश्लेषण के लिए हो या बस अपनी प्रस्तुतियों को बेहतर बनाने के लिए हो। आइए अपनी तस्वीरों को पूरी तरह से संरेखित करने की बारीकियों में गोता लगाएँ!
## आवश्यक शर्तें
इससे पहले कि हम वास्तविक कोडिंग में उतरें, कुछ चीजें हैं जिन्हें आपको अपनी मशीन पर सेट करना होगा:
1. विज़ुअल स्टूडियो: सुनिश्चित करें कि आपके पास विज़ुअल स्टूडियो स्थापित है, क्योंकि यह आपके .NET प्रोजेक्ट के लिए सुविधाजनक वातावरण प्रदान करेगा।
2.  Aspose.Cells लाइब्रेरी: आपको Aspose.Cells लाइब्रेरी की आवश्यकता होगी। आप इसका निःशुल्क परीक्षण प्राप्त कर सकते हैं या इसे यहाँ से खरीद सकते हैं।[Aspose वेबसाइट](https://purchase.aspose.com/buy).
3. C# का बुनियादी ज्ञान: C# प्रोग्रामिंग से थोड़ी परिचितता, उन उदाहरणों को समझने में काफी सहायक होगी जिन पर हम चर्चा करेंगे।
4. एक छवि फ़ाइल: एक छवि तैयार रखें (जैसे आपका लोगो) जिसे आप एक्सेल शीट में सम्मिलित करना चाहते हैं।
अब जब आपके पास सब कुछ तैयार है, तो चलिए कोडिंग शुरू करते हैं!
## पैकेज आयात करें
अपने प्रोजेक्ट में Aspose.Cells का उपयोग शुरू करने के लिए, आपको विशिष्ट नामस्थानों को आयात करना होगा। ऐसा करने का तरीका यहां बताया गया है:
### एक नया प्रोजेक्ट बनाएं
Visual Studio में, एक नया प्रोजेक्ट बनाएं:
- विजुअल स्टूडियो खोलें.
- "नया प्रोजेक्ट बनाएं" पर क्लिक करें।
- अपनी पसंद के अनुसार "क्लास लाइब्रेरी (.NET फ्रेमवर्क)" या "कंसोल एप्लीकेशन" चुनें।
### Aspose.Cells स्थापित करें
आप NuGet के माध्यम से अपने प्रोजेक्ट में Aspose.Cells पैकेज जोड़ सकते हैं। यहाँ बताया गया है कि कैसे:
- समाधान एक्सप्लोरर में अपने प्रोजेक्ट पर राइट-क्लिक करें।
- "NuGet पैकेज प्रबंधित करें" चुनें.
- "Aspose.Cells" खोजें और "इंस्टॉल करें" पर क्लिक करें।
### उपयोग निर्देश जोड़ें
अपनी कोड फ़ाइल के शीर्ष पर निम्नलिखित निर्देश शामिल करें:
```csharp
using System.IO;
using Aspose.Cells;
```
ये निर्देश आपको उन क्लासों तक पहुंच प्रदान करेंगे जिनकी आपको अपनी एक्सेल फाइलों में हेरफेर करने के लिए आवश्यकता होगी।
अब, आइए एक्सेल में एक छवि को आनुपातिक रूप से सफलतापूर्वक स्थितिबद्ध करने के लिए इसे विस्तृत चरणों में विभाजित करें।
## चरण 1: अपनी निर्देशिका सेट करें
सबसे पहले, सुनिश्चित करें कि आपके पास अपने दस्तावेज़ों के लिए एक निर्दिष्ट फ़ोल्डर है। यदि यह मौजूद नहीं है, तो निर्देशिका बनाने का तरीका यहां बताया गया है:
```csharp
string dataDir = "Your Document Directory";
//यदि निर्देशिका पहले से मौजूद नहीं है तो उसे बनाएं।
bool isExists = System.IO.Directory.Exists(dataDir);
if (!isExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
 यह स्निपेट आपकी एक्सेल फ़ाइलों को संग्रहीत करने के लिए एक नई निर्देशिका बनाता है (यदि यह मौजूद नहीं है)। बस बदलें`"Your Document Directory"` उस वास्तविक पथ के साथ जहां आप अपनी फ़ाइलें सहेजना चाहते हैं.
## चरण 2: कार्यपुस्तिका को इंस्टैंसिएट करें
अब, आइए एक नई कार्यपुस्तिका बनाएं:
```csharp
Workbook workbook = new Workbook();
```
यह पंक्ति एक नई कार्यपुस्तिका ऑब्जेक्ट आरंभ करती है, जिससे आपको कार्य करने के लिए एक रिक्त कैनवास प्राप्त होता है।
## चरण 3: एक नई वर्कशीट जोड़ें
अब जबकि हमारी कार्यपुस्तिका तैयार हो गई है, तो आइए इसमें एक नई कार्यपत्रक जोड़ें:
```csharp
int sheetIndex = workbook.Worksheets.Add();
```
इससे एक नई वर्कशीट जुड़ जाएगी और उस शीट का इंडेक्स वापस आ जाएगा, जिसका उपयोग हम बाद में उसमें बदलाव करने के लिए कर सकते हैं।
## चरण 4: नई वर्कशीट तक पहुँचें
नई जोड़ी गई वर्कशीट में बदलाव करने के लिए, आपको इसे एक्सेस करना होगा:
```csharp
Worksheet worksheet = workbook.Worksheets[sheetIndex];
```
 अब,`worksheet` इससे हमें उस विशिष्ट शीट में सामग्री और चित्र जोड़ने की अनुमति मिलेगी।
## चरण 5: चित्र डालें
अब आता है रोमांचक हिस्सा! चलिए आपकी खूबसूरत छवि जोड़ते हैं।`"logo.jpg"` अपनी छवि फ़ाइल के नाम के साथ:
```csharp
int pictureIndex = worksheet.Pictures.Add(5, 5, dataDir + "logo.jpg");
```
 यह पंक्ति सेल F6 पर छवि जोड़ती है (चूंकि पंक्तियाँ और स्तंभ शून्य-अनुक्रमित हैं,`5` (छठे सेल को संदर्भित करता है)।
## चरण 6: जोड़े गए चित्र तक पहुंचें
एक बार छवि डालने के बाद, आप इसे इस प्रकार एक्सेस कर सकते हैं:
```csharp
Aspose.Cells.Drawing.Picture picture = worksheet.Pictures[pictureIndex];
```
यह आपको चित्र के गुणों में हेरफेर करने में सक्षम बनाता है।
## चरण 7: चित्र को आनुपातिक रूप से रखें
अब, चित्र को आनुपातिक रूप से रखें:
```csharp
picture.UpperDeltaX = 200;
picture.UpperDeltaY = 200;
```
 यहाँ,`UpperDeltaX` और`UpperDeltaY` सेल के आयामों के सापेक्ष छवि की स्थिति को समायोजित करें। आप अपनी छवि को बिल्कुल सही बनाने के लिए इन मानों को बदल सकते हैं।
## चरण 8: अपने परिवर्तन सहेजें
अंत में, सभी परिवर्तनों को सुरक्षित रखने के लिए अपनी कार्यपुस्तिका को सहेजें:
```csharp
workbook.Save(dataDir + "book1.out.xls");
```
 यह पंक्ति आपकी कार्यपुस्तिका को इस रूप में सहेजती है`book1.out.xls` निर्दिष्ट निर्देशिका में.
## निष्कर्ष
और अब यह हो गया! आपने अभी सीखा है कि .NET के लिए Aspose.Cells का उपयोग करके Excel में चित्रों को आनुपातिक रूप से कैसे रखा जाए। यह केवल छवियों को सम्मिलित करने के बारे में नहीं है; यह उन्हें आपकी स्प्रेडशीट में सही दिखने के बारे में है। बस याद रखें: एक अच्छी तरह से रखी गई तस्वीर आपके डेटा प्रस्तुति को काफी हद तक बढ़ा सकती है।
अलग-अलग इमेज और प्लेसमेंट के साथ प्रयोग करने का मज़ा लें, और Aspose.Cells द्वारा दी जाने वाली समृद्ध सुविधाओं का गहराई से आनंद लेने में संकोच न करें। आपकी एक्सेल शीट में अब एक बड़ा बदलाव होने वाला है!
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.Cells क्या है?
Aspose.Cells .NET के लिए एक शक्तिशाली लाइब्रेरी है जो उपयोगकर्ताओं को Microsoft Excel स्थापित किए बिना Excel फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने में सक्षम बनाती है।
### क्या मैं Aspose.Cells का निःशुल्क उपयोग कर सकता हूँ?
 हां, Aspose.Cells एक निःशुल्क परीक्षण प्रदान करता है, जिसे आप डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मैं दस्तावेज़ कहां पा सकता हूं?
 आप व्यापक पहुँच प्राप्त कर सकते हैं[प्रलेखन](https://reference.aspose.com/cells/net/) Aspose.Cells के लिए.
### क्या Aspose.Cells सभी छवि प्रारूपों का समर्थन करता है?
Aspose.Cells JPEG, PNG, BMP, GIF, और TIFF सहित विभिन्न प्रारूपों का समर्थन करता है।
### मैं Aspose.Cells के लिए समर्थन कैसे प्राप्त कर सकता हूं?
 किसी भी प्रश्न के लिए, कृपया यहां जाएं[सहयता मंच](https://forum.aspose.com/c/cells/9)जहां आप अपने प्रश्न पूछ सकते हैं.