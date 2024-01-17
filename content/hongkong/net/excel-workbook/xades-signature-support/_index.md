---
title: Xades 簽名支持
linktitle: Xades 簽名支持
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 將 Xades 簽章新增至 Excel 檔案。
type: docs
weight: 190
url: /zh-hant/net/excel-workbook/xades-signature-support/
---
在本文中，我們將帶您一步步解釋下面的 C# 原始程式碼，該程式碼是關於使用 Aspose.Cells 函式庫用於 .NET 的 Xades 簽章支援。您將了解如何使用此程式庫將 Xades 數位簽章新增至 Excel 檔案。我們還將向您提供簽名流程及其執行的概述。請依照以下步驟取得結論性結果。

## 第 1 步：定義來源目錄和輸出目錄
首先，我們需要在程式碼中定義來源目錄和輸出目錄。這些目錄指示來源檔案所在的位置以及輸出檔案的保存位置。這是對應的程式碼：

```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

請務必根據需要調整目錄路徑。

## 第 2 步：載入 Excel 工作簿
下一步是載入我們要新增 Xades 數位簽章的 Excel 工作簿。這是載入工作簿的程式碼：

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

確保在程式碼中正確指定原始檔案名稱。

## 步驟3：設定數位簽名
現在我們將透過提供必要的資訊來配置 Xades 數位簽章。我們必須指定包含數位憑證的 PFX 檔案以及關聯的密碼。這是對應的程式碼：

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

請務必將“pfxPassword”替換為您的實際密碼，並將“pfxFile”替換為 PFX 檔案的路徑。

## 第四步：新增數位簽名
現在我們已經配置了數位簽名，我們可以將其新增到 Excel 工作簿中。這是對應的程式碼：

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

此步驟將 Xades 數位簽章新增至 Excel 工作簿。

## 步驟 5：儲存有簽名的工作簿
最後，我們儲存新增了數位簽章的 Excel 工作簿。這是對應的程式碼：

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

確保根據您的需求調整輸出檔案的名稱。

### 使用 Aspose.Cells for .NET 的 Xades 簽章支援範例原始碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## 結論
恭喜！您已了解如何使用適用於 .NET 的 Aspose.Cells 程式庫將 Xades 數位簽章新增至 Excel 檔案。透過遵循本文中提供的步驟，您將能夠在自己的專案中實現此功能。請隨意嘗試更多該庫並發現它提供的其他強大功能。

### 常見問題解答

#### Q：Xades 是什麼？

答：Xades 是一種先進的電子簽名標準，用於確保數位文件的完整性和真實性。

#### Q：我可以在 Aspose.Cells 中使用其他類型的數位簽章嗎？

答：是的，Aspose.Cells 也支援其他類型的數位簽名，例如 XMLDSig 簽名和 PKCS#7 簽名。

#### Q：我可以將簽章套用到 Excel 檔案以外的其他文件類型嗎？
 
答：是的，Aspose.Cells 還允許將數位簽章套用至其他支援的文件類型，例如 Word、PDF 和 PowerPoint 文件。