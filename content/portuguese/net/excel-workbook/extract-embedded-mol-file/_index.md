---
title: Extrair arquivo Mol incorporado
linktitle: Extrair arquivo Mol incorporado
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como extrair facilmente arquivos MOL incorporados de uma pasta de trabalho do Excel usando Aspose.Cells for .NET.
type: docs
weight: 90
url: /pt/net/excel-workbook/extract-embedded-mol-file/
---
Neste tutorial, orientaremos você passo a passo sobre como extrair um arquivo MOL incorporado de uma pasta de trabalho do Excel usando a biblioteca Aspose.Cells para .NET. Você aprenderá como navegar nas planilhas da pasta de trabalho, extrair os objetos OLE correspondentes e salvar os arquivos MOL extraídos. Siga as etapas abaixo para concluir esta tarefa com êxito.

## Etapa 1: definir diretórios de origem e saída
Primeiro, precisamos definir os diretórios de origem e de saída em nosso código. Esses diretórios indicam onde a pasta de trabalho do Excel de origem está localizada e onde os arquivos MOL extraídos serão salvos. Aqui está o código correspondente:

```csharp
// Diretórios
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
```

Certifique-se de especificar os caminhos apropriados conforme necessário.

## Etapa 2: Carregando a pasta de trabalho do Excel
A próxima etapa é carregar a pasta de trabalho do Excel contendo os objetos OLE incorporados e arquivos MOL. Aqui está o código para carregar a pasta de trabalho:

```csharp
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
```

Certifique-se de especificar o nome do arquivo de origem corretamente no código.

## Etapa 3: percorra as planilhas e extraia os arquivos MOL
Agora percorreremos cada planilha da pasta de trabalho e extrairemos os objetos OLE correspondentes, que contêm os arquivos MOL. Aqui está o código correspondente:

```csharp
var index = 1;
foreach(Worksheet sheet in workbook.Worksheets)
{
     OleObjectCollection oles = sheet.OleObjects;
     foreach(OleObject ole in oles)
     {
         string fileName = outputDir + "OleObject" + index + ".mol";
         FileStream fs = File.Create(fileName);
         fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
         fs. Close();
         index++;
     }
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

Esse código percorre cada planilha da pasta de trabalho, busca os objetos OLE e salva os arquivos MOL extraídos no diretório de saída.

### Exemplo de código-fonte para extrair arquivo Mol incorporado usando Aspose.Cells for .NET 
```csharp
//diretórios
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "EmbeddedMolSample.xlsx");
var index = 1;
foreach (Worksheet sheet in workbook.Worksheets)
{
	OleObjectCollection oles = sheet.OleObjects;
	foreach (OleObject ole in oles)
	{
		string fileName = outputDir + "OleObject" + index + ".mol ";
		FileStream fs = File.Create(fileName);
		fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
		fs.Close();
		index++;
	}
}
Console.WriteLine("ExtractEmbeddedMolFile executed successfully.");
```

## Conclusão
Parabéns! Você aprendeu como extrair um arquivo MOL incorporado de uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Agora você pode aplicar esse conhecimento para extrair arquivos MOL de suas próprias pastas de trabalho do Excel. Sinta-se à vontade para explorar mais a biblioteca Aspose.Cells e aprender sobre seus outros recursos poderosos.

### Perguntas frequentes

#### P: O que é um arquivo MOL?
 
R: Um arquivo MOL é um formato de arquivo usado para representar estruturas químicas em química computacional. Ele contém informações sobre átomos, ligações e outras propriedades moleculares.

#### P: Este método funciona com todos os tipos de arquivo Excel?

R: Sim, este método funciona com todos os tipos de arquivo Excel suportados por Aspose.Cells.

#### P: Posso extrair vários arquivos MOL de uma vez?

R: Sim, você pode extrair vários arquivos MOL de uma vez iterando objetos OLE em cada planilha da pasta de trabalho.