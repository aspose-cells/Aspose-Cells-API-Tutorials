---
title: Detectar tipos de link
linktitle: Detectar tipos de link
second_title: Referência da API Aspose.Cells para .NET
description: Detecte tipos de link em uma pasta de trabalho do Excel usando Aspose.Cells for .NET.
type: docs
weight: 80
url: /pt/net/excel-workbook/detect-link-types/
---
Neste tutorial, orientaremos você passo a passo pelo código-fonte C# fornecido, que permitirá detectar tipos de link em uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Siga as etapas abaixo para realizar esta operação.

## Etapa 1: definir o diretório de origem

```csharp
// diretório de origem
string SourceDir = RunExamples.Get_SourceDirectory();
```

Nesta primeira etapa, definimos o diretório de origem onde está localizada a pasta de trabalho do Excel que contém os links.

## Etapa 2: carregar a pasta de trabalho do Excel

```csharp
// Carregar a pasta de trabalho do Excel
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Carregamos a pasta de trabalho do Excel usando o caminho do arquivo de origem.

## Etapa 3: obtenha a planilha

```csharp
// Obtenha a primeira planilha (padrão)
Worksheet worksheet = workbook.Worksheets[0];
```

 Obtemos a primeira planilha da pasta de trabalho. Você pode alterar o`[0]` index para acessar uma planilha específica, se necessário.

## Etapa 4: crie um intervalo de células

```csharp
// Crie um intervalo de células A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Criamos um intervalo de células, neste exemplo da célula A1 à célula A7. Você pode ajustar as referências de células conforme necessário.

## Etapa 5: coloque os hiperlinks ao alcance

```csharp
// Obtenha os hiperlinks no intervalo
Hyperlink[] hyperlinks = range.Hyperlinks;
```

Obtemos todos os hiperlinks presentes no intervalo especificado.

## Etapa 6: navegar pelos hiperlinks e visualizar os tipos de links

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Percorremos cada link e exibimos o texto de exibição e o tipo de link associado.

### Exemplo de código-fonte para detectar tipos de links usando Aspose.Cells for .NET 
```csharp
//diretório de origem
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// Obtenha a primeira planilha (padrão)
Worksheet worksheet = workbook.Worksheets[0];
// Crie um intervalo A2:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
// Obtenha hiperlinks ao alcance
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Conclusão

Parabéns! Você aprendeu como detectar tipos de link em uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Este recurso permite que você trabalhe com os hiperlinks presentes em suas pastas de trabalho do Excel. Continue explorando os recursos do Aspose.Cells para expandir seus recursos de processamento de pasta de trabalho do Excel.

### Perguntas frequentes

#### P: Como posso instalar o Aspose.Cells for .NET em meu projeto?

 R: Você pode instalar o Aspose.Cells for .NET usando o gerenciador de pacotes NuGet. Procurar[Aspose Lançamentos](https://releases.aspose.com/cells/net) no console do gerenciador de pacotes NuGet e instale a versão mais recente.

#### P: Posso detectar tipos de links em planilhas específicas em vez de na primeira planilha?

 R: Sim, você pode modificar o`workbook.Worksheets[0]` índice para acessar uma planilha específica. Por exemplo, para acessar a segunda planilha, use`workbook.Worksheets[1]`.

#### P: É possível modificar os tipos de links detectados no intervalo?

R: Sim, você pode navegar por hiperlinks e realizar operações de edição, como atualizar URLs ou remover links indesejados.

#### P: Que tipos de links são possíveis no Aspose.Cells for .NET?

R: Os possíveis tipos de links incluem hiperlinks, links para outras planilhas, links para arquivos externos, links para sites, etc.

#### P: O Aspose.Cells for .NET oferece suporte à criação de novos links em uma planilha?

 R: Sim, Aspose.Cells for .NET suporta a criação de novos links usando o`Hyperlink` classe e suas propriedades associadas. Você pode adicionar hiperlinks, links para URLs, links para outras planilhas, etc.

#### P: Posso usar Aspose.Cells for .NET em aplicativos da web?

R: Sim, o Aspose.Cells for .NET pode ser usado em aplicações web. Você pode incorporá-lo em ASP.NET, ASP.NET Core e outras estruturas da web baseadas em .NET.

#### P: Há algum limite de tamanho de arquivo ao usar Aspose.Cells for .NET?

R: Aspose.Cells for .NET pode processar grandes pastas de trabalho do Excel sem limitação específica. No entanto, o tamanho real do arquivo pode ser limitado pelos recursos disponíveis do sistema.