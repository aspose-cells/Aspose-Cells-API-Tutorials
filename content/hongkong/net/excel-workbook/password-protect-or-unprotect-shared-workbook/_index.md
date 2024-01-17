---
title: 密碼保護或取消保護共享工作簿
linktitle: 密碼保護或取消保護共享工作簿
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 對共用工作簿進行密碼保護或取消保護。
type: docs
weight: 120
url: /zh-hant/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
使用密碼保護共享工作簿對於確保資料隱私非常重要。透過 Aspose.Cells for .NET，您可以使用密碼輕鬆保護或取消保護共用工作簿。請按照以下步驟操作以獲得所需的結果：

## 步驟1：指定輸出目錄

首先，您需要指定儲存受保護的 Excel 檔案的輸出目錄。以下是使用 Aspose.Cells 執行此操作的方法：

```csharp
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

## 步驟 2：建立一個空的 Excel 文件

然後，您可以建立一個要對其套用保護或取消保護的空白 Excel 檔案。這是範例程式碼：

```csharp
//建立一個空白的 Excel 工作簿
Workbook wb = new Workbook();
```

## 步驟 3：保護或取消保護共享工作簿

建立工作簿後，您可以透過指定適當的密碼來保護或取消保護共用工作簿。就是這樣：

```csharp
//使用密碼保護共享工作簿
wb.ProtectSharedWorkbook("1234");

//取消註釋此行以取消對共享工作簿的保護
//wb.UnprotectSharedWorkbook("1234");
```

## 步驟 4：儲存輸出 Excel 文件

套用保護或取消保護後，您可以將受保護的 Excel 檔案儲存到指定的輸出目錄。操作方法如下：

```csharp
//儲存輸出的 Excel 文件
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 進行密碼保護或取消保護共用工作簿的範例原始程式碼 
```csharp
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
//建立空白 Excel 文件
Workbook wb = new Workbook();
//使用密碼保護共享工作簿
wb.ProtectSharedWorkbook("1234");
//取消註釋此行以取消對共享工作簿的保護
//wb.UnprotectSharedWorkbook("1234");
//儲存輸出的 Excel 文件
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## 結論

使用密碼保護或取消保護共享工作簿對於確保資料安全至關重要。使用 Aspose.Cells for .NET，您可以輕鬆地將此功能新增至您的 Excel 檔案。透過按照本指南中的步驟操作，您可以使用密碼有效地保護或取消保護您的共用工作簿。嘗試使用您自己的 Excel 文件，並確保維護敏感資料的安全性。

### 常見問題解答

#### Q：我可以對與 Aspose.Cells 共享的工作簿套用哪些類型的保護？
    
答：使用Aspose.Cells，您可以透過指定密碼來保護共用工作簿，以防止未經授權的存取、修改或刪除資料。

#### Q：我可以在不指定密碼的情況下保護共享工作簿嗎？
    
答：是的，您無需指定密碼即可保護共用工作簿。但是，建議使用強密碼以獲得更好的安全性。

#### Q：如何取消保護與 Aspose.Cells 共享的工作簿？
    
答：若要取消共用工作簿的保護，您必須指定與保護工作簿時所使用的密碼相同的密碼。這樣就可以解除保護並自由存取資料。

#### Q：保護共享工作簿是否會影響工作簿中的功能和公式？
    
答：當您保護共用工作簿時，使用者仍然可以存取工作簿中的功能和公式。保護僅影響工作簿的結構變更。