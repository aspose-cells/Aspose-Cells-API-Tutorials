---
title: レンダリング用のワークシートのカスタム用紙サイズを実装する
linktitle: レンダリング用のワークシートのカスタム用紙サイズを実装する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用してカスタム ワークシート サイズを実装するためのステップバイステップ ガイド。寸法を設定し、メッセージを追加して PDF として保存します。
type: docs
weight: 50
url: /ja/net/excel-page-setup/implement-custom-paper-size-of-worksheet-for-rendering/
---
ワークシートにカスタム サイズを実装すると、特定のサイズの PDF ドキュメントを作成する場合に非常に便利です。このチュートリアルでは、Aspose.Cells for .NET を使用してワークシートのカスタム サイズを設定し、ドキュメントを PDF として保存する方法を学びます。

## ステップ 1: 出力フォルダーの作成

開始する前に、生成された PDF ファイルを保存する出力フォルダーを作成する必要があります。出力フォルダーには任意のパスを使用できます。

```csharp
//出力ディレクトリ
string outputDir = "YOUR_OUTPUT_FOLDER";
```

出力フォルダーへの正しいパスを指定していることを確認してください。

## ステップ 2: Workbook オブジェクトの作成

まず、Aspose.Cells を使用して Workbook オブジェクトを作成する必要があります。このオブジェクトはスプレッドシートを表します。

```csharp
//ワークブックオブジェクトを作成する
Workbook wb = new Workbook();
```

## ステップ 3: 最初のワークシートへのアクセス

Workbook オブジェクトを作成した後、その中の最初のワークシートにアクセスできます。

```csharp
//最初のワークシートへのアクセス
Worksheet ws = wb.Worksheets[0];
```

## ステップ 4: カスタム ワークシート サイズの設定

これで、次を使用してカスタムワークシートサイズを設定できるようになりました`CustomPaperSize(width, height)`PageSetup クラスのメソッド。

```csharp
//カスタムワークシートサイズの設定(インチ単位)
ws.PageSetup.CustomPaperSize(6, 4);
```

この例では、ワークシートのサイズを幅 6 インチ、高さ 4 インチに設定しています。

## ステップ 5: セル B4 へのアクセス

その後、ワークシート内の特定のセルにアクセスできるようになります。この場合、セル B4 にアクセスします。

```csharp
//セルB4へのアクセス
Cell b4 = ws.Cells["B4"];
```

## ステップ 6: セル B4 にメッセージを追加する

これで、次のコマンドを使用してセル B4 にメッセージを追加できるようになりました。`PutValue(value)`方法。

```csharp
//セルB4にメッセージを追加します
b4.PutValue("PDF page size: 6.00 x 4.00 inches");
```

この例では、セル B4 に「PDF ページ サイズ: 6.00" x 4.00"」というメッセージを追加しました。

## ステップ 7: ワークシートを PDF 形式で保存する

最後に、次のコマンドを使用してワークシートを PDF 形式で保存できます。`Save(filePath)` Workbook オブジェクトのメソッド。

```csharp
//ワークシートを PDF 形式で保存する
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

前に作成した出力フォルダーを使用して、生成された PDF ファイルへの希望のパスを指定します。

### Aspose.Cells for .NET を使用してレンダリング用のワークシートのカスタム用紙サイズを実装するためのサンプル ソース コード 
```csharp
//出力ディレクトリ
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//ワークブックオブジェクトを作成する
Workbook wb = new Workbook();
//最初のワークシートにアクセスする
Worksheet ws = wb.Worksheets[0];
//カスタム用紙サイズをインチ単位で設定します
ws.PageSetup.CustomPaperSize(6, 4);
//セルB4にアクセスします
Cell b4 = ws.Cells["B4"];
//セルB4にメッセージを追加します
b4.PutValue("Pdf Page Dimensions: 6.00 x 4.00 in");
//ワークブックを PDF 形式で保存する
wb.Save(outputDir + "outputCustomPaperSize.pdf");
```

## 結論

このチュートリアルでは、Aspose.Cells for .NET を使用してワークシートのカスタム サイズを実装する方法を学習しました。これらの手順を使用して、ワークシートに特定のサイズを設定し、ドキュメントを PDF 形式で保存できます。このガイドが、カスタム スプレッドシート サイズを実装するプロセスを理解するのに役立つことを願っています。

### よくある質問 (FAQ)

#### 質問 1: スプレッドシートのレイアウトをさらにカスタマイズできますか?

はい、Aspose.Cells には、ワークシートのレイアウトをカスタマイズするための多くのオプションが用意されています。カスタム寸法、ページの向き、余白、ヘッダーとフッターなどを設定できます。

#### 質問 2: Aspose.Cells は他にどのような出力形式をサポートしていますか?

Aspose.Cells は、PDF、XLSX、XLS、CSV、HTML、TXT などを含むさまざまな出力形式をサポートしています。ニーズに応じて、希望の出力形式を選択できます。