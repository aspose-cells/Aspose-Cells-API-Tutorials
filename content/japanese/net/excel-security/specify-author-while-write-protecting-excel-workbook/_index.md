---
title: Excel ワークブックの書き込み保護時に作成者を指定する
linktitle: Excel ワークブックの書き込み保護時に作成者を指定する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークブックを保護およびカスタマイズする方法を学びます。 C# のステップバイステップのチュートリアル。
type: docs
weight: 30
url: /ja/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

このチュートリアルでは、.NET 用の Aspose.Cells ライブラリを使用して Excel ブックを書き込み保護するときに作成者を指定する方法を説明します。

## ステップ 1: 環境を準備する

始める前に、Aspose.Cells for .NET がマシンにインストールされていることを確認してください。 Aspose 公式 Web サイトからライブラリをダウンロードし、提供されるインストール手順に従います。

## ステップ 2: ソース ディレクトリと出力ディレクトリの構成

提供されたソース コードでは、ソース ディレクトリと出力ディレクトリを指定する必要があります。を変更します。`sourceDir`そして`outputDir` 「YOUR SOURCE DIRECTORY」と「YOUR OUTPUT DIRECTORY」をマシン上のそれぞれの絶対パスに置き換えて変数を追加します。

```csharp
//ソースディレクトリ
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

//出力ディレクトリ
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## ステップ 3: 空の Excel ワークブックを作成する

まず、空の Excel ブックを表す Workbook オブジェクトを作成します。

```csharp
//空のワークブックを作成します。
Workbook wb = new Workbook();
```

## ステップ 4: パスワードによる書き込み保護

次に、Excel ワークブックを書き込み保護するためのパスワードを指定します。`WriteProtection.Password` Workbook オブジェクトのプロパティ。

```csharp
//ワークブックの書き込みをパスワードで保護します。
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## ステップ 5: 著者の指定

次に、次のコマンドを使用して Excel ワークブックの作成者を指定します。`WriteProtection.Author` Workbook オブジェクトのプロパティ。

```csharp
//ワークブックの書き込み保護中に作成者を指定します。
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## ステップ 6: 保護された Excel ワークブックをバックアップする

書き込み保護と作成者を指定したら、次のコマンドを使用して Excel ワークブックを XLSX 形式で保存できます。`Save()`方法。

```csharp
//ワークブックを XLSX 形式で保存します。
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Aspose.Cells for .NET を使用した Excel ワークブックの書き込み保護中に作成者を指定するためのサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = "YOUR SOURCE DIRECTORY";

//出力ディレクトリ
string outputDir = "YOUR OUTPUT DIRECTORY";

//空のワークブックを作成します。
Workbook wb = new Workbook();

//ワークブックの書き込みをパスワードで保護します。
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

//ワークブックの書き込み保護中に作成者を指定します。
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

//ワークブックを XLSX 形式で保存します。
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel ワークブックを書き込み保護するときに作成者を指定する方法を学習しました。これらの手順を独自のプロジェクトに適用して、Excel ワークブックを保護およびカスタマイズできます。

Excel ファイルに対するより高度な操作については、Aspose.Cells for .NET の機能を自由に調べてください。

## よくある質問

#### Q: パスワードを指定せずに Excel ワークブックを書き込み禁止にすることはできますか?

 A: はい、Workbook オブジェクトの`WriteProtect()`パスワードを指定せずに Excel ブックを書き込み保護する方法。これにより、パスワードを必要とせずにブックへの変更が制限されます。

#### Q: Excel ワークブックから書き込み保護を削除するにはどうすればよいですか?

 A: Excel ワークブックから書き込み保護を削除するには、`Unprotect()` Worksheet オブジェクトのメソッド、または`RemoveWriteProtection()`特定の使用例に応じて、Workbook オブジェクトのメソッド。 。

#### Q: Excel ブックを保護するためのパスワードを忘れてしまいました。私に何ができる ？

A: Excel ブックを保護するためのパスワードを忘れた場合、それを直接削除することはできません。ただし、保護された Excel ファイルのパスワード回復機能を提供する専用のサードパーティ ツールを使用してみることもできます。

#### Q: Excel ワークブックを書き込み保護するときに複数の作成者を指定することはできますか?

A: いいえ、Aspose.Cells for .NET ライブラリでは、Excel ワークブックを書き込み保護するときに単一の作成者を指定できます。複数の作成者を指定する場合は、Excel ファイルを直接操作してカスタム ソリューションを検討する必要があります。