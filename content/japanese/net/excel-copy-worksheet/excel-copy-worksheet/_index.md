---
title: Excelコピーワークシート
linktitle: Excelコピーワークシート
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して、ある Excel ワークシートを別の Excel ワークシートにコピーします。
type: docs
weight: 20
url: /ja/net/excel-copy-worksheet/excel-copy-worksheet/
---

このガイドでは、.NET 用の Aspose.Cells ライブラリを使用して Excel ワークシートをコピーする方法を説明します。 C# ソース コードを提供し、このタスクを完了するために必要な手順を説明します。最後に、期待される結果を示します。以下の手順に従って開始してください。

## ステップ 1: 準備

始める前に、Aspose.Cells for .NET がインストールされ、好みの統合開発環境 (IDE) で C# プロジェクトが作成されていることを確認してください。また、操作する Excel ファイルのコピーがあることを確認してください。

## ステップ 2: 必要なライブラリをインポートする

C# ソース ファイルで、次のコマンドを使用して、Aspose.Cells から必要なライブラリをインポートします。`using`指令：

```csharp
using Aspose.Cells;
```

## ステップ 3: ファイルパスを設定する

を宣言します`dataDir`変数を指定し、Excel ファイルを含むディレクトリで初期化します。例えば ：

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

必ず交換してください`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"`ディレクトリへの実際のパスを使用します。

## ステップ 4: 既存の Excel ファイルをロードする

使用`Workbook`Aspose.Cells のクラスを使用して既存の Excel ファイルを開きます。使用`InputPath`ファイルパスを指定する変数:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

交換したことを確認してください`"book1.xls"`Excel ファイルの実際の名前を置き換えます。

## ステップ 5: ワークシートをコピーする

次に、既存のワークシートを新しいワークシートにコピーします。使用`Worksheets`の財産`Workbook`オブジェクトを使用してワークシートのコレクションにアクセスします。

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

次に、`AddCopy`指定されたワークシートをコピーするメソッド。たとえば、「Sheet1」をコピーするには:

```csharp
sheets.AddCopy("Sheet1");
```

## ステップ 6: Excel ファイルを保存する

使用`Save`の方法`Workbook`新しいファイルに変更を保存するオブジェクト:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

出力ファイルに必要なパスとファイル名を必ず指定してください。

### Aspose.Cells for .NET を使用した Excel コピー ワークシートのサンプル ソース コード 

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
//既存の Excel ファイルを開きます。
Workbook wb = new Workbook(InputPath);
//を参照して Worksheets オブジェクトを作成します。
//ワークブックのシート。
WorksheetCollection sheets = wb.Worksheets;
//既存のシートから新しいシートにデータをコピーする
//ワークブック内のシート。
sheets.AddCopy("Sheet1");
// Excel ファイルを保存します。
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel ワークシートをコピーする方法を学習しました。このステップバイステップのガイドでは、必要なライブラリをインポートし、既存の Excel ファイルをロードし、ワークシートをコピーし、変更したファイルを保存する方法を示しました。独自のプロジェクトでこの方法を自由に使用して、Excel ファイルを効率的に操作してください。

### よくある質問

#### Q. Aspose.Cells は他のプログラミング言語と互換性がありますか?

A. はい、Aspose.Cells は、C#、Java、Python などを含む複数のプログラミング言語をサポートしています。

#### Q. ワークシートを別の Excel ワークブックにコピーできますか?

A. はい、使用できます`AddCopy`ワークシートを別の Excel ワークブックにコピーするメソッド。

#### Q. Aspose.Cells は、ワークシートをコピーするときに数式と書式設定を保持しますか?

A. はい、Aspose.Cells はワークシートをコピーするときに数式、書式設定、その他のプロパティを保持します。

#### Q. Aspose.Cells を商用利用するにはライセンスが必要ですか?

A. はい、Aspose.Cells は商用製品であり、商用利用するにはライセンスを購入する必要があります。詳しいライセンス情報は、Aspose の公式 Web サイトでご覧いただけます。