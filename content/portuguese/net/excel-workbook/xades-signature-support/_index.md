---
title: Suporte à assinatura Xades
linktitle: Suporte à assinatura Xades
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como adicionar uma assinatura Xades a um arquivo Excel usando Aspose.Cells for .NET.
type: docs
weight: 190
url: /pt/net/excel-workbook/xades-signature-support/
---
Neste artigo, iremos guiá-lo passo a passo para explicar o código-fonte C# abaixo, que trata do suporte à assinatura Xades usando a biblioteca Aspose.Cells para .NET. Você descobrirá como usar esta biblioteca para adicionar uma assinatura digital Xades a um arquivo Excel. Também forneceremos uma visão geral do processo de assinatura e sua execução. Siga as etapas abaixo para obter resultados conclusivos.

## Etapa 1: definir diretórios de origem e saída
Para começar, precisamos definir os diretórios de origem e de saída em nosso código. Esses diretórios indicam onde os arquivos de origem estão localizados e onde o arquivo de saída será salvo. Aqui está o código correspondente:

```csharp
// Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

Certifique-se de adaptar os caminhos dos diretórios conforme necessário.

## Etapa 2: Carregando a pasta de trabalho do Excel
A próxima etapa é carregar a pasta de trabalho do Excel na qual queremos adicionar a assinatura digital Xades. Aqui está o código para carregar a pasta de trabalho:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Certifique-se de especificar o nome do arquivo de origem corretamente no código.

## Passo 3: Configurando a assinatura digital
Agora iremos configurar a assinatura digital Xades fornecendo as informações necessárias. Devemos especificar o arquivo PFX que contém o certificado digital, bem como a senha associada. Aqui está o código correspondente:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Certifique-se de substituir “pfxPassword” pela sua senha real e “pfxFile” pelo caminho para o arquivo PFX.

## Passo 4: Adicionando a assinatura digital
Agora que configuramos a assinatura digital, podemos adicioná-la à pasta de trabalho do Excel. Aqui está o código correspondente:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Esta etapa adiciona a assinatura digital Xades à pasta de trabalho do Excel.

## Passo 5: Salvando a pasta de trabalho com a assinatura
Por fim, salvamos a pasta de trabalho do Excel com a assinatura digital adicionada. Aqui está o código correspondente:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Certifique-se de adaptar o nome do arquivo de saída de acordo com suas necessidades.

### Exemplo de código-fonte para suporte à assinatura Xades usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
//Diretório de saída
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

## Conclusão
Parabéns! Você aprendeu como usar a biblioteca Aspose.Cells para .NET para adicionar uma assinatura digital Xades a um arquivo Excel. Seguindo as etapas fornecidas neste artigo, você poderá implementar essa funcionalidade em seus próprios projetos. Sinta-se à vontade para experimentar mais a biblioteca e descobrir outros recursos poderosos que ela oferece.

### Perguntas frequentes

#### P: O que é Xades?

R: Xades é um padrão avançado de assinatura eletrônica usado para garantir a integridade e autenticidade de documentos digitais.

#### P: Posso usar outros tipos de assinaturas digitais com Aspose.Cells?

R: Sim, Aspose.Cells também oferece suporte a outros tipos de assinaturas digitais, como assinaturas XMLDSig e assinaturas PKCS#7.

#### P: Posso aplicar uma assinatura a outros tipos de arquivo além dos arquivos do Excel?
 
R: Sim, Aspose.Cells também permite aplicar assinaturas digitais a outros tipos de arquivos suportados, como arquivos Word, PDF e PowerPoint.