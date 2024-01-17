---
title: 保護 Excel 工作表中的特定行
linktitle: 保護 Excel 工作表中的特定行
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 保護 Excel 中的特定行。保護機密資料的逐步指南。
type: docs
weight: 90
url: /zh-hant/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
保護 Excel 電子表格中的機密資料對於確保資訊安全至關重要。 Aspose.Cells for .NET 提供了一個強大的解決方案來保護 Excel 電子表格中的特定行。本指南將引導您了解如何使用提供的 C# 原始程式碼保護 Excel 工作表中的特定行。請依照以下簡單步驟在 Excel 檔案中設定行保護。

## 步驟1：導入所需的庫

首先，請確保您的系統上安裝了 Aspose.Cells for .NET。您還需要在 C# 專案中加入適當的引用才能使用 Aspose.Cells 的功能。以下是導入所需庫的程式碼：

```csharp
//加入必要的參考文獻
using Aspose.Cells;
```

## 步驟 2：建立 Excel 工作簿和電子表格

匯入所需的庫後，您可以建立新的 Excel 工作簿和新工作表。操作方法如下：

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENTS DIRECTORY";

//如果目錄尚不存在，則建立一個目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

//建立一個新工作簿。
Workbook wb = new Workbook();

//建立一個電子表格物件並取得第一個工作表。
Worksheet sheet = wb.Worksheets[0];
```

## 第三步：設定樣式和樣式標誌

現在我們將設定儲存格樣式和樣式標誌以解鎖工作表中的所有欄位。這是必要的程式碼：

```csharp
//設定樣式對象。
Styling styling;

//設定 styleflag 物件。
StyleFlag flag;

//循環遍歷工作表中的所有列並解鎖它們。
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## 步驟 4：保護特定線路

現在我們將保護工作表中的特定行。我們將鎖定第一行以防止任何修改。就是這樣：

```csharp
//取得第一行的樣式。
style = sheet.Cells.Rows[0].Style;

//鎖定它。
style. IsLocked = true;

//實例化標誌。
flag = new StyleFlag();

//設定鎖定參數。
flag. Locked = true;

//將樣式套用到第一行。
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## 步驟 5：保護工作表

最後，我們將保護整個 Excel 工作表以防止未經授權的修改。就是這樣：

```csharp
//保護工作表。
sheet.Protect(ProtectionType.All);
```

## 步驟 6：儲存受保護的 Excel 文件

完成對 Excel 工作表中特定行的保護後，您可以將受保護的 Excel 檔案儲存到系統中。就是這樣：

```csharp
//儲存 Excel 檔案。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

執行這些步驟後，您將成功使用 Aspose.Cells for .NET 保護 Excel 試算表中的特定行。

### 使用 Aspose.Cells for .NET 保護 Excel 工作表中的特定行的範例原始程式碼 
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

保護 Excel 文件中的資料對於防止未經授權的存取或不必要的修改至關重要。使用 .NET 的 Aspose.Cells 庫，您可以使用提供的 C# 原始程式碼輕鬆保護 Excel 電子表格中的特定行。請按照此逐步指南為您的 Excel 檔案新增額外的安全性層。

### 常見問題解答

#### 特定行保護是否適用於所有版本的 Excel？

是的，使用 Aspose.Cells for .NET 的特定行保護適用於所有支援的 Excel 版本。

#### 我可以保護 Excel 電子表格中的多個特定行嗎？

是的，您可以使用本指南中所述的類似方法來保護多個特定行。

#### 如何解鎖 Excel 電子表格中的特定行？

若要解鎖特定行，您必須使用以下命令相應地修改原始程式碼`IsLocked`的方法`Style`目的。