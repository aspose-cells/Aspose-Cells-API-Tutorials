---
title: Crie um gráfico em PDF com o tamanho de página desejado
linktitle: Crie um gráfico em PDF com o tamanho de página desejado
second_title: API de processamento do Excel Aspose.Cells .NET
description: Crie um PDF com seu gráfico do Excel usando Aspose.Cells para .NET. Aprenda como com este guia passo a passo.
type: docs
weight: 12
url: /pt/net/chart-rendering-and-conversion/create-chart-pdf-with-desired-page-size/
---
## Introdução

Criar gráficos visualmente atraentes e informativos é essencial para a representação de dados em vários campos. Não importa se você está lidando com dados de vendas, métricas de desempenho ou qualquer outro tipo de informação, ter a capacidade de produzir gráficos de alta qualidade dá profundidade e clareza às suas descobertas. Se você está trabalhando com aplicativos .NET, o Aspose.Cells é uma biblioteca poderosa que torna o manuseio de documentos do Excel e a geração de gráficos uma brisa. Neste tutorial, nós o guiaremos pelo processo de criação de um PDF de um gráfico a partir de um arquivo do Excel com um tamanho de página desejado.

## Pré-requisitos

Antes de mergulhar no código, há alguns pré-requisitos que você deve cumprir para garantir uma experiência tranquila:

### Conhecimento básico de C# e .NET

Você precisará de um entendimento fundamental de programação em C# e do framework .NET. Isso ajudará você a entender a estrutura do código que você encontrará neste guia.

### Aspose.Cells para .NET

Certifique-se de ter o Aspose.Cells para .NET instalado. Você pode encontrar todos os detalhes no[Documentação do Aspose.Cells](https://reference.aspose.com/cells/net/). 

### Ambiente de Desenvolvimento

 Configure seu ambiente de desenvolvimento. Pode ser o Visual Studio ou qualquer outro IDE que suporte C#. Baixe e instale a biblioteca Aspose.Cells do[página de download](https://releases.aspose.com/cells/net/).

### Exemplo de arquivo Excel

Você precisará de um arquivo Excel de exemplo que contenha pelo menos um gráfico. Você pode criar um arquivo de exemplo ou baixar um para usar ao longo deste tutorial.

## Pacotes de importação

Para começar a trabalhar com Aspose.Cells, você precisa importar os namespaces necessários em seu aplicativo C#. Veja como fazer isso:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Charts;
```

Esses namespaces dão acesso às classes e métodos necessários para manipular pastas de trabalho do Excel e seus conteúdos.

Agora que temos todos os pré-requisitos resolvidos, vamos dividir o processo em etapas detalhadas.

## Etapa 1: Configurar diretórios de saída e origem

Para começar, você precisa definir onde o PDF de saída será salvo e onde seu documento Excel de origem estará localizado.

```csharp
//Diretório de saída
string outputDir = "Your Output Directory";

//Diretório de origem
string sourceDir = "Your Document Directory";
```

Certifique-se de substituir "Your Output Directory" e "Your Document Directory" pelos caminhos reais no seu sistema. Isso determina onde o Aspose salvará o PDF gerado e onde ele encontrará o arquivo Excel.

## Etapa 2: Carregue o arquivo Excel de amostra

Em seguida, você precisa carregar o arquivo Excel que contém o gráfico. Veja como:

```csharp
//Carregue um arquivo Excel de exemplo contendo o gráfico.
Workbook wb = new Workbook(sourceDir + "sampleCreateChartPDFWithDesiredPageSize.xlsx");
```

 O`Workbook` class é central para interagir com seu documento Excel. Certifique-se de que o caminho aponta corretamente para seu arquivo Excel — um erro aqui impedirá que o restante do código seja executado.

## Etapa 3: Acesse a primeira planilha

Depois que a pasta de trabalho for carregada, o próximo passo é acessar a planilha que contém o gráfico desejado.

```csharp
//Acesse a primeira planilha.
Worksheet ws = wb.Worksheets[0];
```

 No Aspose.Cells, as planilhas são indexadas a partir do zero, então`Worksheets[0]` refere-se à primeira folha.

## Etapa 4: Acesse o primeiro gráfico

Agora, vamos acessar o gráfico que você quer exportar para um PDF. Este passo pressupõe que sua planilha contenha pelo menos um gráfico.

```csharp
//Acesse o primeiro gráfico dentro da planilha.
Chart ch = ws.Charts[0];
```

Novamente, isso acessa o primeiro gráfico na planilha; certifique-se de que a estrutura da planilha seja adequada a essa abordagem.

## Etapa 5: Crie um PDF com o tamanho de página desejado

Finalmente, é hora de criar o PDF a partir do gráfico com um tamanho de página especificado. Aqui está a linha mágica de código que faz tudo:

```csharp
//Crie um gráfico em PDF com o tamanho de página desejado.
ch.ToPdf(outputDir + "outputCreateChartPDFWithDesiredPageSize.pdf", 7, 7, PageLayoutAlignmentType.Center, PageLayoutAlignmentType.Center);
```

Neste código:
- O PDF será salvo no diretório de saída que você especificou anteriormente.
-  Os números`7, 7` representam a largura e a altura do tamanho de página desejado, respectivamente.
- PageLayoutAlignmentType.Center garante que o gráfico esteja centralizado na página.

## Etapa 6: Mensagem de confirmação

Para que você (e os outros) saibam que tudo ocorreu sem problemas, inclua uma mensagem de confirmação no final do seu código:

```csharp
Console.WriteLine("CreateChartPDFWithDesiredPageSize executed successfully.");
```

Esta mensagem aparecerá na janela do console quando o processo for concluído, sinalizando que seu PDF foi criado sem problemas.

## Conclusão

Parabéns! Você acabou de aprender como aproveitar o Aspose.Cells para .NET para criar um PDF a partir de um gráfico contido em um arquivo Excel. Esta biblioteca poderosa simplifica o processo de manipulação de documentos Excel e geração de representações visuais de dados, economizando horas de formatação manual. Não deixe de explorar a infinidade de outros recursos que o Aspose.Cells oferece além da geração de PDF — você nunca sabe o que pode aprimorar ainda mais seus projetos!

## Perguntas frequentes

### Para que é usado o Aspose.Cells for .NET?  
O Aspose.Cells para .NET é usado para criar, editar e converter documentos do Excel programaticamente em aplicativos .NET.

### Posso usar o Aspose.Cells gratuitamente?  
 Sim, o Aspose.Cells oferece uma[teste gratuito](https://releases.aspose.com/) para fins de avaliação.

### Existe alguma maneira de estender meu teste além do período inicial?  
 Você pode solicitar um[licença temporária](https://purchase.aspose.com/temporary-license/) para testes estendidos.

### E se eu tiver problemas ou dúvidas?  
 Você pode buscar ajuda na comunidade Aspose em seu[fórum de suporte](https://forum.aspose.com/c/cells/9).

### Como posso comprar o Aspose.Cells?  
 Você pode comprar Aspose.Cells no[página de compra](https://purchase.aspose.com/buy).