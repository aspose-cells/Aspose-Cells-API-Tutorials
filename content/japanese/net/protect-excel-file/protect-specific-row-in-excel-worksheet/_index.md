---
title: Excel ワークシートの特定の行を保護する
linktitle: Excel ワークシートの特定の行を保護する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel の特定の行を保護します。機密データを保護するためのステップバイステップのガイド。
type: docs
weight: 90
url: /ja/net/protect-excel-file/protect-specific-row-in-excel-worksheet/
---
Excel スプレッドシート内の機密データを保護することは、情報セキュリティを確保するために不可欠です。 Aspose.Cells for .NET は、Excel スプレッドシートの特定の行を保護する強力なソリューションを提供します。このガイドでは、提供されている C# ソース コードを使用して Excel ワークシートの特定の行を保護する方法について説明します。次の簡単な手順に従って、Excel ファイルに行保護を設定します。

## ステップ 1: 必要なライブラリをインポートする

開始するには、Aspose.Cells for .NET がシステムにインストールされていることを確認してください。 Aspose.Cells の機能を使用できるようにするには、C# プロジェクトに適切な参照を追加する必要もあります。必要なライブラリをインポートするコードは次のとおりです。

```csharp
//必要な参照を追加します
using Aspose.Cells;
```

## ステップ 2: Excel ワークブックとスプレッドシートを作成する

必要なライブラリをインポートした後、新しい Excel ワークブックと新しいワークシートを作成できます。その方法は次のとおりです。

```csharp
//ドキュメントディレクトリへのパス。
string dataDir = "YOUR DOCUMENTS DIRECTORY";

//ディレクトリが存在しない場合は作成します。
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
     System.IO.Directory.CreateDirectory(dataDir);

//新しいワークブックを作成します。
Workbook wb = new Workbook();

//スプレッドシート オブジェクトを作成し、最初のシートを取得します。
Worksheet sheet = wb.Worksheets[0];
```

## ステップ 3: スタイルとスタイルフラグの設定

次に、セル スタイルとスタイル フラグを設定して、ワークシート内のすべての列のロックを解除します。必要なコードは次のとおりです。

```csharp
//スタイルオブジェクトを設定します。
Styling styling;

//スタイルフラグオブジェクトを設定します。
StyleFlag flag;

//ワークシート内のすべての列をループし、ロックを解除します。
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     flag = new StyleFlag();
     flag. Locked = true;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## ステップ 4: 特定の回線を保護する

次に、ワークシート内の特定の行を保護します。変更を防ぐために最初の行をロックします。その方法は次のとおりです。

```csharp
//最初の行のスタイルを取得します。
style = sheet.Cells.Rows[0].Style;

//それをロック。
style. IsLocked = true;

//フラグをインスタンス化します。
flag = new StyleFlag();

//ロックパラメータを設定します。
flag. Locked = true;

//スタイルを最初の行に適用します。
sheet.Cells.ApplyRowStyle(0, style, flag);
```

## ステップ 5: ワークシートを保護する

最後に、Excel ワークシート全体を保護して、不正な変更を防ぎます。その方法は次のとおりです。

```csharp
//ワークシートを保護します。
sheet.Protect(ProtectionType.All);
```

## ステップ 6: 保護された Excel ファイルを保存する

Excel ワークシートの特定の行の保護が完了したら、保護された Excel ファイルをシステムに保存できます。その方法は次のとおりです。

```csharp
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

これらの手順を実行すると、Aspose.Cells for .NET を使用して Excel スプレッドシートの特定の行を正常に保護できます。

### Aspose.Cells for .NET を使用した Excel ワークシートの特定の行の保護のサンプル ソース コード 
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

Excel ファイル内のデータを保護することは、不正アクセスや望ましくない変更を防ぐために非常に重要です。 .NET 用の Aspose.Cells ライブラリを使用すると、提供されている C# ソース コードを使用して Excel スプレッドシートの特定の行を簡単に保護できます。このステップバイステップ ガイドに従って、Excel ファイルに追加のセキュリティ層を追加します。

### よくある質問

#### 特定の行の保護は Excel のすべてのバージョンで機能しますか?

はい、Aspose.Cells for .NET を使用した特定の行保護は、サポートされているすべてのバージョンの Excel で機能します。

#### Excel スプレッドシート内の複数の特定の行を保護できますか?

はい、このガイドで説明されているのと同様の方法を使用して、複数の特定の行を保護できます。

#### Excel スプレッドシートの特定の行のロックを解除するにはどうすればよいですか?

特定の行のロックを解除するには、それに応じてソース コードを変更する必要があります。`IsLocked`の方法`Style`物体。