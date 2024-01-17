---
title: 先頭のアポストロフィを許可する
linktitle: 先頭のアポストロフィを許可する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークブックの先頭にアポストロフィを使用できるようにします。
type: docs
weight: 60
url: /ja/net/excel-workbook/allow-leading-apostrophe/
---
このステップバイステップのチュートリアルでは、Aspose.Cells for .NET を使用して Excel ブックで先頭のアポストロフィを使用できるようにする、提供されている C# ソース コードについて説明します。この操作を行うには、次の手順に従ってください。

## ステップ 1: ソース ディレクトリと出力ディレクトリを設定する

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

この最初のステップでは、Excel ファイルのソース ディレクトリと出力ディレクトリを定義します。

## ステップ 2: WorkbookDesigner オブジェクトをインスタンス化する

```csharp
//WorkbookDesigner オブジェクトをインスタンス化する
WorkbookDesigner designer = new WorkbookDesigner();
```

のインスタンスを作成します。`WorkbookDesigner` Aspose.Cells のクラス。

## ステップ 3: Excel ワークブックをロードする

```csharp
// Excel ワークブックをロードする
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

指定されたファイルから Excel ワークブックをロードし、最初のアポストロフィのテキスト スタイルへの自動変換を無効にします。

## ステップ 4: データソースの設定

```csharp
//デザイナー ワークブックのデータ ソースを定義する
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

データオブジェクトのリストを定義し、`SetDataSource`デザイナー ワークブックのデータ ソースを設定するメソッド。

## ステップ 5: スマート マーカーを処理する

```csharp
//スマートマーカーを処理する
designer. Process();
```

私たちが使用するのは、`Process`デザイナー ワークブック内のスマート マーカーを処理するメソッド。

## ステップ 6: 変更した Excel ワークブックを保存する

```csharp
//変更した Excel ワークブックを保存する
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

変更を加えた Excel ワークブックを保存します。

### Aspose.Cells for .NET を使用して先頭のアポストロフィを許可するためのサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
//WorkbookDesigner オブジェクトのインスタンス化
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
//スマート マーカーを含むデザイナー スプレッドシートを開く
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
//デザイナー スプレッドシートのデータ ソースを設定する
designer.SetDataSource("sampleData", list);
//スマートマーカーを処理する
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して、Excel ブックで先頭のアポストロフィの使用を許可する方法を学習しました。独自のデータを試して、Excel ワークブックをさらにカスタマイズします。

### よくある質問

#### Q: Excel ワークブックの先頭のアポストロフィ許可とは何ですか?

A: Excel ワークブックで最初のアポストロフィを許可すると、アポストロフィで始まるデータをテキスト スタイルに変換せずに正しく表示できるようになります。これは、アポストロフィをデータの一部として保持したい場合に便利です。

#### Q: 最初のアポストロフィの自動変換をオフにする必要があるのはなぜですか?

A: 先頭の引用符の自動変換を無効にすると、データ内での引用符の使用をそのまま保持できます。これにより、Excel ワークブックを開いたり操作したりする際に、データが意図せず変更されることが回避されます。

#### Q: デザイナー ワークブックでデータソースを設定するにはどうすればよいですか?

 A: デザイナー ワークブックでデータ ソースを設定するには、`SetDataSource`データ ソースの名前と対応するデータ オブジェクトのリストを指定するメソッド。

#### Q: 先頭のアポストロフィを許可すると、Excel ブック内の他のデータに影響しますか?

A: いいえ、先頭のアポストロフィを許可すると、アポストロフィで始まるデータにのみ影響します。 Excel ワークブック内の他のデータは変更されません。

#### Q: この機能を他の Excel ファイル形式で使用できますか?

A: はい、この機能は、.xls、.xlsm など、Aspose.Cells でサポートされている他の Excel ファイル形式で使用できます。