---
title: चार्ट का आकार और स्थिति बदलें
linktitle: चार्ट का आकार और स्थिति बदलें
second_title: Aspose.Cells .NET एक्सेल प्रोसेसिंग API
description: इस आसान-से-अनुसरण गाइड के साथ .NET के लिए Aspose.Cells का उपयोग करके Excel में चार्ट के आकार और स्थिति को बदलना सीखें।
type: docs
weight: 11
url: /hi/net/advanced-chart-operations/change-chart-size-and-position/
---
## परिचय

जब स्प्रेडशीट को प्रोग्रामेटिक रूप से मैनिपुलेट करने की बात आती है, तो .NET के लिए Aspose.Cells की बहुमुखी प्रतिभा और शक्ति को अनदेखा करना मुश्किल है। क्या आपने कभी खुद को अपनी एक्सेल फ़ाइलों में चार्ट का आकार बदलने या फिर से स्थान बदलने में संघर्ष करते हुए पाया है? अगर ऐसा है, तो आपके लिए एक बेहतरीन मौका है! यह गाइड आपको Aspose.Cells का उपयोग करके अपनी स्प्रेडशीट में चार्ट के आकार और स्थिति को बदलने के लिए चौंका देने वाले सरल चरणों से गुज़ारेगी। तैयार हो जाइए, क्योंकि हम इस विषय पर गहराई से चर्चा करने जा रहे हैं!

## आवश्यक शर्तें

इससे पहले कि हम कोडिंग और चार्ट मैनिपुलेशन की बारीकियों में कूदें, आइए कुछ पूर्वापेक्षाएँ स्पष्ट करें। एक ठोस आधार आपकी यात्रा को आसान और अधिक सुखद बना देगा।

### C# का बुनियादी ज्ञान
- C# प्रोग्रामिंग भाषा से परिचित होना बहुत ज़रूरी है। अगर आप C# सिंटैक्स को समझ सकते हैं, तो आप पहले से ही एक कदम आगे हैं!

### .NET लाइब्रेरी के लिए Aspose.Cells
-  आपको Aspose.Cells लाइब्रेरी इंस्टॉल करनी होगी। अगर आपके पास अभी तक यह नहीं है, तो परेशान न हों! आप इसे आसानी से डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cells/net/).

### विकास पर्यावरण
- अपना विकास वातावरण (जैसे विजुअल स्टूडियो) स्थापित करें जहां आप अपना C# कोड निर्बाध रूप से लिख और निष्पादित कर सकें।

### चार्ट के साथ एक्सेल फ़ाइल
- इस ट्यूटोरियल के लिए कम से कम एक चार्ट वाली एक्सेल फाइल का होना उपयोगी होगा, जिसे हम संशोधित कर सकें।

एक बार जब आप अपनी सूची से इन पूर्व-आवश्यकताओं को चिह्नित कर लेते हैं, तो आप एक पेशेवर की तरह चार्ट का आकार और स्थिति बदलना सीख जाएंगे!

## पैकेज आयात करें

अब जब हम सब सेट अप कर चुके हैं, तो चलिए आवश्यक पैकेज आयात करते हैं। यह चरण महत्वपूर्ण है क्योंकि यह हमें एक्सेल फ़ाइलों में हेरफेर करने के लिए आवश्यक Aspose.Cells क्लासेस और विधियों तक पहुँचने की अनुमति देता है।

```csharp
using System;
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Charts;
```

ये कथन संकलक को यह बताते हैं कि हम Aspose.Cells लाइब्रेरी से क्लासेस का उपयोग करेंगे। सुनिश्चित करें कि आपके कोड के शीर्ष पर यह हो ताकि बाद में किसी परेशानी से बचा जा सके!

अब, आइए इस प्रक्रिया को प्रबंधनीय चरणों में विभाजित करें। हम चरण दर चरण आगे बढ़ेंगे, यह सुनिश्चित करते हुए कि सब कुछ बिल्कुल स्पष्ट है।

## चरण 1: स्रोत और आउटपुट निर्देशिकाएँ परिभाषित करें

```csharp
string sourceDir = "Your Document Directory";
string outputDir = "Your Output Directory";
```

सबसे पहले, हमें यह परिभाषित करने की आवश्यकता है कि हमारी स्रोत फ़ाइल कहाँ स्थित है और हम आउटपुट फ़ाइल को कहाँ सहेजना चाहते हैं। "आपकी दस्तावेज़ निर्देशिका" और "आपकी आउटपुट निर्देशिका" को अपने वास्तविक फ़ोल्डर पथों से बदलें। इन निर्देशिकाओं को अपने होम बेस और लॉन्चपैड के रूप में सोचें जहाँ आपकी फ़ाइलें रहती हैं।

## चरण 2: कार्यपुस्तिका लोड करें

```csharp
Workbook workbook = new Workbook(sourceDir + "sampleChangeChartSizeAndPosition.xlsx");
```

 यहाँ, हम एक नया उदाहरण बनाते हैं`Workbook` क्लास में जाकर उसमें अपनी एक्सेल फाइल लोड करें। वर्कबुक को एक डिजिटल नोटबुक के रूप में कल्पना करें जिसमें आपकी सभी शीट और चार्ट शामिल हों। हम जो पैरामीटर पास कर रहे हैं वह हमारी एक्सेल फाइल का पूरा पथ है, इसलिए सुनिश्चित करें कि इसमें फ़ाइल का नाम शामिल हो!

## चरण 3: वर्कशीट तक पहुंचें

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

 अब जबकि हमारी कार्यपुस्तिका लोड हो गई है, हमें उस विशिष्ट कार्यपत्रक तक पहुंचने की आवश्यकता है जिसके साथ हम काम करना चाहते हैं, जो इस मामले में पहली कार्यपत्रक (इंडेक्स) है`[0]`) किसी पुस्तक के सही पृष्ठ पर जाने की तरह, यह चरण हमें अपने संपादन के लिए वांछित शीट पर ध्यान केंद्रित करने में मदद करता है।

## चरण 4: चार्ट लोड करें

```csharp
Chart chart = worksheet.Charts[0];
```

वर्कशीट प्राप्त होने के बाद, हम सीधे चार्ट तक पहुँचते हैं! हम पहला चार्ट (फिर से, इंडेक्स) ले रहे हैं`[0]`)। यह उस कलाकृति का चयन करने जैसा है जिसे आप सजाना चाहते हैं। सुनिश्चित करें कि आपका चार्ट उस वर्कशीट में मौजूद है, अन्यथा आप अपना सिर खुजाते रह जाएँगे!

## चरण 5: चार्ट का आकार बदलें

```csharp
chart.ChartObject.Width = 400;
chart.ChartObject.Height = 300;
```

 अब चार्ट के आयाम बदलने का समय आ गया है! यहाँ, हम चौड़ाई को इस प्रकार सेट कर रहे हैं`400` पिक्सेल और ऊंचाई`300` पिक्सेल। आकार को समायोजित करना आपकी कलाकृति के लिए सही फ्रेम चुनने के समान है - बहुत बड़ा या बहुत छोटा, और यह कमरे में ठीक से फिट नहीं होगा।

## चरण 6: चार्ट को पुनः स्थानित करें

```csharp
chart.ChartObject.X = 250;
chart.ChartObject.Y = 150;
```

 अब जब हमारे पास सही आकार है, तो चलिए चार्ट को आगे बढ़ाते हैं!`X` और`Y` गुण, हम अनिवार्य रूप से वर्कशीट पर चार्ट को पुनः स्थान दे रहे हैं। इसे अपने फ़्रेमयुक्त चित्र को दीवार पर एक नए स्थान पर खींचकर उसकी सुंदरता को बेहतर ढंग से प्रदर्शित करने के रूप में सोचें!

## चरण 7: कार्यपुस्तिका सहेजें

```csharp
workbook.Save(outputDir + "outputChangeChartSizeAndPosition.xlsx");
```

अंत में, हम अपने परिवर्तनों को एक नई एक्सेल फ़ाइल में सहेजते हैं। चीजों को व्यवस्थित रखने के लिए निर्यात की गई फ़ाइल के लिए एक उपयुक्त नाम निर्दिष्ट करें। यह फर्नीचर को इधर-उधर करने के बाद अपने खूबसूरती से व्यवस्थित कमरे का स्नैपशॉट लेने जैसा है - नए लेआउट को संरक्षित करना!

## चरण 8: सफलता की पुष्टि करें

```csharp
Console.WriteLine("ChangeChartSizeAndPosition executed successfully.");
```

काम को अच्छी तरह से निपटाने के लिए, हम इस बारे में फीडबैक देते हैं कि ऑपरेशन सफलतापूर्वक पूरा हुआ या नहीं। यह एक बढ़िया अभ्यास है, जो आपको अपने काम पर स्पष्ट और आत्मविश्वास से भरा समापन देता है - ठीक वैसे ही जैसे फर्नीचर को फिर से व्यवस्थित करने के बाद अपने काम की प्रशंसा करना!

## निष्कर्ष

बधाई हो! आपने अभी सीखा है कि .NET के लिए Aspose.Cells का उपयोग करके Excel में चार्ट का आकार और स्थिति कैसे बदलें। इन चरणों के साथ, आप अपने चार्ट को न केवल बेहतर बना सकते हैं बल्कि अपनी स्प्रेडशीट में भी पूरी तरह से फिट कर सकते हैं, जिसके परिणामस्वरूप आपके डेटा की अधिक पेशेवर प्रस्तुति होगी। क्यों न इसे आजमाएं और आज ही अपने चार्ट में हेरफेर करना शुरू करें? 

## अक्सर पूछे जाने वाले प्रश्न

### .NET के लिए Aspose.Cells क्या है?  
Aspose.Cells for .NET एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को .NET अनुप्रयोगों में Excel फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने की अनुमति देती है।

### क्या मुझे Aspose.Cells का उपयोग करने के लिए लाइसेंस की आवश्यकता है?  
 वैसे तो आप Aspose.Cells को मुफ़्त में आज़मा सकते हैं, लेकिन उत्पादन अनुप्रयोगों में इसके निरंतर उपयोग के लिए लाइसेंस की आवश्यकता होती है। आप इसे प्राप्त कर सकते हैं[यहाँ](https://purchase.aspose.com/buy).

### क्या मैं Visual Studio के बिना Aspose.Cells का उपयोग कर सकता हूँ?  
हां, आप किसी भी .NET-संगत IDE में Aspose.Cells का उपयोग कर सकते हैं, लेकिन Visual Studio ऐसे उपकरण प्रदान करता है जो विकास को आसान बनाते हैं।

### मैं Aspose.Cells के लिए समर्थन कैसे प्राप्त कर सकता हूं?  
 आप उनके समर्पित में समर्थन पा सकते हैं[सहयता मंच](https://forum.aspose.com/c/cells/9).

### क्या कोई अस्थायी लाइसेंस उपलब्ध है?  
 हां, आप छोटी अवधि के लिए Aspose.Cells का मूल्यांकन करने के लिए एक अस्थायी लाइसेंस प्राप्त कर सकते हैं, जो उपलब्ध है[यहाँ](https://purchase.aspose.com/temporary-license/).