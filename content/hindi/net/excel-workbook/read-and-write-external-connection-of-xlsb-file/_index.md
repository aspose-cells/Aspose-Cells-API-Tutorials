---
title: एक्सएलएसबी फ़ाइल का बाहरी कनेक्शन पढ़ें और लिखें
linktitle: एक्सएलएसबी फ़ाइल का बाहरी कनेक्शन पढ़ें और लिखें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके XLSB फ़ाइल के बाहरी कनेक्शन को पढ़ने और संशोधित करने का तरीका जानें।
type: docs
weight: 130
url: /hi/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
आपकी एक्सेल कार्यपुस्तिकाओं में बाहरी स्रोतों से डेटा में हेरफेर करने के लिए एक्सएलएसबी फ़ाइल में बाहरी कनेक्शन को पढ़ना और लिखना आवश्यक है। .NET के लिए Aspose.Cells के साथ आप निम्नलिखित चरणों का उपयोग करके बाहरी कनेक्शन को आसानी से पढ़ और लिख सकते हैं:

## चरण 1: स्रोत निर्देशिका और आउटपुट निर्देशिका निर्दिष्ट करें

सबसे पहले, आपको स्रोत निर्देशिका निर्दिष्ट करनी होगी जहां बाहरी कनेक्शन वाली एक्सएलएसबी फ़ाइल स्थित है, साथ ही आउटपुट निर्देशिका जहां आप संशोधित फ़ाइल को सहेजना चाहते हैं। Aspose.Cells का उपयोग करके इसे कैसे करें यहां बताया गया है:

```csharp
// स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();

// उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
```

## चरण 2: स्रोत एक्सेल XLSB फ़ाइल लोड करें

इसके बाद, आपको स्रोत एक्सेल XLSB फ़ाइल को लोड करना होगा, जिस पर आप बाहरी कनेक्शन पढ़ने और लिखने का संचालन करना चाहते हैं। यहाँ एक नमूना कोड है:

```csharp
// स्रोत एक्सेल XLSB फ़ाइल लोड करें
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## चरण 3: बाहरी कनेक्शन को पढ़ें और संशोधित करें

फ़ाइल लोड करने के बाद, आप पहले बाहरी कनेक्शन तक पहुंच सकते हैं जो वास्तव में एक डेटाबेस कनेक्शन है। आप बाहरी कनेक्शन के विभिन्न गुणों को पढ़ और संशोधित कर सकते हैं। ऐसे:

```csharp
// पहला बाहरी कनेक्शन पढ़ें जो एक डेटाबेस कनेक्शन है
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// डेटाबेस कनेक्शन नाम, कमांड और कनेक्शन जानकारी प्रदर्शित करें
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// कनेक्शन का नाम संशोधित करें
dbCon.Name = "NewCustomer";
```

## चरण 4: आउटपुट एक्सेल XLSB फ़ाइल सहेजें

एक बार जब आप आवश्यक परिवर्तन कर लेते हैं, तो आप संशोधित एक्सेल एक्सएलएसबी फ़ाइल को निर्दिष्ट आउटपुट निर्देशिका में सहेज सकते हैं। इसे करने का तरीका यहां बताया गया है:

```csharp
// आउटपुट Excel XLSB फ़ाइल सहेजें
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### .NET के लिए Aspose.Cells का उपयोग करके XLSB फ़ाइल के बाहरी कनेक्शन को पढ़ने और लिखने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
//उत्पादन निर्देशिका
string outputDir = RunExamples.Get_OutputDirectory();
//स्रोत एक्सेल Xlsb फ़ाइल लोड करें
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//पहला बाहरी कनेक्शन पढ़ें जो वास्तव में एक डीबी-कनेक्शन है
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//डीबी-कनेक्शन का नाम, कमांड और कनेक्शन जानकारी प्रिंट करें
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//कनेक्शन नाम संशोधित करें
dbCon.Name = "NewCust";
//एक्सेल एक्सएलएसबी फ़ाइल सहेजें
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## निष्कर्ष

एक्सएलएसबी फ़ाइल में बाहरी कनेक्शन को पढ़ने और लिखने से आप अपनी एक्सेल वर्कबुक में बाहरी स्रोतों से डेटा में हेरफेर कर सकते हैं। .NET के लिए Aspose.Cells के साथ, आप आसानी से बाहरी कनेक्शन तक पहुंच सकते हैं, कनेक्शन जानकारी पढ़ और संशोधित कर सकते हैं और परिवर्तनों को सहेज सकते हैं। अपनी खुद की एक्सएलएसबी फाइलों के साथ प्रयोग करें और अपने एक्सेल अनुप्रयोगों में बाहरी कनेक्शन की शक्ति का उपयोग करें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: एक्सएलएसबी फ़ाइल में बाहरी कनेक्शन क्या है?
    
ए: एक्सएलएसबी फ़ाइल में एक बाहरी कनेक्शन डेटाबेस जैसे बाहरी डेटा स्रोत के साथ स्थापित कनेक्शन को संदर्भित करता है। यह आपको इस बाहरी स्रोत से एक्सेल वर्कबुक में डेटा आयात करने की अनुमति देता है।

#### प्रश्न: क्या मैं XLSB फ़ाइल में एकाधिक बाहरी कनेक्शन रख सकता हूँ?
     
उ: हाँ, आप एक एक्सएलएसबी फ़ाइल में एकाधिक बाहरी कनेक्शन रख सकते हैं। आप प्रत्येक कनेक्शन ऑब्जेक्ट तक पहुंच कर उन्हें व्यक्तिगत रूप से प्रबंधित कर सकते हैं।

#### प्रश्न: मैं Aspose.Cells के साथ XLSB फ़ाइल में बाहरी कनेक्शन का विवरण कैसे पढ़ सकता हूं?
     
उ: आप बाहरी कनेक्शन के गुणों, जैसे कनेक्शन नाम, संबंधित कमांड और कनेक्शन जानकारी तक पहुंचने के लिए Aspose.Cells द्वारा प्रदान की गई कार्यक्षमता का उपयोग कर सकते हैं।

#### प्रश्न: क्या Aspose.Cells के साथ XLSB फ़ाइल में बाहरी कनेक्शन को संशोधित करना संभव है?
     
उ: हाँ, आप अपनी विशिष्ट आवश्यकताओं को पूरा करने के लिए किसी बाहरी कनेक्शन के गुणों, जैसे कनेक्शन नाम, को संशोधित कर सकते हैं। Aspose.Cells ये परिवर्तन करने के लिए तरीके प्रदान करता है।

#### प्रश्न: मैं Aspose.Cells के साथ बाहरी कनेक्शन में किए गए परिवर्तनों को XLSB फ़ाइल में कैसे सहेज सकता हूं?
     
उ: एक बार जब आप बाहरी कनेक्शन में आवश्यक परिवर्तन कर लेते हैं, तो आप Aspose.Cells द्वारा प्रदान की गई उचित विधि का उपयोग करके संशोधित Excel XLSB फ़ाइल को आसानी से सहेज सकते हैं।