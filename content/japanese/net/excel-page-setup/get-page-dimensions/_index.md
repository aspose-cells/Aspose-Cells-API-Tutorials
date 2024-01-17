---
title: ページの寸法を取得する
linktitle: ページの寸法を取得する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel でページのサイズを取得する方法を学びます。 C# のソース コードを含むステップバイステップ ガイド。
type: docs
weight: 40
url: /ja/net/excel-page-setup/get-page-dimensions/
---
Aspose.Cells for .NET は、開発者がプログラムで Microsoft Excel ファイルを操作できるようにする強力なライブラリです。ページの寸法を取得する機能など、Excel ドキュメントを操作するための幅広い機能を提供します。このチュートリアルでは、Aspose.Cells for .NET を使用してページのサイズを取得する手順を説明します。

## ステップ 1: Workbook クラスのインスタンスを作成する

まず、Excel ワークブックを表す Workbook クラスのインスタンスを作成する必要があります。これは、次のコードを使用して実現できます。

```csharp
Workbook book = new Workbook();
```

## ステップ 2: スプレッドシートへのアクセス

次に、ページ寸法を設定するワークブック内のワークシートに移動する必要があります。この例では、最初のワークシートを操作するとします。次のコードを使用してアクセスできます。

```csharp
Worksheet sheet = book.Worksheets[0];
```

## ステップ 3: 用紙サイズを A2 に設定し、幅と高さをインチ単位で印刷します。

ここで、用紙サイズを A2 に設定し、ページの幅と高さをインチ単位で印刷します。これは、次のコードを使用して実現できます。

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("A2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## ステップ 4: 用紙サイズを A3 に設定し、幅と高さをインチ単位で印刷します。

次に、用紙サイズを A3 に設定し、ページの幅と高さをインチ単位で印刷します。対応するコードは次のとおりです。

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("A3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## ステップ 5: 用紙サイズを A4 に設定し、幅と高さをインチ単位で印刷します。

ここで、用紙サイズを A4 に設定し、ページの幅と高さをインチ単位で印刷します。コードは次のとおりです。

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("A4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

## ステップ 6: 用紙サイズをレターに設定し、幅と高さをインチ単位で印刷します。

最後に、用紙サイズをレターに設定し、ページの幅と高さをインチ単位で印刷します。コードは次のとおりです。

```csharp
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("Letter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
```

### Aspose.Cells for .NET を使用したページ ディメンションの取得のサンプル ソース コード 
```csharp
//Workbookクラスのインスタンスを作成する
Workbook book = new Workbook();
//最初のワークシートにアクセスする
Worksheet sheet = book.Worksheets[0];
//用紙サイズを A2 に設定し、用紙の幅と高さをインチ単位で印刷します。
sheet.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//用紙サイズを A3 に設定し、用紙の幅と高さをインチ単位で印刷します。
sheet.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//用紙サイズを A4 に設定し、用紙の幅と高さをインチ単位で印刷します。
sheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
//用紙サイズをレターに設定し、用紙の幅と高さをインチ単位で印刷します。
sheet.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + sheet.PageSetup.PaperWidth + "x" + sheet.PageSetup.PaperHeight);
Console.WriteLine("GetPageDimensions executed successfully.\r\n");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用してページのサイズを取得する方法を学習しました。この機能は、Excel ファイルのページ寸法に基づいて特定の操作を実行する必要がある場合に役立ちます。

Aspose.Cells のドキュメントをさらに調べて、Aspose.Cells が提供するすべての強力な機能を確認することを忘れないでください。

### よくある質問

#### 1. Aspose.Cells for .NET は他にどのような用紙サイズをサポートしていますか?

Aspose.Cells for .NET は、A1、A5、B4、B5、エグゼクティブ、リーガル、レターなどを含むさまざまな用紙サイズをサポートしています。サポートされている用紙サイズの完全なリストについては、ドキュメントを確認してください。

#### 2. Aspose.Cells for .NET を使用してカスタム ページのサイズを設定できますか?

はい、希望の幅と高さを指定することで、カスタム ページの寸法を設定できます。 Aspose.Cells は、ニーズに合わせてページの寸法をカスタマイズするための完全な柔軟性を提供します。

#### 3. ページの寸法をインチ以外の単位で取得できますか?

はい、Aspose.Cells for .NET を使用すると、インチ、センチメートル、ミリメートル、ポイントなどのさまざまな単位でページの寸法を取得できます。

#### 4. Aspose.Cells for .NET は他のページ設定編集機能をサポートしていますか?

はい、Aspose.Cells は、余白、方向、ヘッダーとフッターなどの設定を含む、ページ設定を編集するためのあらゆる機能を提供します。