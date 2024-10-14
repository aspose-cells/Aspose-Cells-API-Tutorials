---
title: Excel 中的十進位資料驗證
linktitle: Excel 中的十進位資料驗證
second_title: Aspose.Cells .NET Excel 處理 API
description: 透過我們易於遵循的指南，了解如何使用 Aspose.Cells for .NET 在 Excel 中實現十進位資料驗證。輕鬆增強資料完整性。
type: docs
weight: 11
url: /zh-hant/net/excel-autofilter-validation/decimal-data-validation-in-excel/
---
## 介紹

創建包含準確數據的電子表格對於任何企業的清晰溝通都至關重要。確保資料準確性的一種方法是使用 Excel 中的資料驗證。在本教程中，我們將利用 Aspose.Cells for .NET 的強大功能來建立十進位資料驗證機制，以保持資料可靠且乾淨。如果您想提高 Excel 遊戲水平，那麼您來對地方了！

## 先決條件

在深入研究程式碼之前，請確保您已完成一切設定以實現順利的航行體驗：

1. Visual Studio：如果尚未安裝，請下載並安裝 Visual Studio。它是開發 .NET 應用程式的完美環境。
2.  Aspose.Cells for .NET：您需要將 Aspose.Cells 庫新增到您的專案中。您可以透過以下方式下載[這個連結](https://releases.aspose.com/cells/net/).
3. C# 基礎知識：雖然我們將逐步解釋所有內容，但對 C# 程式設計有基本的了解將使您更能掌握這些概念。
4. .NET Framework：請確保您安裝了與 Aspose.Cells 相容的必要 .NET Framework。
5. 函式庫：在專案中引用 Aspose.Cells 函式庫以避免編譯錯誤。

現在我們已經介紹了基礎知識，讓我們進入令人興奮的部分：編碼。

## 導入包

首先，您需要在 C# 檔案中匯入必要的套件。這使您能夠存取 Aspose.Cells 功能。

```csharp
using System.IO;
using Aspose.Cells;
using System;
```

透過在檔案頂部包含這一行，您可以告訴 C# 尋找允許您操作 Excel 檔案的 Aspose.Cells 功能。

現在我們已經做好準備，讓我們完成在 Excel 工作表中建立小數資料驗證所需的步驟。

## 第 1 步：設定您的文件目錄

在儲存任何文件之前，您需要確保文件目錄設定正確：

```csharp
string dataDir = "Your Document Directory";
```

代替`"Your Document Directory"`以及您要儲存 Excel 檔案的路徑。

## 第 2 步：檢查目錄是否存在

此程式碼片段檢查目錄是否存在，如果不存在則建立它：

```csharp
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```

此步驟就像在開始新專案之前確保您的工作區已準備好一樣。沒有混亂，沒有壓力！

## 第 3 步：建立工作簿對象

接下來，讓我們建立一個新的工作簿對象，它本質上是一個 Excel 檔案：

```csharp
Workbook workbook = new Workbook();
```

將工作簿視為資料的空白畫布。此時，它還沒有內容，但已準備好繪製。

## 第 4 步：建立並存取工作表


現在，讓我們建立一個工作表並存取工作簿中的第一個工作表：

```csharp
Worksheet ExcelWorkSheet = workbook.Worksheets[0];
```

就像一本書有多個頁面一樣，一個工作簿可以有多個工作表。我們目前關注的是第一個。

## 第 5 步：取得驗證集合

現在，讓我們從工作表中提取驗證集合，因為這是我們管理資料驗證規則的地方：

```csharp
ValidationCollection validations = ExcelWorkSheet.Validations;
```

此步驟類似於在開始專案之前檢查工具箱。

## 第 6 步：定義用於驗證的儲存格區域

我們需要定義驗證適用的區域：

```csharp
CellArea ca = new CellArea();
ca.StartRow = 0;
ca.EndRow = 0;
ca.StartColumn = 0;
ca.EndColumn = 0;
```

在這裡，我們規定資料驗證將應用於單一儲存格，特別是工作表中的第一個儲存格 (A1)。

## 第 7 步：建立並新增驗證

讓我們建立驗證物件並將其新增至驗證集合：

```csharp
Validation validation = validations[validations.Add(ca)];
```

現在我們有一個驗證對象，我們將配置它來強制執行我們的小數條件。

## 步驟 8：設定驗證類型

接下來，我們將指定我們想要的驗證類型：

```csharp
validation.Type = ValidationType.Decimal;
```

透過將類型設為小數，我們指示 Excel 在已驗證的儲存格中期望小數值。

## 第 9 步：指定操作員

現在，我們將指定允許值的條件。我們希望確保輸入的資料落在兩個範圍之間：

```csharp
validation.Operator = OperatorType.Between;
```

將其視為繪製邊界線。任何超出此範圍的數字都將被拒絕，以保持您的數據乾淨！

## 第 10 步：建立驗證限制

接下來，我們將設定驗證的下限和上限：

```csharp
validation.Formula1 = Decimal.MinValue.ToString();
validation.Formula2 = Decimal.MaxValue.ToString();
```

有了這些限制，每個十進制數，無論大小，只要有效，都可以被接受！

## 第 11 步：自訂錯誤訊息

讓我們透過添加錯誤訊息來確保用戶知道他們的輸入被拒絕的原因：

```csharp
validation.ErrorMessage = "Please enter a valid integer or decimal number";
```

這會帶來用戶友好的體驗，因為它提供了輸入內容的指導。

## 第 12 步：定義驗證區域

現在，讓我們指定將進行此驗證的儲存格：

```csharp
CellArea area;
area.StartRow = 0;
area.EndRow = 9;
area.StartColumn = 0;
area.EndColumn = 0;
```

在此配置中，我們說驗證適用於單元格 A1 到 A10。

## 第 13 步：新增驗證區域

現在我們已經定義了驗證區域，讓我們應用它：

```csharp
validation.AddArea(area);
```

您的驗證現已牢固到位，準備好捕獲任何不適當的輸入！

## 第 14 步：儲存工作簿

最後，讓我們儲存工作簿並進行十進位資料驗證：

```csharp
workbook.Save(dataDir + "output.out.xls");
```

現在你就擁有了！您已使用 Aspose.Cells for .NET 成功建立了具有十進位資料驗證的工作簿。

## 結論

當您遵循這些簡單的步驟時，使用 Aspose.Cells for .NET 在 Excel 中實作十進位資料驗證是一件輕而易舉的事。您不僅可以確保資料保持乾淨和結構化，還可以提高電子表格中的整體資料完整性，使其可靠且使用者友好。
無論您從事財務、專案管理或任何使用數據報告的領域，掌握這些技能都將顯著提高您的工作效率。所以來吧，試試看吧！您的電子表格會為此感謝您。

## 常見問題解答

### Excel 中的資料驗證是什麼？
Excel 中的資料驗證是一項限制可以在特定儲存格或區域中輸入的資料類型的功能，以確保資料完整性。

### 我可以自訂資料驗證中的錯誤訊息嗎？
是的！您可以提供自訂錯誤訊息，以便在輸入錯誤的資料時指導使用者。

### Aspose.Cells 可以免費使用嗎？
 Aspose.Cells 提供免費試用，但您需要許可證才能長期使用。您可以找到有關獲取臨時許可證的更多信息[這裡](https://purchase.aspose.com/temporary-license/).

### 我可以在 Excel 中驗證哪些資料類型？
使用 Aspose.Cells，您可以驗證各種資料類型，包括整數、小數、日期、清單和自訂公式。

### 在哪裡可以找到更多 Aspose.Cells 文件？
您可以探索廣泛的文檔[這裡](https://reference.aspose.com/cells/net/).