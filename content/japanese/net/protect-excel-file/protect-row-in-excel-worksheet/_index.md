---
title: Excelワークシートの行を保護
linktitle: Excelワークシートの行を保護
second_title: Aspose.Cells for .NET API リファレンス
description: このチュートリアルでは、Aspose.Cells for .NET を使用して Excel スプレッドシートの行を保護する方法を説明します。 C# のステップバイステップのチュートリアル。
type: docs
weight: 60
url: /ja/net/protect-excel-file/protect-row-in-excel-worksheet/
---
このチュートリアルでは、Aspose.Cells ライブラリを使用して Excel スプレッドシートの行を保護する C# ソース コードをいくつか見ていきます。コードの各ステップを順に見て、それがどのように機能するかを説明します。望ましい結果を得るには、指示に注意深く従ってください。

## ステップ 1: 前提条件

始める前に、.NET 用の Aspose.Cells ライブラリがインストールされていることを確認してください。 Aspose公式サイトから入手できます。また、最新バージョンの Visual Studio またはその他の C# 開発環境があることを確認してください。

## ステップ 2: 必要な名前空間をインポートする

Aspose.Cells ライブラリを使用するには、必要な名前空間をコードにインポートする必要があります。 C# ソース ファイルの先頭に次の行を追加します。

```csharp
using Aspose.Cells;
```

## ステップ 3: Excel ワークブックの作成

このステップでは、新しい Excel ワークブックを作成します。次のコードを使用して Excel ワークブックを作成します。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

//新しいワークブックを作成します。
Workbook wb = new Workbook();
```

必ず交換してください`"YOUR_DOCUMENTS_DIR"`ドキュメント ディレクトリへの適切なパスを指定します。

## ステップ 4: スプレッドシートの作成

Excel ワークブックを作成したので、ワークシートを作成して最初のシートを取得しましょう。次のコードを使用します。

```csharp
//スプレッドシート オブジェクトを作成し、最初のシートを取得します。
Worksheet sheet = wb.Worksheets[0];
```

## ステップ 5: スタイルを定義する

このステップでは、スプレッドシートの行に適用するスタイルを定義します。次のコードを使用します。

```csharp
//スタイルオブジェクトの定義。
Styling styling;
```

## ステップ 6: ループしてすべての列のロックを解除します

次に、ワークシート内のすべての列をループしてロックを解除します。次のコードを使用します。

```csharp
//ワークシート内のすべての列をループし、ロックを解除します。
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## ステップ 7: 最初の行をロックする

このステップでは、ワークシートの最初の行をロックします。次のコードを使用します。

```csharp
//最初の行のスタイルを取得します。
style = sheet.Cells.Rows[0].Style;
//スタイルをロックします。
style. IsLocked = true;
//スタイルを最初の行に適用します。
sheet.Cells.ApplyRowStyle(0, style);
```

## ステップ 8: ワークシートを保護する

スタイルを設定し、行をロックしたので、スプレッドシートを保護しましょう。次のコードを使用します。

```csharp
//ワークシートを保護します。
sheet.Protect(ProtectionType.All);
```

## ステップ9: Excelファイルを保存する

最後に、変更した Excel ファイルを保存します。次のコードを使用します。

```csharp
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

変更した Excel ファイルを保存するための正しいパスを指定していることを確認してください。

### Aspose.Cells for .NET を使用した Excel ワークシートの行の保護のサンプル ソース コード 
```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENT DIRECTORY";
//ディレクトリが存在しない場合は作成します。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
//新しいワークブックを作成します。
Workbook wb = new Workbook();
//ワークシート オブジェクトを作成し、最初のシートを取得します。
Worksheet sheet = wb.Worksheets[0];
//スタイルオブジェクトを定義します。
Style style;
//スタイルフラグオブジェクトを定義します。
StyleFlag flag;
//ワークシート内のすべての列をループし、ロックを解除します。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
//最初の行のスタイルを取得します。
style = sheet.Cells.Rows[0].Style;
//それをロック。
style.IsLocked = true;
//フラグをインスタンス化します。
flag = new StyleFlag();
//ロックの設定を行います。
flag.Locked = true;
//スタイルを最初の行に適用します。
sheet.Cells.ApplyRowStyle(0, style, flag);
//シートを保護します。
sheet.Protect(ProtectionType.All);
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 結論

おめでとうございます！これで、.NET 用の Aspose.Cells ライブラリを使用して Excel スプレッドシートの行を保護できる C# ソース コードが完成しました。必ず手順を注意深く実行し、特定のニーズに合わせてコードをカスタマイズしてください。

### FAQ（よくある質問）

#### このコードは最近のバージョンの Excel で動作しますか?

はい、このコードは、Excel 2010 以降の形式のファイルを含む、最近のバージョンの Excel で動作します。

#### ワークシート内のすべての行ではなく、特定の行のみを保護できますか?

はい、コードを変更して、保護する特定の行を指定できます。それに応じてループとインデックスを調整する必要があります。

#### ロックされた回線を再度ロック解除するにはどうすればよいですか?

使用できます`IsLocked`の方法`Style`値を設定するオブジェクト`false`そして列のロックを解除します。

#### 同じ Excel ブック内の複数のワークシートを保護することはできますか?

はい、ワークシートの作成、スタイルの設定、ワークブック内の各ワークシートの保護の手順を繰り返すことができます。

#### スプレッドシート保護パスワードを変更するにはどうすればよいですか?

パスワードを変更するには、`Protect`メソッドを使用し、引数として新しいパスワードを指定します。