---
title: Excel ワークブック間でワークシートをコピーする
linktitle: Excel ワークブック間でワークシートをコピーする
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用すると、Excel ワークブック間でワークシートを簡単にコピーできます。
type: docs
weight: 30
url: /ja/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
このチュートリアルでは、.NET 用の Aspose.Cells ライブラリを使用して Excel ワークブック間でワークシートをコピーする手順を説明します。このタスクを完了するには、以下の手順に従ってください。

## ステップ 1: 準備

Aspose.Cells for .NET がインストールされており、優先統合開発環境 (IDE) で C# プロジェクトが作成されていることを確認してください。

## ステップ 2: ドキュメント ディレクトリのパスを設定する

を宣言します`dataDir`変数を指定し、ドキュメント ディレクトリへのパスで初期化します。例えば ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

必ず交換してください`"YOUR_DOCUMENTS_DIRECTORY"`ディレクトリへの実際のパスを使用します。

## ステップ 3: 入力ファイルのパスを定義する

を宣言する`InputPath`変数を指定し、スプレッドシートのコピー元の Excel ファイルの絶対パスで初期化します。例えば ：

```csharp
string InputPath = dataDir + "book1.xls";
```

 Excelファイルがあることを確認してください`book1.xls`ドキュメント ディレクトリ内に保存するか、正しいファイル名と場所を指定します。

## ステップ 4: 最初の Excel ワークブックを作成する

使用`Workbook`Aspose.Cells のクラスを使用して、最初の Excel ワークブックを作成し、指定されたファイルを開きます。

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## ステップ 5: 2 番目の Excel ワークブックを作成する

番目の Excel ワークブックを作成します。

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## ステップ 6: ワークシートを最初のワークブックから 2 番目のワークブックにコピーする

使用`Copy`最初のワークブックから 2 番目のワークブックに最初のワークシートをコピーするメソッド:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## ステップ 7: Excel ファイルを保存する

コピーしたスプレッドシートを含む Excel ファイルを保存します。

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

出力ファイルに必要なパスとファイル名を必ず指定してください。

### Aspose.Cells for .NET を使用してワークブック間でワークシートをコピーする Excel のサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//ワークブックを作成します。
//ファイルを最初のブックに開きます。
Workbook excelWorkbook0 = new Workbook(InputPath);
//別のワークブックを作成します。
Workbook excelWorkbook1 = new Workbook();
// 1 冊目の本の最初のシートを 2 冊目の冊子にコピーします。
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
//ファイルを保存します。
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel ワークブック間でワークシートをコピーする方法を学習しました。独自のプロジェクトでこの方法を自由に使用して、Excel ファイルを効率的に操作してください。

### よくある質問

#### Q.Aspose.Cells for .NET を使用するにはどのようなライブラリが必要ですか?

A. Aspose.Cells for .NET を使用するには、プロジェクトに Aspose.Cells ライブラリを含める必要があります。統合開発環境 (IDE) でこのライブラリが正しく参照されていることを確認してください。

#### Q. Aspose.Cells は、XLSX などの他の Excel ファイル形式をサポートしていますか?

A. はい、Aspose.Cells は、XLSX、XLS、CSV、HTML などを含むさまざまな Excel ファイル形式をサポートしています。 Aspose.Cells for .NET の機能を使用して、これらのファイル形式を操作できます。

#### Q. スプレッドシートをコピーするときにレイアウト オプションをカスタマイズできますか?

A. はい、スプレッドシートをコピーするときに、`PageSetup`物体。ページのヘッダー、フッター、余白、方向などを指定できます。