---
title: अन्य वर्कबुक से एक्सेल कॉपी वर्कशीट
linktitle: अन्य वर्कबुक से एक्सेल कॉपी वर्कशीट
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके एक्सेल वर्कशीट को एक वर्कबुक से दूसरे में आसानी से कॉपी करें।
type: docs
weight: 10
url: /hi/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
इस ट्यूटोरियल में, हम आपको .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके किसी अन्य वर्कबुक से एक्सेल वर्कशीट को कॉपी करने के चरणों के बारे में बताएंगे। इस कार्य को पूरा करने के लिए नीचे दिए गए निर्देशों का पालन करें।

## चरण 1: तैयारी

शुरू करने से पहले, सुनिश्चित करें कि आपने .NET के लिए Aspose.Cells इंस्टॉल कर लिया है और अपने पसंदीदा एकीकृत विकास वातावरण (IDE) में एक C# प्रोजेक्ट बनाया है।

## चरण 2: दस्तावेज़ निर्देशिका पथ सेट करें

 घोषित करें ए`dataDir` वैरिएबल बनाएं और इसे अपने दस्तावेज़ निर्देशिका के पथ के साथ प्रारंभ करें। उदाहरण के लिए :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 प्रतिस्थापित करना सुनिश्चित करें`"YOUR_DOCUMENTS_DIRECTORY"` आपकी निर्देशिका के वास्तविक पथ के साथ।

## चरण 3: एक नई एक्सेल वर्कबुक बनाएं

 उपयोग`Workbook` एक नई एक्सेल वर्कबुक बनाने के लिए Aspose.Cells से कक्षा:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## चरण 4: कार्यपुस्तिका में पहली वर्कशीट प्राप्त करें

इंडेक्स 0 का उपयोग करके कार्यपुस्तिका में पहली वर्कशीट पर जाएँ:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## चरण 5: हेडर पंक्तियों में डेटा जोड़ें (A1:A4)

 का उपयोग करो`for` हेडर पंक्तियों में डेटा जोड़ने के लिए लूप (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## चरण 6: विस्तृत डेटा जोड़ें (A5:A999)

 दूसरे का प्रयोग करें`for` विस्तृत डेटा जोड़ने के लिए लूप (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## चरण 7: लेआउट विकल्प सेट करें

 का उपयोग करके वर्कशीट के लिए पेज सेटअप विकल्प सेट करें`PageSetup` वस्तु:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## चरण 8: एक अन्य एक्सेल वर्कबुक बनाएं

एक अन्य एक्सेल वर्कबुक बनाएं:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## चरण 9: दूसरी वर्कबुक से पहली वर्कशीट प्राप्त करें

दूसरी कार्यपुस्तिका में पहली कार्यपत्रक पर जाएँ:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## चरण 10: वर्कशीट को नाम दें

आग का नाम बताओ

गणना द्वीप:

```csharp
ws1.Name = "MySheet";
```

## चरण 11: पहली वर्कबुक की पहली वर्कशीट से डेटा को दूसरी वर्कबुक की पहली वर्कशीट में कॉपी करें

पहली वर्कबुक की पहली वर्कशीट से डेटा को दूसरी वर्कबुक की पहली वर्कशीट में कॉपी करें:

```csharp
ws1.Copy(ws0);
```

## चरण 12: एक्सेल फ़ाइल सहेजें

एक्सेल फ़ाइल सहेजें:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

आउटपुट फ़ाइल के लिए वांछित पथ और फ़ाइल नाम निर्दिष्ट करना सुनिश्चित करें।

### .NET के लिए Aspose.Cells का उपयोग करके अन्य वर्कबुक से एक्सेल कॉपी वर्कशीट के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// एक नई कार्यपुस्तिका बनाएँ.
Workbook excelWorkbook0 = new Workbook();
// पुस्तक में पहली वर्कशीट प्राप्त करें.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// हेडर पंक्तियों में कुछ डेटा डालें (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// कुछ विस्तृत डेटा डालें (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// पहली वर्कशीट के आधार पर पेजसेटअप ऑब्जेक्ट को परिभाषित करें।
PageSetup pagesetup = ws0.PageSetup;
// प्रत्येक पृष्ठ में पहली पाँच पंक्तियाँ दोहराई जाती हैं...
// इसे प्रिंट प्रीव्यू में देखा जा सकता है.
pagesetup.PrintTitleRows = "$1:$5";
// एक अन्य कार्यपुस्तिका बनाएँ.
Workbook excelWorkbook1 = new Workbook();
// पुस्तक में पहली वर्कशीट प्राप्त करें.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// वर्कशीट को नाम दें.
ws1.Name = "MySheet";
// पहली वर्कबुक की पहली वर्कशीट से डेटा कॉपी करें
// दूसरी वर्कबुक की पहली वर्कशीट.
ws1.Copy(ws0);
// एक्सेल फ़ाइल सहेजें.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## निष्कर्ष

बधाई हो! अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल वर्कशीट को किसी अन्य वर्कबुक से कैसे कॉपी किया जाए। एक्सेल फ़ाइलों में कुशलतापूर्वक हेरफेर करने के लिए अपनी परियोजनाओं में इस पद्धति का उपयोग करने के लिए स्वतंत्र महसूस करें।

### पूछे जाने वाले प्रश्न

#### प्र. .NET के लिए Aspose.Cells का उपयोग करने के लिए किन पुस्तकालयों की आवश्यकता है?

A. .NET के लिए Aspose.Cells का उपयोग करने के लिए, आपको अपने प्रोजेक्ट में Aspose.Cells लाइब्रेरी को शामिल करना होगा। सुनिश्चित करें कि आपने अपने एकीकृत विकास परिवेश (आईडीई) में इस लाइब्रेरी को सही ढंग से संदर्भित किया है।

#### प्र. क्या Aspose.Cells XLSX जैसे अन्य Excel फ़ाइल स्वरूपों का समर्थन करता है?

A. हां, Aspose.Cells XLSX, XLS, CSV, HTML और कई अन्य सहित विभिन्न एक्सेल फ़ाइल स्वरूपों का समर्थन करता है। आप .NET के लिए Aspose.Cells की सुविधाओं का उपयोग करके इन फ़ाइल स्वरूपों में हेरफेर कर सकते हैं।

#### प्र. क्या मैं वर्कशीट की प्रतिलिपि बनाते समय लेआउट विकल्पों को अनुकूलित कर सकता हूँ?

A.  हाँ, आप कार्यपत्रक की प्रतिलिपि बनाते समय इसके गुणों का उपयोग करके पृष्ठ सेटअप विकल्पों को अनुकूलित कर सकते हैं`PageSetup` वस्तु। आप पेज हेडर, फ़ूटर, मार्जिन, ओरिएंटेशन आदि निर्दिष्ट कर सकते हैं।