---
title: Excel ワークシートの特定のセルを保護する
linktitle: Excel ワークシートの特定のセルを保護する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel の特定のセルを保護する方法を学びます。 C# のステップバイステップのチュートリアル。
type: docs
weight: 70
url: /ja/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
このチュートリアルでは、Aspose.Cells ライブラリを使用して Excel スプレッドシート内の特定のセルを保護する C# ソース コードを見ていきます。コードの各ステップを順に見て、それがどのように機能するかを説明します。望ましい結果を得るには、指示に注意深く従ってください。

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

このステップでは、特定のセルに適用するスタイルを定義します。次のコードを使用します。

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

## ステップ 7: 特定のセルをロックする

このステップでは、特定のセルをロックします。次のコードを使用します。

```csharp
// つのセルすべてをロックします...つまり、A1、B1、C1。
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## ステップ 8: ワークシートを保護する

最後に、特定のセルが変更されないようにワークシートを保護します。次のコードを使用します。

```csharp
//ワークシートを保護します。
sheet.Protect(ProtectionType.All);
```

## ステップ9: Excelファイルを保存する

変更した Excel ファイルを保存します。次のコードを使用します。

```csharp
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

変更した Excel ファイルを保存するための正しいパスを指定していることを確認してください。

### Aspose.Cells for .NET を使用して Excel ワークシート内の特定のセルを保護するためのサンプル ソース コード 
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
//スタイルフラグオブジェクトを定義する
StyleFlag styleflag;
//ワークシート内のすべての列をループし、ロックを解除します。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// 3 つのセル (A1、B1、C1) をロックします。
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
//最後に、シートを保護します。
sheet.Protect(ProtectionType.All);
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## 結論

おめでとうございます！これで、.NET 用の Aspose.Cells ライブラリを使用して Excel ワークシート内の特定のセルを保護できる C# ソース コードが完成しました。特定のニーズに合わせてコードを自由にカスタマイズしてください。

### FAQ（よくある質問）

#### このコードは最近のバージョンの Excel で動作しますか?

はい、このコードは、Excel 2010 以降の形式のファイルを含む、最近のバージョンの Excel で動作します。

#### A1、B1、C1 以外のセルを保護できますか?

はい。コードの対応する行でセル参照を調整することで、他の特定のセルをロックするようにコードを変更できます。

#### ロックされたセルを再びロック解除するにはどうすればよいですか?

使用できます`SetStyle`を使用したメソッド`IsLocked`に設定`false`セルのロックを解除します。

#### ワークブックにさらにワークシートを追加できますか?

はい、次のコマンドを使用して他のワークシートをワークブックに追加できます。`Worksheets.Add()`メソッドを実行し、ワークシートごとにセル保護手順を繰り返します。

#### Excelファイルの保存形式を変更するにはどうすればよいですか?

保存形式を変更するには、`SaveFormat`目的の形式のメソッド。たとえば、`SaveFormat.Xlsx` Excel 2007 以降の場合。