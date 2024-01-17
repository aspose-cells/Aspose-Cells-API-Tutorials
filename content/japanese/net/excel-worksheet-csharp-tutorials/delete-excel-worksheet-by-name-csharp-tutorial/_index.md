---
title: Excel ワークシートを名前で削除する C# チュートリアル
linktitle: Excel ワークシートを名前で削除
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用すると、特定の Excel ワークシートを名前で簡単に削除できます。コード例を含む詳細なチュートリアル。
type: docs
weight: 40
url: /ja/net/excel-worksheet-csharp-tutorials/delete-excel-worksheet-by-name-csharp-tutorial/
---
このチュートリアルでは、Aspose.Cells for .NET を使用してその名前を使用して Excel ワークシートを削除できる以下の C# ソース コードを段階的に説明します。プロセスを詳細に理解するのに役立つように、各ステップのサンプル コードが含まれています。

## ステップ 1: ドキュメント ディレクトリを定義する

まず、Excel ファイルが配置されているディレクトリ パスを設定する必要があります。コード内の「YOUR DOCUMENT DIRECTORY」を Excel ファイルの実際のパスに置き換えます。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## ステップ 2: ファイル ストリームを作成し、Excel ファイルを開く

次に、ファイル ストリームを作成し、次のコマンドを使用して Excel ファイルを開く必要があります。`FileStream`クラス。

```csharp
//開く Excel ファイルを含むファイル ストリームを作成します。
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## ステップ 3: ワークブック オブジェクトをインスタンス化する

Excel ファイルを開いたら、インスタンスを作成する必要があります。`Workbook`物体。このオブジェクトは Excel ワークブックを表し、ワークブックを操作するためのさまざまなメソッドとプロパティを提供します。

```csharp
//Workbook オブジェクトをインスタンス化する
//ファイルフロー経由で Excel ファイルを開きます
Workbook workbook = new Workbook(fstream);
```

## ステップ 4: ワークシートを名前で削除する

ワークシートを名前から削除するには、`RemoveAt()`の方法`Worksheets`のオブジェクト`Workbook`物体。削除するワークシートの名前をパラメータとして渡す必要があります。

```csharp
//シート名を使用してワークシートを削除する
workbook.Worksheets.RemoveAt("Sheet1");
```

## ステップ 5: ワークブックを保存する

ワークシートを削除したら、次のコマンドを使用して、変更した Excel ワークブックを保存できます。`Save()`の方法`Workbook`物体。

```csharp
// Excel ワークブックを保存する
workbook.Save(dataDir + "output.out.xls");
```


### Aspose.Cells for .NET を使用した名前による Excel ワークシートの削除 C# チュートリアルのサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//開く Excel ファイルを含むファイル ストリームの作成
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//Workbook オブジェクトのインスタンス化
//ファイル ストリーム経由で Excel ファイルを開く
Workbook workbook = new Workbook(fstream);
//シート名を使用したワークシートの削除
workbook.Worksheets.RemoveAt("Sheet1");
//ワークブックの保存
workbook.Save(dataDir + "output.out.xls");
```

## 結論

このチュートリアルでは、Aspose.Cells for .NET を使用して Excel スプレッドシートを名前で削除する段階的なプロセスについて説明しました。提供されているコード例と説明に従うことで、C# アプリケーションでこのタスクを実行する方法を十分に理解できるようになります。 Aspose.Cells for .NET は、Excel ファイルを操作するための包括的な機能セットを提供し、スプレッドシートや関連データを簡単に操作できるようにします。

### よくある質問 (FAQ)

#### Aspose.Cells for .NET とは何ですか?

Aspose.Cells for .NET は、開発者が .NET アプリケーションで Excel ファイルを作成、操作、変換できるようにする強力なライブラリです。スプレッドシート、セル、数式、スタイルなどを操作するための幅広い機能を提供します。

#### Aspose.Cells for .NET をインストールするにはどうすればよいですか?

Aspose.Cells for .NET をインストールするには、Aspose リリース (https://releases.aspose.com/cells/net)、表示される指示に従ってください。アプリケーションでライブラリを使用するには、有効なライセンスが必要です。

#### 複数のワークシートを一度に削除できますか?

はい、Aspose.Cells for .NET を使用して複数のワークシートを削除できます。削除するワークシートごとに削除手順を繰り返すだけです。

#### スプレッドシートを削除する前に、スプレッドシートが存在するかどうかを確認するにはどうすればよいですか?

ワークシートを削除する前に、次のコマンドを使用してワークシートが存在するかどうかを確認できます。`Contains()`の方法`Worksheets`のオブジェクト`Workbook`物体。このメソッドはスプレッドシート名をパラメータとして受け取り、次の値を返します。`true`スプレッドシートが存在する場合、そうでない場合は戻ります`false`.

#### 削除したスプレッドシートを復元することはできますか?

残念ながら、スプレッドシートを削除すると、Excel ファイルから直接復元することはできません。データの損失を避けるために、スプレッドシートを削除する前に Excel ファイルのバックアップを作成することをお勧めします。