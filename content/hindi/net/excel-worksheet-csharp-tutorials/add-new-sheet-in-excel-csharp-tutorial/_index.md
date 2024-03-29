---
title: Excel C# ट्यूटोरियल में नई शीट जोड़ें
linktitle: एक्सेल में नई शीट जोड़ें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: जानें कि .NET के लिए Aspose.Cells का उपयोग करके Excel में एक नई शीट कैसे जोड़ें। C# में स्रोत कोड के साथ चरण दर चरण ट्यूटोरियल।
type: docs
weight: 20
url: /hi/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
इस ट्यूटोरियल में, हम .NET के लिए Aspose.Cells का उपयोग करके एक्सेल में एक नई शीट जोड़ने के लिए चरण दर चरण C# स्रोत कोड की व्याख्या करेंगे। रिपोर्ट बनाते समय या डेटा में हेरफेर करते समय एक्सेल वर्कबुक में एक नई वर्कशीट जोड़ना एक सामान्य ऑपरेशन है। Aspose.Cells एक शक्तिशाली लाइब्रेरी है जो .NET का उपयोग करके एक्सेल फ़ाइलों में हेरफेर करना और उत्पन्न करना आसान बनाती है। इस कोड को समझने और लागू करने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: दस्तावेज़ निर्देशिका सेटअप

पहला कदम दस्तावेज़ निर्देशिका को परिभाषित करना है जहां एक्सेल फ़ाइल सहेजी जाएगी। यदि निर्देशिका मौजूद नहीं है, तो हम इसे निम्नलिखित कोड का उपयोग करके बनाते हैं:

```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// यदि यह पहले से मौजूद नहीं है तो निर्देशिका बनाएं।
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

अपने दस्तावेज़ निर्देशिका के लिए "आपकी दस्तावेज़ निर्देशिका" को उचित पथ से बदलना सुनिश्चित करें।

## चरण 2: किसी कार्यपुस्तिका ऑब्जेक्ट को इंस्टेंट करना

दूसरा चरण वर्कबुक ऑब्जेक्ट को इंस्टेंट करना है, जो एक्सेल वर्कबुक का प्रतिनिधित्व करता है। निम्नलिखित कोड का प्रयोग करें:

```csharp
Workbook workbook = new Workbook();
```

इस ऑब्जेक्ट का उपयोग नई वर्कशीट जोड़ने और एक्सेल वर्कबुक पर अन्य ऑपरेशन करने के लिए किया जाएगा।

## चरण 3: एक नई वर्कशीट जोड़ना

तीसरा चरण वर्कबुक ऑब्जेक्ट में एक नई वर्कशीट जोड़ना है। निम्नलिखित कोड का प्रयोग करें:

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

यह वर्कबुक ऑब्जेक्ट में एक नई वर्कशीट जोड़ देगा और आपको इसके इंडेक्स का उपयोग करके इस वर्कशीट का एक संदर्भ मिलेगा।

## चरण 4: नई वर्कशीट का नाम सेट करना

चौथा चरण नई वर्कशीट को एक नाम देना है। वर्कशीट का नाम सेट करने के लिए आप निम्नलिखित कोड का उपयोग कर सकते हैं:

```csharp
worksheet.Name = "My Worksheet";
```

नई शीट के लिए "मेरी स्प्रेडशीट" को वांछित नाम से बदलें।

## चरण 5: एक्सेल फ़ाइल को सहेजना

अंत में, अंतिम चरण एक्सेल फ़ाइल को सहेजना है। निम्नलिखित कोड का प्रयोग करें:

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

यह एक्सेल वर्कबुक को नई वर्कशीट के साथ आपके द्वारा निर्दिष्ट दस्तावेज़ निर्देशिका में सहेज लेगा।

### .NET के लिए Aspose.Cells का उपयोग करके Excel C# ट्यूटोरियल में नई शीट जोड़ने के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// यदि यह पहले से मौजूद नहीं है तो निर्देशिका बनाएं।
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
Workbook workbook = new Workbook();
// वर्कबुक ऑब्जेक्ट में एक नई वर्कशीट जोड़ना
int i = workbook.Worksheets.Add();
// नई जोड़ी गई वर्कशीट का शीट इंडेक्स पास करके उसका संदर्भ प्राप्त करना
Worksheet worksheet = workbook.Worksheets[i];
// नई जोड़ी गई वर्कशीट का नाम सेट करना
worksheet.Name = "My Worksheet";
// एक्सेल फ़ाइल सहेजा जा रहा है
workbook.Save(dataDir + "output.out.xls");
```

## निष्कर्ष

अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके Excel में एक नई वर्कशीट कैसे जोड़ें। आप C# का उपयोग करके एक्सेल फ़ाइलों में हेरफेर करने और उत्पन्न करने के लिए इस विधि का उपयोग कर सकते हैं। Aspose.Cells आपके अनुप्रयोगों में एक्सेल फ़ाइलों के प्रबंधन को सरल बनाने के लिए कई शक्तिशाली सुविधाएँ प्रदान करता है।

### अक्सर पूछे जाने वाले प्रश्न (FAQ)

#### क्या मैं Aspose.Cells का उपयोग C# के अलावा अन्य प्रोग्रामिंग भाषाओं के साथ कर सकता हूँ?

हां, Aspose.Cells कई प्रोग्रामिंग भाषाओं जैसे जावा, पायथन, रूबी और कई अन्य भाषाओं का समर्थन करता है।

#### क्या मैं नव निर्मित वर्कशीट में सेल्स में फ़ॉर्मेटिंग जोड़ सकता हूँ?

हां, आप Aspose.Cells के वर्कशीट वर्ग द्वारा प्रदान की गई विधियों का उपयोग करके कोशिकाओं पर फ़ॉर्मेटिंग लागू कर सकते हैं। आप सेल शैली सेट कर सकते हैं, पृष्ठभूमि का रंग बदल सकते हैं, बॉर्डर लगा सकते हैं, आदि।

#### मैं नई वर्कशीट से सेल डेटा तक कैसे पहुँच सकता हूँ?

आप Aspose.Cells के वर्कशीट वर्ग द्वारा प्रदान किए गए गुणों और विधियों का उपयोग करके सेल डेटा तक पहुंच सकते हैं। उदाहरण के लिए, आप किसी विशिष्ट सेल तक पहुंचने और उसके मान को पुनर्प्राप्त या संशोधित करने के लिए सेल प्रॉपर्टी का उपयोग कर सकते हैं।

#### क्या Aspose.Cells एक्सेल में फ़ार्मुलों का समर्थन करता है?

हाँ, Aspose.Cells एक्सेल फ़ार्मुलों का समर्थन करता है। आप सेल क्लास की सेटफॉर्मूला विधि का उपयोग करके वर्कशीट सेल में सूत्र सेट कर सकते हैं।
