---
title: 使用內容類型屬性
linktitle: 使用內容類型屬性
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 處理內容類型屬性。
type: docs
weight: 180
url: /zh-hant/net/excel-workbook/working-with-content-type-properties/
---
內容類型屬性在使用 .NET 的 Aspose.Cells 庫管理和操作 Excel 檔案時發揮著至關重要的作用。這些屬性可讓您為 Excel 檔案定義其他元數據，從而更輕鬆地組織和尋找數據。在本教學中，我們將使用範例 C# 程式碼逐步引導您了解和使用內容類型屬性。

## 先決條件

在開始之前，請確保您具備以下條件：

- Aspose.Cells for .NET 安裝在您的開發電腦上。
- 與 C# 相容的整合開發環境 (IDE)，例如 Visual Studio。

## 第一步：建構環境

在開始使用內容類型屬性之前，請確保您已使用 Aspose.Cells for .NET 設定開發環境。您可以在專案中新增對 Aspose.Cells 庫的引用，並將所需的命名空間匯入到您的類別中。

```csharp
using Aspose.Cells;
```

## 步驟 2：建立新的 Excel 工作簿

首先，我們將使用以下命令建立一個新的 Excel 工作簿`Workbook`Aspose.Cells 提供的類別。以下程式碼示範如何建立新的 Excel 工作簿並將其儲存在指定的輸出目錄中。

```csharp
//目的地目錄
string outputDir = RunExamples.Get_OutputDirectory();

//建立新的 Excel 工作簿
Workbook workbook = new Workbook(FileFormatType.Xlsx);
```

## 步驟 3：新增內容類型屬性

現在我們有了 Excel 工作簿，我們可以使用以下命令新增內容類型屬性`Add`的方法`ContentTypeProperties`的集合`Workbook`班級。每個屬性都由名稱和值表示。你

  您也可以指定屬性的資料類型。

```csharp
//新增第一個內容類型屬性
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;

//新增第二個內容類型屬性
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
```

## 步驟 4：儲存 Excel 工作簿

新增內容類型屬性後，我們可以儲存變更後的 Excel 工作簿。使用`Save`的方法`Workbook`class 指定輸出目錄和檔案名稱。

```csharp
//儲存 Excel 工作簿
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
```

### 使用 Aspose.Cells for .NET 處理內容類型屬性的範例原始碼 
```csharp
//來源目錄
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(FileFormatType.Xlsx);
int index = workbook.ContentTypeProperties.Add("MK31", "Simple Data");
workbook.ContentTypeProperties[index].IsNillable = false;
index = workbook.ContentTypeProperties.Add("MK32", DateTime.Now.ToString("yyyy-MM-dd'T'hh:mm:ss"), "DateTime");
workbook.ContentTypeProperties[index].IsNillable = true;
workbook.Save(outputDir + "WorkingWithContentTypeProperties_out.xlsx");
Console.WriteLine("WorkingWithContentTypeProperties executed successfully.");
```

## 結論

恭喜！您學習如何使用 Aspose.Cells for .NET 處理內容類型屬性。現在，您可以將自訂元資料新增至 Excel 檔案並更有效地管理它們。

### 常見問題解答

#### Q：內容類型屬性是否與所有版本的 Excel 相容？

答：是的，內容類型屬性與所有版本的 Excel 中建立的 Excel 檔案相容。

#### Q：將內容類型屬性新增至 Excel 工作簿後是否可以進行編輯？

答：是的，您可以隨時變更內容類型屬性，方法是轉至`ContentTypeProperties`的集合`Workbook`類別並使用 和 p 方法適當的屬性。

#### Q：儲存為 PDF 時是否支援內容類型屬性？

答：不可以，儲存為 PDF 時不支援內容類型屬性。它們特定於 Excel 文件。