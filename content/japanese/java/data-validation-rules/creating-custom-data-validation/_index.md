---
title: カスタムデータ検証の作成
linktitle: カスタムデータ検証の作成
second_title: Aspose.Cells Java Excel 処理 API
description: Aspose.Cells for Java を使用してカスタム データ検証を作成する方法を学びます。ソースコード付きのステップバイステップガイド。
type: docs
weight: 10
url: /ja/java/data-validation-rules/creating-custom-data-validation/
---

## 導入

データ検証は、ユーザーが間違ったデータまたは無効なデータを Excel スプレッドシートに入力するのを防ぎ、データの整合性を維持するのに役立ちます。 Excel には組み込みのデータ検証オプションが用意されていますが、カスタム検証ルールを定義する必要があるシナリオもあります。 Aspose.Cells for Java を使用すると、これを効率的に達成できます。

## 前提条件

コードに入る前に、次の前提条件を満たしていることを確認してください。

-  Aspose.Cells for Java: からライブラリをダウンロードしてインストールします。[ここ](https://releases.aspose.com/cells/java/).

## ステップ 1: Java プロジェクトのセットアップ

まず、好みの統合開発環境 (IDE) で新しい Java プロジェクトを作成します。 Aspose.Cells for Java ライブラリをプロジェクトのクラスパスに追加します。

## ステップ 2: Excel ワークブックの作成

まず、Aspose.Cells for Java を使用して新しい Excel ワークブックを作成します。

```java
//新しい Excel ワークブックを作成する Java コード
Workbook workbook = new Workbook();
```

## ステップ 3: ワークシートの追加

次に、カスタム データ検証を適用するワークシートをワークブックに追加しましょう。

```java
//ワークシートを追加する Java コード
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## ステップ 4: カスタム検証基準の定義

このステップでは、データが従う必要があるカスタム検証基準を定義します。セルに入力する年齢を 18 ～ 60 歳に制限したいとします。

```java
//カスタム検証基準を定義する Java コード
Validation validation = worksheet.getValidations().add();
validation.setType(ValidationType.WHOLE);
validation.setOperator(OperatorType.BETWEEN);
validation.setFormula1("18");
validation.setFormula2("60");
validation.setShowError(true);
validation.setAlertStyle(ValidationAlertType.STOP);
validation.setErrorTitle("Invalid Age");
validation.setErrorMessage("Age must be between 18 and 60.");
```

## ステップ 5: データ検証を範囲に適用する

カスタム検証基準を定義したので、それを特定の範囲のセルに適用しましょう。

```java
//データ検証を範囲に適用する Java コード
CellArea area = new CellArea();
area.startRow = 0;
area.startColumn = 0;
area.endRow = 9; //最初の 10 行に検証を適用します
area.endColumn = 0;

validation.addArea(area);
```

## ステップ 6: Excel ファイルを保存する

最後に、カスタム データ検証ルールが適用された Excel ファイルを保存します。

```java
// Excel ファイルを保存するための Java コード
workbook.save("CustomDataValidation.xlsx");
```

## 結論

このチュートリアルでは、Aspose.Cells for Java を使用してカスタム データ検証ルールを作成する方法を説明しました。これらの手順に従うことで、Excel データが特定の基準に準拠していることを確認し、データの整合性と正確性を高めることができます。

## よくある質問

### Java 用 Aspose.Cells をダウンロードするにはどうすればよいですか?

 Aspose.Cells for Java は、次の Web サイトからダウンロードできます。[ここ](https://releases.aspose.com/cells/java/).

### 同じワークシート内の複数の範囲にカスタム データ検証を適用できますか?

はい、必要な範囲ごとに手順 5 を繰り返すことで、同じワークシート内の複数の範囲にカスタム データ検証を適用できます。

### Aspose.Cells for Java でサポートされている他のタイプのデータ検証はありますか?

はい、Aspose.Cells for Java は、整数、10 進数、日付、時刻、テキスト長などを含むさまざまなタイプのデータ検証をサポートしています。

### データ検証が失敗したときに表示されるエラー メッセージをカスタマイズするにはどうすればよいですか?

エラー メッセージをカスタマイズするには、`setErrorMessage`ステップ 4 のメソッドで、検証基準を定義します。

### Aspose.Cells for Java はさまざまな形式の Excel ファイルを処理できますか?

はい、Aspose.Cells for Java は、XLS、XLSX、XLSM などを含む幅広い Excel ファイル形式をサポートしています。