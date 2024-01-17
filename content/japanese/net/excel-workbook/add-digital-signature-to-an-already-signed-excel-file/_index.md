---
title: 署名済みの Excel ファイルにデジタル署名を追加する
linktitle: 署名済みの Excel ファイルにデジタル署名を追加する
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して、既存の Excel ファイルにデジタル署名を簡単に追加します。
type: docs
weight: 30
url: /ja/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
このステップバイステップ ガイドでは、Aspose.Cells for .NET を使用して署名済みの Excel ファイルにデジタル署名を追加できるようにする、提供されている C# ソース コードについて説明します。既存の Excel ファイルに新しいデジタル署名を追加するには、次の手順に従います。

## ステップ 1: ソース ディレクトリと出力ディレクトリを設定する

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();

//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

この最初のステップでは、既存の Excel ファイルをロードし、新しいデジタル署名を付けてファイルを保存するために使用されるソース ディレクトリと出力ディレクトリを定義します。

## ステップ 2: 既存の Excel ファイルをロードする

```csharp
//署名済みの Excel ワークブックをロードします
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

ここでは、署名済みの Excel ファイルを次のコマンドを使用してロードします。`Workbook` Aspose.Cells のクラス。

## ステップ 3: デジタル署名のコレクションを作成する

```csharp
//デジタル署名のコレクションを作成する
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

を使用してデジタル署名の新しいコレクションを作成します。`DigitalSignatureCollection`クラス。

## ステップ 4: 新しい証明書を作成する

```csharp
//新しい証明書を作成する
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

ここでは、指定されたファイルとパスワードから新しい証明書を作成します。

## ステップ 5: 新しいデジタル署名をコレクションに追加する

```csharp
//新しいデジタル署名を作成する
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

//デジタル署名をコレクションに追加します
dsCollection.Add(signature);
```

を使用して新しいデジタル署名を作成します。`DigitalSignature`クラスを作成し、デジタル署名のコレクションに追加します。

## ステップ 6: デジタル署名のコレクションをワークブックに追加する

```csharp
//デジタル署名のコレクションをワークブックに追加する
workbook.AddDigitalSignature(dsCollection);
```

を使用して、デジタル署名のコレクションを既存の Excel ワークブックに追加します。`AddDigitalSignature()`方法。

## ステップ 7: ワークブックを保存して閉じる

```csharp
//ワークブックを保存して閉じます
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

新しいデジタル署名を持つワークブックを指定された出力ディレクトリに保存し、それを閉じて、関連するリソースを解放します。

### Aspose.Cells for .NET を使用して署名済みの Excel ファイルにデジタル署名を追加するためのサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
//証明書ファイルとそのパスワード
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//すでにデジタル署名されているワークブックをロードして、新しいデジタル署名を追加します
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//デジタル署名コレクションを作成する
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//新しい証明書を作成する
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//新しいデジタル署名を作成し、デジタル署名コレクションに追加します。
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//ワークブック内にデジタル署名コレクションを追加する
workbook.AddDigitalSignature(dsCollection);
//ワークブックを保存して破棄します。
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## 結論

おめでとうございます！ Aspose.Cells for .NET を使用して、署名済みの Excel ファイルにデジタル署名を追加する方法を学習しました。デジタル署名は Excel ファイルにセキュリティ層を追加し、ファイルの信頼性と完全性を保証します。

### よくある質問

#### Q: Aspose.Cells for .NET とは何ですか?

A: Aspose.Cells for .NET は、.NET 開発者が Excel ファイルを簡単に作成、変更、変換、操作できるようにする強力なクラス ライブラリです。

#### Q: Excel ファイルのデジタル署名とは何ですか?

A: Excel ファイルのデジタル署名は、ドキュメントの信頼性、完全性、および出所を保証する電子マークです。これは、ファイルが署名されてから変更されていないこと、および信頼できるソースからのものであることを検証するために使用されます。

#### Q: Excel ファイルにデジタル署名を追加する利点は何ですか?

A: Excel ファイルにデジタル署名を追加すると、不正な変更からの保護、データの整合性の確保、ドキュメントの作成者の認証、ドキュメントに含まれる情報の信頼性の確保など、いくつかの利点が得られます。

#### Q: Excel ファイルに複数のデジタル署名を追加できますか?

A: はい、Aspose.Cells を使用すると、Excel ファイルに複数のデジタル署名を追加できます。デジタル署名のコレクションを作成し、それらを 1 回の操作でファイルに追加できます。

#### Q: Excel ファイルにデジタル署名を追加するための要件は何ですか?

A: Excel ファイルにデジタル署名を追加するには、ドキュメントの署名に使用される有効なデジタル証明書が必要です。デジタル署名を追加する前に、正しい証明書とパスワードを持っていることを確認してください。