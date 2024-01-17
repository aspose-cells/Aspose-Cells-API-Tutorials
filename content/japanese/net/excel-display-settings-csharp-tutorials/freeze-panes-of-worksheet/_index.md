---
title: ワークシートのペインを固定する
linktitle: ワークシートのペインを固定する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用すると、Excel ワークシートのフリーズ ペインを簡単に操作できます。
type: docs
weight: 70
url: /ja/net/excel-display-settings-csharp-tutorials/freeze-panes-of-worksheet/
---
このチュートリアルでは、C# ソース コードと Aspose.Cells for .NET を使用して Excel ワークシートのペインをロックする方法を説明します。望ましい結果を得るには、以下の手順に従ってください。

## ステップ 1: 必要なライブラリをインポートする

.NET 用の Aspose.Cells ライブラリがインストールされていることを確認し、必要なライブラリを C# プロジェクトにインポートしてください。

```csharp
using Aspose.Cells;
```

## ステップ 2: ディレクトリ パスを設定し、Excel ファイルを開きます

Excel ファイルを含むディレクトリへのパスを設定し、インスタンス化してファイルを開きます。`Workbook`物体。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## ステップ 3: スプレッドシートに移動し、ペインのロック設定を適用します。

を使用して、Excel ファイルの最初のワークシートに移動します。`Worksheet`物体。次に、`FreezePanes`ペインのロック設定を適用するメソッド。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. FreezePanes(3, 2, 3, 2);
```

上の例では、ペインは行 3、列 2 のセルにロックされています。

## ステップ 4: 変更を保存する

必要な変更を加えたら、変更した Excel ファイルを次のコマンドを使用して保存します。`Save`の方法`Workbook`物体。

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET を使用したワークシートのペインの固定のサンプル ソース コード 

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//開く Excel ファイルを含むファイル ストリームの作成
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//Workbook オブジェクトのインスタンス化
//ファイル ストリーム経由で Excel ファイルを開く
Workbook workbook = new Workbook(fstream);
//Excel ファイルの最初のワークシートへのアクセス
Worksheet worksheet = workbook.Worksheets[0];
//フリーズペイン設定の適用
worksheet.FreezePanes(3, 2, 3, 2);
//変更したExcelファイルを保存する
workbook.Save(dataDir + "output.xls");
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

このステップバイステップ ガイドでは、Aspose.Cells for .NET を使用して Excel スプレッドシートのペインをロックする方法を説明しました。提供されている C# ソース コードを使用すると、ペイン ロック設定を簡単にカスタマイズして、Excel ファイル内のデータをより適切に整理および視覚化できます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作するための強力なライブラリです。

#### Aspose.Cells for .NET をインストールするにはどうすればよいですか?

 Aspose.Cells for .NET をインストールするには、関連するパッケージを次からダウンロードする必要があります。[アスポーズリリース](https://releases/aspose.com/cells/net/)それを .NET プロジェクトに追加します。

#### Aspose.Cells for .NET を使用して Excel ワークシートのペインをロックするにはどうすればよいですか?

使用できます`FreezePanes`の方法`Worksheet`ワークシートのペインをロックするオブジェクト。行インデックスと列インデックスを指定して、ロックするセルを指定します。

#### Aspose.Cells for .NET を使用してペイン ロック設定をカスタマイズできますか?

はい、を使用して、`FreezePanes`メソッドを使用すると、必要に応じてロックするセルを指定し、適切な行インデックスと列インデックスを指定できます。
