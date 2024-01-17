---
title: Power Query の数式項目を更新する
linktitle: Power Query の数式項目を更新する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ファイル内の Power Query 数式要素を更新する方法を学習します。
type: docs
weight: 160
url: /ja/net/excel-workbook/update-power-query-formula-item/
---
Power Query の数式項目の更新は、Excel ファイル内のデータを操作する場合の一般的な操作です。 Aspose.Cells for .NET を使用すると、次の手順に従って Power Query の数式項目を簡単に更新できます。

## ステップ 1: ソース ディレクトリと出力ディレクトリを指定する

まず、更新する Power Query 式を含む Excel ファイルが配置されているソース ディレクトリと、変更したファイルを保存する出力ディレクトリを指定する必要があります。 Aspose.Cells を使用してこれを行う方法は次のとおりです。

```csharp
//ソースディレクトリ
string SourceDir = RunExamples.Get_SourceDirectory();

//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

## ステップ 2: ソース Excel ワークブックをロードする

次に、Power Query 数式項目を更新するソース Excel ブックを読み込む必要があります。その方法は次のとおりです。

```csharp
//ソース Excel ワークブックをロードします
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## ステップ 3: Power Query の数式項目を参照して更新する

ブックを読み込んだ後、Power Query 数式コレクションに移動し、各数式とその要素を参照できます。この例では、「Source」という名前の数式項目を検索し、その値を更新します。 Power Query の数式項目を更新するサンプル コードを次に示します。

```csharp
// Power Query 数式コレクションにアクセスする
DataMashup mashupData = workbook.DataMashup;

//Power Query の数式とその要素をループする
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## ステップ 4: 出力された Excel ワークブックを保存する

Power Query の数式項目を更新したら、変更した Excel ブックを指定した出力ディレクトリに保存できます。その方法は次のとおりです。

```csharp
//出力された Excel ワークブックを保存する
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Aspose.Cells for .NET を使用した Power Query 数式項目の更新のサンプル ソース コード 
```csharp
//作業ディレクトリ
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
//出力されたワークブックを保存します。
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## 結論

Power Query の数式要素の更新は、Aspose.Cells を使用して Excel ファイル内のデータを操作および処理する場合に不可欠な操作です。上記の手順に従うことで、数式要素を簡単に更新できます

### よくある質問

#### Q: Excel の Power Query とは何ですか?
     
A: Power Query は、さまざまなソースからデータを収集、変換、ロードするのに役立つ Excel の機能です。 Excel にインポートする前にデータをクリーンアップ、結合、再形成するための強力なツールを提供します。

#### Q: Power Query の数式項目が正常に更新されたかどうかを確認するにはどうすればよいですか?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### Q: 複数の Power Query 数式アイテムを一度に更新できますか?
    
A: はい、特定のニーズに応じて、Power Query の数式項目コレクションをループし、1 回のループで複数の項目を更新できます。

#### Q: Aspose.Cells を使用して Power Query の数式に対して実行できる操作は他にもありますか?
    
A: はい、Aspose.Cells は、Excel ブック内の数式の作成、削除、コピー、検索など、Power Query 数式を操作するためのあらゆる機能を提供します。