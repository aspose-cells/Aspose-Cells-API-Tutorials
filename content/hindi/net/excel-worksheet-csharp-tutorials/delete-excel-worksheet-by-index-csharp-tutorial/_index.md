---
title: इंडेक्स सी# ट्यूटोरियल द्वारा एक्सेल वर्कशीट को हटाएं
linktitle: इंडेक्स द्वारा एक्सेल वर्कशीट हटाएं
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells का उपयोग करके किसी विशिष्ट Excel वर्कशीट को आसानी से हटाएं। कोड उदाहरणों के साथ विस्तृत ट्यूटोरियल।
type: docs
weight: 30
url: /hi/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-index-csharp-tutorial/
---
इस ट्यूटोरियल में, हम आपको नीचे दिए गए C# स्रोत कोड को चरण दर चरण समझाएंगे, जिसमें .NET के लिए Aspose.Cells का उपयोग करके एक एक्सेल वर्कशीट को हटाना है। प्रक्रिया को विस्तार से समझने में आपकी सहायता के लिए हम प्रत्येक चरण के लिए नमूना कोड शामिल करेंगे।

## चरण 1: दस्तावेज़ निर्देशिका को परिभाषित करें

आरंभ करने के लिए, आपको वह निर्देशिका पथ सेट करना होगा जहां आपकी एक्सेल फ़ाइल स्थित है। कोड में "आपकी दस्तावेज़ निर्देशिका" को अपनी एक्सेल फ़ाइल के वास्तविक पथ से बदलें।

```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## चरण 2: एक फ़ाइल स्ट्रीम बनाएं और एक्सेल फ़ाइल खोलें

 इसके बाद, आपको एक फ़ाइल स्ट्रीम बनाने और एक्सेल फ़ाइल को खोलने की आवश्यकता है`FileStream` कक्षा।

```csharp
// एक फ़ाइल स्ट्रीम बनाएं जिसमें खोलने के लिए एक्सेल फ़ाइल हो
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## चरण 3: किसी कार्यपुस्तिका ऑब्जेक्ट को इंस्टेंट करें

 एक्सेल फ़ाइल खोलने के बाद, आपको इंस्टेंटियेट करना होगा`Workbook`वस्तु। यह ऑब्जेक्ट एक्सेल वर्कबुक का प्रतिनिधित्व करता है और वर्कबुक में हेरफेर करने के लिए विभिन्न तरीकों और गुणों की पेशकश करता है।

```csharp
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करें
// फ़ाइल प्रवाह के माध्यम से एक्सेल फ़ाइल खोलें
Workbook workbook = new Workbook(fstream);
```

## चरण 4: इंडेक्स द्वारा वर्कशीट हटाएं

 किसी वर्कशीट को उसके इंडेक्स से हटाने के लिए, आप इसका उपयोग कर सकते हैं`RemoveAt()` की विधि`Worksheets` की वस्तु`Workbook` वस्तु। जिस कार्यपत्रक को आप हटाना चाहते हैं उसका सूचकांक एक पैरामीटर के रूप में पारित किया जाना चाहिए।

```csharp
// किसी वर्कशीट को उसके शीट इंडेक्स का उपयोग करके हटाएं
workbook.Worksheets.RemoveAt(0);
```

## चरण 5: कार्यपुस्तिका सहेजें

 एक बार जब आप वर्कशीट को हटा देते हैं, तो आप संशोधित एक्सेल वर्कबुक को इसका उपयोग करके सहेज सकते हैं`Save()` की विधि`Workbook` वस्तु।

```csharp
// एक्सेल वर्कबुक को सेव करें
workbook.Save(dataDir + "output.out.xls");
```


### .NET के लिए Aspose.Cells का उपयोग करके इंडेक्स C# ट्यूटोरियल द्वारा डिलीट एक्सेल वर्कशीट के लिए नमूना स्रोत कोड 
```csharp
//दस्तावेज़ निर्देशिका का पथ.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// एक फ़ाइल स्ट्रीम बनाना जिसमें एक्सेल फ़ाइल खोली जानी है
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// वर्कबुक ऑब्जेक्ट को इंस्टेंट करना
// फ़ाइल स्ट्रीम के माध्यम से एक्सेल फ़ाइल खोलना
Workbook workbook = new Workbook(fstream);
//किसी वर्कशीट को उसके शीट इंडेक्स का उपयोग करके हटाना
workbook.Worksheets.RemoveAt(0);
// कार्यपुस्तिका सहेजें
workbook.Save(dataDir + "output.out.xls");
```

## निष्कर्ष

इस ट्यूटोरियल में, हमने .NET के लिए Aspose.Cells का उपयोग करके इंडेक्स द्वारा एक्सेल वर्कशीट को हटाने की चरण-दर-चरण प्रक्रिया को कवर किया है। दिए गए कोड उदाहरणों और स्पष्टीकरणों का पालन करके, अब आपको यह अच्छी तरह से समझ में आ जाना चाहिए कि अपने C# अनुप्रयोगों में इस कार्य को कैसे करना है। .NET के लिए Aspose.Cells एक्सेल फ़ाइलों के साथ काम करने के लिए सुविधाओं का एक व्यापक सेट प्रदान करता है, जिससे आप वर्कशीट और संबंधित डेटा में आसानी से हेरफेर कर सकते हैं।

### अक्सर पूछे जाने वाले प्रश्न (FAQ)

#### .NET के लिए Aspose.Cells क्या है?

.NET के लिए Aspose.Cells एक शक्तिशाली लाइब्रेरी है जो डेवलपर्स को अपने .NET अनुप्रयोगों में Excel फ़ाइलों को बनाने, हेरफेर करने और परिवर्तित करने की अनुमति देती है। यह वर्कशीट, सेल, फ़ॉर्मूले, शैलियों और बहुत कुछ के साथ काम करने के लिए सुविधाओं की एक विस्तृत श्रृंखला प्रदान करता है।

#### मैं .NET के लिए Aspose.Cells कैसे स्थापित कर सकता हूँ?

.NET के लिए Aspose.Cells को स्थापित करने के लिए, आप Aspose विज्ञप्ति से इंस्टॉलेशन पैकेज डाउनलोड कर सकते हैं (https://releases.aspose.com/सेल्स/नेट) और दिए गए निर्देशों का पालन करें। आपको अपने एप्लिकेशन में लाइब्रेरी का उपयोग करने के लिए एक वैध लाइसेंस की आवश्यकता होगी।

#### क्या मैं एक साथ कई वर्कशीट हटा सकता हूँ?

हां, आप .NET के लिए Aspose.Cells का उपयोग करके एकाधिक वर्कशीट हटा सकते हैं। आप जिस भी वर्कशीट को हटाना चाहते हैं उसके लिए आप डिलीट चरण को दोहरा सकते हैं।

#### क्या हटाए गए वर्कशीट को पुनर्प्राप्त करना संभव है?

दुर्भाग्य से, एक बार वर्कशीट हटा दिए जाने के बाद, इसे सीधे एक्सेल फ़ाइल से पुनर्प्राप्त नहीं किया जा सकता है। डेटा हानि से बचने के लिए वर्कशीट को हटाने से पहले अपनी एक्सेल फ़ाइल का बैकअप बनाने की अनुशंसा की जाती है।

#### क्या .NET के लिए Aspose.Cells एक्सेल के विभिन्न संस्करणों के साथ संगत है?

हाँ, .NET के लिए Aspose.Cells Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019 और Office 365 के लिए Excel सहित Excel के विभिन्न संस्करणों के साथ संगत है। यह फ़ाइल स्वरूपों .xls और .xlsx का समर्थन करता है।