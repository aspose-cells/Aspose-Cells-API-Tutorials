---
title: ワークシートの改ページプレビュー
linktitle: ワークシートの改ページプレビュー
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用してワークシートの改ページ プレビューを表示するためのステップバイステップ ガイド。
type: docs
weight: 110
url: /ja/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
このチュートリアルでは、Aspose.Cells for .NET を使用してワークシートの改ページ プレビューを表示する方法を説明します。望ましい結果を得るには、次の手順に従います。

## ステップ 1: 環境をセットアップする

Aspose.Cells for .NET がインストールされていることを確認し、開発環境をセットアップしてください。また、改ページプレビューを表示する Excel ファイルのコピーがあることを確認してください。

## ステップ 2: 必要な依存関係をインポートする

Aspose.Cells のクラスを使用するために必要なディレクティブを追加します。

```csharp
using Aspose.Cells;
using System.IO;
```

## ステップ 3: コードの初期化

まず、Excel ドキュメントを含むディレクトリへのパスを初期化します。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## ステップ 4: Excel ファイルを開く

を作成します`FileStream`開く Excel ファイルを含むオブジェクト:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

インスタンス化する`Workbook`オブジェクトを開き、ファイル ストリームを使用して Excel ファイルを開きます。

```csharp
Workbook workbook = new Workbook(fstream);
```

## ステップ 5: スプレッドシートへのアクセス

Excel ファイルの最初のワークシートに移動します。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## ステップ6: ページバイプレビューを表示する

スプレッドシートのページバイ プレビューを有効にします。

```csharp
worksheet. IsPageBreakPreview = true;
```

## ステップ 7: 変更を保存する

Excel ファイルに加えた変更を保存します。

```csharp
workbook.Save(dataDir + "output.xls");
```

## ステップ 8: ファイル ストリームを閉じる

ファイル ストリームを閉じて、すべてのリソースを解放します。

```csharp
fstream.Close();
```

### Aspose.Cells for .NET を使用したワークシートの改ページ プレビューのサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//開く Excel ファイルを含むファイル ストリームの作成
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//Workbook オブジェクトのインスタンス化
//ファイル ストリーム経由で Excel ファイルを開く
Workbook workbook = new Workbook(fstream);
//Excel ファイルの最初のワークシートへのアクセス
Worksheet worksheet = workbook.Worksheets[0];
//ワークシートを改ページプレビューで表示する
worksheet.IsPageBreakPreview = true;
//変更したExcelファイルを保存する
workbook.Save(dataDir + "output.xls");
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

このチュートリアルでは、Aspose.Cells for .NET を使用してワークシートの改ページ プレビューを表示する方法を学習しました。説明されている手順に従うことで、Excel ファイルの外観とレイアウトを簡単に制御できます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作するための一般的なソフトウェア ライブラリです。

#### ワークシート全体ではなく、特定のワークシートのページバイ プレビューを表示できますか?

はい、Aspose.Cells を使用すると、対応する Worksheet オブジェクトにアクセスすることで、特定のワークシートの改ページ プレビューを有効にすることができます。

#### Aspose.Cells は他の Excel ファイル編集機能をサポートしていますか?

はい。Aspose.Cells は、データの追加、書式設定、グラフの作成など、Excel ファイルを編集および操作するための幅広い機能を提供します。

#### Aspose.Cells は .xls 形式の Excel ファイルでのみ動作しますか?

いいえ、Aspose.Cells は .xls や .xlsx などのさまざまな Excel ファイル形式をサポートしています。
	