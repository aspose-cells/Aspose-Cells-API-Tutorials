---
title: Excel 工作表的進階保護設定
linktitle: Excel 工作表的進階保護設定
second_title: Aspose.Cells for .NET API 參考
description: 透過使用 Aspose.Cells for .NET 設定進階保護設定來保護您的 Excel 檔案。
type: docs
weight: 10
url: /zh-hant/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
在本教學中，我們將引導您完成使用 .NET 的 Aspose.Cells 庫為 Excel 電子表格設定進階保護設定的步驟。請按照以下說明完成此任務。

## 第 1 步：準備

確保您已安裝 Aspose.Cells for .NET 並在您首選的整合開發環境 (IDE) 中建立了 C# 專案。

## 第二步：設定文檔目錄路徑

聲明一個`dataDir`變數並使用文檔目錄的路徑對其進行初始化。例如 ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENTS_DIRECTORY"`與目錄的實際路徑。

## 步驟 3：建立文件流程以開啟 Excel 文件

創建一個`FileStream`包含要開啟的 Excel 檔案的物件：

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

確保您有 Excel 文件`book1.xls`在您的文件目錄中或指定正確的檔案名稱和位置。

## 步驟 4：實例化 Workbook 物件並開啟 Excel 文件

使用`Workbook`Aspose.Cells 中的類別實例化 Workbook 物件並透過檔案流開啟指定的 Excel 檔案：

```csharp
Workbook excel = new Workbook(fstream);
```

## 第 5 步：存取第一個工作表

導覽至 Excel 文件的第一個工作表：

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## 步驟 6：設定工作表保護設定

使用工作表物件屬性根據需要設定工作表保護設定。例如 ：

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ....依需求設定其他保護設定...
```

## 步驟7：儲存修改後的Excel文件

使用以下命令儲存修改後的 Excel 文件`Save`Workbook物件的方法：

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

請務必指定輸出檔案所需的路徑和檔案名稱。

## 第8步：關閉文件流

儲存後，關閉檔案流以釋放所有關聯資源：

```csharp
fstream.Close();
```
	
### 使用 Aspose.Cells for .NET 的 Excel 工作表進階保護設定的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立包含要開啟的 Excel 檔案的檔案流
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//實例化 Workbook 物件
//透過檔案流程開啟Excel文件
Workbook excel = new Workbook(fstream);
//存取 Excel 文件中的第一個工作表
Worksheet worksheet = excel.Worksheets[0];
//限制使用者刪除工作表的列
worksheet.Protection.AllowDeletingColumn = false;
//限制使用者刪除工作表的行
worksheet.Protection.AllowDeletingRow = false;
//限制使用者編輯工作表內容
worksheet.Protection.AllowEditingContent = false;
//限制使用者編輯工作表的對象
worksheet.Protection.AllowEditingObject = false;
//限制使用者編輯工作表的場景
worksheet.Protection.AllowEditingScenario = false;
//限制用戶過濾
worksheet.Protection.AllowFiltering = false;
//允許使用者設定工作表單元格的格式
worksheet.Protection.AllowFormattingCell = true;
//允許使用者設定工作表行的格式
worksheet.Protection.AllowFormattingRow = true;
//允許使用者在工作表中插入列
worksheet.Protection.AllowFormattingColumn = true;
//允許使用者在工作表中插入超連結
worksheet.Protection.AllowInsertingHyperlink = true;
//允許使用者在工作表中插入行
worksheet.Protection.AllowInsertingRow = true;
//允許使用者選擇工作表的鎖定儲存格
worksheet.Protection.AllowSelectingLockedCell = true;
//允許使用者選擇工作表中未鎖定的儲存格
worksheet.Protection.AllowSelectingUnlockedCell = true;
//允許使用者排序
worksheet.Protection.AllowSorting = true;
//允許使用者在工作表中使用資料透視表
worksheet.Protection.AllowUsingPivotTable = true;
//儲存修改後的Excel文件
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
//關閉文件流以釋放所有資源
fstream.Close();
```

## 結論

恭喜！現在您已經了解如何使用 Aspose.Cells for .NET 為 Excel 電子表格設定進階保護設定。使用這些知識來保護您的 Excel 檔案並限制使用者操作。

### 常見問題解答

#### Q：如何在 IDE 中建立新的 C# 專案？

答：建立新 C# 專案的步驟可能會有所不同，具體取決於您使用的 IDE。有關詳細說明，請參閱 IDE 的文檔。

#### Q：除了教學中提到的設定之外，是否可以設定自訂保護設定？

答：是的，Aspose.Cells 提供了廣泛的保護設置，您可以根據自己的特定需求進行自訂。有關更多詳細信息，請參閱 Aspose.Cells 文件。

#### Q：範例程式碼中修改後的Excel檔案用什麼檔案格式儲存？

答：在範例程式碼中，修改後的Excel檔案以Excel 97-2003（.xls）格式儲存。如果需要，您可以選擇 Aspose.Cells 支援的其他格式。

#### Q：如何存取 Excel 文件中的其他工作表？

答：您可以使用索引或工作表名稱存取其他工作表，例如：`Worksheet worksheet = excel.Worksheets[1];`或者`Worksheet worksheet = excel.Worksheets[" SheetName"];`.