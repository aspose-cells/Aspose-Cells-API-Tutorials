---
title: एक्सेल में प्रोग्रामेटिक रूप से कॉपी विधि का उपयोग करना
linktitle: एक्सेल में प्रोग्रामेटिक रूप से कॉपी विधि का उपयोग करना
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: एक्सेल फ़ाइलों को कुशलतापूर्वक संचालित करने के लिए Aspose.Cells for .NET में कॉपी विधि का उपयोग करना सीखें। चरण-दर-चरण मार्गदर्शिका शामिल है।
type: docs
weight: 10
url: /hi/net/excel-formatting-methods-and-options/using-copy-method/
---
## परिचय
जब स्प्रेडशीट को प्रोग्रामेटिक रूप से प्रबंधित करने और उसमें हेरफेर करने की बात आती है, तो .NET के लिए Aspose.Cells एक पावरहाउस है जो आपका समय बचा सकता है और आपके वर्कफ़्लो को सुव्यवस्थित कर सकता है। डेवलपर्स के सामने आने वाले आम कार्यों में से एक एक्सेल वर्कबुक के भीतर एक वर्कशीट से दूसरी वर्कशीट में रेंज कॉपी करने की आवश्यकता है। इस ट्यूटोरियल में, हम आपको Aspose.Cells में कॉपी विधि का उपयोग करने के बारे में बताएँगे, आपको स्पष्ट स्पष्टीकरण और कोड उदाहरणों के साथ प्रत्येक चरण के माध्यम से मार्गदर्शन करेंगे।
## आवश्यक शर्तें
इससे पहले कि हम कॉपी विधि का उपयोग करने के चरणों में उतरें, आपको यह सुनिश्चित करना होगा कि आपके पास निम्नलिखित पूर्वापेक्षाएँ मौजूद हैं:
1. .NET फ्रेमवर्क: सुनिश्चित करें कि आपके पास अपनी मशीन पर .NET फ्रेमवर्क स्थापित है। Aspose.Cells विभिन्न संस्करणों के साथ संगत है, इसलिए उनकी जाँच करें[प्रलेखन](https://reference.aspose.com/cells/net/) विशेष जानकारी के लिए कृपया देखें.
2. विज़ुअल स्टूडियो: .NET डेवलपमेंट के लिए विज़ुअल स्टूडियो या कोई भी संगत IDE सेटअप होना ज़रूरी है। इससे आपको अपने प्रोजेक्ट को आराम से बनाने और प्रबंधित करने में मदद मिलेगी।
3.  Aspose.Cells लाइब्रेरी: Aspose.Cells लाइब्रेरी को यहाँ से डाउनलोड करें[विज्ञप्ति पृष्ठ](https://releases.aspose.com/cells/net/) और अपने प्रोजेक्ट में इसका संदर्भ जोड़ें.
4.  नमूना एक्सेल फ़ाइल: एक एक्सेल फ़ाइल बनाएं या तैयार रखें (उदाहरण के लिए,`Book1.xlsx`) जिसके साथ आप इस ट्यूटोरियल में काम करेंगे।
5. बुनियादी C# ज्ञान: C# भाषा की अवधारणाओं और वाक्यविन्यास से परिचित होना।
एक बार ये पूर्वापेक्षाएँ पूरी हो जाने पर, आप कोडिंग शुरू करने के लिए पूरी तरह तैयार हैं!
## पैकेज आयात करें
Aspose.Cells द्वारा प्रदान की गई कार्यक्षमताओं का उपयोग करने के लिए, आपको आवश्यक पैकेज आयात करने की आवश्यकता है। अपने C# प्रोजेक्ट में, अपनी कोड फ़ाइल के शीर्ष पर निम्नलिखित using निर्देश शामिल करना सुनिश्चित करें:
```csharp
using System.IO;
using Aspose.Cells;
using System.Drawing;
```
यह आपको एक्सेल फाइलों में आसानी से हेरफेर करने के लिए आवश्यक कक्षाओं और विधियों तक पहुंचने की अनुमति देता है।
अब जब आपके पास सब कुछ है, तो चलिए कॉपी विधि का उपयोग करने की प्रक्रिया को प्रबंधनीय चरणों में विभाजित करते हैं। हम एक्सेल फ़ाइल लोड करके शुरू करेंगे और फिर वांछित श्रेणी की प्रतिलिपि बनाने के लिए आगे बढ़ेंगे।
## चरण 1: फ़ाइल स्ट्रीम सेट अप करना
पहला कदम एक फ़ाइल स्ट्रीम बनाना है जो हमें अपनी एक्सेल फ़ाइल खोलने और उसके साथ काम करने की अनुमति देगा। यहाँ बताया गया है कि आप इसे कैसे करते हैं:
```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "Your Document Directory";
// खोली जाने वाली एक्सेल फ़ाइल वाली फ़ाइल स्ट्रीम बनाना
FileStream fstream = new FileStream(dataDir + "Book1.xlsx", FileMode.Open);
```
 इस कोड में, आपको वह पथ निर्दिष्ट करना होगा जहाँ आपका`Book1.xlsx` फ़ाइल स्थित है.`FileMode.Open` पैरामीटर यह इंगित करता है कि हम एक मौजूदा फ़ाइल खोलना चाहते हैं।
## चरण 2: कार्यपुस्तिका खोलना
इसके बाद, हम अभी सेट की गई फ़ाइल स्ट्रीम का उपयोग करके वर्कबुक ऑब्जेक्ट बनाएंगे। इससे हमें एक्सेल फ़ाइल की सामग्री तक पहुँच मिलती है।
```csharp
// फ़ाइल स्ट्रीम के माध्यम से एक्सेल फ़ाइल खोलना
Workbook workbook = new Workbook(fstream);
```
इस बिंदु पर, हमने कार्यपुस्तिका खोल ली है और इसकी सामग्री के साथ काम करना शुरू कर सकते हैं।
## चरण 3: वर्कशीट तक पहुँचना
एक बार वर्कबुक लोड हो जाने के बाद, हमें उस विशिष्ट वर्कशीट तक पहुँचना होगा जिस पर हम काम करना चाहते हैं। आमतौर पर, यह वर्कबुक में पहली वर्कशीट होगी।
```csharp
// एक्सेल फ़ाइल में पहली वर्कशीट तक पहुँचना
Worksheet worksheet = workbook.Worksheets[0];
```
 यहाँ,`Worksheets[0]` पहली शीट को पकड़ता है। यदि आप किसी अन्य वर्कशीट तक पहुँचना चाहते हैं, तो बस इंडेक्स बदलें।
## चरण 4: रेंज की प्रतिलिपि बनाना
अब मुख्य भाग आता है—सेल की श्रेणी की प्रतिलिपि बनाना। इस ट्यूटोरियल के लिए, हम दिखाएंगे कि एक सेल से दूसरे सेल में कंडीशनल फ़ॉर्मेटिंग सेटिंग कैसे कॉपी करें, साथ ही एक्सेल शीट की पूरी श्रेणी की प्रतिलिपि कैसे बनाएँ।
### सशर्त स्वरूपण की प्रतिलिपि बनाना (उदाहरण)
```csharp
// सेल "A1" से सेल "B1" में सशर्त प्रारूप सेटिंग की प्रतिलिपि बनाना
// वर्कशीट.कॉपीकंडीशनलफॉर्मेटिंग(0, 0, 0, 1);
```
यह लाइन मूल कोड में टिप्पणी की गई है, लेकिन यह आपको दिखाती है कि उसी वर्कशीट पर सेल A1 से सेल B1 में सशर्त स्वरूपण की प्रतिलिपि कैसे बनाई जाए। पैरामीटर स्रोत और गंतव्य सेल के पंक्ति और स्तंभ सूचकांकों का प्रतिनिधित्व करते हैं। यदि इस कार्यक्षमता की आवश्यकता है तो आप इसे अनकमेंट कर सकते हैं।
### संपूर्ण रेंज की प्रतिलिपि बनाना (उदाहरण)
हम अपनी प्रतिलिपिकरण कार्यक्षमता को आगे बढ़ाकर इसमें संपूर्ण रेंज की प्रतिलिपिकरण भी शामिल कर सकते हैं, जिसके लिए हम सभी कार्यपत्रकों को देखने के लिए एक लूप का उपयोग करेंगे।
```csharp
int TotalRowCount = 0;
for (int i = 0; i < workbook.Worksheets.Count; i++)
{
    // प्रत्येक कार्यपत्रक तक पहुँचना
    Worksheet sourceSheet = workbook.Worksheets[i];
    // वर्कशीट में डिस्प्ले रेंज प्राप्त करना
    Range sourceRange = sourceSheet.Cells.MaxDisplayRange;
    // गंतव्य कार्यपत्रक में श्रेणी बनाना
    Range destRange = worksheet.Cells.CreateRange(
        sourceRange.FirstRow + TotalRowCount,
        sourceRange.FirstColumn,
        sourceRange.RowCount,
        sourceRange.ColumnCount);
    // स्रोत श्रेणी को गंतव्य श्रेणी में कॉपी करना
    destRange.Copy(sourceRange);
    // अगले लूप पुनरावृत्ति के लिए कुल पंक्ति गणना को अद्यतन करना
    TotalRowCount += sourceRange.RowCount; 
}
```
## चरण 5: संशोधित कार्यपुस्तिका को सहेजना
आवश्यक श्रेणियों की प्रतिलिपि बनाने के बाद, आप अपने परिवर्तनों को सुरक्षित रखने के लिए संशोधित कार्यपुस्तिका को सहेजना चाहेंगे। यहाँ बताया गया है कि कैसे:
```csharp
// संशोधित एक्सेल फ़ाइल को सहेजना
workbook.Save(dataDir + "output.xls");
```
 यह कोड आपकी संशोधित कार्यपुस्तिका को इस रूप में सहेज लेगा`output.xls` अपनी निर्दिष्ट निर्देशिका में। अपनी आवश्यकताओं के अनुरूप उपयुक्त प्रारूप चुनना सुनिश्चित करें। 
## चरण 6: फ़ाइल स्ट्रीम बंद करना
अंत में, यह सुनिश्चित करने के लिए कि हमने सिस्टम संसाधनों को मुक्त कर दिया है, हमें उस फ़ाइल स्ट्रीम को बंद करना होगा जिसे हमने शुरू में खोला था।
```csharp
// सभी संसाधनों को मुक्त करने के लिए फ़ाइल स्ट्रीम को बंद करना
fstream.Close();
```
और बस इसी तरह, आपने रेंज की प्रतिलिपि बनाने और अद्यतन एक्सेल फ़ाइल को सहेजने की प्रक्रिया सफलतापूर्वक पूरी कर ली है!
## निष्कर्ष
.NET के लिए Aspose.Cells में कॉपी विधि का उपयोग करने से आपको Excel फ़ाइलों को आसानी से मैनिपुलेट करने की शक्तिशाली क्षमताएँ मिलती हैं। इस चरण-दर-चरण मार्गदर्शिका का पालन करके, आप अपने डेटा प्रबंधन कार्यों को सुव्यवस्थित करते हुए, एक वर्कशीट से दूसरी में सेल रेंज और सशर्त स्वरूपण को प्रभावी ढंग से कॉपी कर सकते हैं। 
## अक्सर पूछे जाने वाले प्रश्न
### .NET के लिए Aspose.Cells क्या है?
Aspose.Cells for .NET एक लाइब्रेरी है जो डेवलपर्स को .NET अनुप्रयोगों में प्रोग्रामेटिक रूप से Excel फ़ाइलों को बनाने, हेरफेर करने और प्रबंधित करने की अनुमति देती है।
### क्या मैं Aspose.Cells का उपयोग करके प्रारूप, सूत्र और मान कॉपी कर सकता हूँ?
हां, Aspose.Cells आपको न केवल मानों को बल्कि श्रेणियों के बीच प्रारूपों और सूत्रों को भी कॉपी करने की अनुमति देता है।
### क्या Aspose.Cells का उपयोग निःशुल्क है?
 Aspose.Cells निःशुल्क परीक्षण प्रदान करता है, लेकिन निरंतर उपयोग के लिए लाइसेंस खरीदना आवश्यक है। आप अधिक जानकारी पा सकते हैं[यहाँ](https://purchase.aspose.com/buy).
### यदि मुझे कोई समस्या आती है तो मैं सहायता कैसे प्राप्त कर सकता हूँ?
 आप Aspose सहायता मंच के माध्यम से सहायता प्राप्त कर सकते हैं[यहाँ](https://forum.aspose.com/c/cells/9).
### मैं Aspose.Cells लाइब्रेरी कहां से डाउनलोड कर सकता हूं?
 आप लाइब्रेरी को रिलीज़ पेज से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cells/net/).