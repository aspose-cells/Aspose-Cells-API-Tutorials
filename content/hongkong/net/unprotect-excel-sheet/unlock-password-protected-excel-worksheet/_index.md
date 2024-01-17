---
title: 解鎖受密碼保護的 Excel 工作表
linktitle: 解鎖受密碼保護的 Excel 工作表
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 解鎖受密碼保護的 Excel 電子表格。 C# 逐步教學。
type: docs
weight: 10
url: /zh-hant/net/unprotect-excel-sheet/unlock-password-protected-excel-worksheet/
---
Excel 電子表格的密碼保護通常用於保護敏感資料。在本教學中，我們將逐步指導您瞭解和實作所提供的 C# 原始碼，以使用適用於 .NET 的 Aspose.Cells 函式庫解鎖受密碼保護的 Excel 電子表格。

## 第一步：準備環境

在開始之前，請確保您的電腦上安裝了 Aspose.Cells for .NET。您可以從Aspose官方網站下載該庫並按照提供的說明進行安裝。

安裝完成後，在您首選的整合開發環境 (IDE) 中建立新的 C# 項目，並匯入適用於 .NET 的 Aspose.Cells 庫。

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

現在我們將使用以下命令解鎖工作表`Unprotect()`Worksheet 物件的方法。將密碼字串留空（`""`) 如果電子表格不受密碼保護。

```csharp
//使用密碼取消對工作表的保護
worksheet.Unprotect("");
```

## 步驟 6：儲存解鎖的 Excel 文件

電子表格解鎖後，我們可以儲存最終的 Excel 檔案。使用`Save()`指定輸出檔案的完整路徑的方法

.

```csharp
//儲存工作簿
workbook.Save(dataDir + "output.out.xls");
```

### 使用 Aspose.Cells for .NET 解鎖受密碼保護的 Excel 工作表的範例原始碼 
```csharp
try
{
    //文檔目錄的路徑。
    string dataDir = "YOUR DOCUMENT DIRECTORY";
    //實例化 Workbook 物件
    Workbook workbook = new Workbook(dataDir + "book1.xls");
    //存取 Excel 文件中的第一個工作表
    Worksheet worksheet = workbook.Worksheets[0];
    //使用密碼取消對工作表的保護
    worksheet.Unprotect("");
    //儲存工作簿
    workbook.Save(dataDir + "output.out.xls");
}
catch (Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 使用 C# 原始碼解鎖受密碼保護的 Excel 電子表格。透過遵循本教學中的步驟，您可以將此功能套用到您自己的專案中，並有效率且安全地處理 Excel 檔案。

請隨意進一步探索 Aspose.Cells 提供的功能以實現更高級的操作。

### 常見問題解答

#### Q：如果電子表格受密碼保護怎麼辦？

答：如果電子表格受密碼保護，您必須在`Unprotect()`方法能夠解鎖它。

#### Q：解鎖受保護的 Excel 電子表格時有什麼限製或註意事項嗎？

答：是的，請確保您擁有解鎖電子表格所需的權限。此外，使用此功能時請務必遵循組織的安全策略。