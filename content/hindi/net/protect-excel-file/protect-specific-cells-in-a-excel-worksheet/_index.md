---
title: एक्सेल वर्कशीट में विशिष्ट सेल को सुरक्षित रखें
linktitle: एक्सेल वर्कशीट में विशिष्ट सेल को सुरक्षित रखें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: जानें कि .NET के लिए Aspose.Cells के साथ Excel में विशिष्ट सेल की सुरक्षा कैसे करें। C# में चरण दर चरण ट्यूटोरियल।
type: docs
weight: 70
url: /hi/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
इस ट्यूटोरियल में, हम C# स्रोत कोड देखेंगे जो एक्सेल स्प्रेडशीट में विशिष्ट कोशिकाओं की सुरक्षा के लिए Aspose.Cells लाइब्रेरी का उपयोग करता है। हम कोड के प्रत्येक चरण पर चलेंगे और बताएंगे कि यह कैसे काम करता है। वांछित परिणाम प्राप्त करने के लिए निर्देशों का ध्यानपूर्वक पालन करें।

## चरण 1: पूर्वावश्यकताएँ

शुरू करने से पहले, सुनिश्चित करें कि आपने .NET के लिए Aspose.Cells लाइब्रेरी स्थापित कर ली है। आप इसे Aspose की आधिकारिक वेबसाइट से प्राप्त कर सकते हैं। यह भी सुनिश्चित करें कि आपके पास विज़ुअल स्टूडियो या किसी अन्य C# विकास वातावरण का नवीनतम संस्करण है।

## चरण 2: आवश्यक नामस्थान आयात करें

Aspose.Cells लाइब्रेरी का उपयोग करने के लिए, हमें अपने कोड में आवश्यक नेमस्पेस आयात करने की आवश्यकता है। अपनी C# स्रोत फ़ाइल के शीर्ष पर निम्नलिखित पंक्तियाँ जोड़ें:

```csharp
using Aspose.Cells;
```

## चरण 3: एक एक्सेल वर्कबुक बनाना

इस चरण में, हम एक नई एक्सेल वर्कबुक बनाएंगे। एक्सेल वर्कबुक बनाने के लिए निम्नलिखित कोड का उपयोग करें:

```csharp
// दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// एक नई कार्यपुस्तिका बनाएँ.
Workbook wb = new Workbook();
```

 प्रतिस्थापित करना सुनिश्चित करें`"YOUR_DOCUMENTS_DIR"` आपके दस्तावेज़ निर्देशिका के लिए उपयुक्त पथ के साथ।

## चरण 4: एक स्प्रेडशीट बनाना

अब जब हमने एक्सेल वर्कबुक बना ली है, तो आइए एक वर्कशीट बनाएं और पहली शीट प्राप्त करें। निम्नलिखित कोड का प्रयोग करें:

```csharp
// एक स्प्रेडशीट ऑब्जेक्ट बनाएं और पहली शीट प्राप्त करें।
Worksheet sheet = wb.Worksheets[0];
```

## चरण 5: शैली को परिभाषित करना

इस चरण में, हम विशिष्ट कोशिकाओं पर लागू करने के लिए शैली को परिभाषित करेंगे। निम्नलिखित कोड का प्रयोग करें:

```csharp
// शैली वस्तु की परिभाषा.
Styling styling;
```

## चरण 6: सभी कॉलमों को अनलॉक करने के लिए लूप करें

अब हम वर्कशीट में सभी कॉलमों को लूप करेंगे और उन्हें अनलॉक करेंगे। निम्नलिखित कोड का प्रयोग करें:

```csharp
// वर्कशीट में सभी कॉलमों को लूप करें और उन्हें अनलॉक करें।
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## चरण 7: विशिष्ट कोशिकाओं को लॉक करना

इस चरण में, हम विशिष्ट कोशिकाओं को लॉक कर देंगे। निम्नलिखित कोड का प्रयोग करें:

```csharp
//तीनों सेल लॉक हो रहे हैं... यानी A1, B1, C1।
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## चरण 8: वर्कशीट की सुरक्षा करना

अंत में, हम विशिष्ट कोशिकाओं को संशोधित होने से रोकने के लिए वर्कशीट की सुरक्षा करेंगे। निम्नलिखित कोड का प्रयोग करें:

```csharp
// वर्कशीट को सुरक्षित रखें.
sheet.Protect(ProtectionType.All);
```

## चरण 9: एक्सेल फ़ाइल को सहेजना

अब हम संशोधित एक्सेल फाइल को सेव करेंगे। निम्नलिखित कोड का प्रयोग करें:

```csharp
// एक्सेल फ़ाइल सहेजें.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

संशोधित एक्सेल फ़ाइल को सहेजने के लिए सही पथ निर्दिष्ट करना सुनिश्चित करें।

### .NET के लिए Aspose.Cells का उपयोग करके एक्सेल वर्कशीट में विशिष्ट कोशिकाओं को सुरक्षित रखने के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// यदि यह पहले से मौजूद नहीं है तो निर्देशिका बनाएं।
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// एक नई कार्यपुस्तिका बनाएँ.
Workbook wb = new Workbook();
// एक वर्कशीट ऑब्जेक्ट बनाएं और पहली शीट प्राप्त करें।
Worksheet sheet = wb.Worksheets[0];
// स्टाइल ऑब्जेक्ट को परिभाषित करें।
Style style;
// स्टाइलफ्लैग ऑब्जेक्ट को परिभाषित करें
StyleFlag styleflag;
// वर्कशीट में सभी कॉलमों को लूप करें और उन्हें अनलॉक करें।
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// तीन कोशिकाओं को लॉक करें...अर्थात A1, B1, C1।
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// अंत में, अब शीट को सुरक्षित रखें।
sheet.Protect(ProtectionType.All);
// एक्सेल फ़ाइल सहेजें.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## निष्कर्ष

बधाई हो! अब आपके पास C# स्रोत कोड है जो आपको .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल वर्कशीट में विशिष्ट कोशिकाओं की सुरक्षा करने की अनुमति देता है। अपनी विशिष्ट आवश्यकताओं के अनुरूप कोड को अनुकूलित करने के लिए स्वतंत्र महसूस करें।

### अक्सर पूछे जाने वाले प्रश्न (अक्सर पूछे जाने वाले प्रश्न)

#### क्या यह कोड एक्सेल के हाल के संस्करणों के साथ काम करता है?

हाँ, यह कोड Excel के हाल के संस्करणों के साथ काम करता है, जिसमें Excel 2010 और उससे ऊपर के प्रारूप की फ़ाइलें भी शामिल हैं।

#### क्या मैं A1, B1 और C1 के अलावा अन्य कोशिकाओं की सुरक्षा कर सकता हूँ?

हाँ, आप कोड की संगत पंक्तियों में सेल संदर्भों को समायोजित करके अन्य विशिष्ट सेल को लॉक करने के लिए कोड को संशोधित कर सकते हैं।

#### मैं बंद सेल को फिर से कैसे अनलॉक कर सकता हूं?

 आप उपयोग कर सकते हैं`SetStyle` विधि के साथ`IsLocked` करने के लिए सेट`false` कोशिकाओं को अनलॉक करने के लिए.

#### क्या मैं कार्यपुस्तिका में और कार्यपत्रक जोड़ सकता हूँ?

 हां, आप इसका उपयोग करके कार्यपुस्तिका में अन्य कार्यपत्रक जोड़ सकते हैं`Worksheets.Add()`विधि और प्रत्येक वर्कशीट के लिए सेल सुरक्षा चरणों को दोहराएं।

#### मैं एक्सेल फ़ाइल का सेव फॉर्मेट कैसे बदल सकता हूँ?

 आप इसका उपयोग करके सेव फॉर्मेट को बदल सकते हैं`SaveFormat` उदाहरण के लिए, वांछित प्रारूप वाली विधि`SaveFormat.Xlsx` Excel 2007 और बाद के संस्करण के लिए.