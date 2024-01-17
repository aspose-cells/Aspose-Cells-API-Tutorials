---
title: Permitir apóstrofo inicial
linktitle: Permitir apóstrofo inicial
second_title: Referência da API Aspose.Cells para .NET
description: Permitir apóstrofo inicial em pastas de trabalho do Excel com Aspose.Cells for .NET.
type: docs
weight: 60
url: /pt/net/excel-workbook/allow-leading-apostrophe/
---
Neste tutorial passo a passo, explicaremos o código-fonte C# fornecido que permitirá o uso de um apóstrofo inicial em uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Siga as etapas abaixo para realizar esta operação.

## Etapa 1: definir diretórios de origem e saída

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

Nesta primeira etapa, definimos os diretórios de origem e saída dos arquivos Excel.

## Etapa 2: instanciar um objeto WorkbookDesigner

```csharp
// Instanciar um objeto WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
```

 Criamos uma instância do`WorkbookDesigner` classe de Aspose.Cells.

## Etapa 3: carregar a pasta de trabalho do Excel

```csharp
// Carregar a pasta de trabalho do Excel
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
designer.Workbook = workbook;
```

Carregamos a pasta de trabalho do Excel do arquivo especificado e desabilitamos a conversão automática de apóstrofos iniciais em estilo de texto.

## Etapa 4: definir fonte de dados

```csharp
// Definir a fonte de dados da pasta de trabalho do designer
List<DataObject> list = new List<DataObject>
{
new DataObject
{
Id=1,
Name = "demo"
},
new DataObject
{
ID=2,
Name = "'demo"
}
};
designer.SetDataSource("sampleData", list);
```

 Definimos uma lista de objetos de dados e usamos o`SetDataSource` método para definir a fonte de dados para a pasta de trabalho do designer.

## Passo 5: Processar marcadores inteligentes

```csharp
// Processar marcadores inteligentes
designer. Process();
```

 Nós usamos o`Process` método para processar marcadores inteligentes na pasta de trabalho do designer.

## Etapa 6: salve a pasta de trabalho modificada do Excel

```csharp
// Salve a pasta de trabalho do Excel modificada
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
```

Salvamos a pasta de trabalho do Excel modificada com as alterações feitas.

### Exemplo de código-fonte para permitir apóstrofo inicial usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
// Instanciando um objeto WorkbookDesigner
WorkbookDesigner designer = new WorkbookDesigner();
Workbook workbook = new Workbook(sourceDir + "AllowLeadingApostropheSample.xlsx");
workbook.Settings.QuotePrefixToStyle = false;
// Abra uma planilha de designer contendo marcadores inteligentes
designer.Workbook = workbook;
List<DataObject> list = new List<DataObject>
{
	new DataObject
	{
		 Id =1,
		 Name = "demo"
	},
	new DataObject
	{
		Id=2,
		Name = "'demo"
	}
};
// Defina a fonte de dados da planilha do designer
designer.SetDataSource("sampleData", list);
// Processe os marcadores inteligentes
designer.Process();
designer.Workbook.Save(outputDir + "AllowLeadingApostropheSample_out.xlsx");
Console.WriteLine("AllowLeadingApostrophe executed successfully.");
```

## Conclusão

Parabéns! Você aprendeu como permitir o uso de um apóstrofo inicial em uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Experimente seus próprios dados para personalizar ainda mais suas pastas de trabalho do Excel.

### Perguntas frequentes

#### P: O que é permissão de apóstrofo inicial em uma pasta de trabalho do Excel?

R: Permitir o apóstrofo inicial em uma pasta de trabalho do Excel permite que os dados que começam com um apóstrofo sejam exibidos corretamente sem convertê-los em um estilo de texto. Isto é útil quando você deseja manter o apóstrofo como parte dos dados.

#### P: Por que preciso desativar a conversão automática de apóstrofos iniciais?

R: Ao desativar a conversão automática de cotações iniciais, você pode preservar seu uso como está em seus dados. Isso evita qualquer modificação não intencional dos dados ao abrir ou manipular a pasta de trabalho do Excel.

#### P: Como definir a fonte de dados na pasta de trabalho do designer?

 R: Para definir a fonte de dados na pasta de trabalho do designer, você pode usar o`SetDataSource` método especificando o nome da fonte de dados e uma lista de objetos de dados correspondentes.

#### P: Permitir o apóstrofo inicial afeta outros dados na pasta de trabalho do Excel?

R: Não, permitir o apóstrofo inicial afeta apenas os dados que começam com um apóstrofo. Outros dados na pasta de trabalho do Excel permanecem inalterados.

#### P: Posso usar esse recurso com outros formatos de arquivo Excel?

R: Sim, você pode usar este recurso com outros formatos de arquivo Excel suportados pelo Aspose.Cells, como .xls, .xlsm, etc.