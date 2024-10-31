---
title: एक्सेल में टेक्स्ट पर स्ट्राइक आउट प्रभाव बनाना
linktitle: एक्सेल में टेक्स्ट पर स्ट्राइक आउट प्रभाव बनाना
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: इस विस्तृत चरण-दर-चरण ट्यूटोरियल में जानें कि Aspose.Cells for .NET के साथ Excel में टेक्स्ट पर स्ट्राइकआउट प्रभाव कैसे लागू करें।
type: docs
weight: 15
url: /hi/net/working-with-fonts-in-excel/creating-strike-out-effect/
---
## परिचय
जब एक्सेल की बात आती है, तो विज़ुअल तत्व डेटा जितना ही महत्वपूर्ण होते हैं। चाहे आप महत्वपूर्ण परिवर्तनों को हाइलाइट कर रहे हों या उन आइटम को चिह्नित कर रहे हों जो अब प्रासंगिक नहीं हैं, टेक्स्ट पर स्ट्राइकआउट प्रभाव स्प्रेडशीट में विज़ुअल प्रतिनिधित्व को प्रबंधित करने का एक क्लासिक तरीका है। इस गाइड में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके Excel में टेक्स्ट पर स्ट्राइकआउट प्रभाव लागू करने की प्रक्रिया के बारे में बताएँगे। यह ट्यूटोरियल न केवल आवश्यक पूर्वापेक्षाओं को कवर करेगा, बल्कि यह सुनिश्चित करने के लिए चरण-दर-चरण दृष्टिकोण भी प्रदान करेगा कि आप इस प्रभाव को आसानी से दोहरा सकते हैं।
## आवश्यक शर्तें
ट्यूटोरियल में शामिल होने से पहले, सुनिश्चित करें कि आपके पास निम्नलिखित पूर्वापेक्षाएँ पूरी हैं:
1. विकास पर्यावरण: आपके पास .NET विकास पर्यावरण होना चाहिए। यह Visual Studio या कोई अन्य IDE हो सकता है जिसे आप पसंद करते हैं जो .NET विकास का समर्थन करता है।
2. .NET के लिए Aspose.Cells: सुनिश्चित करें कि आपके प्रोजेक्ट में Aspose.Cells इंस्टॉल है। आप इसे निम्न लिंक से डाउनलोड कर सकते हैं:[Aspose.Cells डाउनलोड करें](https://releases.aspose.com/cells/net/).
3. C# का मूलभूत ज्ञान: C# प्रोग्रामिंग की मूलभूत समझ उपयोगी होगी क्योंकि उदाहरणों को C# में कोडित किया जाएगा।
4. .NET फ्रेमवर्क: सुनिश्चित करें कि आपका प्रोजेक्ट संगत .NET फ्रेमवर्क संस्करण, आमतौर पर .NET Core या .NET फ्रेमवर्क 4.5 और इसके बाद के संस्करण को लक्षित कर रहा है।
## पैकेज आयात करें
कोई भी कोड लिखने से पहले, आपको Aspose.Cells से आवश्यक नेमस्पेस आयात करने की आवश्यकता है। लाइब्रेरी द्वारा प्रदान की गई विभिन्न सुविधाओं तक पहुँचने के लिए यह महत्वपूर्ण है। यहाँ बताया गया है कि आप आवश्यक नेमस्पेस कैसे आयात कर सकते हैं:
```csharp
using System.IO;
using Aspose.Cells;
```
इन आयातों के साथ, आपके पास वर्कबुक, वर्कशीट और स्टाइल क्लासों तक पहुंच होगी, जिनका उपयोग इस पूरे ट्यूटोरियल में किया जाएगा।
अब जब हमने स्टेज सेट कर लिया है, तो चलिए इस प्रक्रिया को प्रबंधनीय चरणों में विभाजित करते हैं। प्रत्येक चरण के साथ आपको एक्सेल में टेक्स्ट पर स्ट्राइकआउट प्रभाव बनाने के लिए मार्गदर्शन करने के लिए स्पष्ट निर्देश दिए जाएंगे।
## चरण 1: दस्तावेज़ निर्देशिका निर्धारित करें
सबसे पहले उस पथ को परिभाषित करें जहाँ आपके एक्सेल दस्तावेज़ संग्रहीत किए जाएँगे। यह आपकी आउटपुट फ़ाइलों को सहेजने का स्थान होगा।
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
```
 प्रतिस्थापित करें`"Your Document Directory"` वास्तविक निर्देशिका पथ के साथ जहाँ आप अपनी एक्सेल फ़ाइल को सहेजना चाहते हैं। यह आपके आउटपुट के लिए निर्देशिका सेट करता है।
## चरण 2: निर्देशिका बनाएँ
इसके बाद, आपको यह सुनिश्चित करना होगा कि पिछले चरण में आपके द्वारा निर्दिष्ट निर्देशिका मौजूद है। यदि यह मौजूद नहीं है, तो आप इसे प्रोग्रामेटिक रूप से बना सकते हैं।
```csharp
// यदि निर्देशिका पहले से मौजूद नहीं है तो उसे बनाएं।
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
यह कोड जाँचता है कि निर्देशिका मौजूद है या नहीं और अगर नहीं है तो उसे बनाता है। यह बाद में जब आप अपनी फ़ाइल को सहेजने का प्रयास करते हैं तो त्रुटियों से बचने में मदद करता है।
## चरण 3: वर्कबुक ऑब्जेक्ट को इंस्टैंसिएट करें
अब, एक नया वर्कबुक ऑब्जेक्ट बनाने का समय आ गया है। यह आपकी एक्सेल फ़ाइल का आधार है जहाँ आप डेटा जोड़ेंगे और फ़ॉर्मेट लागू करेंगे।
```csharp
// वर्कबुक ऑब्जेक्ट को इंस्टैंशिएट करना
Workbook workbook = new Workbook();
```
`Workbook` क्लास एक एक्सेल फ़ाइल का प्रतिनिधित्व करता है। इस क्लास का एक उदाहरण बनाकर, आप अनिवार्य रूप से एक नया एक्सेल दस्तावेज़ बना रहे हैं।
## चरण 4: एक नई वर्कशीट जोड़ें
प्रत्येक कार्यपुस्तिका में कई कार्यपत्रक हो सकते हैं। चलिए आगे बढ़ते हैं और अपनी कार्यपुस्तिका में एक नई कार्यपत्रक बनाते हैं।
```csharp
// Excel ऑब्जेक्ट में नई वर्कशीट जोड़ना
int i = workbook.Worksheets.Add();
```
`Add` की विधि`Worksheets` संग्रह कार्यपुस्तिका में एक नई कार्यपत्रक जोड़ता है और उसकी अनुक्रमणिका लौटाता है। 
## चरण 5: नई वर्कशीट का संदर्भ प्राप्त करें
एक बार जब आप वर्कशीट बना लेते हैं, तो आपको भविष्य के कार्यों के लिए इसका संदर्भ लेना होगा।
```csharp
// नई जोड़ी गई वर्कशीट का संदर्भ उसकी शीट इंडेक्स पास करके प्राप्त करना
Worksheet worksheet = workbook.Worksheets[i];
```
यहां, आप इसके इंडेक्स का उपयोग करके नई बनाई गई वर्कशीट प्राप्त कर रहे हैं (`i`) इससे आपको वर्कशीट में बदलाव करने की सुविधा मिलती है।
## चरण 6: किसी सेल तक पहुँचें
 आप अपनी वर्कशीट में एक खास सेल तक पहुंचना चाहेंगे जहां आप स्ट्राइकआउट फ़ॉर्मेट लागू करेंगे। इस उदाहरण में, हम सेल का उपयोग कर रहे हैं`A1`.
```csharp
// वर्कशीट से "A1" सेल तक पहुंचना
Aspose.Cells.Cell cell = worksheet.Cells["A1"];
```
 एक्सेल में, सेल को उनके कॉलम और रो आइडेंटिफ़ायर (जैसे, "A1") द्वारा संदर्भित किया जाता है। हम सेल का संदर्भ प्राप्त कर रहे हैं`A1` आगे हेरफेर के लिए.
## चरण 7: सेल में मान जोड़ें
 अब, सेल में कुछ टेक्स्ट डालें। हम सेल में “Hello Aspose!” लिखेंगे`A1`.
```csharp
// "A1" सेल में कुछ मान जोड़ना
cell.PutValue("Hello Aspose!");
```
`PutValue` विधि का उपयोग सेल को स्ट्रिंग मान निर्दिष्ट करने के लिए किया जाता है। आप इस स्ट्रिंग को अपनी इच्छानुसार प्रदर्शित करने के लिए संशोधित कर सकते हैं।
## चरण 8: सेल की शैली प्राप्त करें
अब जबकि हमारे सेल में टेक्स्ट है, तो अब समय है कि हम सेल की शैली तक पहुंच कर, स्ट्राइकआउट प्रभाव सहित, अपनी इच्छित फॉर्मेटिंग लागू करें।
```csharp
// सेल की शैली प्राप्त करना
Style style = cell.GetStyle();
```
`GetStyle` विधि सेल की वर्तमान शैली को पुनः प्राप्त करती है, जिससे आप फ़ॉन्ट प्रकार, आकार और प्रभाव जैसे गुणों को संशोधित कर सकते हैं।
## चरण 9: स्ट्राइकआउट प्रभाव सेट करें
आइए सेल में मौजूद टेक्स्ट पर स्ट्राइकआउट इफ़ेक्ट लागू करें। हम सेल की फ़ॉन्ट शैली को संशोधित करेंगे।
```csharp
// एक्सस्टार्ट: सेटस्ट्राइकआउट
// फ़ॉन्ट पर स्ट्राइक आउट प्रभाव सेट करना
style.Font.IsStrikeout = true;
// ExEnd:सेटस्ट्राइकआउट
```
 सेटिंग करके`IsStrikeout` यदि आप इसे true पर सेट करते हैं, तो आप Excel को चयनित सेल स्ट्राइकथ्रू में टेक्स्ट को दृष्टिगत रूप से काटने का निर्देश दे रहे हैं - ठीक वैसे ही जैसे किसी सूची से किसी चीज को दृष्टिगत रूप से चिह्नित करना।
## चरण 10: सेल पर स्टाइल लागू करें
शैली को संशोधित करने के बाद, आपको परिवर्तनों को प्रतिबिंबित करने के लिए इसे वापस सेल पर लागू करना होगा।
```csharp
// सेल पर शैली लागू करना
cell.SetStyle(style);
```
`SetStyle` विधि सेल को नई शैली के साथ अद्यतन करती है, जिसमें अब स्ट्राइकआउट स्वरूपण भी शामिल है।
## चरण 11: एक्सेल फ़ाइल को सेव करें
 अंत में, अब समय आ गया है कि आप अपनी कार्यपुस्तिका को निर्दिष्ट निर्देशिका में सहेज लें। इस उदाहरण में, हम फ़ाइल को इस नाम से सहेज रहे हैं`book1.out.xls`.
```csharp
// एक्सेल फ़ाइल को सहेजना
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
`Save`विधि 97-2003 एक्सेल प्रारूप में कार्यपुस्तिका को डिस्क पर लिखती है। यदि आवश्यक हो तो आप अलग-अलग प्रारूप निर्दिष्ट कर सकते हैं।
## निष्कर्ष
.NET के लिए Aspose.Cells का उपयोग करके Excel में टेक्स्ट पर स्ट्राइकआउट प्रभाव बनाना एक सीधी प्रक्रिया है जब आप इसे चरण दर चरण तोड़ते हैं। इस गाइड का पालन करके, अब आपके पास विज़ुअल संकेतों के साथ अपनी स्प्रेडशीट को बढ़ाने का कौशल है, जिससे आपका डेटा न केवल जानकारीपूर्ण बल्कि विज़ुअल रूप से आकर्षक भी बन जाता है।
## अक्सर पूछे जाने वाले प्रश्न
### Aspose.Cells क्या है?
Aspose.Cells .NET अनुप्रयोगों में Excel फ़ाइलों के प्रबंधन के लिए एक शक्तिशाली लाइब्रेरी है, जो आपको प्रोग्रामेटिक रूप से Excel दस्तावेज़ बनाने, हेरफेर करने और परिवर्तित करने में सक्षम बनाती है।
### क्या मैं Aspose.Cells का निःशुल्क उपयोग कर सकता हूँ?
 हां, आप इसे परीक्षण अवधि के दौरान मुफ़्त में इस्तेमाल कर सकते हैं। निःशुल्क परीक्षण यहाँ उपलब्ध है[Aspose.Cells निःशुल्क परीक्षण](https://releases.aspose.com/).
### मैं Aspose.Cells कैसे खरीदूं?
 आप Aspose.Cells के लिए उनकी वेबसाइट के माध्यम से लाइसेंस खरीद सकते हैं[Aspose.Cells खरीदें](https://purchase.aspose.com/buy).
### क्या Aspose.Cells का उपयोग करने के लिए उदाहरण उपलब्ध हैं?
 हां, आप यहां बहुत सारे उदाहरण और कोड स्निपेट पा सकते हैं।[Aspose.Cells दस्तावेज़ीकरण](https://reference.aspose.com/cells/net/).
### मुझे Aspose.Cells के लिए समर्थन कहां मिल सकता है?
 आप समुदाय से समर्थन और सहायता प्राप्त कर सकते हैं[एस्पोज फोरम](https://forum.aspose.com/c/cells/9).