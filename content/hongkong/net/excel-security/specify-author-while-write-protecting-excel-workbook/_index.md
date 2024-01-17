---
title: 寫入保護 Excel 工作簿時指定作者
linktitle: 寫入保護 Excel 工作簿時指定作者
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 保護和自訂 Excel 工作簿。 C# 逐步教學。
type: docs
weight: 30
url: /zh-hant/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

在本教學中，我們將向您展示如何在使用 .NET 的 Aspose.Cells 庫對 Excel 工作簿進行寫入保護時指定作者。

## 第一步：準備環境

在開始之前，請確保您的電腦上安裝了 Aspose.Cells for .NET。從 Aspose 官方網站下載該程式庫並按照提供的安裝說明進行操作。

## 第 2 步：設定來源目錄和輸出目錄

在提供的原始程式碼中，您必須指定來源目錄和輸出目錄。修改`sourceDir`和`outputDir`透過將「YOUR SOURCE DIRECTORY」和「YOUR OUTPUT DIRECTORY」替換為電腦上對應的絕對路徑來變更變數。

```csharp
//原始碼目錄
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

//輸出目錄
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## 步驟 3：建立一個空白的 Excel 工作簿

首先，我們建立一個代表空 Excel 工作簿的 Workbook 物件。

```csharp
//建立空工作簿。
Workbook wb = new Workbook();
```

## 第四步：用密碼寫保護

接下來，我們使用以下指令指定一個密碼來寫入保護 Excel 工作簿`WriteProtection.Password`Workbook 物件的屬性。

```csharp
//使用密碼寫入保護工作簿。
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## 第 5 步：作者說明

現在我們使用以下命令指定 Excel 工作簿的作者`WriteProtection.Author`Workbook 物件的屬性。

```csharp
//寫入保護工作簿時指定作者。
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## 步驟 6：備份受保護的 Excel 工作簿

一旦指定了寫入保護和作者，我們就可以使用以下命令將 Excel 工作簿儲存為 XLSX 格式：`Save()`方法。

```csharp
//將工作簿儲存為 XLSX 格式。
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### 使用 Aspose.Cells for .NET 寫入保護 Excel 工作簿時指定作者的範例原始程式碼 
```csharp
//原始碼目錄
string sourceDir = "YOUR SOURCE DIRECTORY";

//輸出目錄
string outputDir = "YOUR OUTPUT DIRECTORY";

//建立空工作簿。
Workbook wb = new Workbook();

//使用密碼寫入保護工作簿。
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

//寫入保護工作簿時指定作者。
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

//將工作簿儲存為 XLSX 格式。
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## 結論

恭喜！現在您已經了解如何在使用 Aspose.Cells for .NET 對 Excel 工作簿進行寫入保護時指定作者。您可以將這些步驟套用到您自己的專案中，以保護和自訂您的 Excel 工作簿。

請隨意進一步探索 Aspose.Cells for .NET 的功能，以對 Excel 檔案進行更進階的操作。

## 常見問題解答

#### Q：我可以在不指定密碼的情況下對 Excel 工作簿進行寫入保護嗎？

答：是的，您可以使用 Workbook 物件的`WriteProtect()`方法無需指定密碼即可對 Excel 工作簿進行寫入保護。這將限制對工作簿的更改，而無需密碼。

#### Q：如何取消 Excel 工作簿的寫入保護？

答：要取消 Excel 工作簿的寫入保護，您可以使用`Unprotect()`Worksheet 物件的方法或`RemoveWriteProtection()`Workbook 物件的方法，取決於您的具體用例。 。

#### Q：我忘了保護 Excel 工作簿的密碼。我能做些什麼 ？

答：如果您忘記了保護 Excel 工作簿的密碼，則無法直接將其刪除。但是，您可以嘗試使用專門的第三方工具，為受保護的 Excel 檔案提供密碼復原功能。

#### Q：對 Excel 工作簿進行寫入保護時是否可以指定多位作者？

答：不可以，Aspose.Cells for .NET 函式庫允許在對 Excel 工作簿進行寫入保護時指定單一作者。如果要指定多個作者，則需要考慮透過直接操作 Excel 檔案來自訂解決方案。