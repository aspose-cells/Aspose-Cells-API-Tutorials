---
title: Excel 他のワークブックからワークシートをコピー
linktitle: Excel 他のワークブックからワークシートをコピー
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用すると、あるワークブックから別のワークブックに Excel ワークシートを簡単にコピーできます。
type: docs
weight: 10
url: /ja/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
このチュートリアルでは、.NET 用の Aspose.Cells ライブラリを使用して、別のワークブックから Excel ワークシートをコピーする手順を説明します。このタスクを完了するには、以下の手順に従ってください。

## ステップ 1: 準備

始める前に、Aspose.Cells for .NET がインストールされており、好みの統合開発環境 (IDE) で C# プロジェクトが作成されていることを確認してください。

## ステップ 2: ドキュメント ディレクトリのパスを設定する

を宣言します`dataDir`変数を指定し、ドキュメント ディレクトリへのパスで初期化します。例えば ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

必ず交換してください`"YOUR_DOCUMENTS_DIRECTORY"`ディレクトリへの実際のパスを使用します。

## ステップ 3: 新しい Excel ワークブックを作成する

使用`Workbook`Aspose.Cells のクラスを使用して、新しい Excel ワークブックを作成します。

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## ステップ 4: ワークブックの最初のワークシートを取得する

インデックス 0 を使用して、ワークブック内の最初のワークシートに移動します。

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## ステップ 5: ヘッダー行 (A1:A4) にデータを追加します。

使う`for`ヘッダー行 (A1:A4) にデータを追加するループ:

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## ステップ 6: 詳細データの追加 (A5:A999)

別のものを使用する`for`詳細データを追加するループ (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## ステップ 7: レイアウト オプションを設定する

ワークシートのページ設定オプションを設定するには、`PageSetup`物体：

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## ステップ 8: 別の Excel ワークブックを作成する

別の Excel ワークブックを作成します。

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## ステップ 9: 2 番目のワークブックから最初のワークシートを取得する

番目のワークブックの最初のワークシートに移動します。

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## ステップ 10: ワークシートに名前を付ける

火に名前を付けます

計算島:

```csharp
ws1.Name = "MySheet";
```

## ステップ 11: 最初のワークブックの最初のワークシートから 2 番目のワークブックの最初のワークシートにデータをコピーする

最初のワークブックの最初のワークシートから 2 番目のワークブックの最初のワークシートにデータをコピーします。

```csharp
ws1.Copy(ws0);
```

## ステップ 12: Excel ファイルを保存する

Excel ファイルを保存します。

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

出力ファイルに必要なパスとファイル名を必ず指定してください。

### Aspose.Cells for .NET を使用して他のワークブックからワークシートをコピーする Excel のサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//新しいワークブックを作成します。
Workbook excelWorkbook0 = new Workbook();
//この本の最初のワークシートを入手してください。
Worksheet ws0 = excelWorkbook0.Worksheets[0];
//ヘッダー行 (A1:A4) にデータを入力します。
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
//詳細データを入力します (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
//最初のワークシートに基づいて pagesetup オブジェクトを定義します。
PageSetup pagesetup = ws0.PageSetup;
//最初の 5 行が各ページで繰り返されます...
//印刷プレビューで確認できます。
pagesetup.PrintTitleRows = "$1:$5";
//別のワークブックを作成します。
Workbook excelWorkbook1 = new Workbook();
//この本の最初のワークシートを入手してください。
Worksheet ws1 = excelWorkbook1.Worksheets[0];
//ワークシートに名前を付けます。
ws1.Name = "MySheet";
//最初のワークブックの最初のワークシートからデータを
// 番目のワークブックの最初のワークシート。
ws1.Copy(ws0);
// Excel ファイルを保存します。
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して、別のワークブックから Excel ワークシートをコピーする方法を学習しました。独自のプロジェクトでこの方法を自由に使用して、Excel ファイルを効率的に操作してください。

### よくある質問

#### Q.Aspose.Cells for .NET を使用するにはどのようなライブラリが必要ですか?

A. Aspose.Cells for .NET を使用するには、プロジェクトに Aspose.Cells ライブラリを含める必要があります。統合開発環境 (IDE) でこのライブラリが正しく参照されていることを確認してください。

#### Q. Aspose.Cells は、XLSX などの他の Excel ファイル形式をサポートしていますか?

A. はい、Aspose.Cells は、XLSX、XLS、CSV、HTML などを含むさまざまな Excel ファイル形式をサポートしています。 Aspose.Cells for .NET の機能を使用して、これらのファイル形式を操作できます。

#### Q. ワークシートをコピーするときにレイアウト オプションをカスタマイズできますか?

A. はい、ワークシートをコピーするときに、`PageSetup`物体。ページのヘッダー、フッター、余白、方向などを指定できます。