---
title: ワークシートの用紙サイズが自動かどうかを確認する
linktitle: ワークシートの用紙サイズが自動かどうかを確認する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用してスプレッドシートの用紙サイズが自動であるかどうかを判断する方法を学習します。
type: docs
weight: 20
url: /ja/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
この記事では、次の C# ソース コードを段階的に説明します。 Aspose.Cells for .NET を使用して、ワークシートの用紙サイズが自動であるかどうかを確認します。この操作を実行するには、.NET 用の Aspose.Cells ライブラリを使用します。ワークシートの用紙サイズが自動かどうかを確認するには、次の手順に従います。

## ステップ 1: ワークブックをロードする
最初のステップは、ワークブックをロードすることです。 2 つのワークブックがあり、1 つは自動用紙サイズが無効になっており、もう 1 つは自動用紙サイズが有効になっています。ワークブックをロードするコードは次のとおりです。

```csharp
//ソースディレクトリ
string sourceDir = "YOUR_SOURCE_DIR";
//出力ディレクトリ
string outputDir = "YOUR_OUTPUT_DIRECTORY";

//自動用紙サイズを無効にして最初のワークブックをロードします
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

//自動用紙サイズを有効にして 2 番目のワークブックをロードします
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## ステップ 2: スプレッドシートへのアクセス
ワークブックをロードしたので、自動用紙サイズを確認できるようにワークシートにアクセスする必要があります。 2 つのワークブックの最初のワークシートに進みます。これにアクセスするコードは次のとおりです。

```csharp
//最初のワークブックの最初のワークシートに移動します
Worksheet ws11 = wb1.Worksheets[0];

// 番目のワークブックの最初のワークシートに移動します
Worksheet ws12 = wb2.Worksheets[0];
```

## ステップ 3: 自動用紙サイズを確認する
このステップでは、ワークシートの用紙サイズが自動であるかどうかを確認します。を使用します。`PageSetup.IsAutomaticPaperSize`この情報を取得するにはプロパティを使用します。次に結果を表示します。そのコードは次のとおりです。

```csharp
//最初のワークブックの最初のワークシートの IsAutomaticPaperSize プロパティを表示します。
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// 2 番目のワークブックの最初のワークシートの IsAutomaticPaperSize プロパティを表示します。
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Aspose.Cells for .NET を使用してワークシートの用紙サイズが自動であるかどうかを判断するためのサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//出力ディレクトリ
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//自動用紙サイズが false の最初のワークブックをロードします
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//自動用紙サイズが true の 2 番目のワークブックをロードします。
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//両方のワークブックの最初のワークシートにアクセスします
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//両方のワークシートの PageSetup.IsAutomaticPaperSize プロパティを印刷します。
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## 結論
この記事では、Aspose.Cells for .NET を使用してワークシートの用紙サイズが自動であるかどうかを判断する方法を学びました。次の手順に従いました: ワークブックをロードし、

スプレッドシートへのアクセスと自動用紙サイズチェック。この知識を利用して、スプレッドシートの用紙サイズが自動かどうかを判断できるようになりました。

### よくある質問

#### Q: Aspose.Cells for .NET を使用してワークブックをロードするにはどうすればよいですか?

A: Aspose.Cells ライブラリの Workbook クラスを使用してワークブックをロードできます。ファイルからワークブックをロードするには、Workbook.Load メソッドを使用します。

#### Q: 他のスプレッドシートの自動用紙サイズを確認できますか?

A: はい、対応する Worksheet オブジェクトの PageSetup.IsAutomaticPaperSize プロパティにアクセスすることで、ワークシートの自動用紙サイズを確認できます。

#### Q: スプレッドシートの自動用紙サイズを変更するにはどうすればよいですか?

A: ワークシートの自動用紙サイズを変更するには、PageSetup.IsAutomaticPaperSize プロパティを使用し、それを目的の値 (true または false) に設定します。

#### Q: Aspose.Cells for .NET は他にどのような機能を提供しますか?

A: Aspose.Cells for .NET は、ワークブックの作成、変更、変換、データ、数式、書式設定の操作など、スプレッドシートを操作するための多くの機能を提供します。