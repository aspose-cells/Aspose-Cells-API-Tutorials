---
title: 允許使用者編輯 Excel 工作表中的範圍
linktitle: 允許使用者編輯 Excel 工作表中的範圍
second_title: Aspose.Cells for .NET API 參考
description: 允許使用者使用 Aspose.Cells for .NET 編輯 Excel 電子表格中的特定範圍。帶有 C# 原始程式碼的逐步指南。
type: docs
weight: 10
url: /zh-hant/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
在本指南中，我們將引導您了解如何使用 Aspose.Cells for .NET 來允許使用者編輯 Excel 電子表格中的特定範圍。請依照以下步驟完成此任務。

## 第一步：建構環境

確保您已設定開發環境並安裝 Aspose.Cells for .NET。您可以從Aspose官方網站下載最新版本的程式庫。

## 步驟2：導入所需的命名空間

在您的 C# 專案中，匯入必要的命名空間以使用 Aspose.Cells：

```csharp
using Aspose.Cells;
```

## 第三步：設定文檔目錄路徑

聲明一個`dataDir`變數來指定要儲存產生的 Excel 檔案的目錄的路徑：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

一定要更換`"YOUR_DOCUMENT_DIRECTORY"`與系統上的正確路徑。

## 第 4 步：建立工作簿對象

實例化一個新的 Workbook 對象，該物件代表要建立的 Excel 工作簿：

```csharp
Workbook book = new Workbook();
```

## 第 5 步：存取第一個工作表

使用下列程式碼導覽至 Excel 工作簿中的第一個工作表：

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 步驟 6：檢索授權修改範圍

使用以下命令取得允許編輯範圍的集合`AllowEditRanges`財產：

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## 步驟 7：定義保護範圍

使用以下命令定義受保護範圍`Add`的方法`AllowEditRanges`收藏：

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

在這裡，我們創建了一個從單元格 A1 到單元格 C3 的受保護範圍「r2」。

## 步驟 8：指定密碼

使用以下命令指定受保護範圍的密碼`Password`財產：

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

一定要更換`"YOUR_PASSWORD"`使用所需的密碼。

## 步驟 9：保護工作表

使用以下命令保護工作表`Protect`的方法`Worksheet`目的：

```csharp
sheet.Protect(ProtectionType.All);
```

這將透過防止任何超出允許範圍的修改來保護電子表格。

## 第 10 步：註冊

  Excel文件

使用以下命令儲存產生的 Excel 文件`Save`的方法`Workbook`目的：

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

請務必指定所需的檔案名稱和正確的路徑。

### 允許使用者使用 Aspose.Cells for .NET 在 Excel 工作表中編輯範圍的範例原始程式碼 
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
proteced_range.Password = "123";
//保護板材
sheet.Protect(ProtectionType.All);
//儲存 Excel 文件
book.Save(dataDir + "protectedrange.out.xls");
```

## 結論

現在您已經了解如何使用 Aspose.Cells for .NET 來允許使用者編輯 Excel 電子表格中的特定範圍。請隨意進一步探索 Aspose.Cells 提供的功能來滿足您的特定需求。


### 常見問題解答

#### 1. 如何允許使用者編輯Excel電子表格中的特定範圍？

您可以使用`ProtectedRangeCollection`類別來定義允許的修改範圍。使用`Add`方法用所需的儲存格建立新的受保護範圍。

#### 2. 授權修改範圍可以設定密碼嗎？

是的，您可以使用指定密碼`Password`的財產`ProtectedRange`目的。這將限制僅具有密碼的使用者進行存取。

#### 3. 設定允許的範圍後，如何保護電子表格？

使用`Protect`的方法`Worksheet`物件保護工作表。這將防止任何超出允許範圍的更改，如果您指定了密碼，可能會提示輸入密碼。