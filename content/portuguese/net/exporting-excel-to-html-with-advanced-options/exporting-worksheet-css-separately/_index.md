---
title: Exportando CSS da planilha separadamente em HTML de saída
linktitle: Exportando CSS da planilha separadamente em HTML de saída
second_title: API de processamento do Aspose.Cells .NET Excel
description: Aprenda como exportar planilhas do Excel para HTML de forma eficaz com CSS separado usando o Aspose.Cells para .NET neste tutorial abrangente passo a passo.
type: docs
weight: 14
url: /pt/net/exporting-excel-to-html-with-advanced-options/exporting-worksheet-css-separately/
---
## Introdução
Neste guia, você aprenderá como exportar uma planilha do Excel para HTML, com foco especial na exportação do CSS separadamente. Isso não só melhora a manutenibilidade dos seus estilos, mas também aumenta a eficiência do seu fluxo de trabalho. Agora, vamos mergulhar direto nos pré-requisitos e colocar a mão na massa!
## Pré-requisitos
Antes de começarmos o código, aqui está o que você precisa para que este tutorial seja tranquilo:
1. Licença Aspose.Cells para .NET: Você precisará de uma licença para utilizar totalmente os recursos do Aspose.Cells. Você pode[baixe a última versão](https://releases.aspose.com/cells/net/)ou pegue um[licença temporária](https://purchase.aspose.com/temporary-license/) se você está apenas testando as águas.
2. Ambiente de desenvolvimento: o ideal é que você tenha o Visual Studio instalado para executar seus projetos .NET sem problemas.
3. Conhecimento básico de C#: Ter um pouco de conhecimento em programação em C# ajudará você a entender melhor os trechos de código.
4.  Documentação de referência: Familiarize-se com o[Documentação do Aspose.Cells](https://reference.aspose.com/cells/net/) para recursos e capacidades adicionais.
Depois de verificar esses pré-requisitos da lista, estamos prontos para começar a parte emocionante!
## Pacotes de importação
Para começar, você precisará importar os namespaces relevantes do Aspose.Cells. Veja como você pode configurá-lo:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Drawing;
```
Esta configuração fornecerá todas as ferramentas necessárias para criar pastas de trabalho, manipular planilhas e gerenciar estilos.

Vamos dividir isso em partes mais fáceis de gerenciar, com cada etapa levando você mais perto do seu objetivo de exportar aquela planilha vibrante do Excel para um arquivo HTML com todo o CSS separado!
## Etapa 1: Defina o diretório de saída
A primeira coisa que você precisa fazer é decidir onde quer salvar seu arquivo HTML exportado. Isso é crucial porque se você errar, pode acabar procurando seu documento em todos os lugares!
```csharp
string outputDir = "Your Document Directory";
```
 Simplesmente substitua`"Your Document Directory"` com o caminho onde você quer que o arquivo seja salvo. Por exemplo:`string outputDir = @"C:\MyExports\";`.
## Etapa 2: Criar um objeto de pasta de trabalho
Em seguida, precisamos criar um novo objeto de workbook. Pense no workbook como sua tela em branco onde toda a mágica acontece!
```csharp
Workbook wb = new Workbook();
```
 Ao fazer isso, inicializamos uma nova instância da classe Workbook. Esta variável`wb` agora conterá toda a nossa planilha do Excel.
## Etapa 3: Acesse a primeira planilha
Agora é hora de mergulhar na sua tela e pegar a primeira planilha. Esta parte é direta, pois precisamos apenas da primeira planilha para este tutorial.
```csharp
Worksheet ws = wb.Worksheets[0];
```
Esta linha busca a primeira planilha na sua pasta de trabalho, pronta para manipulação.
## Etapa 4: Manipular o valor de uma célula
Agora, a parte divertida — vamos colocar alguns dados em uma célula! Você pode escolher qualquer célula, mas, para este exemplo, usaremos a célula “B5”.
```csharp
Cell cell = ws.Cells["B5"];
cell.PutValue("This is some text.");
```
Com esta linha, inserimos o texto "This is some text." na célula B5. Simples, certo? 
## Etapa 5: Defina o estilo da célula
Vamos adicionar um pouco de estilo! Vamos estilizar nosso texto mudando a cor da fonte para vermelho. 
```csharp
Style st = cell.GetStyle();
st.Font.Color = Color.Red;
cell.SetStyle(st);
```
Esta etapa recupera o estilo existente da célula B5, altera a cor da fonte para vermelho e, em seguida, reaplica o novo estilo. Agora sua célula não é apenas mais uma caixa de texto simples!
## Etapa 6: especifique as opções de salvamento de HTML
Nesta fase, prepararemos as opções de salvamento do HTML. Isso é crucial para garantir que seu CSS seja exportado separadamente.
```csharp
HtmlSaveOptions opts = new HtmlSaveOptions();
opts.ExportWorksheetCSSSeparately = true;
```
 Com o`ExportWorksheetCSSSeparately` opção definida como verdadeira, você está dizendo à biblioteca para manipular estilos CSS distintamente em vez de incorporá-los diretamente no arquivo HTML.
## Etapa 7: Salve a pasta de trabalho como HTML
Finalmente, é hora de salvar todo o trabalho duro! Esta linha salva sua pasta de trabalho no diretório de saída especificado como um arquivo HTML.
```csharp
wb.Save(outputDir + "outputExportWorksheetCSSSeparately.html", opts);
```
Aqui, estamos nomeando nosso arquivo de saída`outputExportWorksheetCSSSeparately.html`. E voilà, você conseguiu!
## Etapa 8: Confirmar execução
Para ter certeza de que tudo ocorreu bem, é sempre uma boa prática enviar uma mensagem de confirmação.
```csharp
Console.WriteLine("ExportWorksheetCSSSeparatelyInOutputHTML executed successfully.");
```
Agora você pode executar seu código e, se vir a mensagem de confirmação, parabéns: você exportou com sucesso sua planilha do Excel com CSS separado!
## Conclusão
E aí está — seu próprio guia para exportar uma planilha do Excel para HTML, mantendo o CSS separado, graças ao Aspose.Cells para .NET. Isso não só mantém seu estilo organizado, mas também lhe dá mais flexibilidade sempre que você precisar fazer alterações no futuro. 
## Perguntas frequentes
### O que é Aspose.Cells?
Aspose.Cells é uma poderosa biblioteca .NET que permite criar, modificar e converter planilhas do Excel sem precisar do Microsoft Excel.
### Como posso obter uma avaliação gratuita do Aspose.Cells?
 Você pode baixar uma versão de avaliação gratuita em[Página de lançamentos do Aspose.Cells](https://releases.aspose.com/).
### Posso personalizar ainda mais a saída HTML?
Sim, o Aspose.Cells oferece várias opções para personalizar a saída HTML de acordo com suas necessidades.
### É possível manipular outros elementos da planilha usando Aspose.Cells?
Absolutamente! O Aspose.Cells permite que você manipule gráficos, imagens e muitos outros elementos dentro de uma planilha.
### Onde posso encontrar recursos adicionais?
 Confira o[Documentação do Aspose.Cells](https://reference.aspose.com/cells/net/) para guias detalhados e referências de API.