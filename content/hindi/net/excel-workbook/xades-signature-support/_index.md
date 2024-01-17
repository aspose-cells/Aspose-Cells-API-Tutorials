---
title: ज़ेडेस सिग्नेचर सपोर्ट
linktitle: ज़ेडेस सिग्नेचर सपोर्ट
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके Excel फ़ाइल में Xades हस्ताक्षर जोड़ने का तरीका जानें।
type: docs
weight: 190
url: /hi/net/excel-workbook/xades-signature-support/
---
इस लेख में, हम आपको नीचे दिए गए C# स्रोत कोड को चरण दर चरण समझाएंगे, जो .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके Xades हस्ताक्षर समर्थन के बारे में है। आप सीखेंगे कि Excel फ़ाइल में Xades डिजिटल हस्ताक्षर जोड़ने के लिए इस लाइब्रेरी का उपयोग कैसे करें। हम आपको हस्ताक्षर प्रक्रिया और उसके निष्पादन का अवलोकन भी प्रदान करेंगे। निर्णायक परिणाम प्राप्त करने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करें
आरंभ करने के लिए, हमें अपने कोड में स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करने की आवश्यकता है। ये निर्देशिकाएँ इंगित करती हैं कि स्रोत फ़ाइलें कहाँ स्थित हैं और आउटपुट फ़ाइल कहाँ सहेजी जाएंगी। यहाँ संबंधित कोड है:

```csharp
// स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
// उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
```

आवश्यकतानुसार निर्देशिका पथों को अनुकूलित करना सुनिश्चित करें।

## चरण 2: एक्सेल कार्यपुस्तिका लोड हो रही है
अगला कदम एक्सेल वर्कबुक को लोड करना है जिस पर हम Xades डिजिटल हस्ताक्षर जोड़ना चाहते हैं। कार्यपुस्तिका लोड करने के लिए कोड यहां दिया गया है:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

कोड में स्रोत फ़ाइल का नाम सही ढंग से निर्दिष्ट करना सुनिश्चित करें।

## चरण 3: डिजिटल हस्ताक्षर कॉन्फ़िगर करना
अब हम आवश्यक जानकारी प्रदान करके Xades डिजिटल हस्ताक्षर को कॉन्फ़िगर करेंगे। हमें डिजिटल प्रमाणपत्र वाली पीएफएक्स फ़ाइल, साथ ही संबंधित पासवर्ड निर्दिष्ट करना होगा। यहाँ संबंधित कोड है:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

"pfxPassword" को अपने वास्तविक पासवर्ड से और "pfxFile" को PFX फ़ाइल के पथ से बदलना सुनिश्चित करें।

## चरण 4: डिजिटल हस्ताक्षर जोड़ना
अब जब हमने डिजिटल हस्ताक्षर कॉन्फ़िगर कर लिया है, तो हम इसे एक्सेल वर्कबुक में जोड़ सकते हैं। यहाँ संबंधित कोड है:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

यह चरण Excel कार्यपुस्तिका में Xades डिजिटल हस्ताक्षर जोड़ता है।

## चरण 5: कार्यपुस्तिका को हस्ताक्षर के साथ सहेजना
अंत में, हम एक्सेल वर्कबुक को डिजिटल हस्ताक्षर के साथ सहेजते हैं। यहाँ संबंधित कोड है:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

अपनी आवश्यकताओं के अनुसार आउटपुट फ़ाइल का नाम अनुकूलित करना सुनिश्चित करें।

### .NET के लिए Aspose.Cells का उपयोग करके Xades सिग्नेचर सपोर्ट के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
//उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## निष्कर्ष
बधाई हो! आपने सीखा है कि Excel फ़ाइल में Xades डिजिटल हस्ताक्षर जोड़ने के लिए .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग कैसे करें। इस आलेख में दिए गए चरणों का पालन करके, आप इस कार्यक्षमता को अपनी परियोजनाओं में लागू करने में सक्षम होंगे। बेझिझक लाइब्रेरी के साथ और अधिक प्रयोग करें और इसके द्वारा प्रदान की जाने वाली अन्य शक्तिशाली सुविधाओं की खोज करें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: ज़ेडेस क्या है?

उत्तर: Xades एक उन्नत इलेक्ट्रॉनिक हस्ताक्षर मानक है जिसका उपयोग डिजिटल दस्तावेज़ों की अखंडता और प्रामाणिकता सुनिश्चित करने के लिए किया जाता है।

#### प्रश्न: क्या मैं Aspose.Cells के साथ अन्य प्रकार के डिजिटल हस्ताक्षरों का उपयोग कर सकता हूँ?

उत्तर: हां, Aspose.Cells अन्य प्रकार के डिजिटल हस्ताक्षरों का भी समर्थन करता है, जैसे XMLDSig हस्ताक्षर और PKCS#7 हस्ताक्षर।

#### प्रश्न: क्या मैं एक्सेल फ़ाइलों के अलावा अन्य फ़ाइल प्रकारों पर हस्ताक्षर लागू कर सकता हूँ?
 
उ: हाँ, Aspose.Cells अन्य समर्थित फ़ाइल प्रकारों जैसे Word, PDF और PowerPoint फ़ाइलों पर डिजिटल हस्ताक्षर लागू करने की भी अनुमति देता है।