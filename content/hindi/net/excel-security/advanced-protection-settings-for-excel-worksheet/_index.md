---
title: एक्सेल वर्कशीट के लिए उन्नत सुरक्षा सेटिंग्स
linktitle: एक्सेल वर्कशीट के लिए उन्नत सुरक्षा सेटिंग्स
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ उन्नत सुरक्षा सेटिंग्स सेट करके अपनी Excel फ़ाइलों को सुरक्षित रखें।
type: docs
weight: 10
url: /hi/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल स्प्रेडशीट के लिए उन्नत सुरक्षा सेटिंग्स सेट करने के चरणों के बारे में बताएंगे। इस कार्य को पूरा करने के लिए नीचे दिए गए निर्देशों का पालन करें।

## चरण 1: तैयारी

सुनिश्चित करें कि आपने .NET के लिए Aspose.Cells स्थापित किया है और अपने पसंदीदा एकीकृत विकास वातावरण (IDE) में एक C# प्रोजेक्ट बनाया है।

## चरण 2: दस्तावेज़ निर्देशिका पथ सेट करें

 घोषित करें ए`dataDir` वैरिएबल बनाएं और इसे अपने दस्तावेज़ निर्देशिका के पथ के साथ प्रारंभ करें। उदाहरण के लिए :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 प्रतिस्थापित करना सुनिश्चित करें`"YOUR_DOCUMENTS_DIRECTORY"` आपकी निर्देशिका के वास्तविक पथ के साथ।

## चरण 3: एक्सेल फ़ाइल खोलने के लिए एक फ़ाइल स्ट्रीम बनाएं

 एक बनाने के`FileStream` खोलने के लिए एक्सेल फ़ाइल युक्त ऑब्जेक्ट:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 सुनिश्चित करें कि आपके पास Excel फ़ाइल है`book1.xls` अपने दस्तावेज़ निर्देशिका में या सही फ़ाइल नाम और स्थान निर्दिष्ट करें।

## चरण 4: वर्कबुक ऑब्जेक्ट को इंस्टेंट करें और एक्सेल फ़ाइल खोलें

 उपयोग`Workbook`वर्कबुक ऑब्जेक्ट को इंस्टेंट करने और फ़ाइल स्ट्रीम के माध्यम से निर्दिष्ट एक्सेल फ़ाइल खोलने के लिए Aspose.Cells से क्लास:

```csharp
Workbook excel = new Workbook(fstream);
```

## चरण 5: पहली वर्कशीट तक पहुंचें

एक्सेल फ़ाइल की पहली वर्कशीट पर जाएँ:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## चरण 6: वर्कशीट सुरक्षा सेटिंग्स सेट करें

आवश्यकतानुसार वर्कशीट सुरक्षा सेटिंग्स सेट करने के लिए वर्कशीट ऑब्जेक्ट गुणों का उपयोग करें। उदाहरण के लिए :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ...आवश्यकतानुसार अन्य सुरक्षा सेटिंग्स सेट करें...
```

## चरण 7: संशोधित एक्सेल फ़ाइल सहेजें

 का उपयोग करके संशोधित एक्सेल फ़ाइल को सहेजें`Save` कार्यपुस्तिका ऑब्जेक्ट की विधि:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

आउटपुट फ़ाइल के लिए वांछित पथ और फ़ाइल नाम निर्दिष्ट करना सुनिश्चित करें।

## चरण 8: फ़ाइल स्ट्रीम बंद करें

एक बार सहेजने के बाद, सभी संबद्ध संसाधनों को जारी करने के लिए फ़ाइल स्ट्रीम को बंद करें:

```csharp
fstream.Close();
```
	
### .NET के लिए Aspose.Cells का उपयोग करके एक्सेल वर्कशीट के लिए उन्नत सुरक्षा सेटिंग्स के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// एक फ़ाइल स्ट्रीम बनाना जिसमें एक्सेल फ़ाइल खोली जानी है
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
// फ़ाइल स्ट्रीम के माध्यम से एक्सेल फ़ाइल खोलना
Workbook excel = new Workbook(fstream);
// एक्सेल फ़ाइल में पहली वर्कशीट तक पहुँचना
Worksheet worksheet = excel.Worksheets[0];
// वर्कशीट के कॉलम हटाने के लिए उपयोगकर्ताओं को प्रतिबंधित करना
worksheet.Protection.AllowDeletingColumn = false;
// वर्कशीट की पंक्ति को हटाने के लिए उपयोगकर्ताओं को प्रतिबंधित करना
worksheet.Protection.AllowDeletingRow = false;
// वर्कशीट की सामग्री को संपादित करने के लिए उपयोगकर्ताओं को प्रतिबंधित करना
worksheet.Protection.AllowEditingContent = false;
// वर्कशीट की वस्तुओं को संपादित करने के लिए उपयोगकर्ताओं को प्रतिबंधित करना
worksheet.Protection.AllowEditingObject = false;
// वर्कशीट के परिदृश्यों को संपादित करने के लिए उपयोगकर्ताओं को प्रतिबंधित करना
worksheet.Protection.AllowEditingScenario = false;
//उपयोगकर्ताओं को फ़िल्टर करने के लिए प्रतिबंधित करना
worksheet.Protection.AllowFiltering = false;
// उपयोगकर्ताओं को वर्कशीट की कोशिकाओं को प्रारूपित करने की अनुमति देना
worksheet.Protection.AllowFormattingCell = true;
// उपयोगकर्ताओं को वर्कशीट की पंक्तियों को प्रारूपित करने की अनुमति देना
worksheet.Protection.AllowFormattingRow = true;
// उपयोगकर्ताओं को वर्कशीट में कॉलम डालने की अनुमति देना
worksheet.Protection.AllowFormattingColumn = true;
// उपयोगकर्ताओं को वर्कशीट में हाइपरलिंक सम्मिलित करने की अनुमति देना
worksheet.Protection.AllowInsertingHyperlink = true;
// उपयोगकर्ताओं को वर्कशीट में पंक्तियाँ सम्मिलित करने की अनुमति देना
worksheet.Protection.AllowInsertingRow = true;
// उपयोगकर्ताओं को कार्यपत्रक की लॉक की गई कोशिकाओं का चयन करने की अनुमति देना
worksheet.Protection.AllowSelectingLockedCell = true;
// उपयोगकर्ताओं को कार्यपत्रक के अनलॉक किए गए कक्षों का चयन करने की अनुमति देना
worksheet.Protection.AllowSelectingUnlockedCell = true;
// उपयोगकर्ताओं को क्रमबद्ध करने की अनुमति देना
worksheet.Protection.AllowSorting = true;
// उपयोगकर्ताओं को वर्कशीट में पिवट टेबल का उपयोग करने की अनुमति देना
worksheet.Protection.AllowUsingPivotTable = true;
// संशोधित एक्सेल फ़ाइल सहेजा जा रहा है
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// सभी संसाधनों को मुक्त करने के लिए फ़ाइल स्ट्रीम को बंद करना
fstream.Close();
```

## निष्कर्ष

बधाई हो! अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल स्प्रेडशीट के लिए उन्नत सुरक्षा सेटिंग्स कैसे सेट करें। अपनी एक्सेल फ़ाइलों को सुरक्षित करने और उपयोगकर्ता गतिविधियों को प्रतिबंधित करने के लिए इस ज्ञान का उपयोग करें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: मैं अपनी IDE में एक नया C# प्रोजेक्ट कैसे बना सकता हूँ?

उ: आपके द्वारा उपयोग किए जा रहे आईडीई के आधार पर एक नया सी# प्रोजेक्ट बनाने के चरण भिन्न हो सकते हैं। विस्तृत निर्देशों के लिए अपने IDE के दस्तावेज़ देखें।

#### प्रश्न: क्या ट्यूटोरियल में उल्लिखित के अलावा अन्य कस्टम सुरक्षा सेटिंग्स सेट करना संभव है?

उत्तर: हाँ, Aspose.Cells सुरक्षा सेटिंग्स की एक विस्तृत श्रृंखला प्रदान करता है जिसे आप अपनी विशिष्ट आवश्यकताओं के अनुसार अनुकूलित कर सकते हैं। अधिक विवरण के लिए Aspose.Cells दस्तावेज़ देखें।

#### प्रश्न: नमूना कोड में संशोधित एक्सेल फ़ाइल को सहेजने के लिए उपयोग किया जाने वाला फ़ाइल प्रारूप क्या है?

उ: नमूना कोड में, संशोधित एक्सेल फ़ाइल Excel 97-2003 (.xls) प्रारूप में सहेजी गई है। यदि आवश्यक हो तो आप Aspose.Cells द्वारा समर्थित अन्य प्रारूप चुन सकते हैं।

#### प्रश्न: मैं एक्सेल फ़ाइल में अन्य वर्कशीट तक कैसे पहुँच सकता हूँ?

 उ: आप इंडेक्स या शीट नाम का उपयोग करके अन्य वर्कशीट तक पहुंच सकते हैं, उदाहरण के लिए:`Worksheet worksheet = excel.Worksheets[1];` या`Worksheet worksheet = excel.Worksheets[" SheetName"];`.