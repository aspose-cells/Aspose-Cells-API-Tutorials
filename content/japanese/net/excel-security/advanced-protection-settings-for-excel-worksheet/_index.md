---
title: Excel ワークシートの高度な保護設定
linktitle: Excel ワークシートの高度な保護設定
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET で高度な保護設定を行って、Excel ファイルを保護します。
type: docs
weight: 10
url: /ja/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
このチュートリアルでは、.NET 用の Aspose.Cells ライブラリを使用して Excel スプレッドシートの高度な保護設定を行う手順を説明します。このタスクを完了するには、以下の手順に従ってください。

## ステップ 1: 準備

Aspose.Cells for .NET がインストールされており、優先統合開発環境 (IDE) で C# プロジェクトが作成されていることを確認してください。

## ステップ 2: ドキュメント ディレクトリのパスを設定する

を宣言します`dataDir`変数を指定し、ドキュメント ディレクトリへのパスで初期化します。例えば ：

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

必ず交換してください`"YOUR_DOCUMENTS_DIRECTORY"`ディレクトリへの実際のパスを使用します。

## ステップ 3: Excel ファイルを開くためのファイル ストリームを作成する

を作成します`FileStream`開く Excel ファイルを含むオブジェクト:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Excelファイルがあることを確認してください`book1.xls`ドキュメント ディレクトリ内に保存するか、正しいファイル名と場所を指定します。

## ステップ 4: Workbook オブジェクトをインスタンス化し、Excel ファイルを開く

使用`Workbook`Aspose.Cells のクラスを使用して Workbook オブジェクトをインスタンス化し、ファイル ストリーム経由で指定された Excel ファイルを開きます。

```csharp
Workbook excel = new Workbook(fstream);
```

## ステップ 5: 最初のワークシートにアクセスする

Excel ファイルの最初のワークシートに移動します。

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## ステップ 6: ワークシート保護設定を行う

必要に応じて、ワークシート オブジェクトのプロパティを使用してワークシートの保護設定を設定します。例えば ：

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ...必要に応じて他の保護設定を設定します...
```

## ステップ 7: 変更した Excel ファイルを保存する

次のコマンドを使用して、変更した Excel ファイルを保存します。`Save` Workbook オブジェクトのメソッド:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

出力ファイルに必要なパスとファイル名を必ず指定してください。

## ステップ 8: ファイル ストリームを閉じる

保存したら、ファイル ストリームを閉じて、関連するすべてのリソースを解放します。

```csharp
fstream.Close();
```
	
### Aspose.Cells for .NET を使用した Excel ワークシートの高度な保護設定のサンプル ソース コード 
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
//ユーザーによるワークシートの列の削除の制限
worksheet.Protection.AllowDeletingColumn = false;
//ユーザーによるワークシートの行の削除の制限
worksheet.Protection.AllowDeletingRow = false;
//ユーザーによるワークシートの内容の編集を制限する
worksheet.Protection.AllowEditingContent = false;
//ユーザーによるワークシートのオブジェクトの編集の制限
worksheet.Protection.AllowEditingObject = false;
//ユーザーによるワークシートのシナリオの編集を制限する
worksheet.Protection.AllowEditingScenario = false;
//ユーザーのフィルタリングを制限する
worksheet.Protection.AllowFiltering = false;
//ユーザーがワークシートのセルを書式設定できるようにする
worksheet.Protection.AllowFormattingCell = true;
//ユーザーがワークシートの行を書式設定できるようにする
worksheet.Protection.AllowFormattingRow = true;
//ユーザーがワークシートに列を挿入できるようにする
worksheet.Protection.AllowFormattingColumn = true;
//ユーザーがワークシートにハイパーリンクを挿入できるようにする
worksheet.Protection.AllowInsertingHyperlink = true;
//ユーザーがワークシートに行を挿入できるようにする
worksheet.Protection.AllowInsertingRow = true;
//ユーザーがワークシートのロックされたセルを選択できるようにする
worksheet.Protection.AllowSelectingLockedCell = true;
//ユーザーがワークシートのロックされていないセルを選択できるようにする
worksheet.Protection.AllowSelectingUnlockedCell = true;
//ユーザーによる並べ替えの許可
worksheet.Protection.AllowSorting = true;
//ユーザーがワークシートでピボット テーブルを使用できるようにする
worksheet.Protection.AllowUsingPivotTable = true;
//変更したExcelファイルを保存する
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
//ファイル ストリームを閉じてすべてのリソースを解放します
fstream.Close();
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Excel スプレッドシートの高度な保護設定を行う方法を学習しました。この知識を活用して Excel ファイルを保護し、ユーザーの操作を制限します。

### よくある質問

#### Q: IDE で新しい C# プロジェクトを作成するにはどうすればよいですか?

A: 新しい C# プロジェクトを作成する手順は、使用している IDE によって異なる場合があります。詳細な手順については、IDE のドキュメントを参照してください。

#### Q: チュートリアルで説明されている以外のカスタム保護設定を設定することは可能ですか?

A: はい、Aspose.Cells は、特定のニーズに合わせてカスタマイズできる幅広い保護設定を提供します。詳細については、Aspose.Cells のドキュメントを参照してください。

#### Q: サンプルコードで変更した Excel ファイルを保存するファイル形式は何ですか?

A: サンプル コードでは、変更された Excel ファイルは Excel 97-2003 (.xls) 形式で保存されます。必要に応じて、Aspose.Cells でサポートされている他の形式を選択できます。

#### Q: Excel ファイル内の他のワークシートにアクセスするにはどうすればよいですか?

 A: インデックスまたはシート名を使用して他のワークシートにアクセスできます。例:`Worksheet worksheet = excel.Worksheets[1];`または`Worksheet worksheet = excel.Worksheets[" SheetName"];`.