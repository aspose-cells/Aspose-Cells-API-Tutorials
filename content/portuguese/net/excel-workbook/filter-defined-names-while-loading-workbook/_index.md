---
title: Filtrar nomes definidos ao carregar a pasta de trabalho
linktitle: Filtrar nomes definidos ao carregar a pasta de trabalho
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como filtrar nomes definidos ao carregar uma pasta de trabalho do Excel com Aspose.Cells for .NET.
type: docs
weight: 100
url: /pt/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Ao trabalhar com pastas de trabalho do Excel em um aplicativo .NET, muitas vezes é necessário filtrar dados durante o carregamento. Aspose.Cells for .NET é uma biblioteca poderosa para manipular facilmente pastas de trabalho do Excel. Neste guia, mostraremos como filtrar os nomes definidos ao carregar uma pasta de trabalho usando Aspose.Cells for .NET. Siga estas etapas simples para obter os resultados desejados:

## Etapa 1: especifique as opções de carregamento

Primeiro, você precisa especificar as opções de carregamento para definir o comportamento de carregamento da pasta de trabalho. No nosso caso, queremos ignorar os nomes definidos no carregamento. Veja como fazer isso usando Aspose.Cells:

```csharp
// Especifica opções de carregamento
LoadOptions opts = new LoadOptions();

// Não carregue nomes definidos
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Etapa 2: carregar a pasta de trabalho

Depois que as opções de carregamento estiverem configuradas, você poderá carregar a pasta de trabalho do Excel do arquivo de origem. Certifique-se de especificar o caminho de arquivo correto. Aqui está um exemplo de código:

```csharp
// Carregar a pasta de trabalho
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Etapa 3: salve a pasta de trabalho filtrada

Depois de carregar a pasta de trabalho, você poderá realizar outras operações ou edições conforme necessário. Em seguida, você pode salvar a pasta de trabalho filtrada em um arquivo de saída. Veja como:

```csharp
// Salve a pasta de trabalho do Excel filtrada
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Exemplo de código-fonte para nomes definidos por filtro ao carregar a pasta de trabalho usando Aspose.Cells for .NET 
```csharp
//Especifique as opções de carregamento
LoadOptions opts = new LoadOptions();
//Não queremos carregar nomes definidos
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Carregar a pasta de trabalho
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Salve o arquivo Excel de saída, isso quebrará a fórmula em C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Conclusão

Filtrar nomes definidos ao carregar uma pasta de trabalho do Excel pode ser crítico para muitos aplicativos. Aspose.Cells for .NET facilita essa tarefa, fornecendo opções flexíveis para carregar e filtrar dados. Seguindo as etapas deste guia, você poderá filtrar com eficácia os nomes definidos e obter os resultados desejados em suas pastas de trabalho do Excel.


### Perguntas frequentes

#### P: O Aspose.Cells oferece suporte a outras linguagens de programação além de C#?
    
R: Sim, Aspose.Cells é uma biblioteca multiplataforma que oferece suporte a muitas linguagens de programação, como Java, Python, C++e muitos mais.

#### P: Posso filtrar outros tipos de dados ao carregar uma pasta de trabalho com Aspose.Cells?
    
R: Sim, Aspose.Cells oferece uma variedade de opções de filtragem de dados, incluindo fórmulas, estilos, macros, etc.

#### P: O Aspose.Cells mantém a formatação e as propriedades da pasta de trabalho original?
    
R: Sim, Aspose.Cells mantém a formatação, estilos, fórmulas e outras propriedades da pasta de trabalho original ao trabalhar com arquivos Excel.