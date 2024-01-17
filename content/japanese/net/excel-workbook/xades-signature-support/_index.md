---
title: Xades 署名のサポート
linktitle: Xades 署名のサポート
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して Xades 署名を Excel ファイルに追加する方法を学習します。
type: docs
weight: 190
url: /ja/net/excel-workbook/xades-signature-support/
---
この記事では、.NET 用の Aspose.Cells ライブラリを使用した Xades 署名のサポートに関する以下の C# ソース コードを段階的に説明します。このライブラリを使用して Xades デジタル署名を Excel ファイルに追加する方法を説明します。また、署名プロセスとその実行の概要についても説明します。最終的な結果を得るには、以下の手順に従ってください。

## ステップ 1: ソース ディレクトリと出力ディレクトリを定義する
まず、コード内でソース ディレクトリと出力ディレクトリを定義する必要があります。これらのディレクトリは、ソース ファイルの場所と出力ファイルの保存場所を示します。対応するコードは次のとおりです。

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

必要に応じてディレクトリ パスを調整してください。

## ステップ 2: Excel ワークブックをロードする
次のステップでは、Xades デジタル署名を追加する Excel ワークブックをロードします。ワークブックをロードするコードは次のとおりです。

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

コード内でソース ファイル名を正しく指定してください。

## ステップ 3: デジタル署名の構成
次に、必要な情報を入力して Xades デジタル署名を構成します。デジタル証明書を含む PFX ファイルと、関連するパスワードを指定する必要があります。対応するコードは次のとおりです。

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

「pfxPassword」を実際のパスワードに置き換え、「pfxFile」を PFX ファイルへのパスに置き換えてください。

## ステップ 4: デジタル署名を追加する
デジタル署名を構成したので、それを Excel ワークブックに追加できます。対応するコードは次のとおりです。

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

この手順では、Xades デジタル署名を Excel ブックに追加します。

## ステップ 5: 署名付きでワークブックを保存する
最後に、デジタル署名を追加して Excel ブックを保存します。対応するコードは次のとおりです。

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

必要に応じて出力ファイルの名前を変更してください。

### Aspose.Cells for .NET を使用した Xades 署名サポートのサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## 結論
おめでとうございます！ .NET 用の Aspose.Cells ライブラリを使用して Xades デジタル署名を Excel ファイルに追加する方法を学習しました。この記事で説明する手順に従うことで、この機能を独自のプロジェクトに実装できるようになります。ライブラリを自由に試してみて、ライブラリが提供する他の強力な機能を発見してください。

### よくある質問

#### Q：ザデスとは何ですか？

A: Xades は、デジタル ドキュメントの完全性と信頼性を保証するために使用される高度な電子署名標準です。

#### Q: Aspose.Cells で他のタイプのデジタル署名を使用できますか?

A: はい、Aspose.Cells は、XMLDSig 署名や PKCS#7 署名など、他のタイプのデジタル署名もサポートしています。

#### Q: Excel ファイル以外のファイル タイプに署名を適用できますか?
 
A: はい、Aspose.Cells では、Word、PDF、PowerPoint ファイルなど、サポートされている他のファイル タイプにデジタル署名を適用することもできます。