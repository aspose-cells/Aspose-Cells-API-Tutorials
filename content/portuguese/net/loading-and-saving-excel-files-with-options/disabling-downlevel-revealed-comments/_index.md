---
title: Desabilitando comentários revelados de nível inferior ao salvar em HTML
linktitle: Desabilitando comentários revelados de nível inferior ao salvar em HTML
second_title: API de processamento do Aspose.Cells .NET Excel
description: Aprenda como desabilitar comentários revelados de nível inferior ao salvar uma pasta de trabalho do Excel em HTML usando o Aspose.Cells para .NET com este guia passo a passo detalhado.
type: docs
weight: 11
url: /pt/net/loading-and-saving-excel-files-with-options/disabling-downlevel-revealed-comments/
---
## Introdução
Você já precisou converter uma pasta de trabalho do Excel para HTML e queria garantir que nenhum comentário desnecessário ou conteúdo oculto fosse revelado durante o processo? É aí que desabilitar comentários revelados de nível inferior é útil. Se estiver usando o Aspose.Cells para .NET, você tem controle total sobre como suas pastas de trabalho do Excel são renderizadas como arquivos HTML. Neste tutorial, vamos guiá-lo por um guia passo a passo simples para ajudá-lo a desabilitar comentários revelados de nível inferior ao salvar uma pasta de trabalho em HTML. 
Ao final deste artigo, você terá uma compreensão clara de como usar esse recurso e garantirá que sua saída HTML seja limpa e sem comentários.
## Pré-requisitos
Antes de mergulharmos no guia passo a passo, vamos abordar algumas coisas que você precisa ter em mãos para seguir adiante sem problemas:
1.  Aspose.Cells para .NET: Você precisará ter a biblioteca Aspose.Cells instalada. Se você ainda não a instalou, você pode baixá-la[aqui](https://releases.aspose.com/cells/net/).
2. IDE: Um ambiente de desenvolvimento como o Visual Studio para escrever e executar seu código C#.
3. Conhecimento básico de C#: familiaridade com a sintaxe C# e programação orientada a objetos ajudará você a acompanhar o código.
4.  Versão temporária ou licenciada: você pode usar a versão de avaliação gratuita ou solicitar uma licença temporária em[aqui](https://purchase.aspose.com/temporary-license/). Isso garante que a biblioteca funcione sem quaisquer limitações.
Agora que você está pronto, vamos direto ao assunto!
## Importar namespaces
Antes de entrarmos nos exemplos de código, é essencial incluir os namespaces necessários para Aspose.Cells. Sem eles, seu código não conseguirá acessar os métodos e propriedades necessários para manipular arquivos do Excel.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Certifique-se de colocar esta linha no topo do seu arquivo C# para importar o namespace Aspose.Cells.
## Etapa 1: Configurar os caminhos do diretório
Antes de qualquer coisa, precisamos configurar o diretório de origem (onde seu arquivo Excel está armazenado) e o diretório de saída (onde seu arquivo HTML será salvo). Isso é crucial porque o Aspose.Cells requer os caminhos exatos dos arquivos para acessar e salvar arquivos.
```csharp
// Diretório de origem onde seu arquivo Excel está localizado
string sourceDir = "Your Document Directory";
// Diretório de saída onde o arquivo HTML resultante será salvo
string outputDir = "Your Document Directory";
```
 Nesta etapa, substitua`"Your Document Directory"` com os caminhos de arquivo reais no seu sistema. Você também pode criar diretórios personalizados para organizar melhor seus arquivos de entrada e saída.
## Etapa 2: Carregue a pasta de trabalho do Excel
 Nesta etapa, carregaremos a pasta de trabalho do Excel na memória para que possamos manipulá-la. Para fins de demonstração, usaremos um arquivo de amostra chamado`"sampleDisableDownlevelRevealedComments.xlsx"`. Você pode usar qualquer pasta de trabalho que preferir.
```csharp
// Carregue a pasta de trabalho de amostra do diretório de origem
Workbook wb = new Workbook(sourceDir + "sampleDisableDownlevelRevealedComments.xlsx");
```
Isso cria um objeto Workbook que contém todos os dados e a estrutura do seu arquivo Excel. A partir daqui, você pode modificá-lo, aplicar configurações e, finalmente, salvá-lo em um formato diferente.
## Etapa 3: Configurar opções de salvamento de HTML
Agora, precisamos configurar o objeto HtmlSaveOptions para desabilitar comentários revelados de nível inferior. Esta opção garante que quaisquer comentários ou conteúdo oculto não serão revelados no arquivo HTML resultante.
```csharp
// Crie um novo objeto HtmlSaveOptions para configurar as opções de salvamento
HtmlSaveOptions opts = new HtmlSaveOptions();
// Desabilitar comentários revelados de nível inferior
opts.DisableDownlevelRevealedComments = true;
```
 Ao definir`DisableDownlevelRevealedComments` para`true`, você garante que, ao salvar a pasta de trabalho como um arquivo HTML, todos os comentários de nível inferior serão desabilitados.
## Etapa 4: Salve a pasta de trabalho como HTML
Depois que o objeto HtmlSaveOptions estiver configurado, o próximo passo é salvar a pasta de trabalho em HTML usando as opções especificadas. É aqui que a conversão real do arquivo acontece.
```csharp
// Salve a pasta de trabalho como um arquivo HTML com as opções de salvamento especificadas
wb.Save(outputDir + "outputDisableDownlevelRevealedComments_true.html", opts);
```
Nesta linha de código, estamos salvando a pasta de trabalho no diretório de saída que você especificou anteriormente e aplicando a configuração DisableDownlevelRevealedComments. O resultado será um arquivo HTML limpo, sem comentários indesejados.
## Etapa 5: verificar e executar
Por fim, para garantir que tudo funcionou conforme o esperado, você pode enviar uma mensagem de sucesso para o console.
```csharp
// Envie uma mensagem de sucesso para o console
Console.WriteLine("DisableDownlevelRevealedCommentsWhileSavingToHTML executed successfully.");
```
Isso permite que você saiba que a operação foi concluída sem erros.
## Conclusão
E aí está! Você aprendeu com sucesso como desabilitar comentários revelados de nível inferior ao salvar uma pasta de trabalho do Excel em HTML usando o Aspose.Cells para .NET. Com esse recurso, agora você pode controlar como suas pastas de trabalho são renderizadas como HTML e evitar revelar qualquer conteúdo desnecessário. Quer você esteja desenvolvendo um aplicativo da web ou simplesmente precise de uma saída HTML limpa, esse método garante que suas conversões de pasta de trabalho sejam precisas e seguras.
Se você achou este tutorial útil, considere explorar outros recursos do Aspose.Cells para aprimorar ainda mais suas capacidades de processamento do Excel.
## Perguntas frequentes
### O que são comentários revelados de nível inferior?
Comentários revelados de nível inferior são normalmente usados no desenvolvimento web para fornecer informações extras para navegadores mais antigos que não suportam certos recursos HTML. Em conversões de Excel para HTML, eles podem às vezes revelar conteúdo ou comentários ocultos, e é por isso que desabilitá-los pode ser útil.
### Posso habilitar comentários de nível inferior se precisar deles?
 Sim, basta definir o`DisableDownlevelRevealedComments` propriedade para`false` se você quiser habilitar comentários de nível inferior ao salvar sua pasta de trabalho como HTML.
### Como obtenho uma licença temporária para o Aspose.Cells?
 Você pode facilmente solicitar uma licença temporária visitando o[Site Aspose](https://purchase.aspose.com/temporary-license/).
### Desabilitar comentários de nível inferior afeta a aparência do HTML?
Não, desabilitar comentários revelados de nível inferior não afeta a aparência visual da saída HTML. Apenas previne a exposição de informações extras destinadas a navegadores mais antigos.
### Posso salvar a pasta de trabalho em outros formatos além de HTML?
 Sim, o Aspose.Cells suporta uma variedade de formatos de saída, como PDF, CSV e TXT. Você pode explorar mais opções no[documentação](https://reference.aspose.com/cells/net/).