---
title: 編輯 Excel 工作表中的範圍
linktitle: 編輯 Excel 工作表中的範圍
second_title: Aspose.Cells for .NET API 參考
description: 了解使用 Aspose.Cells for .NET 編輯 Excel 電子表格中的特定範圍。 C# 逐步教學。
type: docs
weight: 20
url: /zh-hant/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel 是用於建立和管理電子表格的強大工具，提供許多控制和保護資料的功能。其中一項功能是允許使用者編輯工作表中的特定範圍，同時保護其他部分。在本教學中，我們將逐步指導您使用 Aspose.Cells for .NET（一個用於以程式設計方式處理 Excel 檔案的熱門程式庫）來實現此功能。

使用 Aspose.Cells for .NET 將允許您輕鬆操作 Excel 電子表格中的範圍，提供使用者友好的介面和進階功能。請依照下列步驟允許使用者使用 Aspose.Cells for .NET 編輯 Excel 電子表格中的特定範圍。
## 第一步：建構環境

確保您的開發環境中安裝了 Aspose.Cells for .NET。從Aspose官方網站下載庫並查看文件以取得安裝說明。

## 步驟2：初始化工作簿和工作表

首先，我們需要建立一個新工作簿並取得要允許更改範圍的工作表的參考。使用以下程式碼來實現此目的：

```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENTS DIRECTORY";
//如果該目錄尚不存在，則建立該目錄。
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

//實例化新工作簿
Workbook workbook = new Workbook();

//取得第一個工作表（預設）
Worksheet sheet = workbook.Worksheets[0];
```

在此程式碼片段中，我們首先定義儲存 Excel 檔案的目錄路徑。接下來，我們建立一個新的實例`Workbook`類別並使用以下命令取得第一個工作表的引用`Worksheets`財產。

## 第 3 步：取得可編輯範圍

現在我們需要檢索我們想要允許修改的範圍。使用以下程式碼：

```csharp
//取得可修改範圍
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## 第四步：設定保護範圍

在允許修改範圍之前，我們需要定義一個受保護的範圍。就是這樣：

```csharp
//定義保護範圍
ProtectedRange ProtectedRange;

//創建範圍
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

在此程式碼中，我們建立了一個新實例`ProtectedRange`類別並使用`Add`方法指定要保護的範圍。

## 第 5 步：指定密碼

為了增強安全性，您可以為保護範圍指定密碼。就是這樣：

```csharp
//指定密碼
protectedBeach.Password = "YOUR_PASSWORD";
```

## 步驟 6：保護工作表

現在我們已經設定了保護範圍，我們就可以保護工作表以防止未經授權的修改。使用以下程式碼：

```csharp
//保護工作表
leaf.Protect(ProtectionType.All);
```

## 步驟 7：儲存 Excel 文件

最後，我們儲存所做更改的 Excel 檔案。這是必要的程式碼：

```csharp
//儲存 Excel 文件
workbook.Save(dataDir + "protectedrange.out.xls");
```

### 使用 Aspose.Cells for .NET 在 Excel 工作表中編輯範圍的範例原始程式碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//如果目錄尚不存在，則建立該目錄。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);

//實例化一個新的工作簿
Workbook book = new Workbook();

//取得第一個（預設）工作表
Worksheet sheet = book.Worksheets[0];

//取得允許編輯範圍
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;

//定義保護範圍
ProtectedRange proteced_range;

//創建範圍
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];

//指定密碼
proteced_range.Password = "YOUR_PASSWORD";

//保護板材
sheet.Protect(ProtectionType.All);

//儲存 Excel 文件
book.Save(dataDir + "protectedrange.out.xls");
```

## 結論

恭喜！您學習如何允許使用者使用 Aspose.Cells for .NET 編輯 Excel 電子表格中的特定範圍。現在您可以在自己的專案中應用此技術並提高 Excel 檔案的安全性。


#### 常見問題解答

#### Q：為什麼我應該使用 Aspose.Cells for .NET 來編輯 Excel 電子表格中的範圍？

答：Aspose.Cells for .NET 提供了強大且易於使用的 API 來處理 Excel 檔案。它提供了高級功能，例如範圍操作、工作表保護等。

#### Q：我可以在工作表中設定多個可編輯範圍嗎？

答：是的，您可以使用`Add`的方法`ProtectedRangeCollection`收藏。每個範圍都可以有自己的保護設定。

####  Q：定義可編輯範圍後是否可以刪除？

答：是的，您可以使用`RemoveAt`的方法`ProtectedRangeCollection`集合透過指定其索引來刪除特定的可編輯範圍。

#### Q：儲存後如何開啟受保護的 Excel 檔案？

答：您需要提供建立保護範圍時指定的密碼才能開啟受保護的 Excel 檔案。請務必將密碼保存在安全的地方，以防止遺失資料存取權限。