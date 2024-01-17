---
title: ワークシートの用紙の幅と高さを取得する
linktitle: ワークシートの用紙の幅と高さを取得する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用してスプレッドシートの用紙の幅と高さを取得するための次の C# ソース コードを説明するステップバイステップ ガイドを作成します。
type: docs
weight: 80
url: /ja/net/excel-display-settings-csharp-tutorials/get-paper-width-and-height-of-worksheet/
---
このチュートリアルでは、Aspose.Cells for .NET を使用してワークシートの用紙の幅と高さを取得する次の C# ソース コードを段階的に説明します。以下の手順に従います。

## ステップ 1: ワークブックを作成する
まず、次のコマンドを使用して新しいワークブックを作成します。`Workbook`クラス：

```csharp
Workbook wb = new Workbook();
```

## ステップ 2: 最初のワークシートにアクセスする
次に、`Worksheet`クラス：

```csharp
Worksheet ws = wb.Worksheets[0];
```

## ステップ 3: 用紙サイズを A2 に設定し、用紙の幅と高さをインチ単位で表示します。
使用`PaperSize`の財産`PageSetup`オブジェクトを使用して用紙サイズを A2 に設定し、`PaperWidth`そして`PaperHeight`プロパティを使用して、用紙の幅と高さをそれぞれ取得します。これらの値を表示するには、`Console.WriteLine`方法：

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

## ステップ 4: 他の用紙サイズについても手順を繰り返します。
前の手順を繰り返して、用紙サイズを A3、A4、レターに変更し、各サイズの用紙の幅と高さの値を表示します。

```csharp
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);

ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```

### Aspose.Cells for .NET を使用してワークシートの用紙の幅と高さを取得するサンプル ソース コード 

```csharp
//ワークブックの作成
Workbook wb = new Workbook();
//最初のワークシートにアクセスする
Worksheet ws = wb.Worksheets[0];
//用紙サイズを A2 に設定し、用紙の幅と高さをインチ単位で印刷します。
ws.PageSetup.PaperSize = PaperSizeType.PaperA2;
Console.WriteLine("PaperA2: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//用紙サイズを A3 に設定し、用紙の幅と高さをインチ単位で印刷します。
ws.PageSetup.PaperSize = PaperSizeType.PaperA3;
Console.WriteLine("PaperA3: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//用紙サイズを A4 に設定し、用紙の幅と高さをインチ単位で印刷します。
ws.PageSetup.PaperSize = PaperSizeType.PaperA4;
Console.WriteLine("PaperA4: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
//用紙サイズをレターに設定し、用紙の幅と高さをインチ単位で印刷します。
ws.PageSetup.PaperSize = PaperSizeType.PaperLetter;
Console.WriteLine("PaperLetter: " + ws.PageSetup.PaperWidth + "x" + ws.PageSetup.PaperHeight);
```


## 結論

Aspose.Cells for .NET を使用してスプレッドシートの用紙の幅と高さを取得する方法を学習しました。この機能は、Excel ドキュメントの構成と正確なレイアウトに役立ちます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作および処理するための強力なライブラリです。 Excel ファイルを作成、変更、変換、分析するための多くの機能を提供します。

#### Aspose.Cells for .NET を使用してスプレッドシートの用紙サイズを取得するにはどうすればよいですか?

使用できます`PageSetup`のクラス`Worksheet`用紙サイズにアクセスするオブジェクト。使用`PaperSize`用紙サイズを設定するプロパティと`PaperWidth`そして`PaperHeight`プロパティを使用して、用紙の幅と高さをそれぞれ取得します。

#### Aspose.Cells for .NET はどの用紙サイズをサポートしていますか?

Aspose.Cells for .NET は、A2、A3、A4、レターなどの一般的に使用される用紙サイズや、その他の多くのカスタム サイズを幅広くサポートしています。

#### Aspose.Cells for .NET を使用してスプレッドシートの用紙サイズをカスタマイズできますか?

はい、カスタム用紙サイズを設定するには、`PaperWidth`そして`PaperHeight`のプロパティ`PageSetup`クラス。