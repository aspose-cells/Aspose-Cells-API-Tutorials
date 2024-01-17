---
title: 圧縮レベルを調整する
linktitle: 圧縮レベルを調整する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET で圧縮レベルを調整して、Excel ワークブックのサイズを削減します。
type: docs
weight: 50
url: /ja/net/excel-workbook/adjust-compression-level/
---
このステップバイステップのチュートリアルでは、Aspose.Cells for .NET を使用して圧縮レベルを調整できるようにする、提供されている C# ソース コードについて説明します。 Excel ワークブックの圧縮レベルを調整するには、以下の手順に従ってください。

## ステップ 1: ソース ディレクトリと出力ディレクトリを設定する

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outDir = RunExamples.Get_OutputDirectory();
```

この最初のステップでは、Excel ファイルのソース ディレクトリと出力ディレクトリを定義します。

## ステップ 2: Excel ワークブックをロードする

```csharp
// Excel ワークブックをロードする
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

次のコマンドを使用して、指定されたファイルから Excel ワークブックをロードします。`Workbook` Aspose.Cells のクラス。

## ステップ 3: バックアップ オプションを設定する

```csharp
//バックアップ オプションを定義する
XlsbSaveOptions options = new XlsbSaveOptions();
```

のインスタンスを作成します。`XlsbSaveOptions`保存オプションを設定するクラス。

## ステップ 4: 圧縮レベルを調整する (レベル 1)

```csharp
//圧縮レベルを調整します（レベル1）
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

設定により圧縮レベルを調整します`CompressionType`に`Level1`。次に、この圧縮オプションを指定して Excel ワークブックを保存します。

## ステップ 5: 圧縮レベルを調整します (レベル 6)

```csharp
//圧縮レベルを調整します (レベル 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

圧縮レベルを調整するプロセスを繰り返します。`Level6`このオプションを使用して Excel ワークブックを保存します。

## ステップ 6: 圧縮レベルを調整します (レベル 9)

```csharp
//圧縮レベルを調整します (レベル 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

最後にこのプロセスをもう一度繰り返して、圧縮レベルを調整します。`Level9`このオプションを使用して Excel ワークブックを保存します。

### Aspose.Cells for .NET を使用した圧縮レベルの調整のサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel ワークブックの圧縮レベルを調整する方法を学習しました。さまざまな圧縮レベルを試して、ニーズに最も適した圧縮レベルを見つけてください。

### よくある質問

#### Q: Excel ワークブックの圧縮とは何ですか?

A: Excel ワークブックの圧縮は、圧縮アルゴリズムを使用してファイル サイズを削減するプロセスです。これにより、必要なストレージ容量が削減され、ファイルのロードおよび操作時のパフォーマンスが向上します。

#### Q: Aspose.Cells ではどのレベルの圧縮が利用できますか?

A: Aspose.Cells を使用すると、圧縮レベルを 1 から 9 まで調整できます。圧縮レベルが高いほど、ファイル サイズは小さくなりますが、処理時間も長くなる可能性があります。

#### Q: Excel ワークブックに適切な圧縮レベルを選択するにはどうすればよいですか?

A: 圧縮レベルの選択は、特定のニーズによって異なります。最大の圧縮が必要で、処理時間は問題にならない場合は、レベル 9 を選択できます。ファイル サイズと処理時間の間で妥協したい場合は、中間レベルを選択できます。

#### Q: 圧縮は Excel ワークブックのデータ品質に影響しますか?

A: いいえ、圧縮は Excel ワークブックのデータ品質には影響しません。データ自体を変更することなく、圧縮技術を使用してファイル サイズを削減するだけです。

#### Q: Excel ファイルを保存した後に圧縮レベルを調整できますか?

A: いいえ、Excel ファイルを特定の圧縮レベルで保存すると、後で圧縮レベルを調整することはできません。ファイルを変更する場合は、新しい圧縮レベルでファイルを再度保存する必要があります。