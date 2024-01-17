---
title: Excel ページに合わせるオプション
linktitle: Excel ページに合わせるオプション
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel スプレッドシートのページを自動調整する方法を学びます。
type: docs
weight: 30
url: /ja/net/excel-page-setup/fit-to-excel-pages-options/
---
この記事では、次の C# ソース コードを段階的に説明します: Aspose.Cells for .NET を使用した Excel ページ オプションに合わせる。この操作を実行するには、.NET 用の Aspose.Cells ライブラリを使用します。 Excel でページに合わせて設定するには、次の手順に従います。

## ステップ 1: ワークブックの作成
最初のステップはワークブックを作成することです。 Workbook オブジェクトをインスタンス化します。ワークブックを作成するコードは次のとおりです。

```csharp
//ドキュメントディレクトリへのパス
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//Workbook オブジェクトをインスタンス化する
Workbook workbook = new Workbook();
```

## ステップ 2: ワークシートへのアクセス
ワークブックを作成したので、最初のワークシートに移動する必要があります。最初のシートにアクセスするにはインデックス 0 を使用します。これにアクセスするコードは次のとおりです。

```csharp
//ワークブックの最初のワークシートへのアクセス
Worksheet worksheet = workbook.Worksheets[0];
```

## ステップ 3: 「ページに合わせる」を設定する
このステップでは、ワークシートのページに対する調整を構成します。を使用します。`FitToPagesTall`そして`FitToPagesWide`のプロパティ`PageSetup`オブジェクトを使用して、ワークシートの高さと幅に必要なページ数を指定します。そのコードは次のとおりです。

```csharp
//ワークシートの高さのページ数を構成します。
worksheet.PageSetup.FitToPagesTall = 1;

//ワークシートの幅に応じたページ数を構成します。
worksheet.PageSetup.FitToPagesWide = 1;
```

## ステップ 4: ワークブックを保存する
ページに合わせるように設定したので、ワークブックを保存できます。を使用します。`Save`これには Workbook オブジェクトのメソッドを使用します。ワークブックを保存するコードは次のとおりです。

```csharp
//ワークブックを保存する
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Aspose.Cells for .NET を使用した Excel ページに合わせるオプションのサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Workbook オブジェクトのインスタンス化
Workbook workbook = new Workbook();
//Excel ファイルの最初のワークシートへのアクセス
Worksheet worksheet = workbook.Worksheets[0];
//ワークシートの長さにまたがるページ数の設定
worksheet.PageSetup.FitToPagesTall = 1;
//ワークシートの幅が広がるページ数の設定
worksheet.PageSetup.FitToPagesWide = 1;
//ワークブックを保存します。
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## 結論
この記事では、Aspose.Cells for .NET を使用して Excel でページに合わせるように構成する方法を学びました。次の手順を実行しました: ワークブックの作成、ワークシートへのアクセス、ページに合わせる設定、およびワークブックの保存。この知識を使用して、スプレッドシートを目的のページに調整できるようになりました。

### よくある質問

#### Q: Aspose.Cells for .NET をインストールするにはどうすればよいですか?

A: Aspose.Cells for .NET をインストールするには、Visual Studio の NuGet パッケージ マネージャーを使用できます。 「Aspose.Cells」パッケージを見つけてプロジェクトにインストールします。

#### Q: ページの高さと幅の両方を合わせることができますか?

 A: はい、ワークシートの高さと幅の両方を調整できます。`FitToPagesTall`そして`FitToPagesWide`プロパティ。各次元に必要なページ数を指定できます。

#### Q: [ページに合わせる] オプションをカスタマイズするにはどうすればよいですか?

A: ページ数の指定に加えて、ワークシートの縮尺、用紙の方向、余白など、他のページに合わせるオプションもカスタマイズできます。で利用可能なプロパティを使用します。`PageSetup`これに対しては反対です。

#### Q: Aspose.Cells for .NET を使用して既存のワークブックを処理できますか?

A: はい、Aspose.Cells for .NET を使用して既存のワークブックを開いて編集できます。ワークシート、セル、数式、スタイル、その他のワークブック項目にアクセスして、さまざまな操作を実行できます。