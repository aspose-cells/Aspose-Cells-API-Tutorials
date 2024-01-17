---
title: Excelのヘッダーとフッターを設定する
linktitle: Excelのヘッダーとフッターを設定する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel でヘッダーとフッターを設定する方法を学びます。
type: docs
weight: 100
url: /ja/net/excel-page-setup/set-excel-headers-and-footers/
---

このチュートリアルでは、Aspose.Cells for .NET を使用して Excel でヘッダーとフッターを設定する方法を段階的に説明します。 C# ソース コードを使用してプロセスを説明します。

## ステップ 1: 環境をセットアップする

マシンに Aspose.Cells for .NET がインストールされていることを確認してください。また、好みの開発環境で新しいプロジェクトを作成します。

## ステップ 2: 必要なライブラリをインポートする

コード ファイルに、Aspose.Cells を操作するために必要なライブラリをインポートします。対応するコードは次のとおりです。

```csharp
using Aspose.Cells;
```

## ステップ 3: データ ディレクトリを設定する

変更した Excel ファイルを保存するデータ ディレクトリを設定します。次のコードを使用します。

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

必ず完全なディレクトリ パスを指定してください。

## ステップ 4: ワークブックとワークシートの作成

新しい Workbook オブジェクトを作成し、次のコードを使用してワークブック内の最初のワークシートに移動します。

```csharp
Workbook excel = new Workbook();
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
```

これにより、ワークシートを含む空のワークブックが作成され、そのワークシートの PageSetup オブジェクトへのアクセスが提供されます。

## ステップ 5: ヘッダーの設定

を使用してスプレッドシートのヘッダーを設定します。`SetHeader` PageSetup オブジェクトのメソッド。サンプルコードは次のとおりです。

```csharp
pageSetup.SetHeader(0, "&A");
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
```

これにより、ヘッダーにワークシート名、現在の日付と時刻、ファイル名がそれぞれ設定されます。

## ステップ 6: フッターの定義

スプレッドシートのフッターを設定するには、`SetFooter` PageSetup オブジェクトのメソッド。サンプルコードは次のとおりです。

```csharp
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
pageSetup.SetFooter(1, "&P");
pageSetup.SetFooter(2, "&N");
```

これにより、フッター内のテキスト文字列、現在のページ番号、および総ページ数がそれぞれ設定されます。

## ステップ 7: 変更したワークブックを保存する

次のコードを使用して、変更したワークブックを保存します。

```csharp
excel.Save(dataDir + "OutputFileName.xls");
```

これにより、変更されたワークブックが指定されたデータ ディレクトリに保存されます。

### Aspose.Cells for .NET を使用して Excel ヘッダーとフッターを設定するためのサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Workbook オブジェクトのインスタンス化
Workbook excel = new Workbook();
//ワークシートのPageSetupの参照の取得
PageSetup pageSetup = excel.Worksheets[0].PageSetup;
//ヘッダーの左側のセクションにワークシート名を設定します
pageSetup.SetHeader(0, "&A");
//ヘッダーの中央セクションに現在の日付と現在時刻を設定します。
//そしてヘッダーのフォントを変更します
pageSetup.SetHeader(1, "&\"Times New Roman,Bold\"&D-&T");
//ヘッダーの右側のセクションに現在のファイル名を設定し、
//ヘッダーのフォント
pageSetup.SetHeader(2, "&\"Times New Roman,Bold\"&12&F");
//フッター左側に文字列を設定してフォントを変更する
//この文字列の一部（「123」）
pageSetup.SetFooter(0, "Hello World! &\"Courier New\"&14 123");
//フッターの中央セクションに現在のページ番号を設定する
pageSetup.SetFooter(1, "&P");
//フッターの右側のセクションでページ数を設定する
pageSetup.SetFooter(2, "&N");
//ワークブックを保存します。
excel.Save(dataDir + "SetHeadersAndFooters_out.xls");
```


## 結論

Aspose.Cells for .NET を使用して Excel でヘッダーとフッターを設定する方法を学習しました。このチュートリアルでは、環境のセットアップから変更されたワークブックの保存まで、プロセスのすべてのステップを説明しました。 Aspose.Cells の機能を自由に調べて、Excel ファイルでさらに操作を実行してください。

### よくある質問 (FAQ)

#### 1. Aspose.Cells for .NET をシステムにインストールするにはどうすればよいですか?
Aspose.Cells for .NET をインストールするには、Aspose 公式 Web サイトからインストール パッケージをダウンロードし、ドキュメントに記載されている手順に従う必要があります。

#### 2. この方法は Excel のすべてのバージョンで機能しますか?
はい、Aspose.Cells for .NET を使用してヘッダーとフッターを設定する方法は、サポートされているすべてのバージョンの Excel で機能します。

#### 3. ヘッダーとフッターをさらにカスタマイズできますか?
はい、Aspose.Cells は、テキストの配置、色、フォント、ページ番号などを含む、ヘッダーとフッターをカスタマイズするための広範な機能を提供します。

#### 4. ヘッダーとフッターに動的な情報を追加するにはどうすればよいですか?
特別な変数と書式設定コードを使用して、現在の日付、時刻、ファイル名、ページ番号などの動的な情報をヘッダーとフッターに追加できます。

#### 5. ヘッダーとフッターを設定した後に削除できますか?
はい、次のコマンドを使用してヘッダーとフッターを削除できます。`ClearHeaderFooter`の方法`PageSetup`物体。これにより、デフォルトのヘッダーとフッターが復元されます。