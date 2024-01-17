---
title: 保護 Excel 工作表中的行
linktitle: 保護 Excel 工作表中的行
second_title: Aspose.Cells for .NET API 參考
description: 在本教學中了解如何使用 Aspose.Cells for .NET 保護 Excel 電子表格的行。 C# 逐步教學。
type: docs
weight: 60
url: /zh-hant/net/protect-excel-file/protect-row-in-excel-worksheet/
---
在本教程中，我們將查看一些使用 Aspose.Cells 庫來保護 Excel 電子表格中的行的 C# 原始程式碼。我們將逐步完成程式碼的每個步驟並解釋其工作原理。仔細按照說明進行操作以獲得所需的結果。

## 第 1 步：先決條件

在開始之前，請確保您已安裝適用於 .NET 的 Aspose.Cells 庫。您可以從Aspose官方網站取得它。請同時確保您擁有最新版本的 Visual Studio 或任何其他 C# 開發環境。

## 步驟2：導入所需的命名空間

要使用 Aspose.Cells 函式庫，我們需要將必要的命名空間匯入到我們的程式碼中。將以下行新增至 C# 來源檔案的頂部：

```csharp
using Aspose.Cells;
```

## 步驟 3：建立 Excel 工作簿

在此步驟中，我們將建立一個新的 Excel 工作簿。使用以下程式碼建立 Excel 工作簿：

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//建立一個新工作簿。
Workbook wb = new Workbook();
```

一定要更換`"YOUR_DOCUMENTS_DIR"`與您的文件目錄的適當路徑。

## 第 4 步：建立電子表格

現在我們已經建立了 Excel 工作簿，讓我們建立一個工作表並取得第一個工作表。使用以下程式碼：

```csharp
//建立一個電子表格物件並取得第一個工作表。
Worksheet sheet = wb.Worksheets[0];
```

## 第五步：定義風格

在此步驟中，我們將定義套用於電子表格行的樣式。使用以下程式碼：

```csharp
//樣式物件的定義。
Styling styling;
```

## 步驟6：循環解鎖所有列

現在我們將循環遍歷工作表中的所有列並解鎖它們。使用以下程式碼：

```csharp
//循環遍歷工作表中的所有列並解鎖它們。
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## 步驟7：鎖定第一行

在此步驟中，我們將鎖定工作表的第一行。使用以下程式碼：

```csharp
//取得第一行的樣式。
style = sheet.Cells.Rows[0].Style;
//鎖定風格。
style. IsLocked = true;
//將樣式套用到第一行。
sheet.Cells.ApplyRowStyle(0, style);
```

## 步驟 8：保護工作表

現在我們已經設定了樣式並鎖定了行，讓我們保護電子表格。使用以下程式碼：

```csharp
//保護工作表。
sheet.Protect(ProtectionType.All);
```

## 第 9 步：儲存 Excel 文件

最後，我們儲存修改後的Excel檔案。使用以下程式碼：

```csharp
//儲存 Excel 檔案。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

確保指定正確的路徑來儲存修改後的 Excel 檔案。

### 使用 Aspose.Cells for .NET 保護 Excel 工作表中的行的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目錄尚不存在，則建立該目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//建立一個新工作簿。
Workbook wb = new Workbook();
//建立一個工作表物件並取得第一個工作表。
Worksheet sheet = wb.Worksheets[0];
//定義樣式物件。
Style style;
//定義 styleflag 物件。
StyleFlag flag;
//循環遍歷工作表中的所有列並解鎖它們。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
//取得第一行樣式。
style = sheet.Cells.Rows[0].Style;
//鎖定它。
style.IsLocked = true;
//實例化標誌。
flag = new StyleFlag();
//設定鎖定設定。
flag.Locked = true;
//將樣式套用到第一行。
sheet.Cells.ApplyRowStyle(0, style, flag);
//保護板材。
sheet.Protect(ProtectionType.All);
//儲存 Excel 檔案。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 結論

恭喜！您現在擁有 C# 原始程式碼，可讓您使用 .NET 的 Aspose.Cells 庫來保護 Excel 電子表格中的行。請務必仔細遵循這些步驟並根據您的特定需求自訂程式碼。

### 常見問題（常見問題）

#### 此程式碼適用於最新版本的 Excel 嗎？

是的，此程式碼適用於最新版本的 Excel，包括 Excel 2010 及更高版本格式的檔案。

#### 我可以僅保護工作表中的特定行而不是所有行嗎？

是的，您可以修改程式碼來指定要保護的特定行。您將需要相應地調整循環和索引。

#### 如何再次解鎖鎖定的線路？

您可以使用`IsLocked`的方法`Style`將值設定為的對象`false`並解鎖行。

#### 是否可以保護同一 Excel 工作簿中的多個工作表？

是的，您可以為工作簿中的每個工作表重複建立工作表、設定樣式和保護的步驟。

#### 如何更改電子表格保護密碼？

您可以使用以下命令變更密碼`Protect`方法並指定新密碼作為參數。