---
title: 埋め込まれた MOL ファイルの抽出
linktitle: 埋め込まれた MOL ファイルの抽出
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークブックから埋め込み MOL ファイルを簡単に抽出する方法を学びます。
type: docs
weight: 90
url: /ja/net/excel-workbook/extract-embedded-mol-file/
---
このチュートリアルでは、.NET 用の Aspose.Cells ライブラリを使用して Excel ワークブックから埋め込み MOL ファイルを抽出する方法を段階的に説明します。ワークブックのシートを参照し、対応する OLE オブジェクトを抽出し、抽出された MOL ファイルを保存する方法を学習します。このタスクを正常に完了するには、次の手順に従ってください。

## ステップ 1: ソース ディレクトリと出力ディレクトリを定義する
まず、コード内でソース ディレクトリと出力ディレクトリを定義する必要があります。これらのディレクトリは、ソース Excel ワークブックの場所と、抽出された MOL ファイルの保存場所を示します。対応するコードは次のとおりです。

```csharp
//ディレクトリ
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

必要に応じて適切なパスを指定してください。

## ステップ 2: Excel ワークブックをロードする
次の手順では、埋め込み OLE オブジェクトと MOL ファイルを含む Excel ワークブックをロードします。ワークブックをロードするコードは次のとおりです。

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

コード内でソース ファイル名を正しく指定してください。

## ステップ 3: シートをスキャンして MOL ファイルを抽出する
次に、ワークブック内の各シートをループし、MOL ファイルを含む対応する OLE オブジェクトを抽出します。対応するコードは次のとおりです。

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

このコードは、ワークブック内の各シートをループし、OLE オブジェクトを取得し、抽出された MOL ファイルを出力ディレクトリに保存します。

### Aspose.Cells for .NET を使用した埋め込み Mol ファイルの抽出のサンプル ソース コード 
```csharp
//ディレクトリ
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## 結論
おめでとうございます！ Aspose.Cells for .NET を使用して Excel ワークブックから埋め込み MOL ファイルを抽出する方法を学習しました。この知識を応用して、独自の Excel ワークブックから MOL ファイルを抽出できるようになりました。 Aspose.Cells ライブラリをさらに探索して、その他の強力な機能について学んでください。

### よくある質問

#### Q: MOL ファイルとは何ですか?
 
A: MOL ファイルは、計算化学で化学構造を表すために使用されるファイル形式です。原子、結合、その他の分子特性に関する情報が含まれています。

#### Q: この方法はすべての Excel ファイル タイプで機能しますか?

A: はい、この方法は、Aspose.Cells でサポートされているすべての Excel ファイル タイプで機能します。

#### Q: 複数の MOL ファイルを一度に抽出できますか?

A: はい、ワークブック内の各シートの OLE オブジェクトを反復処理することで、複数の MOL ファイルを一度に抽出できます。