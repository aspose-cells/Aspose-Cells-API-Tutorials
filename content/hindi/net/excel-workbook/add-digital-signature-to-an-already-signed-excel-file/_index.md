---
title: पहले से हस्ताक्षरित एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ें
linktitle: पहले से हस्ताक्षरित एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ मौजूदा Excel फ़ाइलों में आसानी से डिजिटल हस्ताक्षर जोड़ें।
type: docs
weight: 30
url: /hi/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
इस चरण-दर-चरण मार्गदर्शिका में, हम दिए गए C# स्रोत कोड की व्याख्या करेंगे जो आपको .NET के लिए Aspose.Cells का उपयोग करके पहले से हस्ताक्षरित एक्सेल फ़ाइल में एक डिजिटल हस्ताक्षर जोड़ने की अनुमति देगा। मौजूदा Excel फ़ाइल में नया डिजिटल हस्ताक्षर जोड़ने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: स्रोत और आउटपुट निर्देशिका सेट करें

```csharp
// स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();

// उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
```

इस पहले चरण में, हम स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करते हैं जिनका उपयोग मौजूदा एक्सेल फ़ाइल को लोड करने और फ़ाइल को नए डिजिटल हस्ताक्षर के साथ सहेजने के लिए किया जाएगा।

## चरण 2: मौजूदा एक्सेल फ़ाइल लोड करें

```csharp
// पहले से हस्ताक्षरित एक्सेल वर्कबुक लोड करें
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 यहां हम पहले से हस्ताक्षरित एक्सेल फ़ाइल का उपयोग करके लोड करते हैं`Workbook` Aspose.Cells का वर्ग।

## चरण 3: डिजिटल हस्ताक्षरों का संग्रह बनाएं

```csharp
// डिजिटल हस्ताक्षरों का संग्रह बनाएं
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 हम इसका उपयोग करके डिजिटल हस्ताक्षरों का एक नया संग्रह बनाते हैं`DigitalSignatureCollection` कक्षा।

## चरण 4: एक नया प्रमाणपत्र बनाएं

```csharp
// नया प्रमाणपत्र बनाएं
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

यहां हम दी गई फ़ाइल और पासवर्ड से एक नया प्रमाणपत्र बनाते हैं।

## चरण 5: संग्रह में एक नया डिजिटल हस्ताक्षर जोड़ें

```csharp
// एक नया डिजिटल हस्ताक्षर बनाएं
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// संग्रह में डिजिटल हस्ताक्षर जोड़ें
dsCollection.Add(signature);
```

 हम इसका उपयोग करके एक नया डिजिटल हस्ताक्षर बनाते हैं`DigitalSignature` कक्षा बनाएं और इसे डिजिटल हस्ताक्षरों के संग्रह में जोड़ें।

## चरण 6: डिजिटल हस्ताक्षरों का संग्रह कार्यपुस्तिका में जोड़ें

```csharp
//कार्यपुस्तिका में डिजिटल हस्ताक्षरों का संग्रह जोड़ें
workbook.AddDigitalSignature(dsCollection);
```

 हम इसका उपयोग करके मौजूदा एक्सेल वर्कबुक में डिजिटल हस्ताक्षरों का संग्रह जोड़ते हैं`AddDigitalSignature()` तरीका।

## चरण 7: कार्यपुस्तिका सहेजें और बंद करें

```csharp
// कार्यपुस्तिका सहेजें और बंद करें
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

हम कार्यपुस्तिका को नए डिजिटल हस्ताक्षर के साथ निर्दिष्ट आउटपुट निर्देशिका में सहेजते हैं, फिर इसे बंद करते हैं और संबंधित संसाधनों को जारी करते हैं।

### .NET के लिए Aspose.Cells का उपयोग करके पहले से हस्ताक्षरित एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
//उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
//प्रमाणपत्र फ़ाइल और उसका पासवर्ड
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//नए डिजिटल हस्ताक्षर जोड़ने के लिए उस कार्यपुस्तिका को लोड करें जो पहले से ही डिजिटल रूप से हस्ताक्षरित है
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//डिजिटल हस्ताक्षर संग्रह बनाएं
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//नया प्रमाणपत्र बनाएं
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//नया डिजिटल हस्ताक्षर बनाएं और इसे डिजिटल हस्ताक्षर संग्रह में जोड़ें
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//कार्यपुस्तिका के अंदर डिजिटल हस्ताक्षर संग्रह जोड़ें
workbook.AddDigitalSignature(dsCollection);
//कार्यपुस्तिका सहेजें और उसका निपटान करें.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## निष्कर्ष

बधाई हो! अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके पहले से हस्ताक्षरित Excel फ़ाइल में डिजिटल हस्ताक्षर कैसे जोड़ें। डिजिटल हस्ताक्षर आपकी एक्सेल फ़ाइलों में सुरक्षा की एक अतिरिक्त परत जोड़ते हैं, जिससे उनकी प्रामाणिकता और अखंडता सुनिश्चित होती है।

### सामान्य प्रश्नोत्तर

#### प्रश्न: .NET के लिए Aspose.Cells क्या है?

उत्तर: .NET के लिए Aspose.Cells एक शक्तिशाली क्लास लाइब्रेरी है जो .NET डेवलपर्स को एक्सेल फ़ाइलों को आसानी से बनाने, संशोधित करने, परिवर्तित करने और हेरफेर करने की अनुमति देता है।

#### प्रश्न: एक्सेल फ़ाइल में डिजिटल हस्ताक्षर क्या है?

उ: एक्सेल फ़ाइल में डिजिटल हस्ताक्षर एक इलेक्ट्रॉनिक चिह्न है जो दस्तावेज़ की प्रामाणिकता, अखंडता और उत्पत्ति की गारंटी देता है। इसका उपयोग यह सत्यापित करने के लिए किया जाता है कि फ़ाइल पर हस्ताक्षर किए जाने के बाद से उसे संशोधित नहीं किया गया है और यह एक विश्वसनीय स्रोत से आई है।

#### प्रश्न: एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ने के क्या लाभ हैं?

उ: एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ने से कई लाभ मिलते हैं, जिनमें अनधिकृत परिवर्तनों के खिलाफ सुरक्षा, डेटा अखंडता सुनिश्चित करना, दस्तावेज़ के लेखक को प्रमाणित करना और इसमें शामिल जानकारी में विश्वास प्रदान करना शामिल है।

#### प्रश्न: क्या मैं एक्सेल फ़ाइल में एकाधिक डिजिटल हस्ताक्षर जोड़ सकता हूँ?

उ: हाँ, Aspose.Cells आपको एक Excel फ़ाइल में एकाधिक डिजिटल हस्ताक्षर जोड़ने की अनुमति देता है। आप डिजिटल हस्ताक्षरों का एक संग्रह बना सकते हैं और उन्हें एक ऑपरेशन में फ़ाइल में जोड़ सकते हैं।

#### प्रश्न: एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ने के लिए क्या आवश्यकताएँ हैं?

उ: एक्सेल फ़ाइल में डिजिटल हस्ताक्षर जोड़ने के लिए, आपको एक वैध डिजिटल प्रमाणपत्र की आवश्यकता होगी जिसका उपयोग दस्तावेज़ पर हस्ताक्षर करने के लिए किया जाएगा। डिजिटल हस्ताक्षर जोड़ने से पहले सुनिश्चित करें कि आपके पास सही प्रमाणपत्र और पासवर्ड है।