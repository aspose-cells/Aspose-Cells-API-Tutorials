---
title: ワークシートのスクロールバーの表示と非表示を切り替える
linktitle: ワークシートのスクロールバーの表示と非表示を切り替える
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークシートのスクロール バーを表示または非表示にします。
type: docs
weight: 50
url: /ja/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
このチュートリアルでは、C# ソース コードと Aspose.Cells for .NET を使用して、Excel ワークシートの垂直スクロール バーと水平スクロール バーを表示または非表示にする方法を説明します。望ましい結果を得るには、以下の手順に従ってください。

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

## ステップ 3: スクロールバーを非表示にする

使用`IsVScrollBarVisible`そして`IsHScrollBarVisible`のプロパティ`Workbook.Settings`オブジェクトを使用して、ワークシートの垂直スクロールバーと水平スクロールバーを非表示にします。

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## ステップ 4: 変更を保存する

必要な変更を加えたら、変更した Excel ファイルを次のコマンドを使用して保存します。`Save`の方法`Workbook`物体。

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET を使用したワークシートのスクロール バーの表示と非表示のサンプル ソース コード 

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//開く Excel ファイルを含むファイル ストリームの作成
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//Workbook オブジェクトのインスタンス化
//ファイル ストリーム経由で Excel ファイルを開く
Workbook workbook = new Workbook(fstream);
//Excelファイルの垂直スクロールバーを非表示にする
workbook.Settings.IsVScrollBarVisible = false;
//Excelファイルの横スクロールバーを非表示にする
workbook.Settings.IsHScrollBarVisible = false;
//変更したExcelファイルを保存する
workbook.Save(dataDir + "output.xls");
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

### 結論

このステップバイステップのガイドでは、Aspose.Cells for .NET を使用して Excel スプレッドシートの垂直スクロール バーと水平スクロール バーを表示または非表示にする方法を説明しました。提供されている C# ソース コードを使用すると、Excel ファイルのスクロールバーの表示を簡単にカスタマイズできます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作するための強力なライブラリです。

#### Aspose.Cells for .NET をインストールするにはどうすればよいですか?

 Aspose.Cells for .NET をインストールするには、関連するパッケージを次からダウンロードする必要があります。[アスポーズリリース](https://releases/aspose.com/cells/net/)それを .NET プロジェクトに追加します。

#### Aspose.Cells for .NET を使用して Excel スプレッドシートのスクロールバーを表示または非表示にするにはどうすればよいですか?

使用できます`IsVScrollBarVisible`そして`IsHScrollBarVisible`のプロパティ`Workbook.Settings`オブジェクトを使用して、Excel ワークシートの垂直スクロール バーと水平スクロール バーをそれぞれ表示または非表示にします。

#### Aspose.Cells for .NET では他にどのような Excel ファイル形式がサポートされていますか?

Aspose.Cells for .NET は、XLS、XLSX、CSV、HTML、PDF などのさまざまな Excel ファイル形式をサポートしています。