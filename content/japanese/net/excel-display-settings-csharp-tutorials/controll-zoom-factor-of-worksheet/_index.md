---
title: ワークシートのズーム率の制御
linktitle: ワークシートのズーム率の制御
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel ワークシートのズーム率を制御します。
type: docs
weight: 20
url: /ja/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
ワークシートのズーム率の制御は、.NET 用の Aspose.Cells ライブラリを使用して Excel ファイルを操作する場合に不可欠な機能です。このガイドでは、Aspose.Cells を使用して、C# ソース コードを使用してワークシートのズーム率を制御する方法を段階的に説明します。

## ステップ 1: 必要なライブラリをインポートする

開始する前に、.NET 用の Aspose.Cells ライブラリがインストールされていることを確認し、必要なライブラリを C# プロジェクトにインポートしてください。

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## ステップ 2: ディレクトリ パスを設定して Excel ファイルを開く

まず、Excel ファイルを含むディレクトリへのパスを設定し、次のコマンドを使用してファイルを開きます。`FileStream`オブジェクトを作成してインスタンス化する`Workbook`Excel ワークブックを表すオブジェクト。

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## ステップ 3: スプレッドシートにアクセスしてズーム率を変更する

このステップでは、インデックスを使用して Excel ワークブックの最初のワークシートにアクセスします。`0`ワークシートのズーム率を次のように設定します。`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## ステップ 4: 変更を保存してファイルを閉じる

ワークシートのズーム率を変更したら、次のコマンドを使用して変更を Excel ファイルに保存します。`Save`の方法`Workbook`物体。次に、ファイル ストリームを閉じて、使用されているすべてのリソースを解放します。

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Aspose.Cells for .NET を使用したワークシートのズーム係数の制御のサンプル ソース コード 

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
//ワークシートのズーム率を 75 に設定する
worksheet.Zoom = 75;
//変更したExcelファイルを保存する
workbook.Save(dataDir + "output.xls");
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

このステップバイステップ ガイドでは、Aspose.Cells for .NET を使用してワークシートのズーム率を制御する方法を説明しました。提供されている C# ソース コードを使用すると、.NET アプリケーションでワークシートのズーム率を簡単に調整できます。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、.NET アプリケーションで Excel ファイルを操作するための機能が豊富なファイリング ライブラリです。

#### Aspose.Cells for .NET をインストールするにはどうすればよいですか?

 Aspose.Cells for .NET をインストールするには、対応する NuGet パッケージを次からダウンロードする必要があります。[アスポーズリリース](https://releases/aspose.com/cells/net/)それを .NET プロジェクトに追加します。

#### Aspose.Cells for .NET はどのような機能を提供しますか?

Aspose.Cells for .NET は、Excel ファイルの作成、編集、変換、高度な操作などの機能を提供します。

#### Aspose.Cells for .NET ではどのようなファイル形式がサポートされていますか?

Aspose.Cells for .NET は、XLSX、XLSM、CSV、HTML、PDF などを含む複数のファイル形式をサポートしています。
