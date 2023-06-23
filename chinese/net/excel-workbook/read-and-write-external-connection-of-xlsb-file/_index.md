---
title: XLSB文件的外部连接读写
linktitle: XLSB文件的外部连接读写
second_title: Aspose.Cells for .NET API 参考
description: 了解如何使用 Aspose.Cells for .NET 读取和修改 XLSB 文件的外部连接。
type: docs
weight: 130
url: /zh/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
读取和写入 XLSB 文件的外部连接对于在 Excel 工作簿中操作来自外部源的数据至关重要。使用 Aspose.Cells for .NET，您可以使用以下步骤轻松读取和写入外部连接：

## 步骤1：指定源目录和输出目录

首先，您必须指定包含外部连接的 XLSB 文件所在的源目录，以及要保存修改后的文件的输出目录。以下是使用 Aspose.Cells 执行此操作的方法：

```csharp
//源目录
string sourceDir = RunExamples.Get_SourceDirectory();

//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
```

## 步骤 2：加载源 Excel XLSB 文件

接下来，您需要加载要对其进行外部连接读写操作的源Excel XLSB文件。这是示例代码：

```csharp
//加载源 Excel XLSB 文件
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## 第三步：读取并修改外部连接

加载文件后，您可以访问第一个外部连接，它实际上是一个数据库连接。您可以读取和修改外部连接的各种属性。就是这样：

```csharp
//读取第一个外部连接，这是一个数据库连接
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

//显示数据库连接名称、命令和连接信息
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

//修改连接名称
dbCon.Name = "NewCustomer";
```

## 步骤 4：保存输出 Excel XLSB 文件

进行必要的更改后，您可以将修改后的 Excel XLSB 文件保存到指定的输出目录。操作方法如下：

```csharp
//保存输出 Excel XLSB 文件
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### 使用 Aspose.Cells for .NET 读取和写入 XLSB 文件外部连接的示例源代码 
```csharp
//源码目录
string sourceDir = RunExamples.Get_SourceDirectory();
//输出目录
string outputDir = RunExamples.Get_OutputDirectory();
//加载源 Excel Xlsb 文件
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//读取第一个外部连接，它实际上是一个 DB-Connection
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//打印 DB 连接的名称、命令和连接信息
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//修改连接名称
dbCon.Name = "NewCust";
//保存 Excel Xlsb 文件
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## 结论

通过读取和写入 XLSB 文件的外部连接，您可以在 Excel 工作簿中操作来自外部源的数据。使用 Aspose.Cells for .NET，您可以轻松访问外部连接、读取和修改连接信息以及保存更改。试验您自己的 XLSB 文件并利用 Excel 应用程序中外部连接的强大功能。

### 常见问题解答

#### 问：XLSB 文件中的外部连接是什么？
    
答：XLSB文件中的外部连接是指与外部数据源（例如数据库）建立的连接。它允许您将此外部源中的数据导入到 Excel 工作簿中。

#### 问：XLSB 文件中可以有多个外部连接吗？
     
答：是的，一个 XLSB 文件中可以有多个外部连接。您可以通过访问每个连接对象来单独管理它们。

#### 问：如何使用 Aspose.Cells 读取 XLSB 文件中外部连接的详细信息？
     
答：您可以使用Aspose.Cells提供的功能来访问外部连接的属性，例如连接名称、关联命令和连接信息。

#### 问：是否可以使用 Aspose.Cells 修改 XLSB 文件中的外部连接？
     
答：是的，您可以修改外部连接的属性，例如连接名称，以满足您的特定需求。 Aspose.Cells 提供了进行这些更改的方法。

#### 问：如何使用 Aspose.Cells 将对外部连接所做的更改保存到 XLSB 文件中？
     
答：对外部连接进行必要的更改后，您可以使用 Aspose.Cells 提供的适当方法简单地保存修改后的 Excel XLSB 文件。