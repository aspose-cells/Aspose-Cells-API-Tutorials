---
title: ワークブックの印刷プレビュー
linktitle: ワークブックの印刷プレビュー
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用してワークブックの印刷プレビューを生成する方法を学習します。
type: docs
weight: 170
url: /ja/net/excel-workbook/workbook-print-preview/
---
ワークブックの印刷プレビューは、Aspose.Cells for .NET を使用して Excel ファイルを操作する場合に不可欠な機能です。次の手順に従って、印刷プレビューを簡単に生成できます。

## ステップ 1: ソース ディレクトリを指定する

まず、プレビューする Excel ファイルが配置されているソース ディレクトリを指定する必要があります。その方法は次のとおりです。

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
```

## ステップ 2: ワークブックをロードする

次に、指定した Excel ファイルから Workbook ワークブックをロードする必要があります。その方法は次のとおりです。

```csharp
// Workbook ワークブックをロードする
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## ステップ 3: 画像と印刷のオプションを構成する

印刷プレビューを生成する前に、必要に応じて画像と印刷のオプションを構成できます。この例では、デフォルトのオプションを使用しています。その方法は次のとおりです。

```csharp
//画像と印刷のオプション
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## ステップ 4: ワークブックの印刷プレビューを生成する

WorkbookPrintingPreview クラスを使用して、Workbook ワークブックの印刷プレビューを生成できるようになりました。その方法は次のとおりです。

```csharp
//ワークブックの印刷プレビュー
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## ステップ 5: ワークシートの印刷プレビューを生成する

特定のワークシートの印刷プレビューを生成したい場合は、SheetPrintingPreview クラスを使用できます。以下に例を示します。

```csharp
//ワークシートの印刷プレビュー
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Aspose.Cells for .NET を使用したワークブック印刷プレビューのサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## 結論

ワークブックの印刷プレビューの生成は、Aspose.Cells for .NET によって提供される強力な機能です。上記の手順に従うと、Excel ワークブックを簡単にプレビューし、印刷するページ数に関する情報を取得できます。

### よくある質問

#### Q: ワークブックをロードするために別のソース ディレクトリを指定するにはどうすればよいですか?
    
 A: を使用できます。`Set_SourceDirectory`別のソース ディレクトリを指定するメソッド。例えば：`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Q: 印刷プレビューを生成するときに画像と印刷のオプションをカスタマイズできますか?
    
 A: はい、プロパティを変更することで、画像と印刷のオプションをカスタマイズできます。`ImageOrPrintOptions`物体。たとえば、画像の解像度、出力ファイル形式などを設定できます。

#### Q: ワークブック内の複数のワークシートの印刷プレビューを生成することはできますか?
    
A: はい、ワークブック内のさまざまなワークシートを反復処理し、各シートの印刷プレビューを生成できます。`SheetPrintingPreview`クラス。

#### Q: 印刷プレビューを画像または PDF ファイルとして保存するにはどうすればよいですか?
    
 A: 使用できます`ToImage`または`ToPdf`の方法`WorkbookPrintingPreview`または`SheetPrintingPreview`印刷プレビューを画像または PDF ファイルとして保存するオブジェクト。

#### Q: 生成された印刷プレビューでは何ができるのですか?
    
A: 印刷プレビューを生成したら、画面上で表示したり、画像または PDF ファイルとして保存したり、電子メールでの送信や印刷などの他の操作に使用したりできます。
	