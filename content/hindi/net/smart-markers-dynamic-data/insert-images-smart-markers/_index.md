---
title: Aspose.Cells में इमेज मार्कर के साथ इमेज डालें
linktitle: Aspose.Cells में इमेज मार्कर के साथ इमेज डालें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: हमारे चरण-दर-चरण गाइड के साथ .NET के लिए Aspose.Cells में छवि मार्करों का उपयोग करके छवियों को सम्मिलित करने का तरीका जानें! अपने एक्सेल रिपोर्ट को प्रभावी ढंग से विज़ुअल के साथ बढ़ाएँ।
type: docs
weight: 16
url: /hi/net/smart-markers-dynamic-data/insert-images-smart-markers/
---
## परिचय
क्या आप अपनी एक्सेल स्प्रेडशीट को कुछ छवियों के साथ और भी बेहतर बनाना चाहते हैं? शायद आप एक ऐसी गतिशील रिपोर्ट बनाना चाहते हैं जिसमें सीधे आपके डेटा स्रोत से छवियां शामिल हों? अगर ऐसा है, तो आप सही जगह पर हैं! इस गाइड में, हम .NET के लिए Aspose.Cells लाइब्रेरी में इमेज मार्कर का उपयोग करके इमेज डालने की प्रक्रिया के बारे में बताएँगे। यह ट्यूटोरियल .NET डेवलपर्स के लिए एकदम सही है जो अपनी एक्सेल रिपोर्ट को बेहतर बनाना चाहते हैं और समग्र उपयोगकर्ता जुड़ाव में सुधार करना चाहते हैं।
## आवश्यक शर्तें
कोडिंग की बारीकियों में उतरने से पहले, यह सुनिश्चित करना आवश्यक है कि आपने कुछ चीजें सेट कर ली हैं:
1. .NET वातावरण: एक कार्यशील .NET विकास वातावरण रखें। आप Visual Studio या अपनी पसंद का कोई अन्य .NET IDE उपयोग कर सकते हैं।
2.  Aspose.Cells for .NET लाइब्रेरी: आपको Aspose.Cells लाइब्रेरी डाउनलोड करनी होगी और उस तक पहुँच प्राप्त करनी होगी। आप नवीनतम संस्करण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/cells/net/).
3. आवश्यक छवियाँ: सुनिश्चित करें कि आपके द्वारा उपयोग की जाने वाली छवियाँ आपकी परियोजना निर्देशिका में संग्रहीत हैं।
4. C# की बुनियादी समझ: C# की बुनियादी समझ और डेटाटेबल्स के साथ काम करने से आपको आसानी से काम करने में मदद मिलेगी।
अब जब हमने मंच तैयार कर लिया है, तो आइए आवश्यक पैकेजों को आयात करके शुरुआत करें!
## पैकेज आयात करें
किसी भी फ़ंक्शन को निष्पादित करने से पहले, हमें आवश्यक नेमस्पेस को आयात करने की आवश्यकता होती है। अपनी C# फ़ाइल में, सुनिश्चित करें कि आपने निम्नलिखित को शामिल किया है:
```csharp
using System.IO;
using Aspose.Cells;
using System.Data;
```
ये नामस्थान आपको एक्सेल फाइलों में हेरफेर करने और डेटा तालिकाओं को संभालने के लिए कक्षाएं और कार्यात्मकताएं प्रदान करेंगे।
अब, आइए Aspose.Cells का उपयोग करके इमेज डालने की प्रक्रिया को सरल चरणों में विभाजित करें। हम आपकी डेटा तालिका सेट अप करने, इमेज लोड करने और अंतिम Excel फ़ाइल को सहेजने के लिए आवश्यक चरणों पर काम करेंगे।
## चरण 1: अपनी दस्तावेज़ निर्देशिका निर्दिष्ट करें
सबसे पहले, आपको वह डॉक्यूमेंट डायरेक्टरी निर्दिष्ट करनी होगी जहाँ आपकी छवियाँ और टेम्पलेट फ़ाइल स्थित हैं। यह डायरेक्टरी आपके सभी फ़ाइल संचालन के लिए आधार पथ के रूप में काम करेगी।
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory"; // इसे अपनी वास्तविक निर्देशिका में बदलें
```
 प्रतिस्थापित करें`"Your Document Directory"` आपके इमेज और टेम्पलेट फ़ाइल को स्टोर करने के लिए पथ के साथ। यह एक सापेक्ष या निरपेक्ष पथ हो सकता है।
## चरण 2: अपनी छवियों को बाइट एरे में लोड करें
इसके बाद, हम उन छवियों को पढ़ेंगे जिन्हें आप एक्सेल फ़ाइल में सम्मिलित करना चाहते हैं। आपको एक डेटाटेबल बनाना होगा जिसमें छवि डेटा हो।
```csharp
// छवि डेटा प्राप्त करें.
byte[] imageData = File.ReadAllBytes(dataDir + "aspose-logo.jpg");
```
`File.ReadAllBytes()` विधि का उपयोग इमेज फ़ाइल को बाइट ऐरे में पढ़ने के लिए किया जाता है। आप प्रत्येक फ़ाइल के लिए प्रक्रिया को दोहराकर कई छवियों के लिए ऐसा कर सकते हैं।
## चरण 3: छवियाँ रखने के लिए डेटाटेबल बनाएँ
अब हम एक DataTable बनाएंगे। यह टेबल हमें अपने इमेज डेटा को संरचित तरीके से संग्रहीत करने की अनुमति देगा।
```csharp
// एक डेटाटेबल बनाएं.
DataTable t = new DataTable("Table1");
// चित्रों को सहेजने के लिए एक कॉलम जोड़ें.
DataColumn dc = t.Columns.Add("Picture");
// इसका डेटा प्रकार सेट करें.
dc.DataType = typeof(object);
```
 यहाँ, हम "Table1" नामक एक नया DataTable बनाते हैं और "Picture" नामक एक कॉलम जोड़ते हैं। इस कॉलम के लिए डेटा प्रकार सेट किया गया है`object`, जो बाइट एरे को संग्रहीत करने के लिए आवश्यक है।
## चरण 4: डेटाटेबल में छवि रिकॉर्ड जोड़ें
एक बार डेटाटेबल सेट हो जाने के बाद, हम इसमें छवियाँ जोड़ना शुरू कर सकते हैं।
```csharp
// इसमें एक नया रिकार्ड जोड़ें.
DataRow row = t.NewRow();
row[0] = imageData;
t.Rows.Add(row);
// इसमें एक और रिकार्ड (चित्र सहित) जोड़ें।
imageData = File.ReadAllBytes(dataDir + "image2.jpg");
row = t.NewRow();
row[0] = imageData;
t.Rows.Add(row);
```
 प्रत्येक छवि के लिए एक नई पंक्ति बनाएं और पहले कॉलम का मान छवि डेटा पर सेट करें।`t.Rows.Add(row)` पंक्ति को DataTable में जोड़ने के लिए। इस तरह आप गतिशील रूप से छवियों का संग्रह बनाते हैं।
## चरण 5: वर्कबुकडिज़ाइनर ऑब्जेक्ट बनाएँ
 अब समय है एक नया ब्लॉग बनाने का`WorkbookDesigner` ऑब्जेक्ट, जिसका उपयोग एक्सेल टेम्पलेट को संसाधित करने के लिए किया जाएगा।
```csharp
// वर्कबुकडिजाइनर ऑब्जेक्ट बनाएं.
WorkbookDesigner designer = new WorkbookDesigner();
```
`WorkbookDesigner`क्लास आपको टेम्पलेट्स का उपयोग करके जटिल रिपोर्ट डिज़ाइन करने में मदद करके आपकी एक्सेल फ़ाइलों के साथ अधिक लचीले ढंग से काम करने की अनुमति देता है।
## चरण 6: अपनी टेम्पलेट एक्सेल फ़ाइल खोलें
 आपको अपनी एक्सेल टेम्पलेट फ़ाइल को इसमें लोड करना होगा`WorkbookDesigner`यह आधार के रूप में कार्य करता है जहां आपके छवि मार्करों को संसाधित किया जाएगा।
```csharp
// टेम्पलेट एक्सेल फ़ाइल खोलें.
designer.Workbook = new Workbook(dataDir + "TestSmartMarkers.xlsx");
```
 प्रतिस्थापित करें`"TestSmartMarkers.xlsx"` अपने वास्तविक टेम्पलेट के नाम के साथ। इस फ़ाइल में स्मार्ट मार्कर के रूप में जाने जाने वाले प्लेसहोल्डर होने चाहिए, जो Aspose.Cells को बताते हैं कि छवि डेटा को कहाँ रखना है।
## चरण 7: अपने वर्कबुकडिज़ाइनर के लिए डेटा स्रोत सेट करें
कार्यपुस्तिका खोलने के बाद, अगला चरण आपके DataTable को WorkbookDesigner से जोड़ना है।
```csharp
// डेटा स्रोत सेट करें.
designer.SetDataSource(t);
```
यह लाइन डिज़ाइनर को आपके द्वारा बनाए गए DataTable को डेटा स्रोत के रूप में उपयोग करने के लिए कहती है। यह आपके इमेज डेटा और टेम्पलेट के बीच एक लिंक स्थापित करता है।
## चरण 8: अपने टेम्पलेट में मार्करों को प्रोसेस करें
अब जादू होने का समय आ गया है! हम टेम्पलेट में मार्करों को प्रोसेस करेंगे, जो प्लेसहोल्डर्स को वास्तविक इमेज डेटा से बदल देगा।
```csharp
// मार्करों की प्रक्रिया करें.
designer.Process();
```
`Process()` विधि स्मार्ट मार्करों के लिए टेम्पलेट को स्कैन करती है और डेटाटेबल से डेटा का उपयोग करके उन्हें भरती है।
## चरण 9: अंतिम एक्सेल फ़ाइल सहेजें
आखिरी चरण, निश्चित रूप से, नई बनाई गई एक्सेल फ़ाइल को छवियों के साथ सहेजना है। चलिए अब यह करते हैं!
```csharp
// एक्सेल फ़ाइल को सहेजें.
designer.Workbook.Save(dataDir + "output.xls");
```
आप सहेजी गई फ़ाइल के लिए अपना पसंदीदा प्रारूप चुन सकते हैं। इस मामले में, हम इसे "output.xls" के रूप में सहेज रहे हैं। अपनी आवश्यकताओं के अनुसार फ़ाइल नाम को संशोधित करें।
## निष्कर्ष
और अब आपके पास यह है! इमेज मार्कर की मदद से Aspose.Cells का उपयोग करके एक्सेल स्प्रेडशीट में इमेज डालने के लिए एक सुव्यवस्थित गाइड। यह सुविधा आपके डेटा स्रोत के आधार पर इमेज शामिल करने वाली डायनामिक रिपोर्ट बनाने के लिए अविश्वसनीय रूप से उपयोगी है। चाहे आप व्यवसाय विश्लेषण या शैक्षिक सामग्री पर काम कर रहे हों, ये विधियाँ आपके दस्तावेज़ प्रस्तुति को महत्वपूर्ण रूप से बढ़ा सकती हैं।
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.Cells क्या है?
Aspose.Cells .NET के लिए एक शक्तिशाली लाइब्रेरी है जो उपयोगकर्ताओं को प्रोग्रामेटिक रूप से Excel फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने की अनुमति देती है।
### क्या मैं Aspose.Cells का निःशुल्क उपयोग कर सकता हूँ?
हाँ! आप Aspose.Cells का निःशुल्क परीक्षण संस्करण प्राप्त कर सकते हैं[यहाँ](https://releases.aspose.com/).
### मैं Aspose.Cells का उपयोग करने के बारे में अधिक जानकारी कहां से प्राप्त कर सकता हूं?
 आप इसमें गोता लगा सकते हैं[Aspose.Cells दस्तावेज़ीकरण](https://reference.aspose.com/cells/net/) विस्तृत मार्गदर्शिका और संसाधनों के लिए.
### क्या मुझे अपने एप्लिकेशन के साथ Aspose.Cells को तैनात करने के लिए लाइसेंस की आवश्यकता है?
 हां, उत्पादन उपयोग के लिए आपको लाइसेंस की आवश्यकता होगी। आप एक अस्थायी लाइसेंस प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/temporary-license/).
### मैं Aspose.Cells के लिए तकनीकी सहायता कैसे प्राप्त करूं?
 तकनीकी प्रश्नों के लिए आप यहां जा सकते हैं[Aspose समर्थन मंच](https://forum.aspose.com/c/cells/9).