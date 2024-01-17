---
title: ワークシートのペインを分割する
linktitle: ワークシートのペインを分割する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークシートのペインを分割するためのステップバイステップ ガイド。
type: docs
weight: 130
url: /ja/net/excel-display-settings-csharp-tutorials/split-panes-of-worksheet/
---
このチュートリアルでは、Aspose.Cells for .NET を使用して Excel ワークシートのペインを分割する方法を説明します。望ましい結果を得るには、次の手順に従います。

## ステップ 1: 環境をセットアップする

Aspose.Cells for .NET がインストールされていることを確認し、開発環境をセットアップしてください。また、ペインを分割する Excel ファイルのコピーがあることを確認してください。

## ステップ 2: 必要な依存関係をインポートする

Aspose.Cells のクラスを使用するために必要なディレクティブを追加します。

```csharp
using Aspose.Cells;
```

## ステップ 3: コードの初期化

まず、Excel ドキュメントを含むディレクトリへのパスを初期化します。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## ステップ 4: Excel ファイルを開く

新しいインスタンスを作成する`Workbook`オブジェクトを選択し、次のコマンドを使用して Excel ファイルを開きます。`Open`方法：

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## ステップ 5: アクティブセルを定義する

を使用してワークシートのアクティブセルを設定します。`ActiveCell`財産：

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## ステップ6: フラップの分割

を使用してワークシート ウィンドウを分割します。`Split`方法：

```csharp
book.Worksheets[0].Split();
```

## ステップ 7: 変更を保存する

Excel ファイルに加えた変更を保存します。

```csharp
book.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET を使用したワークシートの分割ペインのサンプル ソース コード 

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//新しいワークブックをインスタンス化し、テンプレート ファイルを開く
Workbook book = new Workbook(dataDir + "Book1.xls");
//アクティブセルを設定する
book.Worksheets[0].ActiveCell = "A20";
//ワークシートウィンドウを分割する
book.Worksheets[0].Split();
//Excelファイルを保存します
book.Save(dataDir + "output.xls");
```

## 結論

このチュートリアルでは、Aspose.Cells for .NET を使用して Excel ワークシートのペインを分割する方法を学習しました。説明されている手順に従うことで、Excel ファイルの外観と動作を簡単にカスタマイズできます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作するための一般的なソフトウェア ライブラリです。

#### Aspose.Cells でワークシートのアクティブ セルを設定するにはどうすればよいですか?

を使用してアクティブセルを設定できます。`ActiveCell`Worksheet オブジェクトのプロパティ。

#### ワークシート ウィンドウの水平または垂直ペインのみを分割できますか?

はい、Aspose.Cells を使用すると、次のような適切な方法を使用してのみ水平または垂直のペインを分割できます。`SplitColumn`または`SplitRow`.

#### Aspose.Cells は .xls 形式の Excel ファイルでのみ動作しますか?

いいえ、Aspose.Cells は .xls や .xlsx などのさまざまな Excel ファイル形式をサポートしています。