---
title: ユーザーが Excel ワークシートで範囲を編集できるようにする
linktitle: ユーザーが Excel ワークシートで範囲を編集できるようにする
second_title: Aspose.Cells for .NET API リファレンス
description: ユーザーが Aspose.Cells for .NET を使用して Excel スプレッドシートの特定の範囲を編集できるようにします。 C# のソース コードを含むステップバイステップ ガイド。
type: docs
weight: 10
url: /ja/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
このガイドでは、Aspose.Cells for .NET を使用して、ユーザーが Excel スプレッドシート内の特定の範囲を編集できるようにする方法を説明します。このタスクを実行するには、次の手順に従ってください。

## ステップ 1: 環境をセットアップする

開発環境をセットアップし、Aspose.Cells for .NET をインストールしていることを確認してください。 Aspose 公式 Web サイトからライブラリの最新バージョンをダウンロードできます。

## ステップ 2: 必要な名前空間をインポートする

C# プロジェクトで、Aspose.Cells を操作するために必要な名前空間をインポートします。

```csharp
using Aspose.Cells;
```

## ステップ 3: ドキュメント ディレクトリへのパスを設定する

を宣言します`dataDir`変数を使用して、生成された Excel ファイルを保存するディレクトリへのパスを指定します。

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

必ず交換してください`"YOUR_DOCUMENT_DIRECTORY"`システム上の正しいパスを使用してください。

## ステップ 4: ワークブック オブジェクトの作成

作成する Excel ワークブックを表す新しい Workbook オブジェクトをインスタンス化します。

```csharp
Workbook book = new Workbook();
```

## ステップ 5: 最初のワークシートへのアクセス

次のコードを使用して、Excel ワークブックの最初のワークシートに移動します。

```csharp
Worksheet sheet = book.Worksheets[0];
```

## ステップ 6: 許可された変更範囲の取得

を使用して、許可された編集範囲のコレクションを取得します。`AllowEditRanges`財産：

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## ステップ 7: 保護範囲を定義する

を使用して保護範囲を定義します。`Add`の方法`AllowEditRanges`コレクション：

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

ここでは、セル A1 からセル C3 までにわたる保護範囲「r2」を作成しました。

## ステップ 8: パスワードを指定する

保護範囲のパスワードを指定します。`Password`財産：

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

必ず交換してください`"YOUR_PASSWORD"`希望のパスワードを入力します。

## ステップ 9: ワークシートを保護する

を使用してワークシートを保護します。`Protect`の方法`Worksheet`物体：

```csharp
sheet.Protect(ProtectionType.All);
```

これにより、許可された範囲外の変更が防止され、スプレッドシートが保護されます。

## ステップ 10:

  Excelファイル

生成された Excel ファイルを次のコマンドを使用して保存します。`Save`の方法`Workbook`物体：

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

目的のファイル名と正しいパスを必ず指定してください。

### Aspose.Cells for .NET を使用してユーザーに Excel ワークシートの範囲の編集を許可するためのサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//ディレクトリが存在しない場合は作成します。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//新しいワークブックをインスタンス化する
Workbook book = new Workbook();
//最初の (デフォルト) ワークシートを取得する
Worksheet sheet = book.Worksheets[0];
//編集許可範囲を取得する
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
//ProtectedRange の定義
ProtectedRange proteced_range;
//範囲を作成する
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
//パスワードを指定してください
proteced_range.Password = "123";
//シートを保護する
sheet.Protect(ProtectionType.All);
//Excelファイルを保存します
book.Save(dataDir + "protectedrange.out.xls");
```

## 結論

これで、Aspose.Cells for .NET を使用して、ユーザーが Excel スプレッドシート内の特定の範囲を編集できるようにする方法を学習しました。特定のニーズを満たすために、Aspose.Cells が提供する機能を自由にさらに探索してください。


### よくある質問

#### 1. ユーザーが Excel スプレッドシートで特定の範囲を編集できるようにするにはどうすればよいですか?

使用できます`ProtectedRangeCollection`変更の許可範囲を定義するクラス。使用`Add`メソッドを使用して、目的のセルを含む新しい保護範囲を作成します。

#### 2. 変更を許可する範囲にパスワードを設定できますか?

はい、次のコマンドを使用してパスワードを指定できます。`Password`の財産`ProtectedRange`物体。これにより、パスワードを持っているユーザーのみにアクセスが制限されます。

#### 3. 許可範囲を設定した後、スプレッドシートを保護するにはどうすればよいですか?

使用`Protect`の方法`Worksheet`ワークシートを保護するオブジェクト。これにより、許可された範囲外の変更が防止され、パスワードを指定した場合はパスワードの入力を求めるプロンプトが表示される可能性があります。