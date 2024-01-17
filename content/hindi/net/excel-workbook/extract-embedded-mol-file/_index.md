---
title: एंबेडेड मोल फ़ाइल निकालें
linktitle: एंबेडेड मोल फ़ाइल निकालें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके एक्सेल वर्कबुक से एम्बेडेड MOL फ़ाइलों को आसानी से निकालने का तरीका जानें।
type: docs
weight: 90
url: /hi/net/excel-workbook/extract-embedded-mol-file/
---
इस ट्यूटोरियल में, हम आपको चरण-दर-चरण बताएंगे कि .NET के लिए Aspose.Cells लाइब्रेरी का उपयोग करके एक्सेल वर्कबुक से एक एम्बेडेड MOL फ़ाइल कैसे निकालें। आप सीखेंगे कि वर्कबुक शीट कैसे ब्राउज़ करें, संबंधित OLE ऑब्जेक्ट कैसे निकालें और निकाली गई MOL फ़ाइलों को कैसे सहेजें। इस कार्य को सफलतापूर्वक पूरा करने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करें
सबसे पहले, हमें अपने कोड में स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करने की आवश्यकता है। ये निर्देशिकाएं बताती हैं कि स्रोत एक्सेल वर्कबुक कहां स्थित है और निकाली गई एमओएल फाइलें कहां सहेजी जाएंगी। यहाँ संबंधित कोड है:

```csharp
// निर्देशिका
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

आवश्यकतानुसार उचित पथ निर्दिष्ट करना सुनिश्चित करें।

## चरण 2: एक्सेल कार्यपुस्तिका लोड हो रही है
अगला चरण एम्बेडेड OLE ऑब्जेक्ट और MOL फ़ाइलों वाली Excel कार्यपुस्तिका को लोड करना है। कार्यपुस्तिका लोड करने के लिए कोड यहां दिया गया है:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

कोड में स्रोत फ़ाइल का नाम सही ढंग से निर्दिष्ट करना सुनिश्चित करें।

## चरण 3: शीटों को पार करें और एमओएल फ़ाइलें निकालें
अब हम कार्यपुस्तिका में प्रत्येक शीट के माध्यम से लूप करेंगे और संबंधित OLE ऑब्जेक्ट निकालेंगे, जिसमें MOL फ़ाइलें हैं। यहाँ संबंधित कोड है:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

यह कोड कार्यपुस्तिका में प्रत्येक शीट के माध्यम से लूप करता है, OLE ऑब्जेक्ट लाता है, और निकाली गई MOL फ़ाइलों को आउटपुट निर्देशिका में सहेजता है।

### .NET के लिए Aspose.Cells का उपयोग करके एंबेडेड मोल फ़ाइल निकालने के लिए नमूना स्रोत कोड 
```csharp
//निर्देशिका
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## निष्कर्ष
बधाई हो! आपने सीखा है कि .NET के लिए Aspose.Cells का उपयोग करके Excel कार्यपुस्तिका से एक एम्बेडेड MOL फ़ाइल कैसे निकाली जाती है। अब आप इस ज्ञान को अपनी Excel कार्यपुस्तिकाओं से MOL फ़ाइलें निकालने के लिए लागू कर सकते हैं। Aspose.Cells लाइब्रेरी को बेझिझक देखें और इसकी अन्य शक्तिशाली विशेषताओं के बारे में जानें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: एमओएल फ़ाइल क्या है?
 
ए: एमओएल फ़ाइल एक फ़ाइल प्रारूप है जिसका उपयोग कम्प्यूटेशनल रसायन विज्ञान में रासायनिक संरचनाओं का प्रतिनिधित्व करने के लिए किया जाता है। इसमें परमाणुओं, बंधों और अन्य आणविक गुणों के बारे में जानकारी शामिल है।

#### प्रश्न: क्या यह विधि सभी एक्सेल फ़ाइल प्रकारों के साथ काम करती है?

उत्तर: हाँ, यह विधि Aspose.Cells द्वारा समर्थित सभी Excel फ़ाइल प्रकारों के साथ काम करती है।

#### प्रश्न: क्या मैं एक साथ अनेक एमओएल फ़ाइलें निकाल सकता हूँ?

उत्तर: हाँ, आप कार्यपुस्तिका में प्रत्येक शीट पर OLE ऑब्जेक्ट के माध्यम से पुनरावृत्ति करके एक साथ कई MOL फ़ाइलें निकाल सकते हैं।