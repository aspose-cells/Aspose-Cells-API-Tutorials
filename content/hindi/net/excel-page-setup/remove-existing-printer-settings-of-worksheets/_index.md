---
title: वर्कशीट की मौजूदा प्रिंटर सेटिंग्स हटाएं
linktitle: वर्कशीट की मौजूदा प्रिंटर सेटिंग्स हटाएं
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ एक्सेल स्प्रेडशीट से मौजूदा प्रिंटर सेटिंग्स को हटाने का तरीका जानें।
type: docs
weight: 80
url: /hi/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
इस ट्यूटोरियल में, हम आपको चरण दर चरण बताएंगे कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल में वर्कशीट से मौजूदा प्रिंटर सेटिंग्स को कैसे हटाया जाए। हम प्रक्रिया को स्पष्ट करने के लिए C# स्रोत कोड का उपयोग करेंगे।

## चरण 1: वातावरण स्थापित करना

सुनिश्चित करें कि आपकी मशीन पर .NET के लिए Aspose.Cells स्थापित है। अपने पसंदीदा विकास परिवेश में एक नया प्रोजेक्ट भी बनाएं।

## चरण 2: आवश्यक पुस्तकालय आयात करें

अपनी कोड फ़ाइल में, Aspose.Cells के साथ काम करने के लिए आवश्यक लाइब्रेरी आयात करें। यहाँ संबंधित कोड है:

```csharp
using Aspose.Cells;
```

## चरण 3: स्रोत और आउटपुट निर्देशिका सेट करें

स्रोत और आउटपुट निर्देशिकाओं को सेट करें जहां मूल एक्सेल फ़ाइल स्थित है और जहां आप संशोधित फ़ाइल को क्रमशः सहेजना चाहते हैं। निम्नलिखित कोड का प्रयोग करें:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

पूर्ण निर्देशिका पथ निर्दिष्ट करना सुनिश्चित करें.

## चरण 4: स्रोत एक्सेल फ़ाइल लोड हो रही है

निम्नलिखित कोड का उपयोग करके स्रोत एक्सेल फ़ाइल लोड करें:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

यह निर्दिष्ट एक्सेल फ़ाइल को वर्कबुक ऑब्जेक्ट में लोड करेगा।

## चरण 5: कार्यपत्रकों को नेविगेट करें

एक लूप का उपयोग करके कार्यपुस्तिका में सभी कार्यपत्रकों को दोहराएँ। निम्नलिखित कोड का प्रयोग करें:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // बाकी कोड अगले चरण में जोड़ा जाएगा.
}
```

## चरण 6: मौजूदा प्रिंटर सेटिंग्स हटाएँ

जांचें कि क्या प्रत्येक वर्कशीट के लिए प्रिंटर सेटिंग्स मौजूद हैं और यदि आवश्यक हो तो उन्हें हटा दें। निम्नलिखित कोड का प्रयोग करें:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## चरण 7: संशोधित कार्यपुस्तिका को सहेजना

निम्नलिखित कोड का उपयोग करके संशोधित कार्यपुस्तिका सहेजें:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

यह संशोधित कार्यपुस्तिका को निर्दिष्ट आउटपुट निर्देशिका में सहेजेगा।

### .NET के लिए Aspose.Cells का उपयोग करके वर्कशीट की मौजूदा प्रिंटर सेटिंग्स को हटाने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
//उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
//स्रोत एक्सेल फ़ाइल लोड करें
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//कार्यपुस्तिका की शीट संख्या प्राप्त करें
int sheetCount = wb.Worksheets.Count;
//सभी शीटों को पुनरावृत्त करें
for (int i = 0; i < sheetCount; i++)
{
    //i-वें वर्कशीट तक पहुंचें
    Worksheet ws = wb.Worksheets[i];
    //वर्कशीट पेज सेटअप तक पहुंचें
    PageSetup ps = ws.PageSetup;
    //जांचें कि क्या इस वर्कशीट के लिए प्रिंटर सेटिंग्स मौजूद हैं
    if (ps.PrinterSettings != null)
    {
        //निम्नलिखित संदेश प्रिंट करें
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //प्रिंट शीट का नाम और उसके कागज का आकार
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //प्रिंटर सेटिंग्स को शून्य सेट करके हटाएँ
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//अगर
}//के लिए
//कार्यपुस्तिका सहेजें
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## निष्कर्ष

अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके एक्सेल में वर्कशीट से मौजूदा प्रिंटर सेटिंग्स को कैसे हटाया जाए। इस ट्यूटोरियल ने आपको पर्यावरण की स्थापना से लेकर स्प्रेडशीट के माध्यम से नेविगेट करने और प्रिंटर सेटिंग्स को साफ़ करने तक प्रक्रिया के हर चरण के बारे में बताया। अब आप इस ज्ञान का उपयोग अपनी एक्सेल फ़ाइलों में प्रिंटर सेटिंग्स को प्रबंधित करने के लिए कर सकते हैं।

### अक्सर पूछे जाने वाले प्रश्न

#### Q1: मुझे कैसे पता चलेगा कि स्प्रेडशीट में मौजूदा प्रिंटर सेटिंग्स हैं?

 A1: आप इस पर पहुंच कर जांच सकते हैं कि वर्कशीट के लिए प्रिंटर सेटिंग्स मौजूद हैं या नहीं`PrinterSettings` की संपत्ति`PageSetup` वस्तु। यदि मान शून्य नहीं है, तो इसका मतलब है कि मौजूदा प्रिंटर सेटिंग्स मौजूद हैं।

#### Q2: क्या मैं केवल विशिष्ट स्प्रेडशीट के लिए प्रिंटर सेटिंग्स हटा सकता हूँ?

 उ2: हां, आप किसी विशिष्ट वर्कशीट तक पहुंच कर प्रिंटर सेटिंग्स को हटाने के लिए उसी दृष्टिकोण का उपयोग कर सकते हैं`PageSetup` वस्तु।

#### Q3: क्या यह विधि अन्य लेआउट सेटिंग्स को भी हटा देती है?

उ3: नहीं, यह विधि केवल प्रिंटर सेटिंग्स को हटाती है। अन्य लेआउट सेटिंग्स, जैसे मार्जिन, पेपर ओरिएंटेशन, आदि अपरिवर्तित रहती हैं।

#### Q4: क्या यह विधि सभी Excel फ़ाइल स्वरूपों, जैसे .xls और .xlsx, के लिए काम करती है?

A4: हाँ, यह विधि .xls और .xlsx सहित Aspose.Cells द्वारा समर्थित सभी Excel फ़ाइल स्वरूपों के लिए काम करती है।

#### Q5: क्या प्रिंटर सेटिंग्स में किए गए परिवर्तन संपादित एक्सेल फ़ाइल में स्थायी हैं?

उ5: हां, प्रिंटर सेटिंग्स में परिवर्तन संपादित एक्सेल फ़ाइल में स्थायी रूप से सहेजे जाते हैं।