---
title: एक्सेल में वर्कशीट में कॉम्बो बॉक्स जोड़ें
linktitle: एक्सेल में वर्कशीट में कॉम्बो बॉक्स जोड़ें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके प्रोग्रामेटिक रूप से Excel वर्कशीट में कॉम्बो बॉक्स जोड़ने का तरीका जानें। यह चरण-दर-चरण मार्गदर्शिका आपको प्रत्येक विवरण के माध्यम से मार्गदर्शन करती है।
type: docs
weight: 21
url: /hi/net/excel-shapes-controls/add-combo-box-to-worksheet-excel/
---
## परिचय
इंटरैक्टिव एक्सेल स्प्रेडशीट बनाने से उपयोगकर्ता अनुभव में बहुत सुधार हो सकता है, खासकर जब आप कॉम्बो बॉक्स जैसे फ़ॉर्म तत्व जोड़ते हैं। कॉम्बो बॉक्स उपयोगकर्ताओं को पूर्वनिर्धारित सूची से विकल्प चुनने की अनुमति देते हैं, जिससे डेटा इनपुट में आसानी और दक्षता बढ़ती है। .NET के लिए Aspose.Cells के साथ, आप सीधे Excel का उपयोग किए बिना Excel शीट में कॉम्बो बॉक्स बना सकते हैं। यह शक्तिशाली लाइब्रेरी डेवलपर्स को विभिन्न तरीकों से एक्सेल फ़ाइलों में हेरफेर करने की अनुमति देती है, जिसमें फ़ॉर्म नियंत्रणों को स्वचालित करने की क्षमता भी शामिल है।
इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells का उपयोग करके Excel में वर्कशीट में कॉम्बो बॉक्स जोड़ने की प्रक्रिया से परिचित कराएँगे। यदि आप गतिशील, उपयोगकर्ता-अनुकूल स्प्रेडशीट बनाना चाहते हैं, तो यह मार्गदर्शिका आपको आरंभ करने में मदद करेगी।
## आवश्यक शर्तें
इससे पहले कि हम कोड में उतरें, आइए सुनिश्चित करें कि आपके पास वह सब कुछ है जो आपको चाहिए:
- Aspose.Cells for .NET: Aspose.Cells for .NET लाइब्रेरी को डाउनलोड करें और इंस्टॉल करें[डाउनलोड पृष्ठ](https://releases.aspose.com/cells/net/).
- .NET फ्रेमवर्क: सुनिश्चित करें कि आपके मशीन पर .NET फ्रेमवर्क स्थापित है। Aspose.Cells द्वारा समर्थित कोई भी संस्करण काम करेगा।
- विकास वातावरण: अपने प्रोजेक्ट को प्रबंधित करने और कोड लिखने के लिए विजुअल स्टूडियो जैसे IDE का उपयोग करें।
-  लाइसेंस का प्रस्ताव: आप मूल्यांकन मोड में बिना लाइसेंस के काम कर सकते हैं, लेकिन पूर्ण संस्करण के लिए, आपको लाइसेंस लागू करना होगा।[अस्थायी लाइसेंस](https://purchase.aspose.com/temporary-license/) यदि ज़रूरत हो तो।
## पैकेज आयात करें
आरंभ करने के लिए, आपको अपने प्रोजेक्ट में आवश्यक नेमस्पेस आयात करने की आवश्यकता है। यहाँ आपको क्या चाहिए:
```csharp
using System.IO;
using Aspose.Cells;
```
ये एक्सेल फाइलों के साथ इंटरैक्ट करने और कार्यपुस्तिका में कॉम्बो बॉक्स जैसे फॉर्म तत्वों में हेरफेर करने के लिए आवश्यक हैं।
आइए आसानी से समझने के लिए कॉम्बो बॉक्स जोड़ने की प्रक्रिया को कई सरल चरणों में विभाजित करें।
## चरण 1: दस्तावेज़ निर्देशिका सेट करें
पहला कदम एक डायरेक्टरी बनाना है जहाँ आपकी एक्सेल फ़ाइलें सहेजी जाएँगी। यदि यह पहले से मौजूद नहीं है तो आप एक नया फ़ोल्डर बना सकते हैं।
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
//यदि निर्देशिका पहले से मौजूद नहीं है तो उसे बनाएं।
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
- dataDir: वह स्थान निर्दिष्ट करता है जहाँ आउटपुट फ़ाइल सहेजी जाएगी।
- System.IO.Directory.Exists: जाँचता है कि क्या निर्देशिका पहले से मौजूद है।
- System.IO.Directory.CreateDirectory: यदि निर्देशिका अनुपलब्ध है तो उसे बनाता है।
## चरण 2: नई कार्यपुस्तिका बनाएँ
अब, एक नई एक्सेल वर्कबुक बनाएं जहां आप कॉम्बो बॉक्स जोड़ेंगे।

```csharp
// एक नई कार्यपुस्तिका बनाएँ.
Workbook workbook = new Workbook();
```

- कार्यपुस्तिका कार्यपुस्तिका: कार्यपुस्तिका वर्ग का एक नया उदाहरण आरंभ करता है, जो एक Excel फ़ाइल का प्रतिनिधित्व करता है।
## चरण 3: वर्कशीट और सेल प्राप्त करें
इसके बाद, कार्यपुस्तिका से पहली वर्कशीट तक पहुंचें और उन कक्षों के संग्रह को पुनः प्राप्त करें जहां आप डेटा इनपुट करेंगे।

```csharp
// पहली वर्कशीट प्राप्त करें.
Worksheet sheet = workbook.Worksheets[0];
// वर्कशीट सेल संग्रह प्राप्त करें.
Cells cells = sheet.Cells;
```

- वर्कशीट शीट: वर्कबुक से पहली वर्कशीट लाता है।
- कक्ष कक्ष: कार्यपत्रक से कक्षों का संग्रह प्राप्त करता है।
## चरण 4: कॉम्बो बॉक्स के लिए इनपुट मान
अब, हमें सेल में कुछ मान इनपुट करने की आवश्यकता है। ये मान कॉम्बो बॉक्स के लिए विकल्प के रूप में काम करेंगे।

```csharp
// एक मान इनपुट करें.
cells["B3"].PutValue("Employee:");
// इसे बोल्ड करें.
cells["B3"].GetStyle().Font.IsBold = true;
// कुछ मान इनपुट करें जो कॉम्बो बॉक्स के लिए इनपुट रेंज को दर्शाते हैं।
cells["A2"].PutValue("Emp001");
cells["A3"].PutValue("Emp002");
cells["A4"].PutValue("Emp003");
cells["A5"].PutValue("Emp004");
cells["A6"].PutValue("Emp005");
cells["A7"].PutValue("Emp006");
```

- कोशिकाओं["B3"].PutValue: लेबल "कर्मचारी" को सेल B3 में रखता है.
- Font.IsBold = true: पाठ को स्पष्ट दिखाने के लिए उसे बोल्ड पर सेट करता है।
- इनपुट रेंज: सेल A2 से A7 में कई कर्मचारी आईडी इनपुट करता है। ये कॉम्बो बॉक्स ड्रॉपडाउन में दिखाई देंगे।
## चरण 5: वर्कशीट में कॉम्बो बॉक्स जोड़ें
अगला कदम आपके वर्कशीट में कॉम्बो बॉक्स नियंत्रण जोड़ना है। यह कॉम्बो बॉक्स उपयोगकर्ताओं को आपके द्वारा पहले दर्ज की गई कर्मचारी आईडी में से एक चुनने देगा।

```csharp
// एक नया कॉम्बो बॉक्स जोड़ें.
Aspose.Cells.Drawing.ComboBox comboBox = sheet.Shapes.AddComboBox(2, 0, 2, 0, 22, 100);
```

- AddComboBox: वर्कशीट में एक नया कॉम्बो बॉक्स जोड़ता है। संख्याएँ (2, 0, 2, 0, 22, 100) कॉम्बो बॉक्स की स्थिति और आयाम दर्शाती हैं।
## चरण 6: कॉम्बो बॉक्स को सेल से लिंक करें और इनपुट रेंज सेट करें
कॉम्बो बॉक्स को कार्यात्मक बनाने के लिए, हमें इसे एक विशिष्ट सेल से लिंक करना होगा तथा उन सेल की श्रेणी निर्धारित करनी होगी, जहां से यह अपने विकल्प खींचेगा।

```csharp
// लिंक किए गए सेल को सेट करें.
comboBox.LinkedCell = "A1";
// इनपुट रेंज सेट करें.
comboBox.InputRange = "A2:A7";
```

- लिंक्डसेल: कॉम्बो बॉक्स के चयन को सेल A1 से लिंक करता है। कॉम्बो बॉक्स से चयनित मान इस सेल में दिखाई देगा।
- इनपुटरेंज: सेल रेंज (A2:A7) को परिभाषित करता है जिसमें वे मान होते हैं जो कॉम्बो बॉक्स विकल्पों को भरेंगे।
## चरण 7: कॉम्बो बॉक्स का स्वरूप अनुकूलित करें
आप ड्रॉपडाउन लाइनों की संख्या निर्दिष्ट करके और बेहतर सौंदर्य के लिए 3D शेडिंग को सक्षम करके कॉम्बो बॉक्स को और अधिक अनुकूलित कर सकते हैं।

```csharp
// कॉम्बो बॉक्स के सूची भाग में प्रदर्शित सूची पंक्तियों की संख्या निर्धारित करें।
comboBox.DropDownLines = 5;
// कॉम्बो बॉक्स को 3-डी शेडिंग के साथ सेट करें।
comboBox.Shadow = true;
```

- ड्रॉपडाउनलाइन्स: यह नियंत्रित करता है कि कॉम्बो बॉक्स ड्रॉपडाउन में एक बार में कितने विकल्प दिखाई देंगे।
- छाया: कॉम्बो बॉक्स में 3D छायांकन प्रभाव जोड़ता है।
## चरण 8: कॉलम को ऑटोफिट करें और कार्यपुस्तिका को सहेजें
अंत में, आइए एक साफ लेआउट के लिए कॉलमों को स्वचालित रूप से फिट करें और कार्यपुस्तिका को सेव करें।

```csharp
// ऑटोफिट कॉलम
sheet.AutoFitColumns();
// फ़ाइल को सहेजता है.
workbook.Save(dataDir + "book1.out.xls");
```

- AutoFitColumns: सामग्री को फिट करने के लिए कॉलम की चौड़ाई को स्वचालित रूप से समायोजित करता है।
- सहेजें: कार्यपुस्तिका को निर्दिष्ट निर्देशिका में Excel फ़ाइल के रूप में सहेजता है।

## निष्कर्ष
.NET के लिए Aspose.Cells का उपयोग करके अपने Excel वर्कशीट में कॉम्बो बॉक्स जोड़ना एक सीधी प्रक्रिया है जो डेटा इनपुट लचीलेपन में बहुत सुधार करती है। प्रोग्रामेटिक रूप से फ़ॉर्म नियंत्रण बनाकर, आप आसानी से इंटरैक्टिव स्प्रेडशीट बना सकते हैं। इस ट्यूटोरियल ने आपको Aspose.Cells का उपयोग करके कॉम्बो बॉक्स जोड़ने, उसे सेल से लिंक करने और उसकी इनपुट रेंज कॉन्फ़िगर करने का तरीका दिखाया।
 Aspose.Cells एक्सेल फ़ाइल हेरफेर के लिए सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है, जो इसे स्प्रेडशीट कार्यों को स्वचालित करने की तलाश करने वाले डेवलपर्स के लिए एक आदर्श विकल्प बनाता है। इसे आज़माएँ[मुफ्त परीक्षण](https://releases.aspose.com/).
## अक्सर पूछे जाने वाले प्रश्न
### क्या मैं Excel इंस्टॉल किए बिना Aspose.Cells का उपयोग कर सकता हूँ?
हां, Aspose.Cells Excel से स्वतंत्र रूप से काम करता है और इसके लिए Excel को इंस्टॉल करने की आवश्यकता नहीं होती है।
### मैं Aspose.Cells में लाइसेंस कैसे लागू करूँ?
 आप लाइसेंस प्राप्त करके आवेदन कर सकते हैं[यहाँ](https://purchase.aspose.com/buy) और कॉलिंग`License.SetLicense()` अपने कोड में.
### Aspose.Cells फ़ाइलों को सहेजने के लिए किन प्रारूपों का समर्थन करता है?
Aspose.Cells XLSX, XLS, CSV, PDF, आदि जैसे कई प्रारूपों में फ़ाइलों को सहेजने का समर्थन करता है।
### क्या कॉम्बो बॉक्स की संख्या की कोई सीमा है जिसे मैं जोड़ सकता हूँ?
नहीं, इसमें कोई सख्त सीमा नहीं है; आप अपनी परियोजना की आवश्यकतानुसार उतने कॉम्बो बॉक्स जोड़ सकते हैं।
### मैं Aspose.Cells के लिए समर्थन कैसे प्राप्त करूं?
 आप यहाँ से सहायता प्राप्त कर सकते हैं[एस्पोज फोरम](https://forum.aspose.com/c/cells/9).