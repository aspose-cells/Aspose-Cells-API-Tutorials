---
title: 正規表現の置換
linktitle: 正規表現の置換
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ファイルで正規表現置換を実行する方法を学びます。
type: docs
weight: 140
url: /ja/net/excel-workbook/regex-replace/
---
正規表現 (Regex) に基づくテキストの置換は、Excel ファイル内のデータを操作する際の一般的なタスクです。 Aspose.Cells for .NET を使用すると、次の手順に従って正規表現の置換を簡単に実行できます。

## ステップ 1: ソース ディレクトリと出力ディレクトリを指定する

まず、置換するデータを含む Excel ファイルが配置されているソース ディレクトリと、変更したファイルを保存する出力ディレクトリを指定する必要があります。 Aspose.Cells を使用してこれを行う方法は次のとおりです。

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();

//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

## ステップ 2: ソース Excel ファイルをロードする

次に、正規表現置換を実行するソース Excel ファイルをロードする必要があります。その方法は次のとおりです。

```csharp
//ソース Excel ファイルをロードします
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## ステップ 3: 正規表現の置換を実行する

ファイルをアップロードした後、大文字と小文字の区別やセル内容の正確な一致などの置換オプションを設定できます。 Regex 置換を実行するサンプル コードを次に示します。

```csharp
//置換オプションを設定する
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

//検索キーが正規表現であることを定義します
replace. RegexKey = true;

//正規表現の置換を実行する
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## ステップ 4: 出力された Excel ファイルを保存する

正規表現の置換が完了したら、変更した Excel ファイルを指定した出力ディレクトリに保存できます。その方法は次のとおりです。

```csharp
//出力された Excel ファイルを保存する
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Aspose.Cells for .NET を使用した Regex Replace のサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
//true に設定すると、検索されたキーが正規表現であることを示します
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## 結論

正規表現の置換は、Excel ファイル内のデータを動的に変更するための強力な手法です。 Aspose.Cells for .NET を使用すると、上記の手順に従って正規表現の置換を簡単に実行できます。独自の正規表現を試して、Aspose.Cells が提供する柔軟性を活用してください。

### よくある質問

#### Q: 正規表現置換とは何ですか?
    
A: 正規表現置換は、Excel ファイル内の正規表現に基づいてテキスト パターンを置換するために使用される技術です。これにより、データを迅速かつ正確に変更できます。

#### Q: 正規表現の置換では大文字と小文字が区別されますか?
    
A: いいえ、Aspose.Cells を使用すると、正規表現の置換で大文字と小文字を区別するかどうかを指定できます。この機能は完全に制御できます。

#### Q: Regex を置き換える場合、セルの内容の完全一致を指定するにはどうすればよいですか?
    
A: Aspose.Cells を使用すると、正規表現の置換がセルの内容と正確に一致するかどうかを定義できます。このオプションは必要に応じて調整できます。

#### Q: Regex を Aspose.Cells に置き換える場合、高度な正規表現を使用できますか?
    
A: はい、Aspose.Cells は高度な正規表現をサポートしているため、Excel ファイル内で複雑で洗練された置換を実行できます。

#### Q: 正規表現の置換が成功したかどうかを確認するにはどうすればよいですか?
    
A: Regex 置換を実行した後、出力をチェックし、出力 Excel ファイルが正しく作成されたことを確認することで、操作が成功したかどうかを確認できます。
	