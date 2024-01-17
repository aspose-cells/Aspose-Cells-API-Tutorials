---
title: ワークシートのグリッド線の表示と非表示を切り替える
linktitle: ワークシートのグリッド線の表示と非表示を切り替える
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークシートのグリッド線の表示を制御します。
type: docs
weight: 30
url: /ja/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
このチュートリアルでは、C# ソース コードと Aspose.Cells for .NET を使用して Excel ワークシートでグリッド線を表示および非表示にする方法を説明します。望ましい結果を得るには、以下の手順に従ってください。

## ステップ 1: 必要なライブラリをインポートする

.NET 用の Aspose.Cells ライブラリがインストールされていることを確認し、必要なライブラリを C# プロジェクトにインポートしてください。

```csharp
using Aspose.Cells;
using System.IO;
```

## ステップ 2: ディレクトリ パスを設定し、Excel ファイルを開きます

 Excel ファイルを含むディレクトリへのパスを設定し、ファイル ストリームを作成してファイルをインスタンス化してファイルを開きます。`Workbook`物体。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## ステップ 3: 最初のワークシートに移動し、グリッド線を非表示にします

Excel ファイルの最初のワークシートにアクセスするには、`Worksheets`の財産`Workbook`物体。次に、`IsGridlinesVisible`の財産`Worksheet`オブジェクトを使用してグリッド線を非表示にします。

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## ステップ 4: 変更を保存する

必要な変更を加えたら、変更した Excel ファイルを次のコマンドを使用して保存します。`Save`の方法`Workbook`物体。

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET を使用したワークシートのグリッド線の表示と非表示のサンプル ソース コード 

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
//Excelファイルの最初のワークシートのグリッド線を非表示にする
worksheet.IsGridlinesVisible = false;
//変更したExcelファイルを保存する
workbook.Save(dataDir + "output.xls");
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

このステップバイステップのガイドでは、Aspose.Cells for .NET を使用して Excel スプレッドシートのグリッド線を表示および非表示にする方法を説明しました。提供されている C# ソース コードを使用すると、Excel ファイルのグリッド線の表示を簡単にカスタマイズできます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作するための強力なライブラリです。

#### Aspose.Cells for .NET をインストールするにはどうすればよいですか?

 Aspose.Cells for .NET をインストールするには、関連するパッケージを次からダウンロードする必要があります。[アスポーズリリース](https://releases/aspose.com/cells/net/)それを .NET プロジェクトに追加します。

#### Aspose.Cells for .NET を使用して Excel スプレッドシートのグリッド線を表示または非表示にするにはどうすればよいですか?

使用できます`IsGridlinesVisible`の財産`Worksheet`グリッド線を表示または非表示にするオブジェクト。に設定します`true`それらを見せて、`false`それらを隠すために。

#### Aspose.Cells for .NET では他にどのような Excel ファイル形式がサポートされていますか?

Aspose.Cells for .NET は、XLS、XLSX、CSV、HTML、PDF など、さまざまな Excel ファイル形式をサポートしています。

