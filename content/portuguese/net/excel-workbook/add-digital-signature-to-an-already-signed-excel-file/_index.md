---
title: Adicionar assinatura digital a um arquivo Excel já assinado
linktitle: Adicionar assinatura digital a um arquivo Excel já assinado
second_title: Referência da API Aspose.Cells para .NET
description: Adicione facilmente assinaturas digitais a arquivos Excel existentes com Aspose.Cells for .NET.
type: docs
weight: 30
url: /pt/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Neste guia passo a passo, explicaremos o código-fonte C# fornecido que permitirá adicionar uma assinatura digital a um arquivo Excel já assinado usando Aspose.Cells for .NET. Siga as etapas abaixo para adicionar uma nova assinatura digital a um arquivo Excel existente.

## Etapa 1: definir diretórios de origem e saída

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();

// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

Nesta primeira etapa, definimos os diretórios de origem e saída que serão utilizados para carregar o arquivo Excel existente e salvar o arquivo com a nova assinatura digital.

## Etapa 2: carregar o arquivo Excel existente

```csharp
// Carregue a pasta de trabalho do Excel já assinada
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Aqui carregamos o arquivo Excel já assinado usando o`Workbook` classe de Aspose.Cells.

## Etapa 3: Crie a coleção de assinaturas digitais

```csharp
// Crie a coleção de assinaturas digitais
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Criamos uma nova coleção de assinaturas digitais usando o`DigitalSignatureCollection` aula.

## Etapa 4: crie um novo certificado

```csharp
// Crie um novo certificado
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Aqui criamos um novo certificado a partir do arquivo e senha fornecidos.

## Etapa 5: adicione uma nova assinatura digital à coleção

```csharp
// Crie uma nova assinatura digital
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Adicione a assinatura digital à coleção
dsCollection.Add(signature);
```

 Criamos uma nova assinatura digital usando o`DigitalSignature` class e adicioná-lo à coleção de assinaturas digitais.

## Etapa 6: adicionar a coleção de assinaturas digitais à pasta de trabalho

```csharp
//Adicione a coleção de assinaturas digitais à pasta de trabalho
workbook.AddDigitalSignature(dsCollection);
```

 Adicionamos a coleção de assinaturas digitais à pasta de trabalho existente do Excel usando o`AddDigitalSignature()` método.

## Etapa 7: salve e feche a pasta de trabalho

```csharp
// Salve a pasta de trabalho e feche-a
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Salvamos a pasta de trabalho com a nova assinatura digital no diretório de saída especificado, fechamos e liberamos os recursos associados.

### Exemplo de código-fonte para adicionar assinatura digital a um arquivo Excel já assinado usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
//Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
//Arquivo de certificado e sua senha
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Carregue a pasta de trabalho que já está assinada digitalmente para adicionar uma nova assinatura digital
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Crie a coleção de assinatura digital
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Criar novo certificado
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Crie uma nova assinatura digital e adicione-a à coleção de assinaturas digitais
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Adicionar coleção de assinatura digital dentro da pasta de trabalho
workbook.AddDigitalSignature(dsCollection);
//Salve a pasta de trabalho e descarte-a.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Conclusão

Parabéns! Agora você aprendeu como adicionar uma assinatura digital a um arquivo Excel já assinado usando Aspose.Cells for .NET. As assinaturas digitais adicionam uma camada extra de segurança aos seus arquivos Excel, garantindo sua autenticidade e integridade.

### Perguntas frequentes

#### P: O que é Aspose.Cells para .NET?

R: Aspose.Cells for .NET é uma biblioteca de classes poderosa que permite aos desenvolvedores .NET criar, modificar, converter e manipular arquivos Excel com facilidade.

#### P: O que é uma assinatura digital em um arquivo Excel?

R: A assinatura digital em arquivo Excel é uma marca eletrônica que garante a autenticidade, integridade e origem do documento. É usado para verificar se o arquivo não foi modificado desde que foi assinado e vem de uma fonte confiável.

#### P: Quais são os benefícios de adicionar uma assinatura digital a um arquivo Excel?

R: Adicionar uma assinatura digital a um arquivo Excel oferece vários benefícios, incluindo proteção contra alterações não autorizadas, garantindo a integridade dos dados, autenticando o autor do documento e proporcionando confiança nas informações que ele contém.

#### P: Posso adicionar várias assinaturas digitais a um arquivo Excel?

R: Sim, Aspose.Cells permite adicionar várias assinaturas digitais a um arquivo Excel. Você pode criar uma coleção de assinaturas digitais e adicioná-las ao arquivo em uma única operação.

#### P: Quais são os requisitos para adicionar uma assinatura digital a um arquivo Excel?

R: Para adicionar uma assinatura digital a um arquivo Excel, você precisa de um certificado digital válido que será usado para assinar o documento. Certifique-se de ter o certificado e a senha corretos antes de adicionar a assinatura digital.