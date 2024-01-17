---
title: XLSB檔案的外部連線讀寫
linktitle: XLSB檔案的外部連線讀寫
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 讀取和修改 XLSB 檔案的外部連線。
type: docs
weight: 130
url: /zh-hant/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
讀取和寫入 XLSB 檔案的外部連線對於在 Excel 工作簿中操作來自外部來源的資料至關重要。使用 Aspose.Cells for .NET，您可以使用以下步驟輕鬆讀取和寫入外部連線：

## 步驟1：指定來源目錄和輸出目錄

首先，您必須指定包含外部連線的 XLSB 檔案所在的來源目錄，以及要儲存修改後的檔案的輸出目錄。以下是使用 Aspose.Cells 執行此操作的方法：

```csharp
//來源目錄
string sourceDir = RunExamples.Get_SourceDirectory();

//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
```

## 步驟 2：載入來源 Excel XLSB 文件

接下來，您需要載入要對其進行外部連線讀寫操作的來源Excel XLSB檔案。這是範例程式碼：

```csharp
//載入來源 Excel XLSB 文件
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## 第三步：讀取並修改外部連接

載入檔案後，您可以存取第一個外部連接，它實際上是一個資料庫連接。您可以讀取和修改外部連線的各種屬性。就是這樣：

```csharp
//讀取第一個外部連接，這是一個資料庫連接
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

//顯示資料庫連線名稱、命令和連接訊息
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

//修改連接名稱
dbCon.Name = "NewCustomer";
```

## 步驟 4：儲存輸出 Excel XLSB 文件

進行必要的變更後，您可以將修改後的 Excel XLSB 檔案儲存到指定的輸出目錄。操作方法如下：

```csharp
//儲存輸出 Excel XLSB 文件
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 讀取和寫入 XLSB 檔案外部連接的範例原始程式碼 
```csharp
//原始碼目錄
string sourceDir = RunExamples.Get_SourceDirectory();
//輸出目錄
string outputDir = RunExamples.Get_OutputDirectory();
//載入來源 Excel Xlsb 文件
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//讀取第一個外部連接，它實際上是一個 DB-Connection
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//列印 DB 連接的名稱、命令和連接訊息
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//修改連接名稱
dbCon.Name = "NewCust";
//儲存 Excel Xlsb 文件
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## 結論

透過讀取和寫入 XLSB 檔案的外部連接，您可以在 Excel 工作簿中操作來自外部來源的資料。使用 Aspose.Cells for .NET，您可以輕鬆存取外部連接、讀取和修改連接資訊以及儲存變更。試驗您自己的 XLSB 檔案並利用 Excel 應用程式中外部連接的強大功能。

### 常見問題解答

#### Q：XLSB 檔案中的外部連線是什麼？
    
答：XLSB檔案中的外部連線是指與外部資料來源（例如資料庫）建立的連線。它允許您將此外部來源中的資料匯入到 Excel 工作簿中。

#### Q：XLSB 檔案中可以有多個外部連線嗎？
     
答：是的，一個 XLSB 檔案中可以有多個外部連線。您可以透過存取每個連接對象來單獨管理它們。

#### Q：如何使用 Aspose.Cells 讀取 XLSB 檔案中外部連接的詳細資訊？
     
答：您可以使用Aspose.Cells提供的功能來存取外部連線的屬性，例如連線名稱、關聯指令和連線資訊。

#### Q：是否可以使用 Aspose.Cells 修改 XLSB 檔案中的外部連線？
     
答：是的，您可以修改外部連線的屬性，例如連線名稱，以滿足您的特定需求。 Aspose.Cells 提供了進行這些更改的方法。

#### Q：如何使用 Aspose.Cells 將對外部連線所做的變更儲存到 XLSB 檔案中？
     
答：對外部連線進行必要的變更後，您可以使用 Aspose.Cells 提供的適當方法簡單地儲存修改後的 Excel XLSB 檔案。