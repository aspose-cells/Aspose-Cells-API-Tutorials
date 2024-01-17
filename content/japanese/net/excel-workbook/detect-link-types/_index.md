---
title: リンクタイプの検出
linktitle: リンクタイプの検出
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークブック内のリンク タイプを検出します。
type: docs
weight: 80
url: /ja/net/excel-workbook/detect-link-types/
---
このチュートリアルでは、Aspose.Cells for .NET を使用して Excel ワークブック内のリンク タイプを検出できるようにする、提供されている C# ソース コードをステップごとに説明します。この操作を行うには、次の手順に従ってください。

## ステップ 1: ソース ディレクトリを設定する

```csharp
//ソースディレクトリ
string SourceDir = RunExamples.Get_SourceDirectory();
```

この最初のステップでは、リンクを含む Excel ワークブックが配置されるソース ディレクトリを定義します。

## ステップ 2: Excel ワークブックをロードする

```csharp
// Excel ワークブックをロードする
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

ソース ファイル パスを使用して Excel ワークブックを読み込みます。

## ステップ 3: スプレッドシートを取得する

```csharp
//最初のワークシートを取得します (デフォルト)
Worksheet worksheet = workbook.Worksheets[0];
```

ワークブックの最初のワークシートを取得します。変更できます`[0]`必要に応じてインデックスを使用して特定のワークシートにアクセスします。

## ステップ 4: セル範囲を作成する

```csharp
//セル範囲 A1:B3 を作成する
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

この例ではセル A1 からセル A7 までのセル範囲を作成します。必要に応じてセル参照を調整できます。

## ステップ 5: 範囲内のハイパーリンクを取得する

```csharp
//範囲内のハイパーリンクを取得します
Hyperlink[] hyperlinks = range.Hyperlinks;
```

指定された範囲内に存在するすべてのハイパーリンクを取得します。

## ステップ 6: ハイパーリンクを参照し、リンク タイプを表示する

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

各リンクをループして、表示テキストと関連するリンク タイプを表示します。

### Aspose.Cells for .NET を使用したリンク タイプの検出のサンプル ソース コード 
```csharp
//ソースディレクトリ
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
//最初の (デフォルト) ワークシートを取得する
Worksheet worksheet = workbook.Worksheets[0];
//範囲A2:B3を作成します
Range range = worksheet.Cells.CreateRange("A1", "A7");
//範囲内のハイパーリンクを取得
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel ワークブック内のリンク タイプを検出する方法を学習しました。この機能を使用すると、Excel ワークブックに存在するハイパーリンクを操作できるようになります。 Aspose.Cells の機能を引き続き探索して、Excel ワークブックの処理機能を拡張してください。

### よくある質問

#### Q: Aspose.Cells for .NET をプロジェクトにインストールするにはどうすればよいですか?

 A: NuGet パッケージ マネージャーを使用して、Aspose.Cells for .NET をインストールできます。検索する[アスポーズリリース](https://releases.aspose.com/cells/net)NuGet パッケージ マネージャー コンソールで、最新バージョンをインストールします。

#### Q: 最初のシートではなく特定のワークシートでリンク タイプを検出できますか?

 A: はい、変更できます。`workbook.Worksheets[0]`インデックスを使用して特定のワークシートにアクセスします。たとえば、2 番目のシートにアクセスするには、次を使用します。`workbook.Worksheets[1]`.

#### Q: 範囲内で検出されたリンクのタイプを変更することはできますか?

A: はい、ハイパーリンクを参照し、URL の更新や不要なリンクの削除などの編集操作を実行できます。

#### Q: Aspose.Cells for .NET ではどのようなタイプのリンクが可能ですか?

A: 考えられるリンクの種類には、ハイパーリンク、他のワークシートへのリンク、外部ファイルへのリンク、Web サイトへのリンクなどが含まれます。

#### Q: Aspose.Cells for .NET は、スプレッドシートでの新しいリンクの作成をサポートしていますか?

 A: はい、Aspose.Cells for .NET は、`Hyperlink`クラスとその関連プロパティ。ハイパーリンク、URL へのリンク、他のスプレッドシートへのリンクなどを追加できます。

#### Q: Web アプリケーションで Aspose.Cells for .NET を使用できますか?

A: はい、Aspose.Cells for .NET は Web アプリケーションで使用できます。 ASP.NET、ASP.NET Core、およびその他の .NET ベースの Web フレームワークに埋め込むことができます。

#### Q: Aspose.Cells for .NET を使用する場合、ファイル サイズの制限はありますか?

A: Aspose.Cells for .NET は、特別な制限なく大規模な Excel ワークブックを処理できます。ただし、実際のファイル サイズは、利用可能なシステム リソースによって制限される場合があります。