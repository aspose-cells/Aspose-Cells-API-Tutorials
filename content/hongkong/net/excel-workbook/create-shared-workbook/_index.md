---
title: 建立共享工作簿
linktitle: 建立共享工作簿
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 建立 Excel 共享工作簿以實現並發資料協作。
type: docs
weight: 70
url: /zh-hant/net/excel-workbook/create-shared-workbook/
---
在本教程中，我們將引導您完成所提供的 C# 原始程式碼，該程式碼將允許您使用 Aspose.Cells for .NET 建立共用工作簿。請按照以下步驟執行此操作。

## 第1步：設定輸出目錄

```csharp
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

在第一步驟中，我們定義將儲存共享工作簿的輸出目錄。

## 第 2 步：建立工作簿對象

```csharp
//建立工作簿對象
Workbook wb = new Workbook();
```

我們正在建立一個新的 Workbook 物件來代表我們的 Excel 工作簿。

## 步驟 3：啟用工作簿共享

```csharp
//分享工作簿
wb.Settings.Shared = true;
```

我們透過設定來啟用工作簿的共享功能`Shared`Workbook 物件的屬性`true`.

## 步驟 4：儲存共享工作簿

```csharp
//儲存共享工作簿
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

我們透過指定輸出檔案的路徑和名稱來保存共享工作簿。

### 使用 Aspose.Cells for .NET 建立共享工作簿的範例原始程式碼 
```csharp
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
//建立工作簿對象
Workbook wb = new Workbook();
//分享工作簿
wb.Settings.Shared = true;
//儲存共享工作簿
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## 結論

恭喜！您學習如何使用 Aspose.Cells for .NET 建立共用工作簿。多個使用者可以同時使用共享工作簿來協作處理資料。使用您自己的數據進行實驗並進一步探索 Aspose.Cells 的功能，以建立強大且個人化的 Excel 工作簿。

### 常見問題解答

#### Q：什麼是共享工作簿？

答：共享工作簿是可供多個使用者同時使用以協同處理資料的 Excel 工作簿。每個使用者都可以對工作簿進行更改，其他使用者將即時看到更新。

#### Q：如何在 Aspose.Cells for .NET 中啟用工作簿共用？

答：要在 Aspose.Cells for .NET 中啟用工作簿共享，您必須設定`Shared`Workbook 物件的屬性`true`。這將允許使用者同時處理工作簿。

#### Q：我可以限制共享工作簿中的使用者權限嗎？

答：是的，您可以使用 Excel 的安全功能限制共用工作簿中的使用者權限。您可以為每個使用者設定特定的權限，例如編輯、唯讀等。

#### Q：如何與其他使用者分享工作簿？

答：建立共用工作簿後，您可以透過向其他使用者發送 Excel 檔案來與他們共用。其他用戶將能夠打開該文件並同時對其進行處理。

#### Q：共享工作簿是否支援所有 Excel 功能？

答：共用工作簿支援大多數 Excel 功能。但是，某些進階功能（例如巨集和加載項）在共用工作簿中使用時可能有限製或約束。