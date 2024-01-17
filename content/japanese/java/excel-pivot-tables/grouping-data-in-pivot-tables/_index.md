---
title: ピボットテーブルでのデータのグループ化
linktitle: ピボットテーブルでのデータのグループ化
second_title: Aspose.Cells Java Excel 処理 API
description: Aspose.Cells for Java を使用して Excel でピボット テーブルを作成する方法を学びます。ソース コードのサンプルを使用してデータのグループ化と分析を自動化します。
type: docs
weight: 14
url: /ja/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

ピボット テーブルは、スプレッドシート内のデータを分析および要約するための強力なツールです。データをグループ化および分類して、貴重な洞察を得ることができます。この記事では、Aspose.Cells for Java を使用してピボット テーブル内のデータを効果的にグループ化する方法を、ソース コードの例とともに説明します。

## 導入

ピボット テーブルは、大規模なデータセットのデータを整理して要約するための柔軟な方法を提供します。データをカテゴリまたは階層にグループ化することで、データのカスタム ビューを作成できます。これにより、データ内の傾向、パターン、外れ値をより簡単に特定できます。

## ステップ 1: ピボット テーブルを作成する

まずは、Aspose.Cells for Java を使用してピボット テーブルを作成しましょう。以下は、サンプル Excel ファイルからピボット テーブルを作成する方法の例です。

```java
// Excelファイルをロードする
Workbook workbook = new Workbook("sample.xlsx");

//データを含むワークシートにアクセスする
Worksheet worksheet = workbook.getWorksheets().get(0);

//データ範囲を指定する
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; //データが 20 行あると仮定します
sourceData.startColumn = 0;
sourceData.endColumn = 3; //データが 4 列あると仮定します

//データ範囲に基づいてピボット テーブルを作成する
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

//インデックスでピボットテーブルを取得する
PivotTable pivotTable = worksheet.getPivotTables().get(index);

//行と列にフィールドを追加する
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

//値を追加して集計を適用する
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

//変更した Excel ファイルを保存します
workbook.save("output.xlsx");
```

## ステップ 2: データをグループ化する

Aspose.Cells for Java では、`PivotField`クラス。次に、ピボット テーブルでフィールドをグループ化する方法の例を示します。

```java
//ピボットテーブルの「Product」フィールドにアクセスします。
PivotField productField = pivotTable.getPivotFields().get("Product");

//「Product」フィールドを特定の基準（開始文字など）でグループ化します。
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

//グループ化されたデータを含む変更された Excel ファイルを保存します
workbook.save("output_grouped.xlsx");
```

## ステップ 3: グループ化をカスタマイズする

日付ベースのグループ化間隔やカスタム グループ化ルールを指定するなど、グループ化設定をさらにカスタマイズできます。日付ベースのグループ化をカスタマイズする例を次に示します。

```java
//ピボット テーブルの「日付」フィールドにアクセスします (日付フィールドであると仮定します)。
PivotField dateField = pivotTable.getPivotFields().get("Date");

//日付を月ごとにグループ化する
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

//カスタム日付グループを使用して変更した Excel ファイルを保存します
workbook.save("output_custom_grouping.xlsx");
```

## 結論

ピボット テーブルでのデータのグループ化は、Excel でデータを分析および要約するための貴重なテクニックであり、Aspose.Cells for Java を使用すると、このプロセスを簡単に自動化できます。提供されているソース コードの例を使用すると、ピボット テーブルを作成し、グループ化をカスタマイズし、データから効率的に洞察を得ることができます。

## よくある質問

### 1. Excel のピボット テーブルの目的は何ですか?

Excel のピボット テーブルは、大規模なデータセットを要約して分析するために使用されます。データのカスタム ビューを作成できるため、パターンや傾向を特定しやすくなります。

### 2. ピボット テーブル内のデータのグループ化をカスタマイズするにはどうすればよいですか?

ピボット テーブル内のデータのグループ化をカスタマイズするには、`PivotField` Aspose.Cells for Java のクラス。これにより、日付ベースの間隔やカスタム ルールなどのグループ化基準を指定できます。

### 3. Aspose.Cells for Java を使用してピボット テーブルの作成を自動化できますか?

はい、提供されているソース コードの例で示されているように、Aspose.Cells for Java を使用して Excel でのピボット テーブルの作成を自動化できます。