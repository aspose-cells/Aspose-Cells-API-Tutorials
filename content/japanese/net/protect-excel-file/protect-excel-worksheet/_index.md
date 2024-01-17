---
title: Excel ワークシートを保護する
linktitle: Excel ワークシートを保護する
second_title: Aspose.Cells for .NET API リファレンス
description: このチュートリアルでは、Aspose.Cells for .NET を使用して Excel スプレッドシートを保護する方法を説明します。 C# のステップバイステップガイド。
type: docs
weight: 50
url: /ja/net/protect-excel-file/protect-excel-worksheet/
---
このチュートリアルでは、Aspose.Cells ライブラリを使用して Excel スプレッドシートを保護する C# ソース コードをいくつか見ていきます。コードの各ステップを順に見て、それがどのように機能するかを説明します。望ましい結果を得るために、必ず指示に注意深く従ってください。

## ステップ 1: 前提条件

始める前に、.NET 用の Aspose.Cells ライブラリがインストールされていることを確認してください。 Aspose公式サイトから入手できます。また、最新バージョンの Visual Studio またはその他の C# 開発環境があることを確認してください。

## ステップ 2: 必要な名前空間をインポートする

Aspose.Cells ライブラリを使用するには、必要な名前空間をコードにインポートする必要があります。 C# ソース ファイルの先頭に次の行を追加します。

```csharp
using Aspose.Cells;
using System.IO;
```

## ステップ 3: Excel ファイルをロードする

このステップでは、保護する Excel ファイルを読み込みます。 Excel ファイルが含まれるディレクトリへの正しいパスを必ず指定してください。次のコードを使用してファイルをアップロードします。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//開く Excel ファイルを含むファイルのストリームを作成します。
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Workbook オブジェクトをインスタンス化します。
//ファイルストリーム経由で Excel ファイルを開きます。
Workbook excel = new Workbook(fstream);
```

必ず交換してください`"YOUR_DOCUMENTS_DIR"`ドキュメント ディレクトリへの適切なパスを指定します。

## ステップ 4: スプレッドシートにアクセスする

Excel ファイルをロードしたので、最初のワークシートにアクセスできます。次のコードを使用して、最初のワークシートにアクセスします。

```csharp
// Excel ファイルの最初のワークシートにアクセスします。
Worksheet worksheet = excel.Worksheets[0];
```

## ステップ 5: ワークシートを保護する

このステップでは、パスワードを使用してスプレッドシートを保護します。スプレッドシートを保護するには、次のコードを使用します。

```csharp
//ワークシートをパスワードで保護します。
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

交換する`"YOUR_PASSWORD"`スプレッドシートを保護するために使用するパスワードを入力します。

## ステップ 6: 保護が完了したので、変更した Excel ファイルを保存します。

é スプレッドシートでは、変更した Excel ファイルをデフォルト形式で保存します。次のコードを使用して Excel ファイルを保存します。

```csharp
//変更した Excel ファイルをデフォルト形式で保存します。
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

変更した Excel ファイルを保存するための正しいパスを指定していることを確認してください。

## ステップ 7: ファイル ストリームを閉じる

すべてのリソースを解放するには、Excel ファイルのロードに使用されたファイル ストリームを閉じる必要があります。ファイル ストリームを閉じるには、次のコードを使用します。

```csharp
//ファイル ストリームを閉じて、すべてのリソースを解放します。
fstream.Close();
```

必ずこのステップをコードの最後に含めてください。


### Aspose.Cells for .NET を使用して Excel ワークシートを保護するためのサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//開く Excel ファイルを含むファイル ストリームの作成
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
//Workbook オブジェクトのインスタンス化
//ファイル ストリーム経由で Excel ファイルを開く
Workbook excel = new Workbook(fstream);
//Excel ファイルの最初のワークシートへのアクセス
Worksheet worksheet = excel.Worksheets[0];
//ワークシートをパスワードで保護する
worksheet.Protect(ProtectionType.All, "aspose", null);
//変更した Excel ファイルをデフォルト形式で保存する
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

おめでとうございます！これで、.NET 用の Aspose.Cells ライブラリを使用して Excel スプレッドシートを保護できる C# ソース コードが完成しました。必ず手順を注意深く実行し、特定のニーズに合わせてコードをカスタマイズしてください。

### FAQ（よくある質問）

#### 1 つの Excel ファイルで複数のワークシートを保護することはできますか?

A: はい、ワークシートごとに手順 4 ～ 6 を繰り返すことで、1 つの Excel ファイルで複数のワークシートを保護できます。

#### 承認されたユーザーに特定の権限を指定するにはどうすればよいですか?

 A: によって提供される追加オプションを使用できます。`Protect`許可されたユーザーに特定の権限を指定するメソッド。詳細については、Aspose.Cells のドキュメントを参照してください。

#### Excel ファイル自体をパスワードで保護できますか?

A: はい、Aspose.Cells ライブラリが提供する他の方法を使用して、Excel ファイル自体をパスワードで保護できます。具体的な例についてはドキュメントを参照してください。

#### Aspose.Cells ライブラリは他の Excel ファイル形式をサポートしていますか?

A: はい、Aspose.Cells ライブラリは、XLSX、XLSM、XLSB、CSV などを含む幅広い Excel ファイル形式をサポートしています。