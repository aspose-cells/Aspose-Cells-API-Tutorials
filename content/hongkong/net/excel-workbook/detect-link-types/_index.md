---
title: 檢測連結類型
linktitle: 檢測連結類型
second_title: Aspose.Cells for .NET API 參考
description: 使用 Aspose.Cells for .NET 偵測 Excel 工作簿中的連結類型。
type: docs
weight: 80
url: /zh-hant/net/excel-workbook/detect-link-types/
---
在本教學中，我們將逐步引導您完成所提供的 C# 原始程式碼，使您能夠使用 Aspose.Cells for .NET 來偵測 Excel 工作簿中的連結類型。請按照以下步驟執行此操作。

## 第1步：設定來源目錄

```csharp
//來源目錄
string SourceDir = RunExamples.Get_SourceDirectory();
```

在第一步中，我們定義包含連結的 Excel 工作簿所在的來源目錄。

## 第 2 步：載入 Excel 工作簿

```csharp
//載入 Excel 工作簿
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

我們使用來源檔案路徑載入 Excel 工作簿。

## 第 3 步：取得電子表格

```csharp
//取得第一個工作表（預設）
Worksheet worksheet = workbook.Worksheets[0];
```

我們得到工作簿的第一個工作表。您可以更改`[0]`如果需要，可以使用索引來存取特定的工作表。

## 步驟 4：建立單元格範圍

```csharp
//建立單元格區域 A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

我們建立一系列儲存格，在此範例中從儲存格 A1 到儲存格 A7。您可以根據需要調整儲存格參考。

## 第五步：取得範圍內的超鏈接

```csharp
//獲取範圍內的超鏈接
Hyperlink[] hyperlinks = range.Hyperlinks;
```

我們獲得指定範圍內存在的所有超連結。

## 步驟 6：瀏覽超連結並查看連結類型

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

我們循環遍歷每個連結並顯示顯示文字和關聯的連結類型。

### 使用 Aspose.Cells for .NET 偵測連結類型的範例原始碼 
```csharp
//來源目錄
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
//取得第一個（預設）工作表
Worksheet worksheet = workbook.Worksheets[0];
//建立範圍 A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
//獲取範圍內的超鏈接
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## 結論

恭喜！您已了解如何使用 Aspose.Cells for .NET 偵測 Excel 工作簿中的連結類型。此功能可讓您使用 Excel 工作簿中的超連結。不斷探索 Aspose.Cells 的功能來擴展您的 Excel 工作簿處理能力。

### 常見問題解答

#### Q：如何在我的專案中安裝 Aspose.Cells for .NET？

答：您可以使用 NuGet 套件管理器安裝 Aspose.Cells for .NET。搜尋[Aspose 發布](https://releases.aspose.com/cells/net)在 NuGet 套件管理器控制台中並安裝最新版本。

#### Q：我可以檢測特定工作表而不是第一個工作表中的連結類型嗎？

答：是的，您可以修改`workbook.Worksheets[0]`用於存取特定工作表的索引。例如，要存取第二張表，請使用`workbook.Worksheets[1]`.

#### Q：是否可以修改範圍內偵測到的連結類型？

答：是的，您可以瀏覽超連結並執行編輯操作，例如更新 URL 或刪除不需要的連結。

#### Q：Aspose.Cells for .NET 中可以使用哪些類型的連結？

答：可能的連結類型包括超連結、其他工作表的連結、外部文件的連結、網站的連結等。

#### Q：Aspose.Cells for .NET 支援在電子表格中建立新連結嗎？

答：是的，Aspose.Cells for .NET 支援使用以下命令建立新鏈接`Hyperlink`類別及其相關屬性。您可以新增超連結、URL 連結、其他電子表格的連結等。

#### Q：我可以在 Web 應用程式中使用 Aspose.Cells for .NET 嗎？

答：是的，Aspose.Cells for .NET 可以在 Web 應用程式中使用。您可以將其嵌入到 ASP.NET、ASP.NET Core 和其他基於 .NET 的 Web 框架中。

#### Q：使用 Aspose.Cells for .NET 時有檔案大小限制嗎？

答：Aspose.Cells for .NET 可以處理大型 Excel 工作簿，沒有特定限制。但是，實際檔案大小可能受到可用系統資源的限制。