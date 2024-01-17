---
title: 將數位簽章新增至已簽署的 Excel 文件
linktitle: 將數位簽章新增至已簽署的 Excel 文件
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 輕鬆將數位簽章新增至現有 Excel 檔案。
type: docs
weight: 30
url: /zh-hant/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
在本逐步指南中，我們將解釋提供的 C# 原始程式碼，該程式碼可讓您使用 Aspose.Cells for .NET 將數位簽章新增至已簽署的 Excel 檔案。請依照下列步驟為現有 Excel 檔案新增新的數位簽章。

## 第 1 步：設定來源目錄和輸出目錄

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();

//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

在第一步中，我們定義將用於載入現有 Excel 檔案並使用新數位簽章儲存檔案的來源目錄和輸出目錄。

## 步驟 2： 載入現有 Excel 文件

```csharp
//載入已簽署的 Excel 工作簿
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

這裡我們使用以下命令來載入已經簽署的 Excel 文件`Workbook`Aspose.Cells 類別。

## 步驟 3：建立數位簽章集合

```csharp
//建立數位簽章集合
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

我們使用以下方法建立了一個新的數位簽章集合`DigitalSignatureCollection`班級。

## 第 4 步：建立新證書

```csharp
//建立新證書
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

在這裡，我們根據提供的文件和密碼建立一個新證書。

## 步驟 5：將新的數位簽章加入集合中

```csharp
//建立新的數位簽名
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

//將數位簽名加入集合中
dsCollection.Add(signature);
```

我們使用以下方法建立一個新的數位簽名`DigitalSignature`類別並將其添加到數位簽名集合中。

## 步驟 6：將數位簽章集合新增至工作簿中

```csharp
//將數位簽章集合加入工作簿中
workbook.AddDigitalSignature(dsCollection);
```

我們使用以下命令將數位簽章集合新增至現有 Excel 工作簿中`AddDigitalSignature()`方法。

## 步驟 7：儲存並關閉工作簿

```csharp
//儲存工作簿並關閉它
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

我們將帶有新數位簽章的工作簿儲存到指定的輸出目錄，然後關閉它並釋放關聯的資源。

### 使用 Aspose.Cells for .NET 將數位簽章新增至已簽署的 Excel 檔案的範例原始程式碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
//證書文件及其密碼
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//載入已經數位簽署的工作簿以新增新的數位簽名
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//建立數位簽章集合
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//建立新證書
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//建立新的數位簽章並將其新增至數位簽章集合中
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//在工作簿中新增數位簽章集合
workbook.AddDigitalSignature(dsCollection);
//保存工作簿並將其丟棄。
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 將數位簽章新增至已簽署的 Excel 檔案。數位簽章為您的 Excel 檔案添加了額外的安全層，確保其真實性和完整性。

### 常見問題解答

#### Q：什麼是 Aspose.Cells for .NET？

答：Aspose.Cells for .NET 是一個功能強大的類別庫，可讓.NET 開發人員輕鬆建立、修改、轉換和操作 Excel 檔案。

#### Q：什麼是 Excel 檔案中的數位簽章？

答：Excel文件中的數位簽章是保證文件真實性、完整性和來源的電子標記。它用於驗證文件自簽名以來未被修改過並且來自可靠的來源。

#### Q：在 Excel 檔案中新增數位簽章有什麼好處？

答：在 Excel 文件中新增數位簽章有多種好處，包括防止未經授權的變更、確保資料完整性、驗證文件作者的身份以及提供對其所包含資訊的信心。

#### Q：我可以在 Excel 檔案中新增多個數位簽章嗎？

答：是的，Aspose.Cells 允許您在 Excel 檔案中新增多個數位簽章。您可以建立數位簽章集合並透過一次操作將它們新增至文件。

#### Q：Excel 檔案添加數位簽章有什麼要求？

答：要為 Excel 檔案新增數位簽名，您需要一個有效的數位憑證來簽署文件。在新增數位簽章之前，請確保您擁有正確的憑證和密碼。