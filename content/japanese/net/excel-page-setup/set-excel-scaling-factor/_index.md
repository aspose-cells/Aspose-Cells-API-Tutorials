---
title: Excel の倍率を設定する
linktitle: Excel の倍率を設定する
second_title: Aspose.Cells for .NET API リファレンス
description: Excel ファイルを簡単に操作し、Aspose.Cells for .NET を使用してスケール係数をカスタマイズする方法を学びます。
type: docs
weight: 180
url: /ja/net/excel-page-setup/set-excel-scaling-factor/
---
このガイドでは、Aspose.Cells for .NET を使用して Excel スプレッドシートでスケール係数を設定する方法を説明します。このタスクを実行するには、次の手順に従ってください。

## ステップ 1: 環境をセットアップする

開発環境をセットアップし、Aspose.Cells for .NET をインストールしていることを確認してください。 Aspose 公式 Web サイトからライブラリの最新バージョンをダウンロードできます。

## ステップ 2: 必要な名前空間をインポートする

C# プロジェクトで、Aspose.Cells を操作するために必要な名前空間をインポートします。

```csharp
using Aspose.Cells;
```

## ステップ 3: ドキュメント ディレクトリへのパスを設定する

を宣言します`dataDir`変数を使用して、生成された Excel ファイルを保存するディレクトリへのパスを指定します。

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

必ず交換してください`"YOUR_DOCUMENT_DIRECTORY"`システム上の正しいパスを使用してください。

## ステップ 4: ワークブック オブジェクトの作成

作成する Excel ワークブックを表す Workbook オブジェクトをインスタンス化します。

```csharp
Workbook workbook = new Workbook();
```

## ステップ 5: 最初のワークシートへのアクセス

次のコードを使用して、Excel ワークブックの最初のワークシートに移動します。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## ステップ 6: スケーリング係数を設定する

次のコードを使用してスケーリング係数を設定します。

```csharp
worksheet.PageSetup.Zoom = 100;
```

ここでは倍率を 100 に設定しています。これは、スプレッドシートが印刷時に通常のサイズの 100% で表示されることを意味します。

## ステップ 7: Excel ワークブックを保存する

定義された倍率で Excel ワークブックを保存するには、`Save` Workbook オブジェクトのメソッド:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

これにより、指定したディレクトリに Excel ワークブックが「ScalingFactor_out.xls」というファイル名で保存されます。

### Aspose.Cells for .NET を使用した Set Excel Scaling Factor のサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Workbook オブジェクトのインスタンス化
Workbook workbook = new Workbook();
//Excel ファイルの最初のワークシートへのアクセス
Worksheet worksheet = workbook.Worksheets[0];
//スケーリング係数を 100 に設定する
worksheet.PageSetup.Zoom = 100;
//ワークブックを保存します。
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel スプレッドシートでスケール係数を設定する方法を学習しました。倍率を使用すると、印刷時にスプレッドシートのサイズを調整して最適な表示を得ることができます。

### よくある質問

#### 1. Aspose.Cells for .NET を使用して Excel スプレッドシートでスケーリング係数を設定するにはどうすればよいですか?

使用`Zoom`の財産`PageSetup`オブジェクトを使用してスケーリング係数を設定します。例えば、`worksheet.PageSetup.Zoom = 100;`スケーリング係数を 100% に設定します。

#### 2. ニーズに応じて倍率をカスタマイズできますか?

はい、スケール係数は、に割り当てられた値を変更することで調整できます。`Zoom`財産。例えば、`worksheet.PageSetup.Zoom = 75;`スケーリング係数を 75% に設定します。

#### 3. 定義された倍率で Excel ワークブックを保存することはできますか?

はい、使用できます`Save`の方法`Workbook`オブジェクトを使用して、定義された倍率で Excel ワークブックを保存します。