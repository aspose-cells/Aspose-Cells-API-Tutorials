---
title: एक्सेल टेक्स्ट फ़ंक्शंस का रहस्योद्घाटन
linktitle: एक्सेल टेक्स्ट फ़ंक्शंस का रहस्योद्घाटन
second_title: Aspose.Cells जावा एक्सेल प्रोसेसिंग एपीआई
description: जावा के लिए Aspose.Cells के साथ एक्सेल टेक्स्ट फ़ंक्शंस के रहस्यों को अनलॉक करें। एक्सेल में टेक्स्ट को आसानी से हेरफेर करना, निकालना और बदलना सीखें।
type: docs
weight: 18
url: /hi/java/basic-excel-functions/excel-text-functions-demystified/
---

# जावा के लिए Aspose.Cells का उपयोग करके एक्सेल टेक्स्ट फ़ंक्शंस का रहस्योद्घाटन किया गया

इस ट्यूटोरियल में, हम जावा एपीआई के लिए Aspose.Cells का उपयोग करके एक्सेल में टेक्स्ट मैनिपुलेशन की दुनिया में गहराई से उतरेंगे। चाहे आप एक अनुभवी एक्सेल उपयोगकर्ता हों या अभी शुरुआत कर रहे हों, टेक्स्ट फ़ंक्शंस को समझना आपके स्प्रेडशीट कौशल को महत्वपूर्ण रूप से बढ़ा सकता है। हम विभिन्न टेक्स्ट फ़ंक्शंस का पता लगाएंगे और उनके उपयोग को स्पष्ट करने के लिए व्यावहारिक उदाहरण प्रदान करेंगे।

## शुरू करना

 शुरू करने से पहले, सुनिश्चित करें कि आपके पास जावा के लिए Aspose.Cells स्थापित है। आप इसे डाउनलोड कर सकते हैं[यहाँ](https://releases.aspose.com/cells/java/). एक बार जब आप इसे सेट कर लें, तो आइए एक्सेल टेक्स्ट फ़ंक्शंस की आकर्षक दुनिया में उतरें।

## CONCATENATE - पाठ का संयोजन

`CONCATENATE`फ़ंक्शन आपको विभिन्न सेल से टेक्स्ट को मर्ज करने की अनुमति देता है। आइए देखें कि जावा के लिए Aspose.Cells के साथ इसे कैसे करें:

```java
// Aspose.Cells का उपयोग करके पाठ को संयोजित करने के लिए जावा कोड
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.getWorksheets().get(0);
Cell cell = worksheet.getCells().get("A1");

cell.putValue("Hello, ");
cell = worksheet.getCells().get("B1");
cell.putValue("World!");

// A1 और B1 को C1 में जोड़ें
cell = worksheet.getCells().get("C1");
cell.setFormula("=CONCATENATE(A1,B1)");

workbook.calculateFormula();
```

अब, सेल C1 में "हैलो, वर्ल्ड!" होगा।

## बाएँ और दाएँ - पाठ निकालना

`LEFT` और`RIGHT` फ़ंक्शंस आपको टेक्स्ट स्ट्रिंग के बाएँ या दाएँ से निर्दिष्ट संख्या में वर्ण निकालने की अनुमति देते हैं। यहां बताया गया है कि आप उनका उपयोग कैसे कर सकते हैं:

```java
// Aspose.Cells का उपयोग करके टेक्स्ट निकालने के लिए जावा कोड
Cell cell = worksheet.getCells().get("A2");
cell.putValue("Excel Rocks!");

// पहले 5 अक्षर निकालें
cell = worksheet.getCells().get("B2");
cell.setFormula("=LEFT(A2, 5)");

// अंतिम 5 अक्षर निकालें
cell = worksheet.getCells().get("C2");
cell.setFormula("=RIGHT(A2, 5)");

workbook.calculateFormula();
```

सेल B2 में "एक्सेल" होगा, और सेल C2 में "रॉक्स!" होगा।

## LEN - वर्णों की गिनती

`LEN` फ़ंक्शन टेक्स्ट स्ट्रिंग में वर्णों की संख्या की गणना करता है। आइए देखें कि जावा के लिए Aspose.Cells के साथ इसका उपयोग कैसे करें:

```java
// Aspose.Cells का उपयोग करके वर्णों की गणना करने के लिए जावा कोड
Cell cell = worksheet.getCells().get("A3");
cell.putValue("Excel");

// पात्रों की गिनती करें
cell = worksheet.getCells().get("B3");
cell.setFormula("=LEN(A3)");

workbook.calculateFormula();
```

सेल बी3 में "5" होगा, जैसे "एक्सेल" में 5 अक्षर होते हैं।

## ऊपरी और निचला - बदलता मामला

`UPPER` और`LOWER` फ़ंक्शंस आपको टेक्स्ट को अपरकेस या लोअरकेस में बदलने की अनुमति देते हैं। यहां बताया गया है कि आप यह कैसे कर सकते हैं:

```java
// Aspose.Cells का उपयोग करके केस बदलने के लिए जावा कोड
Cell cell = worksheet.getCells().get("A4");
cell.putValue("java programming");

// अपरकेस में कनवर्ट करें
cell = worksheet.getCells().get("B4");
cell.setFormula("=UPPER(A4)");

// लोअरकेस में कनवर्ट करें
cell = worksheet.getCells().get("C4");
cell.setFormula("=LOWER(A4)");

workbook.calculateFormula();
```

सेल बी4 में "जावा प्रोग्रामिंग" होगी, और सेल सी4 में "जावा प्रोग्रामिंग" होगी।

## ढूंढें और बदलें - टेक्स्ट का पता लगाएं और बदलें

`FIND` फ़ंक्शन आपको स्ट्रिंग के भीतर किसी विशिष्ट वर्ण या पाठ की स्थिति का पता लगाने की अनुमति देता है, जबकि`REPLACE` फ़ंक्शन आपको टेक्स्ट को प्रतिस्थापित करने में मदद करता है। आइए उन्हें क्रियान्वित होते देखें:

```java
// Aspose.Cells का उपयोग करके खोजने और बदलने के लिए जावा कोड
Cell cell = worksheet.getCells().get("A5");
cell.putValue("Search for me");

// "के लिए" की स्थिति खोजें
cell = worksheet.getCells().get("B5");
cell.setFormula("=FIND(\"for\", A5)");

// "for" को "with" से बदलें
cell = worksheet.getCells().get("C5");
cell.setFormula("=REPLACE(A5, B5, 3, \"with\")");

workbook.calculateFormula();
```

सेल B5 में "9" ("for" की स्थिति) होगी, और सेल C5 में "मेरे साथ खोजें" होगी।

## निष्कर्ष

एक्सेल में टेक्स्ट फ़ंक्शन टेक्स्ट डेटा में हेरफेर और विश्लेषण करने के लिए शक्तिशाली उपकरण हैं। जावा के लिए Aspose.Cells के साथ, आप आसानी से इन कार्यों को अपने जावा अनुप्रयोगों में शामिल कर सकते हैं, पाठ-संबंधित कार्यों को स्वचालित कर सकते हैं और अपनी एक्सेल क्षमताओं को बढ़ा सकते हैं। अधिक टेक्स्ट फ़ंक्शंस का अन्वेषण करें और जावा के लिए Aspose.Cells के साथ एक्सेल की पूरी क्षमता का उपयोग करें।

## पूछे जाने वाले प्रश्न

### मैं एकाधिक कक्षों से पाठ को कैसे संयोजित करूं?

 एकाधिक कक्षों से पाठ को संयोजित करने के लिए, इसका उपयोग करें`CONCATENATE` समारोह। उदाहरण के लिए:
```java
Cell cell = worksheet.getCells().get("A1");
cell.setFormula("=CONCATENATE(A1, B1)");
```

### क्या मैं टेक्स्ट स्ट्रिंग से पहला और आखिरी अक्षर निकाल सकता हूँ?

 हाँ, आप इसका उपयोग कर सकते हैं`LEFT` और`RIGHT` टेक्स्ट स्ट्रिंग के आरंभ या अंत से वर्ण निकालने का कार्य। उदाहरण के लिए:
```java
Cell cell = worksheet.getCells().get("A2");
cell.setFormula("=LEFT(A2, 5)");
```

### मैं टेक्स्ट स्ट्रिंग में वर्णों की गिनती कैसे कर सकता हूं?

 उपयोग`LEN` टेक्स्ट स्ट्रिंग में वर्णों की गिनती करने का फ़ंक्शन। उदाहरण के लिए:
```java
Cell cell = worksheet.getCells().get("A3");
cell.setFormula("=LEN(A3)");
```

### क्या टेक्स्ट का केस बदलना संभव है?

 हां, आप इसका उपयोग करके टेक्स्ट को अपरकेस या लोअरकेस में बदल सकते हैं`UPPER` और`LOWER` कार्य. उदाहरण के लिए:
```java
Cell cell = worksheet.getCells().get("A4");
cell.setFormula("=UPPER(A4)");
```

### मैं स्ट्रिंग के भीतर टेक्स्ट को कैसे ढूंढूं और बदलूं?

किसी स्ट्रिंग में टेक्स्ट ढूंढने और बदलने के लिए, इसका उपयोग करें`FIND` और`REPLACE` कार्य. उदाहरण के लिए:
```java
Cell cell = worksheet.getCells().get("A5");
cell.setFormula("=FIND(\"for\", A5)");
```