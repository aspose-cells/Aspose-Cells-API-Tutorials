---
title: Ler e gravar conexão externa do arquivo XLSB
linktitle: Ler e gravar conexão externa do arquivo XLSB
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como ler e modificar as conexões externas de um arquivo XLSB usando Aspose.Cells for .NET.
type: docs
weight: 130
url: /pt/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Ler e gravar conexões externas em um arquivo XLSB é essencial para manipular dados de fontes externas em suas pastas de trabalho do Excel. Com Aspose.Cells for .NET você pode ler e escrever facilmente conexões externas usando as seguintes etapas:

## Etapa 1: especifique o diretório de origem e o diretório de saída

Primeiro, você deve especificar o diretório de origem onde está localizado o arquivo XLSB que contém a conexão externa, bem como o diretório de saída onde deseja salvar o arquivo modificado. Veja como fazer isso usando Aspose.Cells:

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();

// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

## Etapa 2: carregar o arquivo Excel XLSB de origem

Em seguida, você precisa carregar o arquivo Excel XLSB de origem no qual deseja realizar operações de leitura e gravação de conexão externa. Aqui está um exemplo de código:

```csharp
// Carregue o arquivo Excel XLSB de origem
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Etapa 3: leia e modifique a conexão externa

Após carregar o arquivo, você pode acessar a primeira conexão externa que na verdade é uma conexão de banco de dados. Você pode ler e modificar diversas propriedades da conexão externa. Veja como:

```csharp
// Leia a primeira conexão externa que é uma conexão de banco de dados
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Exibir o nome da conexão do banco de dados, comando e informações de conexão
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Modifique o nome da conexão
dbCon.Name = "NewCustomer";
```

## Etapa 4: salve o arquivo Excel XLSB de saída

Depois de fazer as alterações necessárias, você pode salvar o arquivo Excel XLSB modificado no diretório de saída especificado. Veja como fazer isso:

```csharp
// Salve o arquivo Excel XLSB de saída
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Exemplo de código-fonte para conexão externa de leitura e gravação de arquivo XLSB usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
//Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
//Carregue o arquivo Excel Xlsb de origem
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Leia a primeira conexão externa que na verdade é uma conexão de banco de dados
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Imprima o nome, comando e informações de conexão da conexão de banco de dados
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Modifique o nome da conexão
dbCon.Name = "NewCust";
//Salve o arquivo Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Conclusão

Ler e gravar conexões externas em um arquivo XLSB permite manipular dados de fontes externas em suas pastas de trabalho do Excel. Com Aspose.Cells for .NET, você pode acessar facilmente conexões externas, ler e modificar informações de conexão e salvar alterações. Experimente seus próprios arquivos XLSB e aproveite o poder das conexões externas em seus aplicativos Excel.

### Perguntas frequentes

#### P: O que é uma conexão externa em um arquivo XLSB?
    
R: Uma conexão externa em um arquivo XLSB refere-se a uma conexão estabelecida com uma fonte de dados externa, como um banco de dados. Ele permite importar dados desta fonte externa para a pasta de trabalho do Excel.

#### P: Posso ter múltiplas conexões externas em um arquivo XLSB?
     
R: Sim, você pode ter múltiplas conexões externas em um arquivo XLSB. Você pode gerenciá-los individualmente acessando cada objeto de conexão.

#### P: Como posso ler os detalhes de uma conexão externa em um arquivo XLSB com Aspose.Cells?
     
R: Você pode usar a funcionalidade fornecida por Aspose.Cells para acessar propriedades de uma conexão externa, como nome da conexão, comando associado e informações de conexão.

#### P: É possível modificar uma conexão externa em um arquivo XLSB com Aspose.Cells?
     
R: Sim, você pode modificar as propriedades de uma conexão externa, como o nome da conexão, para atender às suas necessidades específicas. Aspose.Cells fornece métodos para fazer essas alterações.

#### P: Como posso salvar as alterações feitas em uma conexão externa em um arquivo XLSB com Aspose.Cells?
     
R: Depois de fazer as alterações necessárias em uma conexão externa, você pode simplesmente salvar o arquivo Excel XLSB modificado usando o método apropriado fornecido por Aspose.Cells.