---
title: 共有ワークブックのパスワード保護または保護解除
linktitle: 共有ワークブックのパスワード保護または保護解除
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して共有ブックをパスワード保護または保護解除する方法を学びます。
type: docs
weight: 120
url: /ja/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
共有ワークブックをパスワードで保護することは、データのプライバシーを確保するために重要です。 Aspose.Cells for .NET を使用すると、パスワードを使用して共有ワークブックを簡単に保護または保護解除できます。望ましい結果を得るには、以下の手順に従ってください。

## ステップ 1: 出力ディレクトリを指定する

まず、保護された Excel ファイルが保存される出力ディレクトリを指定する必要があります。 Aspose.Cells を使用してこれを行う方法は次のとおりです。

```csharp
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

## ステップ 2: 空の Excel ファイルを作成する

次に、保護または保護解除を適用する空の Excel ファイルを作成できます。サンプルコードは次のとおりです。

```csharp
//空の Excel ワークブックを作成する
Workbook wb = new Workbook();
```

## ステップ 3: 共有ワークブックを保護または保護解除する

ワークブックを作成した後、適切なパスワードを指定して、共有ワークブックを保護または保護解除できます。その方法は次のとおりです。

```csharp
//共有ブックをパスワードで保護する
wb.ProtectSharedWorkbook("1234");

//共有ワークブックの保護を解除するには、この行のコメントを解除します。
// wb.UnprotectSharedWorkbook("1234");
```

## ステップ 4: 出力された Excel ファイルを保存する

保護または保護解除を適用すると、保護された Excel ファイルを指定した出力ディレクトリに保存できます。その方法は次のとおりです。

```csharp
//出力された Excel ファイルを保存する
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Aspose.Cells for .NET を使用した共有ワークブックのパスワード保護または保護解除のサンプル ソース コード 
```csharp
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
//空の Excel ファイルを作成する
Workbook wb = new Workbook();
//共有ワークブックをパスワードで保護する
wb.ProtectSharedWorkbook("1234");
//共有ワークブックの保護を解除するには、この行のコメントを解除します。
//wb.UnprotectSharedWorkbook("1234");
//出力された Excel ファイルを保存する
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## 結論

共有ワークブックをパスワードで保護または保護解除することは、データのセキュリティを確保するために不可欠です。 Aspose.Cells for .NET を使用すると、この機能を Excel ファイルに簡単に追加できます。このガイドの手順に従うと、パスワードを使用して共有ワークブックを効果的に保護または保護解除できます。独自の Excel ファイルを試して、機密データのセキュリティを必ず維持してください。

### よくある質問

#### Q: Aspose.Cells と共有されているワークブックにはどのような種類の保護を適用できますか?
    
A: Aspose.Cells を使用すると、パスワードを指定して共有ワークブックを保護し、データの不正アクセス、変更、削除を防ぐことができます。

#### Q: パスワードを指定せずに共有ワークブックを保護できますか?
    
A: はい、パスワードを指定せずに共有ワークブックを保護できます。ただし、セキュリティを強化するために、強力なパスワードを使用することをお勧めします。

#### Q: Aspose.Cells と共有されているワークブックの保護を解除するにはどうすればよいですか?
    
A: 共有ワークブックの保護を解除するには、ワークブックを保護するときに使用したのと同じパスワードを指定する必要があります。これにより、保護が解除され、データに自由にアクセスできるようになります。

#### Q: 共有ワークブックを保護すると、ワークブック内の機能や数式に影響しますか?
    
A: 共有ブックを保護しても、ユーザーは引き続きブック内の機能や数式にアクセスできます。保護は、ワークブックの構造変更にのみ影響します。