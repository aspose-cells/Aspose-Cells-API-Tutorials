---
title: 在頁眉頁腳中插入圖像
linktitle: 在頁眉頁腳中插入圖像
second_title: Aspose.Cells for .NET API 參考
description: 了解如何使用 Aspose.Cells for .NET 將影像插入 Excel 文件的頁首或頁尾。帶有 C# 原始程式碼的逐步指南。
type: docs
weight: 60
url: /zh-hant/net/excel-page-setup/insert-image-in-header-footer/
---
在 Excel 文件的頁首或頁尾中插入圖像的功能對於自訂報告或新增公司徽標非常有用。在本文中，我們將逐步指導您使用 Aspose.Cells for .NET 在 Excel 文件的頁首或頁尾中插入圖像。您將學習如何使用 C# 原始程式碼來完成此任務。

## 第一步：建構環境

在開始之前，請確保您的電腦上安裝了 Aspose.Cells for .NET。也可以在您首選的開發環境中建立一個新專案。

## 第二步：導入必要的函式庫

在您的程式碼檔案中，匯入使用 Aspose.Cells 所需的程式庫。這是對應的程式碼：

```csharp
using Aspose.Cells;
```

## 第三步：設定文檔目錄

設定要使用的 Excel 文件所在的目錄。使用以下程式碼設定目錄：

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

請務必指定完整的目錄路徑。

## 第 4 步：建立工作簿對象

Workbook 物件代表您將使用的 Excel 文件。您可以使用以下程式碼建立它：

```csharp
Workbook workbook = new Workbook();
```

這將建立一個新的空 Workbook 物件。

## 第 5 步：儲存影像 URL

定義要在頁首或頁尾中插入的圖像的 URL 或路徑。使用以下程式碼來儲存圖像 URL：

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

確保指定的路徑正確且影像存在於該位置。

## 第6步：開啟影像文件

要開啟圖像文件，我們將使用 FileStream 物件並從圖像中讀取二進位資料。這是對應的程式碼：

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

確保影像路徑正確並且您具有正確的存取權限。

## 第7步：配置頁面設定

PageSetup 物件用於設定 Excel 文件頁面設置，包括頁首和頁尾。使用下列程式碼取得第一個工作表的 PageSetup 物件：

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

這將允許您存取工作簿中第一個工作表的頁面設定。

## 第 8 步：將圖像新增至標題中

使用 PageSetup 物件的 SetHeaderPicture() 方法可以在頁首的中間部分設定影像。這是對應的程式碼：

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

這會將指定的圖像新增至頁首。

## 第 9 步：將腳本新增至標頭

若要將腳本新增至頁眉，請使用 PageSetup 物件的 SetHeader() 方法。這是對應的程式碼：

```csharp
pageSetup.SetHeader(1, "&G");
```

這會將指定的腳本新增至頁首。在此範例中，「&G」腳本顯示頁碼。

## 第 10 步：將工作表名稱新增至頁眉

若要在頁首中顯示工作表名稱，請再次使用 PageSetup 物件的 SetHeader() 方法。這是對應的程式碼：

```csharp
pageSetup.SetHeader(2, "&A");
```

這會將工作表名稱新增至頁首。 “&A”腳本用於表示工作表名稱。

## 第 11 步：儲存工作簿

若要儲存工作簿的更改，請使用 Workbook 物件的 Save() 方法。這是對應的程式碼：

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

這會將工作簿及其變更儲存到指定目錄。

## 第12步：關閉文件流

從映像中讀取二進位資料後，請務必關閉 FileStream 以釋放資源。使用以下程式碼關閉 FileStream：

```csharp
inFile.Close();
```

使用完 FileStream 後，請務必將其關閉。

### 使用 Aspose.Cells for .NET 在頁首頁腳中插入影像的範例原始碼 
```csharp
//文檔目錄的路徑。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//建立工作簿對象
Workbook workbook = new Workbook();
//建立一個字串變數來儲存徽標/圖片的 url
string logo_url = dataDir + "aspose-logo.jpg";
//聲明 FileStream 對象
FileStream inFile;
//聲明一個位元組數組
byte[] binaryData;
//建立 FileStream 物件的實例以開啟流中的標誌/圖片
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
//實例化 FileStream 物件大小的位元組數組
binaryData = new Byte[inFile.Length];
//從流中讀取位元組區塊並將資料寫入位元組數組的給定緩衝區中。
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
//建立 PageSetup 物件以取得工作簿第一個工作表的頁面設置
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
//將標誌/圖片設定在頁首的中央部分
pageSetup.SetHeaderPicture(1, binaryData);
//設定徽標/圖片的腳本
pageSetup.SetHeader(1, "&G");
//使用腳本在頁首的右側部分設定工作表的名稱
pageSetup.SetHeader(2, "&A");
//儲存工作簿
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//關閉 FileStream 對象
inFile.Close();       
```
## 結論

恭喜！現在您知道如何使用 Aspose.Cells for .NET 在 Excel 文件的頁首或頁尾中插入圖像。本教學將引導您完成流程的每一步，從設定環境到儲存修改後的工作簿。請隨意嘗試更多 Aspose.Cells 的功能，以建立個人化和專業的 Excel 文件。

### 常見問題解答

#### Q1: Excel 文件的頁首或頁尾中是否可以插入多張圖片？

A1：是的，您可以透過對每個附加影像重複步驟 8 和 9，將多個影像插入 Excel 文件的頁首或頁尾中。

#### Q2：頁首或頁尾支援哪些影像格式插入？
A2：Aspose.Cells支援多種常見的圖片格式，如JPEG、PNG、GIF、BMP等。

#### Q3：我可以進一步自訂頁首或頁尾的外觀嗎？

A3：是的，您可以使用特殊的腳本和程式碼來進一步格式化和自訂頁首或頁尾的外觀。有關自訂選項的更多信息，請參閱 Aspose.Cells 文件。

#### Q4：Aspose.Cells 是否適用於不同版本的 Excel？

A4: 是的，Aspose.Cells 與不同版本的 Excel 相容，包括 Excel 2003、Excel 2007、Excel 2010、Excel 2013、Excel 2016 和 Excel 2019。

#### Q5：是否可以在Excel文件的其他部分插入圖像，例如儲存格或圖表？

A5：是的，Aspose.Cells 提供了廣泛的功能，可以將圖像插入 Excel 文件的不同部分，包括單元格、圖表和繪圖物件。