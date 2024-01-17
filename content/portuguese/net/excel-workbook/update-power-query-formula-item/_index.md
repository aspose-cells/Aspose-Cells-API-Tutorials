---
title: Atualizar item de fórmula do Power Query
linktitle: Atualizar item de fórmula do Power Query
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como atualizar elementos de fórmula do Power Query em arquivos Excel usando Aspose.Cells for .NET.
type: docs
weight: 160
url: /pt/net/excel-workbook/update-power-query-formula-item/
---
Atualizar um item de fórmula do Power Query é uma operação comum ao trabalhar com dados em arquivos Excel. Com Aspose.Cells for .NET, você pode atualizar facilmente um item de fórmula do Power Query seguindo estas etapas:

## Etapa 1: especificar os diretórios de origem e de saída

Primeiro, você precisa especificar o diretório de origem onde está localizado o arquivo Excel que contém as fórmulas do Power Query a serem atualizadas, bem como o diretório de saída onde deseja salvar o arquivo modificado. Veja como fazer isso usando Aspose.Cells:

```csharp
// diretório de origem
string SourceDir = RunExamples.Get_SourceDirectory();

// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

## Etapa 2: carregar a pasta de trabalho do Excel de origem

Em seguida, você precisa carregar a pasta de trabalho do Excel de origem na qual deseja atualizar o item de fórmula do Power Query. Veja como fazer isso:

```csharp
// Carregar a pasta de trabalho do Excel de origem
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## Etapa 3: navegar e atualizar itens da fórmula do Power Query

Depois de carregar a pasta de trabalho, você pode navegar até a coleção de fórmulas do Power Query e navegar por cada fórmula e seus elementos. Neste exemplo, procuramos o item da fórmula com o nome “Fonte” e atualizamos seu valor. Aqui está um exemplo de código para atualizar um item de fórmula do Power Query:

```csharp
// Acesse a coleção de fórmulas do Power Query
DataMashup mashupData = workbook.DataMashup;

// Percorra as fórmulas do Power Query e seus elementos
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## Etapa 4: salve a pasta de trabalho do Excel de saída

Depois de atualizar o item de fórmula do Power Query, você pode salvar a pasta de trabalho modificada do Excel no diretório de saída especificado. Veja como fazer isso:

```csharp
// Salve a pasta de trabalho do Excel de saída
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Exemplo de código-fonte para atualizar item de fórmula do Power Query usando Aspose.Cells for .NET 
```csharp
// Diretórios de trabalho
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Salve a pasta de trabalho de saída.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Conclusão

A atualização dos elementos da fórmula do Power Query é uma operação essencial ao usar Aspose.Cells para manipular e processar dados em arquivos Excel. Seguindo as etapas fornecidas acima, você pode atualizar facilmente os elementos da fórmula

### Perguntas frequentes

#### P: O que é Power Query no Excel?
     
R: O Power Query é um recurso do Excel que ajuda a coletar, transformar e carregar dados de diferentes fontes. Oferece ferramentas poderosas para limpar, combinar e remodelar dados antes de importá-los para o Excel.

#### P: Como posso saber se um item de fórmula do Power Query foi atualizado com sucesso?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### P: Posso atualizar vários itens de fórmula do Power Query de uma só vez?
    
R: Sim, você pode percorrer a coleção de itens de fórmula do Power Query e atualizar vários itens em um único loop, dependendo de suas necessidades específicas.

#### P: Existem outras operações que posso realizar em fórmulas do Power Query com Aspose.Cells?
    
R: Sim, Aspose.Cells oferece uma gama completa de recursos para trabalhar com fórmulas do Power Query, incluindo criação, exclusão, cópia e pesquisa de fórmulas em uma pasta de trabalho do Excel.