---
title: XLSB ファイルの外部接続の読み取りおよび書き込み
linktitle: XLSB ファイルの外部接続の読み取りおよび書き込み
second_title: Aspose.Cells for .NET API リファレンス
description: Aspose.Cells for .NET を使用して XLSB ファイルの外部接続を読み取り、変更する方法を学びます。
type: docs
weight: 130
url: /ja/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
XLSB ファイルへの外部接続の読み取りと書き込みは、Excel ワークブックで外部ソースからのデータを操作するために不可欠です。 Aspose.Cells for .NET を使用すると、次の手順で外部接続の読み取りと書き込みを簡単に行うことができます。

## ステップ 1: ソース ディレクトリと出力ディレクトリを指定する

まず、外部接続を含む XLSB ファイルが配置されているソース ディレクトリと、変更したファイルを保存する出力ディレクトリを指定する必要があります。 Aspose.Cells を使用してこれを行う方法は次のとおりです。

```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();

//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
```

## ステップ 2: ソース Excel XLSB ファイルをロードする

次に、外部接続の読み取りおよび書き込み操作を実行するソース Excel XLSB ファイルをロードする必要があります。サンプルコードは次のとおりです。

```csharp
//ソース Excel XLSB ファイルをロードします
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## ステップ 3: 外部接続の読み取りと変更

ファイルをロードした後、実際にはデータベース接続である最初の外部接続にアクセスできます。外部接続のさまざまなプロパティを読み取り、変更できます。その方法は次のとおりです。

```csharp
//データベース接続である最初の外部接続を読み取ります。
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

//データベース接続名、コマンド、接続情報を表示します。
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

//接続の名前を変更する
dbCon.Name = "NewCustomer";
```

## ステップ 4: 出力 Excel XLSB ファイルを保存する

必要な変更を加えたら、変更した Excel XLSB ファイルを指定した出力ディレクトリに保存できます。その方法は次のとおりです。

```csharp
//出力された Excel XLSB ファイルを保存します。
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Aspose.Cells for .NET を使用した XLSB ファイルの読み取りおよび書き込み外部接続のサンプル ソース コード 
```csharp
//ソースディレクトリ
string sourceDir = RunExamples.Get_SourceDirectory();
//出力ディレクトリ
string outputDir = RunExamples.Get_OutputDirectory();
//ソース Excel Xlsb ファイルをロードします
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//実際には DB 接続である最初の外部接続を読み取ります。
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//DB 接続の名前、コマンド、および接続情報を出力します。
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//接続名の変更
dbCon.Name = "NewCust";
//ExcelのXlsbファイルを保存します。
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## 結論

XLSB ファイルへの外部接続の読み取りと書き込みにより、Excel ワークブック内の外部ソースからのデータを操作できるようになります。 Aspose.Cells for .NET を使用すると、外部接続に簡単にアクセスし、接続情報を読み取りおよび変更し、変更を保存できます。独自の XLSB ファイルを試して、Excel アプリケーションで外部接続の力を活用してください。

### よくある質問

#### Q: XLSB ファイルの外部接続とは何ですか?
    
A: XLSB ファイル内の外部接続は、データベースなどの外部データ ソースと確立された接続を指します。これにより、この外部ソースから Excel ワークブックにデータをインポートできるようになります。

#### Q: XLSB ファイル内に複数の外部接続を含めることはできますか?
     
A: はい、XLSB ファイル内に複数の外部接続を含めることができます。各接続オブジェクトにアクセスすることで、それらを個別に管理できます。

#### Q: Aspose.Cells を使用して XLSB ファイル内の外部接続の詳細を読み取るにはどうすればよいですか?
     
A: Aspose.Cells が提供する機能を使用して、接続名、関連コマンド、接続情報などの外部接続のプロパティにアクセスできます。

#### Q: Aspose.Cells を使用して XLSB ファイル内の外部接続を変更することはできますか?
     
A: はい、特定のニーズに合わせて、接続名などの外部接続のプロパティを変更できます。 Aspose.Cells は、これらの変更を行うためのメソッドを提供します。

#### Q: Aspose.Cells を使用して、外部接続に加えた変更を XLSB ファイルに保存するにはどうすればよいですか?
     
A: 外部接続に必要な変更を加えたら、Aspose.Cells が提供する適切なメソッドを使用して、変更した Excel XLSB ファイルを保存するだけです。