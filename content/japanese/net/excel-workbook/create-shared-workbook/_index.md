---
title: 共有ワークブックの作成
linktitle: 共有ワークブックの作成
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Excel 共有ワークブックを作成し、同時データ コラボレーションを可能にします。
type: docs
weight: 70
url: /ja/net/excel-workbook/create-shared-workbook/
---
このチュートリアルでは、Aspose.Cells for .NET を使用して共有ワークブックを作成できるようにする、提供されている C# ソース コードについて説明します。この操作を行うには、次の手順に従ってください。

## ステップ 1: 出力ディレクトリを設定する

```csharp
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

この最初のステップでは、共有ワークブックが保存される出力ディレクトリを定義します。

## ステップ 2: ワークブック オブジェクトを作成する

```csharp
//ワークブックオブジェクトを作成する
Workbook wb = new Workbook();
```

Excel ワークブックを表す新しい Workbook オブジェクトを作成しています。

## ステップ 3: ワークブックの共有を有効にする

```csharp
//ワークブックを共有する
wb.Settings.Shared = true;
```

ワークブックの共有機能を有効にするには、`Shared` Workbook オブジェクトのプロパティを`true`.

## ステップ 4: 共有ワークブックを保存する

```csharp
//共有ワークブックを保存する
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

出力ファイルのパスと名前を指定して、共有ワークブックを保存します。

### Aspose.Cells for .NET を使用して共有ワークブックを作成するためのサンプル ソース コード 
```csharp
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
//ワークブックオブジェクトの作成
Workbook wb = new Workbook();
//ワークブックを共有する
wb.Settings.Shared = true;
//共有ワークブックを保存する
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して共有ワークブックを作成する方法を学習しました。共有ワークブックは、複数のユーザーが同時に使用してデータを共同作業できます。独自のデータを試し、Aspose.Cells の機能をさらに探索して、強力でパーソナライズされた Excel ワークブックを作成します。

### よくある質問

#### Q: 共有ワークブックとは何ですか?

A: 共有ワークブックは、複数のユーザーがデータを共同作業するために同時に使用できる Excel ワークブックです。各ユーザーはワークブックに変更を加えることができ、他のユーザーはリアルタイムで更新を確認できます。

#### Q: Aspose.Cells for .NET でワークブックの共有を有効にするにはどうすればよいですか?

 A: Aspose.Cells for .NET でワークブックの共有を有効にするには、`Shared` Workbook オブジェクトのプロパティを`true`。これにより、ユーザーはワークブックで同時に作業できるようになります。

#### Q: 共有ワークブックでユーザー権限を制限できますか?

A: はい、Excel のセキュリティ機能を使用して、共有ブックのユーザー権限を制限できます。編集権限、読み取り専用権限など、ユーザーごとに特定の権限を設定できます。

#### Q: ワークブックを他のユーザーと共有するにはどうすればよいですか?

A: 共有ワークブックを作成したら、Excel ファイルを他のユーザーに送信して共有できます。他のユーザーはファイルを開いて同時に作業できるようになります。

#### Q: Excel のすべての機能は共有ブックでサポートされていますか?

A: ほとんどの Excel 機能は共有ブックでサポートされています。ただし、マクロやアドインなどの一部の高度な機能は、共有ブックで使用する場合に制限がある場合があります。