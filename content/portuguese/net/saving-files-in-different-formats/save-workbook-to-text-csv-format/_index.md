---
title: Salvar pasta de trabalho em formato de texto CSV
linktitle: Salvar pasta de trabalho em formato de texto CSV
second_title: API de processamento do Aspose.Cells .NET Excel
description: Aprenda a converter facilmente pastas de trabalho do Excel para o formato CSV com o Aspose.Cells neste tutorial abrangente e passo a passo projetado para desenvolvedores .NET.
type: docs
weight: 17
url: /pt/net/saving-files-in-different-formats/save-workbook-to-text-csv-format/
---
## Introdução
Ao lidar com dados, o formato que você escolher pode realmente determinar o quão facilmente você pode trabalhar com eles. Entre os formatos mais comuns para lidar com dados tabulares está o CSV (Comma-Separated Values). Se você é um desenvolvedor trabalhando com arquivos Excel e precisa converter planilhas para o formato CSV, o Aspose.Cells for .NET é uma biblioteca fantástica que simplifica essa tarefa. Neste tutorial, detalharemos as etapas para converter uma planilha do Excel para um formato de texto CSV perfeitamente.
## Pré-requisitos
Antes de começarmos, vamos garantir que você tenha tudo pronto para começar:
1. Conhecimento básico de C# e .NET: como escreveremos código em C#, a familiaridade com a linguagem e o framework .NET é essencial.
2. Biblioteca Aspose.Cells: Certifique-se de ter a biblioteca Aspose.Cells for .NET instalada em seu ambiente de desenvolvimento. Você pode baixá-la[aqui](https://releases.aspose.com/cells/net/).
3. Visual Studio ou qualquer IDE C#: Você precisará de um ambiente de desenvolvimento integrado (IDE) para escrever e executar seu código. O Visual Studio é uma escolha popular.
4. Pasta de trabalho do Excel: prepare uma pasta de trabalho do Excel de exemplo (por exemplo, "book1.xls") que contenha alguns dados para testar a conversão.
## Pacotes de importação
Agora que cobrimos nossos pré-requisitos, o primeiro passo do processo é importar os pacotes necessários. No seu projeto C#, você precisa incluir o seguinte namespace no topo do seu arquivo de código:
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
Esses namespaces darão acesso às classes e métodos necessários para trabalhar com arquivos do Excel e gerenciar fluxos de memória.
## Etapa 1: Defina o caminho para o diretório de documentos
primeiro passo do nosso processo é definir onde nossos documentos (pastas de trabalho do Excel) são armazenados. Isso é essencial, pois permite que nosso programa saiba onde encontrar os arquivos que precisa processar. 
```csharp
// O caminho para o diretório de documentos.
string dataDir = "Your Document Directory";
```
 Certifique-se de substituir`"Your Document Directory"` com o caminho real onde seu arquivo "book1.xls" reside. Pode ser um diretório no seu computador ou um caminho para um servidor.
## Etapa 2: Carregue sua pasta de trabalho de origem
Em seguida, precisamos carregar a pasta de trabalho do Excel que será convertida para o formato CSV.
```csharp
// Carregue sua pasta de trabalho de origem
Workbook workbook = new Workbook(dataDir + "book1.xls");
```
 O`Workbook` A classe da biblioteca Aspose.Cells permite manipulação e acesso a planilhas do Excel. Ao passar o caminho do arquivo, estamos carregando a planilha especificada para processamento.
## Etapa 3: Inicializar uma matriz de bytes para dados da pasta de trabalho
Antes de começarmos a converter a pasta de trabalho em CSV, precisamos inicializar uma matriz de bytes vazia que conterá todos os dados da planilha.
```csharp
// Matriz de 0 bytes
byte[] workbookData = new byte[0];
```
Esta matriz de bytes combinará os dados de cada planilha em uma única estrutura que podemos gravar em um arquivo posteriormente.
## Etapa 4: Configurar opções de salvamento de texto
Agora, vamos configurar as opções de como queremos salvar o formato do texto. Você pode escolher delimitadores personalizados ou ficar com tabulações.
```csharp
// Opções de salvamento de texto. Você pode usar qualquer tipo de separador
TxtSaveOptions opts = new TxtSaveOptions();
opts.Separator = '\t'; // Definir tabulação como separador
```
 Neste exemplo, estamos usando um caractere de tabulação como separador. Você pode substituir`'\t'` com qualquer caractere que você desejar, como uma vírgula (`,`), dependendo de como você deseja que seu CSV seja formatado.
## Etapa 5: iterar por cada planilha
 Em seguida, percorreremos todas as planilhas da pasta de trabalho, salvando cada uma em nosso`workbookData` matriz, mas primeiro você deve selecionar em qual planilha trabalhar.
```csharp
// Copie cada dado da planilha em formato de texto dentro da matriz de dados da pasta de trabalho
for (int idx = 0; idx < workbook.Worksheets.Count; idx++)
{
    // Salvar a planilha ativa em formato de texto
    MemoryStream ms = new MemoryStream();
    workbook.Worksheets.ActiveSheetIndex = idx;
    workbook.Save(ms, opts);
```
 O loop percorre cada planilha na pasta de trabalho.`ActiveSheetIndex` é definido para que cada vez que passarmos pelo loop, estejamos salvando a planilha atual. Os resultados serão salvos na memória usando um`MemoryStream`.
## Etapa 6: recuperar dados da planilha
 Depois de salvar uma planilha no fluxo de memória, a próxima etapa é recuperar esses dados e anexá-los ao nosso`workbookData` variedade.
```csharp
    // Salvar os dados da planilha na matriz de dados da planilha
    ms.Position = 0; // Redefinir posição do fluxo de memória
    byte[] sheetData = ms.ToArray(); // Obter a matriz de bytes
```
`ms.Position = 0;` redefine a posição para leitura após a escrita. Então, usamos`ToArray()` para converter o fluxo de memória em uma matriz de bytes que contém os dados da planilha.
## Etapa 7: Combine os dados da planilha
 Agora, combinaremos os dados de cada planilha em uma única`workbookData` matriz inicializada anteriormente.
```csharp
    // Combine os dados desta planilha em uma matriz de dados da pasta de trabalho
    byte[] combinedArray = new byte[workbookData.Length + sheetData.Length];
    Array.Copy(workbookData, 0, combinedArray, 0, workbookData.Length);
    Array.Copy(sheetData, 0, combinedArray, workbookData.Length, sheetData.Length);
    workbookData = combinedArray;
}
```
Criamos um novo array que é grande o suficiente para conter dados existentes da pasta de trabalho e novos dados da planilha. Então, copiamos os dados existentes e novos para esse array combinado para uso posterior.
## Etapa 8: salvar todos os dados da pasta de trabalho em um arquivo
 Finalmente, com todos os dados combinados em nosso`workbookData` array, podemos salvar este array em um caminho de arquivo especificado.
```csharp
//Salvar todos os dados da pasta de trabalho em um arquivo
File.WriteAllBytes(dataDir + "out.txt", workbookData);
```
`WriteAllBytes` pega a matriz de bytes combinada e a grava em um arquivo de texto chamado "out.txt" no diretório especificado.
## Conclusão
E aí está! Você converteu com sucesso uma pasta de trabalho do Excel para um formato CSV usando o Aspose.Cells para .NET. Esse processo não é apenas eficiente, mas também permite fácil manipulação de dados do Excel para análise ou relatórios posteriores. Agora você pode automatizar suas tarefas de processamento de dados ou até mesmo integrar essa funcionalidade em aplicativos maiores.
## Perguntas frequentes
### Posso usar delimitadores diferentes para o arquivo CSV?
 Sim, você pode mudar o`opts.Separator` para qualquer caractere que você quiser, como vírgulas ou barras verticais.
### O Aspose.Cells é gratuito?
 Aspose.Cells não é gratuito, mas você pode obter uma avaliação gratuita[aqui](https://releases.aspose.com/).
### Em quais tipos de formatos posso salvar além de CSV?
O Aspose.Cells permite salvar em vários formatos, incluindo XLSX, PDF e muito mais.
### Posso processar arquivos grandes do Excel usando o Aspose.Cells?
Sim, o Aspose.Cells foi projetado para lidar com arquivos grandes de forma eficiente, mas o desempenho pode depender dos recursos do sistema.
### Onde posso encontrar documentação mais detalhada?
Você pode encontrar documentação abrangente e exemplos em seus[site de referência](https://reference.aspose.com/cells/net/).