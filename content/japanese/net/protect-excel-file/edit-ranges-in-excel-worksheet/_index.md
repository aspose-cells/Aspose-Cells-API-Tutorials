---
title: Excel ワークシートで範囲を編集する
linktitle: Excel ワークシートで範囲を編集する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel スプレッドシートの特定の範囲を編集する方法を学びます。 C# のステップバイステップのチュートリアル。
type: docs
weight: 20
url: /ja/net/protect-excel-file/edit-ranges-in-excel-worksheet/
---
Microsoft Excel は、スプレッドシートを作成および管理するための強力なツールであり、データを制御および保護するための多くの機能を提供します。そのような機能の 1 つは、ユーザーが他の部分を保護しながらワークシート内の特定の範囲を編集できるようにすることです。このチュートリアルでは、Excel ファイルをプログラムで操作するための一般的なライブラリである Aspose.Cells for .NET を使用してこの機能を実装する方法を段階的に説明します。

Aspose.Cells for .NET を使用すると、Excel スプレッドシート内の範囲を簡単に操作できるようになり、使いやすいインターフェイスと高度な機能が提供されます。ユーザーが Aspose.Cells for .NET を使用して Excel スプレッドシートの特定の範囲を編集できるようにするには、以下の手順に従います。
## ステップ 1: 環境をセットアップする

開発環境に Aspose.Cells for .NET がインストールされていることを確認してください。 Aspose 公式 Web サイトからライブラリをダウンロードし、インストール手順についてはドキュメントを確認してください。

## ステップ 2: ワークブックとワークシートの初期化

まず、新しいワークブックを作成し、範囲を変更できるようにするワークシートへの参照を取得する必要があります。これを実現するには、次のコードを使用します。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENTS DIRECTORY";
//ディレクトリがまだ存在しない場合は作成します。
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

//新しいワークブックをインスタンス化する
Workbook workbook = new Workbook();

//最初のワークシートを取得します (デフォルト)
Worksheet sheet = workbook.Worksheets[0];
```

このコード スニペットでは、最初に Excel ファイルが保存されるディレクトリへのパスを定義します。次に、の新しいインスタンスを作成します。`Workbook`クラスを作成し、次を使用して最初のワークシートへの参照を取得します。`Worksheets`財産。

## ステップ 3: 編集可能な範囲を取得する

次に、変更を許可する範囲を取得する必要があります。次のコードを使用します。

```csharp
//変更可能な範囲を取得する
ProtectedRangeCollection EditableRanges = Sheet.AllowEditRanges;
```

## ステップ 4: 保護範囲を設定する

範囲の変更を許可する前に、保護範囲を定義する必要があります。その方法は次のとおりです。

```csharp
//保護範囲を定義する
ProtectedRange ProtectedRange;

//範囲を作成する
int index = ModifiableRanges.Add("r2", 1, 1, 3, 3);
rangeProtected = rangesEditable[index];
```

このコードでは、`ProtectedRange`クラスを作成して使用します`Add`保護する範囲を指定する方法です。

## ステップ 5: パスワードを指定する

セキュリティを強化するために、保護範囲にパスワードを指定できます。その方法は次のとおりです。

```csharp
//パスワードを指定してください
protectedBeach.Password = "YOUR_PASSWORD";
```

## ステップ 6: ワークシートを保護する

保護範囲を設定したので、不正な変更を防ぐためにワークシートを保護できます。次のコードを使用します。

```csharp
//ワークシートを保護する
leaf.Protect(ProtectionType.All);
```

## ステップ 7: Excel ファイルを保存する

最後に、変更を加えた Excel ファイルを保存します。必要なコードは次のとおりです。

```csharp
//Excelファイルを保存します
workbook.Save(dataDir + "protectedrange.out.xls");
```

### Aspose.Cells for .NET を使用した Excel ワークシートの範囲の編集のサンプル ソース コード 
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
proteced_range.Password = "YOUR_PASSWORD";

//シートを保護する
sheet.Protect(ProtectionType.All);

//Excelファイルを保存します
book.Save(dataDir + "protectedrange.out.xls");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して、ユーザーが Excel スプレッドシートの特定の範囲を編集できるようにする方法を学習しました。この手法を独自のプロジェクトに適用して、Excel ファイルのセキュリティを向上できるようになりました。


#### よくある質問

#### Q: Excel スプレッドシートの範囲を編集するには、Aspose.Cells for .NET を使用する必要があるのはなぜですか?

A: Aspose.Cells for .NET は、Excel ファイルを操作するための強力で使いやすい API を提供します。範囲操作、ワークシート保護などの高度な機能を提供します。

#### Q: ワークシート内に複数の編集可能範囲を設定できますか?

 A: はい、`Add`の方法`ProtectedRangeCollection`コレクション。各範囲には独自の保護設定を設定できます。

####  Q: 編集可能範囲を定義した後に削除することはできますか?

 A: はい、使用できます。`RemoveAt`の方法`ProtectedRangeCollection`コレクションを使用して、インデックスを指定して特定の編集可能な範囲を削除します。

#### Q: 保護された Excel ファイルを保存した後に開くにはどうすればよいですか?

A: 保護された Excel ファイルを開くには、保護範囲の作成時に指定したパスワードを入力する必要があります。データへのアクセスの損失を防ぐために、パスワードは必ず安全な場所に保管してください。