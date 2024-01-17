---
title: 解鎖受保護的 Excel 工作表
linktitle: 解鎖受保護的 Excel 工作表
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 解鎖受保護的 Excel 電子表格。 C# 逐步教學。
type: docs
weight: 20
url: /zh-hant/net/unprotect-excel-sheet/unlock-protected-excel-sheet/
---
保護 Excel 電子表格通常用於限制對資料的存取和修改。在本教程中，我們將指導您逐步理解和實現所提供的 C# 原始程式碼，以使用適用於 .NET 的 Aspose.Cells 庫解鎖受保護的 Excel 電子表格。

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

電子表格解鎖後，我們可以儲存最終的 Excel 檔案。使用`Save()`方法來指定輸出檔案的完整路徑。

```csharp
//儲存工作簿


workbook.Save(dataDir + "output.out.xls");
```

### 使用 Aspose.Cells for .NET 解鎖受保護的 Excel 工作表的範例原始程式碼 
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
catch(Exception ex)
{
    Console.WriteLine(ex.Message);
    Console.ReadLine();
}
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 透過 C# 原始碼解鎖受保護的 Excel 電子表格。透過遵循本教學中的步驟，您可以將此功能套用到您自己的專案中，並有效率且安全地處理 Excel 檔案。

請隨意進一步探索 Aspose.Cells 提供的功能以實現更高級的操作。

### 常見問題解答

#### Q：解鎖受保護的 Excel 電子表格時應採取哪些預防措施？

答：解鎖受保護的 Excel 電子表格時，請確保您擁有存取該文件所需的權限。另外，請檢查您是否使用了正確的解鎖方法並提供正確的密碼（如果適用）。

#### Q：我如何知道電子表格是否受密碼保護？

答：您可以使用 .NET 的 Aspose.Cells 庫中的屬性或方法來檢查工作表是否受密碼保護。例如，您可以使用`IsProtected()`Worksheet 物件的方法來檢查工作表的保護狀態。

#### Q：我在嘗試解鎖電子表格時遇到異常。我該怎麼辦 ？

答：如果您在解鎖電子表格時遇到異常，請確保您已正確指定 Excel 文件路徑，並驗證您是否具有存取該文件的必要權限。如果問題仍然存在，請隨時聯絡 Aspose.Cells 支援以獲得進一步協助。