---
title: Obtenha detalhes do Odata
linktitle: Obtenha detalhes do Odata
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como recuperar detalhes OData de uma pasta de trabalho do Excel usando Aspose.Cells for .NET.
type: docs
weight: 110
url: /pt/net/excel-workbook/get-odata-details/
---
O uso de OData é comum quando se trata de recuperar dados estruturados de fontes de dados externas. Com Aspose.Cells for .NET, você pode recuperar facilmente detalhes OData de uma pasta de trabalho do Excel. Siga as etapas abaixo para obter os resultados desejados:

## Etapa 1: especifique o diretório de origem

Primeiro, você precisa especificar o diretório de origem onde está localizado o arquivo Excel que contém os detalhes do OData. Veja como fazer isso usando Aspose.Cells:

```csharp
// diretório de origem
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Etapa 2: carregar a pasta de trabalho

Depois que o diretório de origem for especificado, você poderá carregar a pasta de trabalho do Excel do arquivo. Aqui está um exemplo de código:

```csharp
// Carregar a pasta de trabalho
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## Etapa 3: obtenha os detalhes do OData

Depois de carregar a pasta de trabalho, você poderá acessar os detalhes do OData usando a coleção PowerQueryFormulas. Veja como:

```csharp
// Recuperar a coleção de fórmulas do Power Query
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Percorra cada fórmula do Power Query
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Recuperar a coleção de elementos da fórmula do Power Query
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Iterar através de cada elemento da fórmula do Power Query
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Exemplo de código-fonte para obter detalhes do Odata usando Aspose.Cells for .NET 
```csharp
// diretório de origem
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Conclusão

Recuperar detalhes OData de uma pasta de trabalho do Excel agora é fácil com Aspose.Cells for .NET. Seguindo as etapas descritas neste guia, você poderá acessar e processar dados OData com eficiência. Experimente seus próprios arquivos Excel contendo detalhes OData e aproveite ao máximo esse recurso poderoso.

### Perguntas frequentes

#### P: O Aspose.Cells oferece suporte a outras fontes de dados além do OData?
    
R: Sim, Aspose.Cells oferece suporte a várias fontes de dados, como bancos de dados SQL, arquivos CSV, serviços da web, etc.

#### P: Como posso usar detalhes OData recuperados em meu aplicativo?
    
R: Depois de recuperar os detalhes do OData usando Aspose.Cells, você poderá usá-los para análise de dados, geração de relatórios ou qualquer outra manipulação em seu aplicativo.

#### P: Posso filtrar ou classificar dados OData ao recuperar com Aspose.Cells?
    
R: Sim, Aspose.Cells oferece funcionalidade avançada para filtrar, classificar e manipular dados OData para atender às suas necessidades específicas.

#### P: Posso automatizar o processo de recuperação de detalhes OData com Aspose.Cells?
    
R: Sim, você pode automatizar o processo de recuperação de detalhes OData integrando Aspose.Cells em seus fluxos de trabalho ou usando scripts de programação.