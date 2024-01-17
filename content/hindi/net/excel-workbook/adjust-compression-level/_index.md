---
title: संपीड़न स्तर समायोजित करें
linktitle: संपीड़न स्तर समायोजित करें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ संपीड़न स्तर को समायोजित करके अपनी Excel कार्यपुस्तिकाओं का आकार कम करें।
type: docs
weight: 50
url: /hi/net/excel-workbook/adjust-compression-level/
---
इस चरण-दर-चरण ट्यूटोरियल में, हम दिए गए C# स्रोत कोड की व्याख्या करेंगे जो आपको .NET के लिए Aspose.Cells का उपयोग करके संपीड़न स्तर को समायोजित करने की अनुमति देगा। अपनी Excel कार्यपुस्तिका में संपीड़न स्तर को समायोजित करने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: स्रोत और आउटपुट निर्देशिका सेट करें

```csharp
// स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
// उत्पादन निर्देशिका
string outDir = RunExamples.Get_OutputDirectory();
```

इस पहले चरण में, हम एक्सेल फ़ाइलों के लिए स्रोत और आउटपुट निर्देशिकाओं को परिभाषित करते हैं।

## चरण 2: एक्सेल वर्कबुक लोड करें

```csharp
// एक्सेल वर्कबुक लोड करें
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

हम एक्सेल वर्कबुक को निर्दिष्ट फ़ाइल से लोड करते हैं`Workbook` Aspose.Cells से कक्षा।

## चरण 3: बैकअप विकल्प सेट करें

```csharp
// बैकअप विकल्पों को परिभाषित करें
XlsbSaveOptions options = new XlsbSaveOptions();
```

 हम इसका एक उदाहरण बनाते हैं`XlsbSaveOptions` सेव विकल्प सेट करने के लिए क्लास।

## चरण 4: संपीड़न स्तर समायोजित करें (स्तर 1)

```csharp
// संपीड़न स्तर समायोजित करें (स्तर 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 हम सेटिंग द्वारा संपीड़न स्तर को समायोजित करते हैं`CompressionType` को`Level1`. फिर हम एक्सेल वर्कबुक को इस निर्दिष्ट संपीड़न विकल्प के साथ सहेजते हैं।

## चरण 5: संपीड़न स्तर समायोजित करें (स्तर 6)

```csharp
// संपीड़न स्तर समायोजित करें (स्तर 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 हम संपीड़न स्तर को समायोजित करने के लिए प्रक्रिया को दोहराते हैं`Level6` और इस विकल्प के साथ एक्सेल वर्कबुक को सेव करें।

## चरण 6: संपीड़न स्तर समायोजित करें (स्तर 9)

```csharp
// संपीड़न स्तर समायोजित करें (स्तर 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 हम संपीड़न स्तर को समायोजित करने के लिए प्रक्रिया को आखिरी बार दोहराते हैं`Level9` और इस विकल्प के साथ एक्सेल वर्कबुक को सेव करें।

### .NET के लिए Aspose.Cells का उपयोग करके संपीड़न स्तर को समायोजित करने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## निष्कर्ष

बधाई हो! आपने सीखा कि .NET के लिए Aspose.Cells का उपयोग करके Excel कार्यपुस्तिका में संपीड़न स्तर को कैसे समायोजित किया जाए। जो आपकी आवश्यकताओं के लिए सबसे उपयुक्त हो उसे खोजने के लिए संपीड़न के विभिन्न स्तरों के साथ प्रयोग करें।

### पूछे जाने वाले प्रश्न

#### प्रश्न: एक्सेल वर्कबुक में कम्प्रेशन क्या है?

उ: एक्सेल वर्कबुक में संपीड़न संपीड़न एल्गोरिदम का उपयोग करके फ़ाइल आकार को कम करने की एक प्रक्रिया है। इससे आवश्यक भंडारण स्थान कम हो जाता है और फ़ाइल को लोड और हेरफेर करते समय प्रदर्शन में सुधार होता है।

#### प्रश्न: Aspose.Cells के साथ संपीड़न के कौन से स्तर उपलब्ध हैं?

उत्तर: Aspose.Cells के साथ, आप संपीड़न स्तर को 1 से 9 तक समायोजित कर सकते हैं। संपीड़न स्तर जितना अधिक होगा, फ़ाइल का आकार उतना ही छोटा होगा, लेकिन यह प्रसंस्करण समय भी बढ़ा सकता है।

#### प्रश्न: मैं अपनी एक्सेल वर्कबुक के लिए सही संपीड़न स्तर कैसे चुनूं?

उ: संपीड़न स्तर का चुनाव आपकी विशिष्ट आवश्यकताओं पर निर्भर करता है। यदि आप अधिकतम संपीड़न चाहते हैं और प्रसंस्करण समय कोई समस्या नहीं है, तो आप स्तर 9 पर जा सकते हैं। यदि आप फ़ाइल आकार और प्रसंस्करण समय के बीच समझौता पसंद करते हैं, तो आप एक मध्यवर्ती स्तर चुन सकते हैं।

#### प्रश्न: क्या संपीड़न Excel कार्यपुस्तिका में डेटा गुणवत्ता को प्रभावित करता है?

उ: नहीं, संपीड़न Excel कार्यपुस्तिका में डेटा गुणवत्ता को प्रभावित नहीं करता है। यह डेटा को बदले बिना संपीड़न तकनीकों का उपयोग करके फ़ाइल का आकार कम कर देता है।

#### प्रश्न: क्या मैं एक्सेल फ़ाइल को सहेजने के बाद संपीड़न स्तर को समायोजित कर सकता हूँ?

उ: नहीं, एक बार जब आप एक्सेल फ़ाइल को एक विशिष्ट संपीड़न स्तर के साथ सहेज लेते हैं, तो आप बाद में संपीड़न स्तर को समायोजित नहीं कर सकते। यदि आप इसे संशोधित करना चाहते हैं तो आपको फ़ाइल को नए संपीड़न स्तर के साथ फिर से सहेजना होगा।