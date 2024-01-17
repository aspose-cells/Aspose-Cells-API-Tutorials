---
title: 他のワークシートからページ設定設定をコピー
linktitle: 他のワークシートからページ設定設定をコピー
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して、あるスプレッドシートから別のスプレッドシートにページ構成設定をコピーする方法を学びます。このライブラリの使用を最適化するためのステップバイステップのガイド。
type: docs
weight: 10
url: /ja/net/excel-page-setup/copy-page-setup-settings-from-other-worksheet/
---
この記事では、次の C# ソース コードについて順を追って説明します。 Aspose.Cells for .NET を使用して、別のスプレッドシートからページ構成設定をコピーします。この操作を実行するには、.NET 用の Aspose.Cells ライブラリを使用します。ページ設定設定をあるワークシートから別のワークシートにコピーする場合は、次の手順に従います。

## ステップ 1: ワークブックの作成
最初のステップはワークブックを作成することです。この例では、Aspose.Cells ライブラリによって提供される Workbook クラスを使用します。ワークブックを作成するコードは次のとおりです。

```csharp
Workbook wb = new Workbook();
```

## ステップ 2: テスト ワークシートの追加
ワークブックを作成した後、テスト ワークシートを追加する必要があります。この例では、2 つのワークシートを追加します。 2 つのワークシートを追加するコードは次のとおりです。

```csharp
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
```

## ステップ 3: ワークシートへのアクセス
ワークシートを追加したので、設定を変更できるようにワークシートにアクセスする必要があります。 「TestSheet1」と「TestSheet2」のワークシートに、それぞれの名前を使用してアクセスします。これにアクセスするコードは次のとおりです。

```csharp
Worksheet TestSheet1 = wb. Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb. Worksheets["TestSheet2"];
```

## ステップ 4: 用紙サイズの設定
このステップでは、「TestSheet1」ワークシートの用紙サイズを設定します。を使用します。`PageSetup.PaperSize`用紙サイズを設定するプロパティ。ここでは例として、用紙サイズを「PaperA3ExtraTransverse」に設定します。そのコードは次のとおりです。

```csharp
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
```

## ステップ 5: ページ設定の設定をコピーする
次に、ページ構成設定を「TestSheet1」ワークシートから「TestSheet2」にコピーします。を使用します。`PageSetup.Copy`この操作を実行するメソッド。そのコードは次のとおりです。

```csharp
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
```

## ステップ 6: 用紙サイズを印刷する
ページ設定設定をコピーした後、2 つのワークシートの用紙サイズを印刷します。我々は使用するだろう`Console.WriteLine`用紙サイズを表示します。そのコードは次のとおりです。

```csharp
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
```

### Aspose.Cells for .NET を使用して他のワークシートからページ設定設定をコピーするためのサンプル ソース コード 
```csharp
//ワークブックの作成
Workbook wb = new Workbook();
//つのテスト ワークシートを追加する
wb.Worksheets.Add("TestSheet1");
wb.Worksheets.Add("TestSheet2");
//両方のワークシートに TestSheet1 および TestSheet2 としてアクセスします
Worksheet TestSheet1 = wb.Worksheets["TestSheet1"];
Worksheet TestSheet2 = wb.Worksheets["TestSheet2"];
//TestSheet1の用紙サイズをPaperA3ExtraTransverseに設定します
TestSheet1.PageSetup.PaperSize = PaperSizeType.PaperA3ExtraTransverse;
//両方のワークシートの用紙サイズを印刷します。
Console.WriteLine("Before Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("Before Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
//PageSetup を TestSheet1 から TestSheet2 にコピーします
TestSheet2.PageSetup.Copy(TestSheet1.PageSetup, new CopyOptions());
//両方のワークシートの用紙サイズを印刷します。
Console.WriteLine("After Paper Size: " + TestSheet1.PageSetup.PaperSize);
Console.WriteLine("After Paper Size: " + TestSheet2.PageSetup.PaperSize);
Console.WriteLine();
Console.WriteLine("CopyPageSetupSettingsFromSourceWorksheetToDestinationWorksheet executed successfully.\r\n");
```

## 結論
この記事では、Aspose.Cells for .NET を使用して、あるワークシートから別のワークシートにページ構成設定をコピーする方法を学びました。次の手順を実行しました: ワークブックの作成、テスト ワークシートの追加、ワークシートへのアクセス、用紙サイズの設定、ページ設定設定のコピー、および用紙サイズの印刷。この知識を利用して、ページ構成設定を独自のプロジェクトにコピーできるようになりました。

### よくある質問

#### Q: 異なるワークブック インスタンス間でページ構成設定をコピーできますか?

 A: はい。`PageSetup.Copy` Aspose.Cells ライブラリのメソッド。

#### Q: 方向や余白など、他のページ設定設定をコピーできますか?

 A: はい、次のコマンドを使用して他のページ設定設定をコピーできます。`PageSetup.Copy`メソッドに適切なオプションを付けます。たとえば、次を使用して方向をコピーできます。`CopyOptions.Orientation`とマージンを使用して`CopyOptions.Margins`.

#### Q: 用紙サイズに使用できるオプションを確認するにはどうすればよいですか?

A: 用紙サイズに使用できるオプションについては、Aspose.Cells ライブラリ API リファレンスを確認してください。という列挙型があります`PaperSizeType`これは、サポートされているさまざまな用紙サイズのリストです。

#### Q: .NET 用の Aspose.Cells ライブラリをダウンロードするにはどうすればよいですか?

 A: .NET 用の Aspose.Cells ライブラリは、以下からダウンロードできます。[アスポーズリリース](https://releases.aspose.com/cells/net)。無料の試用版のほか、商用利用可能な有料ライセンスもあります。

#### Q: Aspose.Cells ライブラリは他のプログラミング言語をサポートしていますか?

A: はい、Aspose.Cells ライブラリは、C#、Java、Python などを含む複数のプログラミング言語をサポートしています。