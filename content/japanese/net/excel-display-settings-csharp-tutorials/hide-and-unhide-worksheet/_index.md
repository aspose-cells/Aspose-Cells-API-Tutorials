---
title: ワークシートの非表示と再表示
linktitle: ワークシートの非表示と再表示
second_title: Aspose.Cells for .NET API リファレンス
description: データの作成、変更、操作など、Excel ファイルを操作するための強力なライブラリです。
type: docs
weight: 90
url: /ja/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
このチュートリアルでは、Aspose.Cells for .NET を使用してワークシートを非表示にしたり表示したりするために使用される次の C# ソース コードを段階的に説明します。以下の手順に従います。

## ステップ 1: 環境を準備する

始める前に、Aspose.Cells for .NET がシステムにインストールされていることを確認してください。まだインストールしていない場合は、Aspose の公式 Web サイトからダウンロードできます。インストールしたら、好みの統合開発環境 (IDE) で新しいプロジェクトを作成できます。

## ステップ 2: 必要な名前空間をインポートする

C# ソース ファイルに、Aspose.Cells の機能を使用するために必要な名前空間を追加します。ファイルの先頭に次の行を追加します。

```csharp
using Aspose.Cells;
using System.IO;
```

## ステップ 3: Excel ファイルをロードする

ワークシートを非表示または再表示する前に、Excel ファイルをアプリケーションにロードする必要があります。使用する Excel ファイルがプロジェクトと同じディレクトリにあることを確認してください。次のコードを使用して Excel ファイルをロードします。

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

必ず「PATH TO YOUR DOCUMENTS DIRECTORY」を Excel ファイルが含まれるディレクトリへの実際のパスに置き換えてください。

## ステップ 4: スプレッドシートにアクセスする

Excel ファイルがロードされたら、非表示または再表示するワークシートに移動できます。ファイル内の最初のワークシートにアクセスするには、次のコードを使用します。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## ステップ 5: ワークシートを非表示にする

ワークシートにアクセスしたので、次のコマンドを使用してワークシートを非表示にできます。`IsVisible`財産。ファイル内の最初のワークシートを非表示にするには、次のコードを使用します。

```csharp
worksheet. IsVisible = false;
```

## ステップ 6: ワークシートを再表示する

以前に非表示にしたワークシートを再表示したい場合は、`IsVisible`財産。最初のワークシートを再表示するには、次のコードを使用します。

```csharp
worksheet. IsVisible = true;
```

## ステップ 7: 変更を保存する

一度あなたが

  必要に応じてワークシートを非表示または再表示した場合は、変更を Excel ファイルに保存する必要があります。次のコードを使用して変更を保存します。

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

変更した Excel ファイルを保存するには、必ず正しい出力パスを指定してください。

### Aspose.Cells for .NET を使用したワークシートの非表示と再表示のサンプル ソース コード 

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//開く Excel ファイルを含むファイル ストリームの作成
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//ファイル ストリームを通じて Excel ファイルを開いて Workbook オブジェクトをインスタンス化する
Workbook workbook = new Workbook(fstream);
//Excel ファイルの最初のワークシートへのアクセス
Worksheet worksheet = workbook.Worksheets[0];
//Excel ファイルの最初のワークシートを非表示にする
worksheet.IsVisible = false;
//Excel ファイルの最初のワークシートを表示します
//Worksheet.IsVisible = true;
//変更した Excel ファイルをデフォルト (つまり Excel 2003) 形式で保存する
workbook.Save(dataDir + "output.out.xls");
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用してスプレッドシートを非表示にしたり表示したりする方法を学習しました。この機能を使用して、Excel ファイル内のスプレッドシートの表示/非表示を制御できるようになりました。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET をインストールするにはどうすればよいですか?

関連する NuGet パッケージを次からダウンロードすることで、Aspose.Cells for .NET をインストールできます。[アスポーズリリース](https://releases/aspose.com/cells/net/)それを Visual Studio プロジェクトに追加します。

#### Aspose.Cells for .NET を使用するために最低限必要な .NET Framework のバージョンは何ですか?

Aspose.Cells for .NET は、.NET Framework 2.0 以降をサポートします。

#### Aspose.Cells for .NET を使用して既存の Excel ファイルを開いて編集できますか?

はい、Aspose.Cells for .NET を使用して既存の Excel ファイルを開いて編集できます。 Excel ファイルのワークシート、セル、数式、その他の要素にアクセスできます。

#### Aspose.Cells for .NET はレポート作成と他のファイル形式へのエクスポートをサポートしていますか?

はい、Aspose.Cells for .NET はレポートの生成と PDF、HTML、CSV、TXT などの形式へのエクスポートをサポートしています。

#### Excel ファイルの変更は永続的なものですか?

はい、Excel ファイルの編集は一度保存すると永続的になります。元のファイルに変更を加える前に、必ずバックアップ コピーを保存してください。