---
title: Substituição de Regex
linktitle: Substituição de Regex
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como realizar a substituição de Regex em arquivos Excel usando Aspose.Cells for .NET.
type: docs
weight: 140
url: /pt/net/excel-workbook/regex-replace/
---
substituição de texto baseada em expressões regulares (Regex) é uma tarefa comum na manipulação de dados em arquivos Excel. Com Aspose.Cells for .NET, você pode facilmente realizar uma substituição de Regex seguindo estas etapas:

## Etapa 1: especifique o diretório de origem e o diretório de saída

Em primeiro lugar, deve-se especificar o diretório de origem onde se encontra o arquivo Excel que contém os dados a serem substituídos, bem como o diretório de saída onde deseja salvar o arquivo modificado. Veja como fazer isso usando Aspose.Cells:

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();

// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

## Etapa 2: carregue o arquivo Excel de origem

Em seguida, você precisa carregar o arquivo Excel de origem no qual deseja realizar a substituição do Regex. Veja como fazer isso:

```csharp
// Carregue o arquivo Excel de origem
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## Etapa 3: realizar a substituição de Regex

Depois de carregar o arquivo, você pode definir opções de substituição, incluindo distinção entre maiúsculas e minúsculas e correspondência exata do conteúdo da célula. Aqui está um exemplo de código para realizar a substituição do Regex:

```csharp
// Definir opções de substituição
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Defina que a chave de pesquisa é uma expressão regular
replace. RegexKey = true;

// Execute a substituição do Regex
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Etapa 4: salve o arquivo Excel de saída

Depois que a substituição do Regex for concluída, você poderá salvar o arquivo Excel modificado no diretório de saída especificado. Veja como fazer isso:

```csharp
// Salve o arquivo Excel de saída
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Exemplo de código-fonte para Regex Replace usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
//Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Defina como verdadeiro para indicar que a chave pesquisada é regex
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Conclusão

A substituição de Regex é uma técnica poderosa para modificar dados dinamicamente em um arquivo Excel. Com Aspose.Cells for .NET, você pode facilmente realizar uma substituição de Regex seguindo as etapas descritas acima. Experimente suas próprias expressões regulares e aproveite a flexibilidade oferecida pelo Aspose.Cells.

### Perguntas frequentes

#### P: O que é substituição de Regex?
    
R: A substituição de Regex é uma técnica usada para substituir padrões de texto baseados em expressões regulares em um arquivo Excel. Isso permite alterações rápidas e precisas nos dados.

#### P: A substituição do Regex diferencia maiúsculas de minúsculas?
    
R: Não, com Aspose.Cells você pode especificar se a substituição do Regex deve diferenciar maiúsculas de minúsculas ou não. Você tem controle total sobre esse recurso.

#### P: Como posso especificar uma correspondência exata do conteúdo da célula ao substituir o Regex?
    
R: Aspose.Cells permite definir se a substituição do Regex deve corresponder exatamente ao conteúdo da célula ou não. Você pode ajustar esta opção de acordo com suas necessidades.

#### P: Posso usar expressões regulares avançadas ao substituir Regex por Aspose.Cells?
    
R: Sim, Aspose.Cells oferece suporte a expressões regulares avançadas, permitindo realizar substituições complexas e sofisticadas em seus arquivos Excel.

#### P: Como posso verificar se a substituição do Regex foi bem-sucedida?
    
R: Após realizar a substituição do Regex, você pode verificar se a operação foi bem-sucedida verificando a saída e garantindo que o arquivo Excel de saída foi criado corretamente.
	