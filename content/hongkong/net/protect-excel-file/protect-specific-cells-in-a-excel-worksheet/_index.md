---
title: 保護 Excel 工作表中的特定儲存格
linktitle: 保護 Excel 工作表中的特定儲存格
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 來保護 Excel 中的特定儲存格。 C# 逐步教學。
type: docs
weight: 70
url: /zh-hant/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
在本教程中，我們將查看使用 Aspose.Cells 庫來保護 Excel 電子表格中的特定單元格的 C# 原始程式碼。我們將逐步完成程式碼的每個步驟並解釋其工作原理。仔細按照說明進行操作以獲得所需的結果。

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

在此步驟中，我們將定義套用於特定單元格的樣式。使用以下程式碼：

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

## 第 7 步：鎖定特定儲存格

在此步驟中，我們將鎖定特定單元格。使用以下程式碼：

```csharp
//鎖定所有三個儲存格...即 A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## 步驟 8：保護工作表

最後，我們將保護工作表以防止特定儲存格被修改。使用以下程式碼：

```csharp
//保護工作表。
sheet.Protect(ProtectionType.All);
```

## 第 9 步：儲存 Excel 文件

現在我們將儲存修改後的 Excel 檔案。使用以下程式碼：

```csharp
//儲存 Excel 檔案。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

確保指定正確的路徑來儲存修改後的 Excel 檔案。

### 使用 Aspose.Cells for .NET 保護 Excel 工作表中的特定單元格的範例原始程式碼 
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
//定義 styleflag 對象
StyleFlag styleflag;
//循環遍歷工作表中的所有列並解鎖它們。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
//鎖定三個儲存格...即 A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
//最後，現在保護紙張。
sheet.Protect(ProtectionType.All);
//儲存 Excel 檔案。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## 結論

恭喜！您現在擁有 C# 原始程式碼，可讓您使用 .NET 的 Aspose.Cells 程式庫保護 Excel 工作表中的特定儲存格。請隨意自訂程式碼以滿足您的特定需求。

### 常見問題（常見問題）

#### 此程式碼適用於最新版本的 Excel 嗎？

是的，此程式碼適用於最新版本的 Excel，包括 Excel 2010 及更高版本格式的檔案。

#### 除了A1、B1和C1之外，我還能保護其他細胞嗎？

是的，您可以透過調整對應程式碼行中的儲存格參考來修改程式碼以鎖定其他特定儲存格。

#### 如何再次解鎖已鎖定的儲存格？

您可以使用`SetStyle`方法與`IsLocked`設定`false`解鎖細胞。

#### 我可以為工作簿新增更多工作表嗎？

是的，您可以使用以下命令將其他工作表新增至工作簿中`Worksheets.Add()`方法並為每個工作表重複細胞保護步驟。

#### 如何更改Excel檔案的保存格式？

您可以使用以下命令變更儲存格式`SaveFormat`具有所需格式的方法，例如`SaveFormat.Xlsx`適用於 Excel 2007 及更高版本。