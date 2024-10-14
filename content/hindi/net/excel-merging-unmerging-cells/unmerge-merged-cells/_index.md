---
title: एक्सेल में मर्ज किए गए कक्षों को अलग करें
linktitle: एक्सेल में मर्ज किए गए कक्षों को अलग करें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: .NET के लिए Aspose.Cells का उपयोग करके Excel में मर्ज किए गए सेल को आसानी से अनमर्ज करें। बेहतर स्प्रेडशीट बनाने के लिए हमारे चरण-दर-चरण गाइड का पालन करें।
type: docs
weight: 10
url: /hi/net/excel-merging-unmerging-cells/unmerge-merged-cells/
---
## परिचय

क्या आप अपनी एक्सेल स्प्रेडशीट में मर्ज की गई कोशिकाओं से निपटने से थक गए हैं? आप अकेले नहीं हैं! मर्ज की गई कोशिकाएँ फ़ॉर्मेटिंग के लिए एक उपयोगी सुविधा हो सकती हैं, लेकिन जब डेटा हेरफेर और विश्लेषण की बात आती है तो वे अक्सर सिरदर्द का कारण बन सकती हैं। लेकिन अंदाज़ा लगाइए क्या? उन कष्टप्रद कोशिकाओं को अलग करना जितना आप सोच सकते हैं उससे कहीं ज़्यादा आसान है - खासकर जब आप .NET के लिए Aspose.Cells का उपयोग करते हैं। इस लेख में, मैं आपको मर्ज की गई कोशिकाओं को चरण दर चरण अलग करने का तरीका बताऊंगा, यह सुनिश्चित करते हुए कि आपका डेटा साफ-सुथरा, सुव्यवस्थित और कार्रवाई के लिए तैयार है! तो, अपनी कोडिंग टोपी पकड़ो, और Aspose.Cells की दुनिया में गोता लगाएँ।

## आवश्यक शर्तें

इससे पहले कि हम अपने हाथ गंदे करें, कुछ आवश्यक चीजें हैं जिन्हें आपको तैयार रखना होगा:

### C# और .NET फ्रेमवर्क का बुनियादी ज्ञान
यदि आप C# प्रोग्रामिंग से परिचित हैं और .NET फ्रेमवर्क की बुनियादी समझ रखते हैं, तो आप पहले से ही एक बेहतरीन शुरुआत कर चुके हैं। यदि नहीं, तो चिंता न करें! यह ट्यूटोरियल सरल होने के लिए डिज़ाइन किया गया है, ताकि आप आवश्यक अवधारणाओं को सीख सकें।

### Aspose.Cells लाइब्रेरी
सुनिश्चित करें कि आपके .NET वातावरण में Aspose.Cells लाइब्रेरी स्थापित है। आप इसे आसानी से यहाँ जाकर प्राप्त कर सकते हैं।[Aspose.Cells डाउनलोड पृष्ठ](https://releases.aspose.com/cells/net/).

### आईडीई सेटअप
आपके पास विजुअल स्टूडियो जैसा एक विकास वातावरण स्थापित होना चाहिए, जहां आप अपना C# कोड लिख और निष्पादित कर सकें।

### नमूना एक्सेल फ़ाइल
एक नमूना एक्सेल फ़ाइल लें जिसमें कुछ मर्ज किए गए सेल हों - आप इस फ़ाइल का उपयोग मर्ज हटाने का अभ्यास करने के लिए करेंगे।

इन सभी पूर्व-आवश्यकताओं को पूरा करने के बाद, अब हम रोमांचक भाग में प्रवेश कर सकते हैं - हमारे समाधान की कोड-कोडिंग!

## पैकेज आयात करें

सबसे पहले, आइए आवश्यक पैकेज आयात करें। Aspose.Cells के साथ, आप अपनी Excel फ़ाइलों को प्रभावी ढंग से प्रबंधित करने के लिए विभिन्न क्लासों के साथ बातचीत करेंगे। यहाँ बताया गया है कि आपको अपनी C# फ़ाइल के शीर्ष पर क्या शामिल करना होगा:

```csharp
using System;
using System.IO;

using Aspose.Cells;
```

इस पैकेज को शामिल करके, आपको Aspose.Cells द्वारा दी जाने वाली सभी सुविधाओं तक पहुंच प्राप्त होगी।

आइए, विलयन प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें। प्रत्येक चरण को स्पष्ट रूप से परिभाषित किया जाएगा ताकि आप आसानी से उसका अनुसरण कर सकें।

## चरण 1: निर्देशिकाएँ परिभाषित करें

पहला कदम उन निर्देशिकाओं को परिभाषित करना है जहाँ आपकी इनपुट एक्सेल फ़ाइल (जिसमें मर्ज किए गए सेल हैं) और आपकी आउटपुट फ़ाइल (जहाँ अनमर्ज किए गए डेटा को सहेजा जाएगा) स्थित हैं। इसे सेट अप करने का तरीका यहाँ बताया गया है:

```csharp
// स्रोत निर्देशिका
string sourceDir = "Your Document Directory"; 

// आउटपुट निर्देशिका
string outputDir = "Your Document Directory"; 
```

 प्रतिस्थापित करना सुनिश्चित करें`"Your Document Directory"` आपकी फ़ाइलों के वास्तविक पथ के साथ.

## चरण 2: कार्यपुस्तिका बनाएँ

अब जब आपने निर्देशिकाएँ सेट कर ली हैं, तो अब वर्कबुक ऑब्जेक्ट बनाने का समय आ गया है। यह ऑब्जेक्ट आपको एक्सेल फ़ाइल में हेरफेर करने की अनुमति देगा। आप निम्न कोड के साथ ऐसा कर सकते हैं:

```csharp
// कार्यपुस्तिका बनाएं
Workbook wbk = new Aspose.Cells.Workbook(sourceDir + "sampleUnMergingtheMergedCells.xlsx");
```

कोड की यह पंक्ति आपकी नमूना एक्सेल फ़ाइल को पढ़ती है और उसे प्रसंस्करण के लिए तैयार करती है। 

## चरण 3: वर्कशीट तक पहुंचें

हर वर्कबुक में शीट होती हैं। आपको उस खास वर्कशीट तक पहुंचना होगा जहां आप सेल को अनमर्ज करना चाहते हैं। ऐसा करने का तरीका यहां बताया गया है:

```csharp
// वर्कशीट बनाएं और पहली शीट प्राप्त करें
Worksheet worksheet = wbk.Worksheets[0];
```

यह कोड पहली वर्कशीट को पकड़ता है। यदि आपकी मर्ज की गई सेल किसी दूसरी शीट पर हैं, तो इंडेक्स को उसी के अनुसार अपडेट करें।

## चरण 4: वर्कशीट में कक्षों तक पहुँचें

इसके बाद, आपको अपनी वर्कशीट में मौजूद सेल का संदर्भ प्राप्त करना होगा। इसे निम्न का उपयोग करके पूरा किया जा सकता है:

```csharp
//सभी कोशिकाओं को लाने के लिए एक सेल ऑब्जेक्ट बनाएं
Cells cells = worksheet.Cells;
```

इस पंक्ति के साथ, अब आपके पास वर्कशीट पर सभी कक्षों तक पहुंच होगी, जिससे आप आवश्यकतानुसार उनमें परिवर्तन कर सकेंगे।

## चरण 5: कोशिकाओं को अलग करें

अब महत्वपूर्ण चरण आता है—सेल्स को अलग करना! आपको मर्ज की गई उन सेल की सीमा निर्दिष्ट करनी होगी जिन्हें आप अलग करना चाहते हैं। निम्न कोड का उपयोग करें:

```csharp
// कोशिकाओं को अलग करें
cells.UnMerge(5, 2, 2, 3);
```

 इस उदाहरण में,`UnMerge` विधि चार पैरामीटर लेती है: प्रारंभिक पंक्ति इंडेक्स (5), प्रारंभिक कॉलम इंडेक्स (2), अनमर्ज की जाने वाली पंक्तियों की संख्या (2), और अनमर्ज किए जाने वाले कॉलम की संख्या (3)। अपनी एक्सेल फ़ाइल में विशिष्ट मर्ज किए गए सेल से मिलान करने के लिए इन पैरामीटर को समायोजित करें।

## चरण 6: कार्यपुस्तिका सहेजें

अनमर्ज करने के बाद, आप अपने बदलावों को एक नई एक्सेल फ़ाइल में सहेजना चाहेंगे। ऐसा करने का तरीका यहां बताया गया है:

```csharp
// फ़ाइल सहेजें
wbk.Save(outputDir + "outputUnMergingtheMergedCells.xlsx");
```

यह लाइन आपके अनमर्ज्ड डेटा को निर्दिष्ट आउटपुट डायरेक्टरी में सहेजती है। इतना ही सरल!

## चरण 7: प्रक्रिया की पुष्टि करें

अंत में, यह पुष्टि करना अच्छा विचार है कि सब कुछ सुचारू रूप से चला। आप कंसोल पर एक संदेश प्रिंट कर सकते हैं ताकि आपको पता चल सके कि ऑपरेशन सफलतापूर्वक निष्पादित हुआ:

```csharp
Console.WriteLine("UnMerging the Cells executed successfully.");
```

और बस हो गया! आपने .NET के लिए Aspose.Cells का उपयोग करके Excel फ़ाइल में सफलतापूर्वक सेल को अनमर्ज कर दिया है।

## निष्कर्ष

सेल को अलग करना थकाऊ लग सकता है, खासकर यदि आप बड़ी स्प्रेडशीट के साथ काम कर रहे हैं, लेकिन .NET के लिए Aspose.Cells के साथ, यह बहुत आसान है! इस ट्यूटोरियल ने आपको अपने वातावरण को सेट करने से लेकर सेल को प्रभावी ढंग से अलग करने के लिए आवश्यक कोड को निष्पादित करने तक सब कुछ सिखाया है। Aspose.Cells लाइब्रेरी द्वारा दी जाने वाली लचीलापन आपको स्प्रेडशीट को कुशलतापूर्वक संसाधित करने की अनुमति देता है, जिससे यह एक्सेल फ़ाइलों के साथ काम करने वाले डेवलपर्स के लिए एक आदर्श विकल्प बन जाता है। तो, इसमें गोता लगाएँ, और साफ-सुथरी, अधिक प्रबंधनीय स्प्रेडशीट का आनंद लेना शुरू करें।

## अक्सर पूछे जाने वाले प्रश्न

### Aspose.Cells क्या है?  
Aspose.Cells .NET अनुप्रयोगों में Excel दस्तावेज़ों को बनाने, हेरफेर करने और परिवर्तित करने के लिए एक शक्तिशाली लाइब्रेरी है।

### क्या मुझे Aspose.Cells का उपयोग करने के लिए लाइसेंस की आवश्यकता है?  
 जबकि Aspose.Cells एक निःशुल्क परीक्षण प्रदान करता है, पूर्ण उपयोग के लिए लाइसेंस की आवश्यकता होती है। आप एक प्राप्त कर सकते हैं[अस्थायी लाइसेंस यहाँ](https://purchase.aspose.com/temporary-license/).

### क्या मैं एक साथ कई शीटों में से कोशिकाओं को अलग कर सकता हूँ?  
हां, आप एक कार्यपुस्तिका के भीतर एकाधिक कार्यपत्रकों के बीच लूप कर सकते हैं और आवश्यकतानुसार कक्षों को अलग कर सकते हैं।

### क्या Aspose.Cells .NET कोर के साथ संगत है?  
हां, Aspose.Cells .NET Core के साथ संगत है, जो इसे विभिन्न .NET अनुप्रयोगों के लिए बहुमुखी बनाता है।

### मैं Aspose.Cells पर अधिक दस्तावेज़ कहां पा सकता हूं?  
 आप संपूर्ण दस्तावेज़ यहां देख सकते हैं[Aspose.Cells संदर्भ पृष्ठ](https://reference.aspose.com/cells/net/).