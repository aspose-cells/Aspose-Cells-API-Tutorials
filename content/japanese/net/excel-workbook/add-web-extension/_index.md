---
title: Web 拡張機能の追加
linktitle: Web 拡張機能の追加
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用すると、Web 拡張機能を Excel ワークブックに簡単に追加できます。
type: docs
weight: 40
url: /ja/net/excel-workbook/add-web-extension/
---
このステップバイステップのチュートリアルでは、Aspose.Cells for .NET を使用して Web 拡張機能を追加できるようにする、提供されている C# ソース コードについて説明します。 Excel ワークブックに Web 拡張機能を追加するには、以下の手順に従ってください。

## ステップ 1: 出力ディレクトリを設定する

```csharp
//出力ディレクトリ
string outDir = RunExamples.Get_OutputDirectory();
```

この最初のステップでは、変更された Excel ワークブックが保存される出力ディレクトリを定義します。

## ステップ 2: 新しいワークブックを作成する

```csharp
//新しいワークブックを作成する
Workbook workbook = new Workbook();
```

ここでは、`Workbook` Aspose.Cells のクラス。

## ステップ 3: Web 拡張機能コレクションにアクセスする

```csharp
//Web 拡張機能のコレクションにアクセスする
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
```

Excel ワークブックの Web 拡張機能コレクションにアクセスするには、`WebExtensions`の財産`Worksheets`物体。

## ステップ 4: 新しい Web 拡張機能を追加する

```csharp
//新しい Web 拡張機能を追加する
int extensionIndex = extensions.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
```

新しい Web 拡張機能を拡張機能コレクションに追加しています。拡張機能の参照 ID、ストア名、ストア タイプを定義します。

## ステップ 5: Web 拡張機能タスク ウィンドウ コレクションにアクセスする

```csharp
//Web 拡張機能の作業ウィンドウ コレクションにアクセスする
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
```

Excel ワークブック Web 拡張作業ウィンドウ コレクションにアクセスするには、`WebExtensionTaskPanes`の財産`Worksheets`物体。

## ステップ 6: 新しい作業ウィンドウを追加する

```csharp
//新しい作業ウィンドウを追加する
int taskPaneIndex = taskPanes.Add();
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane. IsVisible = true;
taskPane. DockState = "right";
taskPane. WebExtension = extension;
```

新しい作業ウィンドウを作業ウィンドウ コレクションに追加します。ペインの表示設定、ドッキング状態、および関連する Web 拡張機能を設定します。

## ステップ 7: ワークブックを保存して閉じる

```csharp
//ワークブックを保存して閉じます
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

変更したワークブックを指定された出力ディレクトリに保存して閉じます。

### Aspose.Cells for .NET を使用した Web 拡張機能の追加のサンプル ソース コード 
```csharp
//ソースディレクトリ
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook();
WebExtensionCollection extensions = workbook.Worksheets.WebExtensions;
WebExtensionTaskPaneCollection taskPanes = workbook.Worksheets.WebExtensionTaskPanes;
int extensionIndex = extensions.Add();
int taskPaneIndex = taskPanes.Add();
WebExtension extension = extensions[extensionIndex];
extension.Reference.Id = "wa104379955";
extension.Reference.StoreName = "en-US";
extension.Reference.StoreType = WebExtensionStoreType.OMEX;
WebExtensionTaskPane taskPane = taskPanes[taskPaneIndex];
taskPane.IsVisible = true;
taskPane.DockState = "right";
taskPane.WebExtension = extension;
workbook.Save(outDir + "AddWebExtension_Out.xlsx");
Console.WriteLine("AddWebExtension executed successfully.");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して Web 拡張機能を追加する方法を学習しました。 Excel ワークブックでの Web 拡張機能の操作を最大限に活用するには、コードを試して Aspose.Cells の追加機能を調べてください。

## よくある質問

#### Q: Excel ワークブックの Web 拡張機能とは何ですか?

A: Excel ブックの Web 拡張機能は、Web アプリケーションを統合することで Excel に追加機能を追加できるコンポーネントです。インタラクティブな機能、カスタム ダッシュボード、外部統合などを提供できます。

#### Q: Aspose.Cells を使用して Excel ワークブックに Web 拡張機能を追加するにはどうすればよいですか?

 A: Aspose.Cells を使用して Web 拡張機能を Excel ワークブックに追加するには、ステップバイステップ ガイドに記載されている手順に従うことができます。使用`WebExtensionCollection`そして`WebExtensionTaskPaneCollection`Web 拡張機能と関連する作業ウィンドウを追加および構成するためのクラス。

#### Q: Web 拡張機能を追加するにはどのような情報が必要ですか?

A: Web 拡張機能を追加するときは、拡張機能の SKU ID、ストア名、ストア タイプを指定する必要があります。この情報は、拡張機能を正しく識別してロードするのに役立ちます。

#### Q: 複数の Web 拡張機能を 1 つの Excel ワークブックに追加できますか?

 A: はい、複数の Web 拡張機能を 1 つの Excel ワークブックに追加できます。使用`Add`Web 拡張機能コレクションのメソッドを使用して各拡張機能を追加し、それらを対応する作業ウィンドウに関連付けます。