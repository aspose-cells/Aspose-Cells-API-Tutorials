---
title: 在 Excel 中新增工作表 C# 教學課程
linktitle: 在 Excel 中新增工作表
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 在 Excel 中新增工作表。帶有 C# 原始程式碼的逐步教程。
type: docs
weight: 20
url: /zh-hant/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
在本教學中，我們將逐步解釋使用 Aspose.Cells for .NET 在 Excel 中新增工作表的 C# 原始程式碼。將新工作表新增至 Excel 工作簿是建立報表或操作資料時的常見動作。 Aspose.Cells 是一個功能強大的函式庫，可以輕鬆使用 .NET 操作和產生 Excel 檔案。請按照以下步驟瞭解並實作此程式碼。

## 第 1 步：文檔目錄設置

第一步是定義儲存 Excel 檔案的文檔目錄。如果該目錄不存在，我們使用以下程式碼建立它：

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENTS DIRECTORY";
//如果該目錄尚不存在，則建立該目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

請務必將「您的文件目錄」替換為文件目錄的適當路徑。

## 第 2 步：實例化工作簿對象

第二步是實例化一個 Workbook 對象，它代表 Excel 工作簿。使用以下程式碼：

```csharp
Workbook workbook = new Workbook();
```

該物件將用於新增工作表以及對 Excel 工作簿執行其他操作。

## 步驟 3：新增工作表

第三步是為 Workbook 物件新增一個新工作表。使用以下程式碼：

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

這將向 Workbook 物件新增一個新工作表，並且您將使用其索引來獲得對此工作表的參考。

## 第四步：設定新工作表的名稱

第四步是為新工作表命名。您可以使用以下程式碼來設定工作表名稱：

```csharp
worksheet.Name = "My Worksheet";
```

將“我的電子表格”替換為新工作表所需的名稱。

## 步驟 5：儲存 Excel 文件

最後最後一步是儲存Excel檔案。使用以下程式碼：

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

這會將帶有新工作表的 Excel 工作簿儲存到您指定的文件目錄中。

### 使用 Aspose.Cells for .NET 在 Excel C# 教學課程中新增工作表的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目錄尚不存在，則建立該目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
//實例化 Workbook 物件
Workbook workbook = new Workbook();
//將新工作表新增至 Workbook 對象
int i = workbook.Worksheets.Add();
//透過傳遞工作表索引來取得新新增的工作表的引用
Worksheet worksheet = workbook.Worksheets[i];
//設定新新增的工作表名稱
worksheet.Name = "My Worksheet";
//儲存 Excel 文件
workbook.Save(dataDir + "output.out.xls");
```

## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 在 Excel 中新增工作表。您可以使用此方法使用 C# 操作和產生 Excel 檔案。 Aspose.Cells 提供了許多強大的功能來簡化應用程式中 Excel 檔案的處理。

### 常見問題 (FAQ)

#### 我可以將 Aspose.Cells 與 C# 以外的其他程式語言一起使用嗎？

是的，Aspose.Cells 支援多種程式語言，例如 Java、Python、Ruby 等。

#### 我可以為新建立的工作表中的儲存格新增格式嗎？

是的，您可以使用 Aspose.Cells 的 Worksheet 類別提供的方法將格式套用到儲存格。您可以設定儲存格樣式、變更背景顏色、套用邊框等。

#### 如何從新工作表存取儲存格資料？

您可以使用 Aspose.Cells 的 Worksheet 類別提供的屬性和方法來存取單元格資料。例如，您可以使用 Cells 屬性存取特定儲存格並檢索或修改其值。

#### Aspose.Cells 支援 Excel 中的公式嗎？

是的，Aspose.Cells 支援 Excel 公式。您可以使用 Cell 類別的 SetFormula 方法在工作表儲存格中設定公式。
