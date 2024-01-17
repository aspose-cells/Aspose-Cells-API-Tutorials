---
title: वेब एक्सटेंशन जोड़ें
linktitle: वेब एक्सटेंशन जोड़ें
second_title: .NET API संदर्भ के लिए Aspose.Cells
description: .NET के लिए Aspose.Cells के साथ आसानी से अपनी Excel कार्यपुस्तिकाओं में वेब एक्सटेंशन जोड़ें।
type: docs
weight: 40
url: /hi/net/excel-workbook/add-web-extension/
---
इस चरण-दर-चरण ट्यूटोरियल में, हम दिए गए C# स्रोत कोड की व्याख्या करेंगे जो आपको .NET के लिए Aspose.Cells का उपयोग करके एक वेब एक्सटेंशन जोड़ने की अनुमति देगा। अपनी एक्सेल वर्कबुक में वेब एक्सटेंशन जोड़ने के लिए नीचे दिए गए चरणों का पालन करें।

## चरण 1: आउटपुट निर्देशिका सेट करें

```csharp
// उत्पादन निर्देशिका
string outDir = RunExamples.Get_OutputDirectory();
```

इस पहले चरण में, हम आउटपुट निर्देशिका को परिभाषित करते हैं जहां संशोधित एक्सेल वर्कबुक सहेजी जाएगी।

## चरण 2: एक नई कार्यपुस्तिका बनाएँ

```csharp
// एक नई कार्यपुस्तिका बनाएँ
Workbook workbook = new Workbook();
```

यहां हम इसका उपयोग करके एक नई एक्सेल वर्कबुक बना रहे हैं`Workbook` Aspose.Cells से कक्षा।

## चरण 3: वेब एक्सटेंशन संग्रह तक पहुंचें

```csharp
// वेब एक्सटेंशन के संग्रह तक पहुंचें
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

 हम एक्सेल वर्कबुक के वेब एक्सटेंशन संग्रह का उपयोग करके एक्सेस करते हैं`WebExtensions` की संपत्ति`Worksheets` वस्तु।

## चरण 4: एक नया वेब एक्सटेंशन जोड़ें

```csharp
// एक नया वेब एक्सटेंशन जोड़ें
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

हम एक्सटेंशन संग्रह में एक नया वेब एक्सटेंशन जोड़ रहे हैं। हम एक्सटेंशन की संदर्भ आईडी, स्टोर नाम और स्टोर प्रकार को परिभाषित करते हैं।

## चरण 5: वेब एक्सटेंशन कार्य फलक संग्रह तक पहुंचें

```csharp
// वेब एक्सटेंशन के कार्य फलक संग्रह तक पहुंचें
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

 हम इसका उपयोग करके एक्सेल वर्कबुक वेब एक्सटेंशन टास्क पैन संग्रह तक पहुंचते हैं`WebExtensionTaskPanes` की संपत्ति`Worksheets` वस्तु।

## चरण 6: एक नया कार्य फलक जोड़ें

```csharp
// एक नया कार्य फलक जोड़ें
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

हम कार्य फलक संग्रह में एक नया कार्य फलक जोड़ रहे हैं। हम फलक की दृश्यता, उसकी डॉकिंग स्थिति और संबंधित वेब एक्सटेंशन सेट करते हैं।

## चरण 7: कार्यपुस्तिका सहेजें और बंद करें

```csharp
// कार्यपुस्तिका सहेजें और बंद करें
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

हम संशोधित कार्यपुस्तिका को निर्दिष्ट आउटपुट निर्देशिका में सहेजते हैं और फिर उसे बंद कर देते हैं।

### .NET के लिए Aspose.Cells का उपयोग करके वेब एक्सटेंशन जोड़ने के लिए नमूना स्रोत कोड 
```csharp
//स्रोत निर्देशिका
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## निष्कर्ष

बधाई हो! अब आपने सीख लिया है कि .NET के लिए Aspose.Cells का उपयोग करके वेब एक्सटेंशन कैसे जोड़ें। अपने एक्सेल वर्कबुक में वेब एक्सटेंशन में हेरफेर से अधिकतम लाभ प्राप्त करने के लिए कोड के साथ प्रयोग करें और Aspose.Cells की अतिरिक्त सुविधाओं का पता लगाएं।

## पूछे जाने वाले प्रश्न

#### प्रश्न: एक्सेल वर्कबुक में वेब एक्सटेंशन क्या है?

उ: एक्सेल वर्कबुक में एक वेब एक्सटेंशन एक घटक है जो आपको वेब अनुप्रयोगों को एकीकृत करके एक्सेल में अतिरिक्त कार्यक्षमता जोड़ने की अनुमति देता है। यह इंटरैक्टिव सुविधाएँ, कस्टम डैशबोर्ड, बाहरी एकीकरण और बहुत कुछ प्रदान कर सकता है।

#### प्रश्न: Aspose.Cells के साथ एक्सेल वर्कबुक में वेब एक्सटेंशन कैसे जोड़ें?

 उ: Aspose.Cells के साथ एक्सेल वर्कबुक में एक वेब एक्सटेंशन जोड़ने के लिए, आप हमारे चरण-दर-चरण मार्गदर्शिका में दिए गए चरणों का पालन कर सकते हैं। उपयोग`WebExtensionCollection` और`WebExtensionTaskPaneCollection` वेब एक्सटेंशन और संबंधित कार्य फलक को जोड़ने और कॉन्फ़िगर करने के लिए कक्षाएं।

#### प्रश्न: वेब एक्सटेंशन जोड़ने के लिए कौन सी जानकारी आवश्यक है?

उ: वेब एक्सटेंशन जोड़ते समय, आपको एक्सटेंशन SKU आईडी, स्टोर का नाम और स्टोर प्रकार प्रदान करना होगा। यह जानकारी एक्सटेंशन को सही ढंग से पहचानने और लोड करने में मदद करती है।

#### प्रश्न: क्या मैं एक एक्सेल वर्कबुक में एकाधिक वेब एक्सटेंशन जोड़ सकता हूँ?

 उ: हां, आप एक ही एक्सेल वर्कबुक में कई वेब एक्सटेंशन जोड़ सकते हैं। उपयोग`Add` प्रत्येक एक्सटेंशन को जोड़ने के लिए वेब एक्सटेंशन संग्रह की विधि, फिर उन्हें संबंधित कार्य फलक के साथ संबद्ध करें।