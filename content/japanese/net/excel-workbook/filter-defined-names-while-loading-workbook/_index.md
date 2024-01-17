---
title: ワークブックのロード中に定義された名前をフィルタリングする
linktitle: ワークブックのロード中に定義された名前をフィルタリングする
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークブックを読み込むときに、定義された名前をフィルターする方法を学びます。
type: docs
weight: 100
url: /ja/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
.NET アプリケーションで Excel ワークブックを操作する場合、多くの場合、読み込み時にデータをフィルターすることが必要になります。 Aspose.Cells for .NET は、Excel ワークブックを簡単に操作するための強力なライブラリです。このガイドでは、Aspose.Cells for .NET を使用してワークブックを読み込むときに定義された名前をフィルターする方法を説明します。望ましい結果を得るには、次の簡単な手順に従ってください。

## ステップ 1: 読み込みオプションを指定する

まず、読み込みオプションを指定して、ワークブックの読み込み動作を定義する必要があります。この例では、ロード時に設定された名前を無視したいと考えています。 Aspose.Cells を使用してこれを行う方法は次のとおりです。

```csharp
//読み込みオプションを指定します
LoadOptions opts = new LoadOptions();

//定義された名前をロードしない
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## ステップ 2: ワークブックをロードする

ロード オプションを構成したら、ソース ファイルから Excel ワークブックをロードできるようになります。必ず正しいファイル パスを指定してください。サンプルコードは次のとおりです。

```csharp
//ワークブックをロードする
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## ステップ 3: フィルタリングされたワークブックを保存する

ワークブックをロードした後、必要に応じて他の操作や編集を実行できます。その後、フィルター処理されたワークブックを出力ファイルに保存できます。その方法は次のとおりです。

```csharp
//フィルタリングされた Excel ワークブックを保存する
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Aspose.Cells for .NET を使用したワークブックのロード中に定義された名前をフィルターするためのサンプル ソース コード 
```csharp
//ロードオプションを指定する
LoadOptions opts = new LoadOptions();
//定義された名前をロードしたくない
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//ワークブックをロードする
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//出力 Excel ファイルを保存すると、C1 の数式が壊れます。
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## 結論

Excel ワークブックをロードするときに定義された名前をフィルタリングすることは、多くのアプリケーションにとって重要です。 Aspose.Cells for .NET は、データのロードとフィルタリングのための柔軟なオプションを提供することで、このタスクを容易にします。このガイドの手順に従うことで、定義された名前を効果的に除外し、Excel ワークブックで望ましい結果を得ることができます。


### よくある質問

#### Q: Aspose.Cells は C# 以外のプログラミング言語をサポートしていますか?
    
A: はい、Aspose.Cells は、Java、Python、C などの多くのプログラミング言語をサポートするクロスプラットフォーム ライブラリです。++、 などなど。

#### Q: Aspose.Cells を使用してワークブックを読み込むときに、他のデータ型をフィルターできますか?
    
A: はい、Aspose.Cells は、数式、スタイル、マクロなどを含むデータのさまざまなフィルター オプションを提供します。

#### Q: Aspose.Cells は元のワークブックの書式設定とプロパティを保持しますか?
    
A: はい、Aspose.Cells は Excel ファイルを操作するときに、元のブックの書式設定、スタイル、数式、その他のプロパティを保持します。