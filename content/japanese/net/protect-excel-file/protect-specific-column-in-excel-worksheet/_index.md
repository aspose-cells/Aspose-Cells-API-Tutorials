---
title: Excel ワークシートの特定の列を保護する
linktitle: Excel ワークシートの特定の列を保護する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel シートの特定の列を保護する方法を学びます。 C# のステップバイステップガイド。
type: docs
weight: 80
url: /ja/net/protect-excel-file/protect-specific-column-in-excel-worksheet/
---
C# で Excel ワークシートを操作する場合、偶発的な変更を防ぐために特定の列を保護することが必要になることがよくあります。このチュートリアルでは、Aspose.Cells for .NET ライブラリを使用して Excel ワークシートの特定の列を保護するプロセスを説明します。このタスクに必要な C# ソース コードを段階的に説明します。それでは、始めましょう!

## Excel ワークシートの特定の列の保護の概要

Excel ワークシート内の特定の列を保護すると、それらの列はロックされたままになり、適切な承認なしに変更できなくなります。これは、ユーザーがワークシートの残りの部分を操作できるようにしながら、特定のデータまたは式への編集アクセスを制限したい場合に特に便利です。 Aspose.Cells for .NET ライブラリは、列保護など、Excel ファイルをプログラムで操作するための包括的な機能セットを提供します。

## 環境のセットアップ

始める前に、開発環境に Aspose.Cells for .NET ライブラリがインストールされていることを確認してください。 Aspose の公式 Web サイトからライブラリをダウンロードし、提供されているインストーラーを使用してインストールできます。

## 新しいワークブックとワークシートの作成

特定の列の保護を開始するには、Aspose.Cells for .NET を使用して新しいワークブックとワークシートを作成する必要があります。コードスニペットは次のとおりです。

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
```

「YOUR DOCUMENT DIRECTORY」を Excel ファイルを保存する実際のディレクトリ パスに置き換えてください。

## スタイルおよびスタイルフラグオブジェクトの定義

列に特定のスタイルと保護フラグを設定するには、スタイルとスタイル フラグ オブジェクトを定義する必要があります。コードスニペットは次のとおりです。

```csharp
//スタイルオブジェクトを定義します。
Style style;

//スタイルフラグオブジェクトを定義します。
StyleFlag flag;
```

## 列をループしてロックを解除する

次に、ワークシート内のすべての列をループして、ロックを解除する必要があります。これにより、保護したい列を除くすべての列が編集可能になります。コードスニペットは次のとおりです。

```csharp
//ワークシート内のすべての列をループし、ロックを解除します。
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    flag = new StyleFlag();
    flag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, flag);
}
```

## 特定の列をロックする

次に、特定の列をロックしてみましょう。この例では、最初の列 (列インデックス 0) をロックします。コードスニペットは次のとおりです。

```csharp
//最初の列スタイルを取得します。
style = sheet.Cells.Columns[0].Style;

//それをロック。
style.IsLocked = true;
```

## 列へのスタイルの適用

特定の列をロックした後、その列にスタイルとフラグを適用する必要があります。コードスニペットは次のとおりです。

```csharp
//フラグをインスタンス化します。
flag = new StyleFlag();

//ロックの設定を行います。
flag.Locked = true;

//最初の列にスタイルを適用します。
sheet.Cells.Columns[0].ApplyStyle(style, flag);
```

## ワークシートの保護

保護を完了するには、ロックされた列が変更できないようにワークシートを保護する必要があります。コードスニペットは次のとおりです。

```csharp
//シートを保護します。
sheet.Protect(ProtectionType.All);
```

## Excelファイルの保存

最後に、変更した Excel ファイルを目的の場所に保存します。コードスニペットは次のとおりです。

```csharp
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

「output.out.xls」を目的のファイル名と拡張子に置き換えてください。

### Aspose.Cells for .NET を使用して Excel ワークシートの特定の列を保護するためのサンプル ソース コード 
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
//最初の列スタイルを取得します。
style = sheet.Cells.Columns[0].Style;
//それをロック。
style.IsLocked = true;
//フラグをインスタンス化します。
flag = new StyleFlag();
//ロックの設定を行います。
flag.Locked = true;
//最初の列にスタイルを適用します。
sheet.Cells.Columns[0].ApplyStyle(style, flag);
//シートを保護します。
sheet.Protect(ProtectionType.All);
// Excel ファイルを保存します。
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

## 結論

このチュートリアルでは、Aspose.Cells for .NET ライブラリを使用して Excel ワークシートの特定の列を保護する手順を段階的に説明しました。まず新しいワークブックとワークシートを作成し、スタイルとスタイル フラグ オブジェクトを定義してから、特定の列のロックを解除およびロックする作業に進みました。最後に、ワークシートを保護し、変更した Excel ファイルを保存しました。このガイドに従うことで、C# と Aspose.Cells for .NET を使用して Excel ワークシートの特定の列を保護できるようになります。

### よくある質問 (FAQ)

#### この方法を使用して複数の列を保護できますか?

はい、コードを適宜変更することで、複数の列を保護できます。目的の列範囲をループし、ロック スタイルとフラグを適用するだけです。

#### 保護されたワークシートをパスワードで保護することはできますか?

はい、呼び出し時にパスワードを指定することで、保護されたワークシートにパスワード保護を追加できます。`Protect`方法。

#### Aspose.Cells for .NET は他の Excel ファイル形式をサポートしていますか?

はい、Aspose.Cells for .NET は、XLS、XLSX、XLSM などを含むさまざまな Excel ファイル形式をサポートしています。

#### 列ではなく特定の行を保護できますか?

はい。列のセルではなく行のセルにスタイルとフラグを適用することで、列ではなく特定の行を保護するようにコードを変更できます。