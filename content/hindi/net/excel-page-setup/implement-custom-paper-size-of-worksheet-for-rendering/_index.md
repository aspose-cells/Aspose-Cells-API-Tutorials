---
title: रेंडरिंग के लिए वर्कशीट का कस्टम पेपर आकार लागू करें
linktitle: रेंडरिंग के लिए वर्कशीट का कस्टम पेपर आकार लागू करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ कस्टम वर्कशीट आकार को लागू करने के लिए चरण-दर-चरण मार्गदर्शिका। आयाम सेट करें, एक संदेश जोड़ें और पीडीएफ के रूप में सहेजें।
type: docs
weight: 50
url: /hi/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
जब आप किसी विशिष्ट आकार के साथ एक पीडीएफ दस्तावेज़ बनाना चाहते हैं तो अपनी वर्कशीट के लिए एक कस्टम आकार लागू करना बहुत उपयोगी हो सकता है। इस ट्यूटोरियल में, हम सीखेंगे कि वर्कशीट के लिए कस्टम आकार सेट करने के लिए .NET के लिए Aspose.Cells का उपयोग कैसे करें और फिर दस्तावेज़ को पीडीएफ के रूप में सहेजें।

## चरण 1: आउटपुट फ़ोल्डर बनाना

शुरू करने से पहले, आपको एक आउटपुट फ़ोल्डर बनाना होगा जहां जेनरेट की गई पीडीएफ फाइल सहेजी जाएगी। आप अपने आउटपुट फ़ोल्डर के लिए जो भी पथ चाहें उसका उपयोग कर सकते हैं।

```csharp
// आउटपुट निर्देशिकाएँ
string outputDir = "YOUR_OUTPUT_FOLDER";
```

सुनिश्चित करें कि आपने अपने आउटपुट फ़ोल्डर के लिए सही पथ निर्दिष्ट किया है।

## चरण 2: कार्यपुस्तिका ऑब्जेक्ट बनाना

आरंभ करने के लिए, आपको Aspose.Cells का उपयोग करके एक वर्कबुक ऑब्जेक्ट बनाना होगा। यह ऑब्जेक्ट आपकी स्प्रैडशीट का प्रतिनिधित्व करता है।

```csharp
// वर्कबुक ऑब्जेक्ट बनाएं
Workbook wb = new Workbook();
```

## चरण 3: पहली वर्कशीट तक पहुंच

वर्कबुक ऑब्जेक्ट बनाने के बाद, आप इसके भीतर पहली वर्कशीट तक पहुंच सकते हैं।

```csharp
// पहली वर्कशीट तक पहुंच
Worksheet ws = wb.Worksheets[0];
```

## चरण 4: कस्टम वर्कशीट आकार सेट करना

 अब आप इसका उपयोग करके कस्टम वर्कशीट आकार सेट कर सकते हैं`CustomPaperSize(width, height)` पेजसेटअप क्लास की विधि।

```csharp
// कस्टम वर्कशीट आकार सेट करें (इंच में)
ws.PageSetup.CustomPaperSize(6, 4);
```

इस उदाहरण में, हमने वर्कशीट का आकार 6 इंच चौड़ा और 4 इंच ऊंचा निर्धारित किया है।

## चरण 5: सेल बी4 तक पहुंच

उसके बाद, हम वर्कशीट में एक विशिष्ट सेल तक पहुंच सकते हैं। इस स्थिति में, हम सेल B4 तक पहुंचेंगे।

```csharp
// सेल B4 तक पहुंच
Cell b4 = ws.Cells["B4"];
```

## चरण 6: सेल बी4 में संदेश जोड़ना

 अब हम इसका उपयोग करके सेल B4 में एक संदेश जोड़ सकते हैं`PutValue(value)` तरीका।

```csharp
// संदेश को सेल B4 में जोड़ें
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

इस उदाहरण में, हमने सेल B4 में "पीडीएफ पृष्ठ आकार: 6.00" x 4.00" संदेश जोड़ा है।

## चरण 7: वर्कशीट को पीडीएफ प्रारूप में सहेजना

 अंत में, हम इसका उपयोग करके वर्कशीट को पीडीएफ प्रारूप में सहेज सकते हैं`Save(filePath)` कार्यपुस्तिका ऑब्जेक्ट की विधि.

```csharp
// वर्कशीट को पीडीएफ फॉर्मेट में सेव करें
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

पहले बनाए गए आउटपुट फ़ोल्डर का उपयोग करके, जेनरेट की गई पीडीएफ फ़ाइल के लिए वांछित पथ निर्दिष्ट करें।

### .NET के लिए Aspose.Cells का उपयोग करके रेंडरिंग के लिए वर्कशीट के कस्टम पेपर आकार को लागू करने के लिए नमूना स्रोत कोड 
```csharp
//उत्पादन निर्देशिका
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//कार्यपुस्तिका ऑब्जेक्ट बनाएं
Workbook wb = new Workbook();
//पहली वर्कशीट तक पहुंचें
Worksheet ws = wb.Worksheets[0];
//इंच की इकाई में कस्टम पेपर आकार सेट करें
ws.PageSetup.CustomPaperSize(6, 4);
//एक्सेस सेल B4
Cell b4 = ws.Cells["B4"];
//संदेश को सेल B4 में जोड़ें
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//वर्कबुक को पीडीएफ फॉर्मेट में सेव करें
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## निष्कर्ष

इस ट्यूटोरियल में, आपने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके वर्कशीट के कस्टम आकार को कैसे लागू किया जाए। आप अपनी वर्कशीट के लिए विशिष्ट आयाम सेट करने के लिए इन चरणों का उपयोग कर सकते हैं और फिर दस्तावेज़ों को पीडीएफ प्रारूप में सहेज सकते हैं। हमें उम्मीद है कि यह मार्गदर्शिका कस्टम स्प्रेडशीट आकार को लागू करने की प्रक्रिया को समझने में सहायक रही होगी।

### अक्सर पूछे जाने वाले प्रश्न (FAQ)

#### प्रश्न 1: क्या मैं स्प्रेडशीट लेआउट को और अधिक अनुकूलित कर सकता हूँ?

हाँ, Aspose.Cells आपके वर्कशीट लेआउट को अनुकूलित करने के लिए कई विकल्प प्रदान करता है। आप कस्टम आयाम, पेज ओरिएंटेशन, मार्जिन, हेडर और फ़ुटर और बहुत कुछ सेट कर सकते हैं।

#### प्रश्न 2: Aspose.Cells अन्य किन आउटपुट स्वरूपों का समर्थन करता है?

Aspose.Cells PDF, XLSX, XLS, CSV, HTML, TXT और कई अन्य सहित कई अलग-अलग आउटपुट स्वरूपों का समर्थन करता है। आप अपनी आवश्यकताओं के अनुसार वांछित आउटपुट स्वरूप चुन सकते हैं।