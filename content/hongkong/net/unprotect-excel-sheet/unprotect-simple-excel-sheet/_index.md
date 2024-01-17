---
title: 取消保護簡單的 Excel 工作表
linktitle: 取消保護簡單的 Excel 工作表
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 取消對 Excel 電子表格的保護。 C# 逐步教學。
type: docs
weight: 30
url: /zh-hant/net/unprotect-excel-sheet/unprotect-simple-excel-sheet/
---
在本教學中，我們將引導您完成使用 .NET 的 Aspose.Cells 庫解鎖簡單 Excel 電子表格所需的步驟。

## 第一步：準備環境

在開始之前，請確保您的電腦上安裝了 Aspose.Cells for .NET。從 Aspose 官方網站下載該程式庫並按照提供的安裝說明進行操作。

## 第二步：配置文檔目錄路徑

在提供的原始碼中，您需要指定要解鎖的Excel檔案所在的目錄路徑。修改`dataDir`變量，將“YOUR DOCUMENT DIRECTORY”替換為計算機上目錄的絕對路徑。

```csharp
//文檔目錄的路徑。
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## 第 3 步：建立工作簿對象

首先，我們需要建立一個代表 Excel 檔案的 Workbook 物件。使用 Workbook 類別建構函式並指定要開啟的 Excel 檔案的完整路徑。

```csharp
//實例化 Workbook 物件
Workbook workbook = new Workbook(dataDir + "book1.xls");
```

## 第 4 步：存取電子表格

接下來，我們需要導覽到 Excel 文件中的第一個工作表。使用`Worksheets`Workbook 物件的屬性來存取工作表集合，然後使用`[0]`用於存取第一張表的索引。

```csharp
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
```

## 第 5 步：解鎖電子表格

現在我們將使用以下命令解鎖工作表`Unprotect()` Worksheet 物件的方法。此方法不需要密碼。

```csharp
//在沒有密碼的情況下取消對工作表的保護
worksheet.Unprotect();
```

## 步驟 6：儲存解鎖的 Excel 文件

電子表格解鎖後，我們可以儲存最終的 Excel 檔案。使用`Save()`方法指定輸出檔案的完整路徑和儲存格式。

```csharp
//儲存工作簿
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```
### 使用 Aspose.Cells for .NET 取消保護簡單 Excel 工作表的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//實例化 Workbook 物件
Workbook workbook = new Workbook(dataDir + "book1.xls");
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = workbook.Worksheets[0];
//在沒有密碼的情況下取消對工作表的保護
worksheet.Unprotect();
//儲存工作簿
workbook.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 結論

恭喜！您現在已經了解如何使用 Aspose.Cells for .NET 解鎖簡單的 Excel 電子表格。透過遵循本教學中的步驟，您可以輕鬆地將此功能應用到您自己的專案中。

歡迎探索 Aspose.Cells 的更多功能
對 Excel 檔案進行更進階的操作。

### 常見問題解答

#### Q：解鎖 Excel 電子表格時應採取哪些預防措施？

答：解鎖 Excel 電子表格時，請確保您擁有存取該檔案所需的權限。另外，請務必使用正確的解鎖方法並提供正確的密碼（如果適用）。

#### Q：我如何知道電子表格是否受密碼保護？

答：您可以使用 .NET 的 Aspose.Cells 函式庫提供的屬性或方法來檢查工作表是否受密碼保護。例如，您可以使用`IsProtected()`Worksheet 物件的方法來檢查工作表是否受到保護。

#### Q：我在嘗試解鎖電子表格時遇到異常。我該怎麼辦 ？

答：如果您在解鎖電子表格時遇到異常，請確保您已正確指定 Excel 檔案的路徑，並檢查您是否具有存取該檔案所需的權限。如果問題仍然存在，請隨時聯絡 Aspose.Cells 支援以獲得進一步協助。