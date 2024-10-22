---
title: 將組合方塊新增至 Excel 中的工作表
linktitle: 將組合方塊新增至 Excel 中的工作表
second_title: Aspose.Cells .NET Excel 處理 API
description: 了解如何使用 Aspose.Cells for .NET 以程式設計方式將組合方塊新增至 Excel 工作表。本逐步指南將引導您完成每個細節。
type: docs
weight: 21
url: /zh-hant/net/excel-shapes-controls/add-combo-box-to-worksheet-excel/
---
## 介紹
建立互動式 Excel 電子表格可以大幅增強使用者體驗，尤其是當您新增組合方塊等表單元素時。組合框允許使用者從預定義清單中選擇選項，從而增加資料輸入的簡單性和效率。透過 Aspose.Cells for .NET，您可以透過程式設計方式在 Excel 工作表中建立組合框，而無需直接使用 Excel。這個功能強大的程式庫允許開發人員以各種方式操作 Excel 文件，包括自動化表單控制項的能力。
在本教學中，我們將引導您完成使用 Aspose.Cells for .NET 將組合方塊新增至 Excel 工作表的過程。如果您希望建立動態、使用者友好的電子表格，本指南將幫助您入門。
## 先決條件
在我們深入研究程式碼之前，讓我們確保您擁有所需的一切：
- Aspose.Cells for .NET：從下列位置下載並安裝 Aspose.Cells for .NET 函式庫：[下載頁面](https://releases.aspose.com/cells/net/).
- .NET Framework：請確定您的電腦上安裝了 .NET Framework。 Aspose.Cells 支援的任何版本都可以使用。
- 開發環境：使用 Visual Studio 等 IDE 來管理專案和編寫程式碼。
-  Aspose 許可證：您可以在評估模式下無需許可證即可工作，但對於完整版本，您需要申請許可證。獲得一個[臨時執照](https://purchase.aspose.com/temporary-license/)如果需要的話。
## 導入包
首先，您需要將所需的命名空間匯入到您的專案中。這是您需要的：
```csharp
using System.IO;
using Aspose.Cells;
```
這些對於與 Excel 檔案互動和操作工作簿中的組合框等表單元素至關重要。
為了便於理解，我們將添加組合框的過程分解為多個簡單的步驟。
## 第 1 步：設定文檔目錄
第一步是建立一個用於儲存 Excel 檔案的目錄。如果新資料夾尚不存在，您可以建立一個。
```csharp
//文檔目錄的路徑。
string dataDir = "Your Document Directory";
//如果目錄尚不存在，則建立該目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
- dataDir：指定輸出檔案的保存位置。
- System.IO.Directory.Exists：檢查目錄是否已存在。
- System.IO.Directory.CreateDirectory：如果目錄遺失，則建立該目錄。
## 第 2 步：建立新工作簿
現在，建立一個新的 Excel 工作簿，您將在其中新增組合方塊。

```csharp
//建立一個新的工作簿。
Workbook workbook = new Workbook();
```

- Workbook 工作簿：初始化 Workbook 類別的新實例，代表 Excel 檔案。
## 第 3 步：取得工作表和儲存格
接下來，存取工作簿中的第一個工作表並檢索將在其中輸入資料的儲存格集合。

```csharp
//取得第一個工作表。
Worksheet sheet = workbook.Worksheets[0];
//取得工作表單元格集合。
Cells cells = sheet.Cells;
```

- 工作表工作表：從工作簿取得第一個工作表。
- Cells cells：從工作表中取得儲存格的集合。
## 第 4 步：為組合框輸入值
現在，我們需要在儲存格中輸入一些值。這些值將用作組合框的選項。

```csharp
//輸入一個值。
cells["B3"].PutValue("Employee:");
//將其設為粗體。
cells["B3"].GetStyle().Font.IsBold = true;
//輸入一些表示組合框輸入範圍的值。
cells["A2"].PutValue("Emp001");
cells["A3"].PutValue("Emp002");
cells["A4"].PutValue("Emp003");
cells["A5"].PutValue("Emp004");
cells["A6"].PutValue("Emp005");
cells["A7"].PutValue("Emp006");
```

- 細胞["B3"].PutValue：將標籤「Employee」放置在儲存格 B3 中。
- Font.IsBold = true：將文字設為粗體使其反白。
- 輸入範圍：在A2至A7儲存格中輸入多個員工ID。這些將出現在組合框下拉清單中。
## 步驟 5：將組合方塊新增至工作表中
下一步是將組合框控制項新增到工作表中。此組合方塊將允許使用者選擇您先前輸入的員工 ID 之一。

```csharp
//新增一個新的組合框。
Aspose.Cells.Drawing.ComboBox comboBox = sheet.Shapes.AddComboBox(2, 0, 2, 0, 22, 100);
```

- AddComboBox：為工作表新增新的組合方塊。數字 (2, 0, 2, 0, 22, 100) 表示組合框的位置和尺寸。
## 第 6 步：將組合框連結到儲存格並設定輸入範圍
為了使組合框發揮作用，我們需要將其連結到特定單元格並定義它將從中提取選項的單元格範圍。

```csharp
//設定連結的儲存格。
comboBox.LinkedCell = "A1";
//設定輸入範圍。
comboBox.InputRange = "A2:A7";
```

- LinkedCell：將組合方塊的選擇連結到儲存格 A1。從組合方塊中選取的值將會出現在該儲存格中。
- 輸入範圍：定義包含將填滿組合框選項的值的儲存格範圍 (A2:A7)。
## 第 7 步：自訂組合框外觀
您可以透過指定下拉行數並啟用 3D 著色來進一步自訂組合框，以獲得更好的美觀效果。

```csharp
//設定編號。組合框清單部分中顯示的清單行數。
comboBox.DropDownLines = 5;
//使用 3-D 陰影設定組合框。
comboBox.Shadow = true;
```

- DropDownLines：控制組合方塊下拉清單中一次可見的選項數量。
- 陰影：為組合框添加 3D 陰影效果。
## 步驟 8：自動調整列並儲存工作簿
最後，讓我們自動調整列以獲得乾淨的佈局並儲存工作簿。

```csharp
//自動調整列
sheet.AutoFitColumns();
//儲存文件。
workbook.Save(dataDir + "book1.out.xls");
```

- AutoFitColumns：自動調整列寬以適合內容。
- 儲存：將工作簿另存為Excel檔案到指定目錄中。

## 結論
使用 Aspose.Cells for .NET 將組合方塊新增至 Excel 工作表是一個簡單的過程，可大幅提高資料輸入的靈活性。透過以程式設計方式建立表單控制項，您可以輕鬆建立互動式電子表格。本教學向您展示如何新增組合方塊、將其連結到儲存格以及配置其輸入範圍，所有這些都使用 Aspose.Cells。
 Aspose.Cells 提供了廣泛的 Excel 檔案操作功能，使其成為希望自動化電子表格任務的開發人員的理想選擇。嘗試一下[免費試用](https://releases.aspose.com/).
## 常見問題解答
### 我可以在沒有安裝 Excel 的情況下使用 Aspose.Cells 嗎？
是的，Aspose.Cells 獨立於 Excel 工作，不需要安裝 Excel。
### 如何在 Aspose.Cells 中申請許可證？
您可以透過以下方式申請許可證：[這裡](https://purchase.aspose.com/buy)並打電話`License.SetLicense()`在你的程式碼中。
### Aspose.Cells 支援哪些格式儲存檔案？
Aspose.Cells 支援以多種格式儲存文件，如 XLSX、XLS、CSV、PDF 等。
### 我可以添加的組合框數量有限制嗎？
不，沒有嚴格限制；您可以根據項目需求新增任意數量的組合方塊。
### 我如何獲得 Aspose.Cells 的支援？
您可以從以下方面獲得支持[Aspose論壇](https://forum.aspose.com/c/cells/9).