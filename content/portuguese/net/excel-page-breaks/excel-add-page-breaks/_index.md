---
title: Excel Adicionar quebras de página
linktitle: Excel Adicionar quebras de página
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como adicionar quebras de página no Excel com Aspose.Cells for .NET. Tutorial passo a passo para gerar relatórios bem estruturados.
type: docs
weight: 10
url: /pt/net/excel-page-breaks/excel-add-page-breaks/
---
Adicionar quebras de página em um arquivo Excel é um recurso essencial ao criar relatórios ou documentos grandes. Neste tutorial, exploraremos como adicionar quebras de página em um arquivo Excel usando a biblioteca Aspose.Cells para .NET. Iremos guiá-lo passo a passo para entender e implementar o código-fonte C# fornecido.

## Passo 1: Preparando o ambiente

 Antes de começar, certifique-se de ter o Aspose.Cells for .NET instalado em sua máquina. Você pode baixar a biblioteca do[Aspose Lançamentos](https://releases.aspose.com/cells/net) instale-o seguindo as instruções fornecidas.

Assim que a instalação for concluída, crie um novo projeto C# em seu ambiente de desenvolvimento integrado (IDE) preferido e importe a biblioteca Aspose.Cells para .NET.

## Etapa 2: configurar o caminho do diretório do documento

 No código-fonte fornecido, você precisa especificar o caminho do diretório onde deseja salvar o arquivo Excel gerado. Modifique o`dataDir` variável substituindo "SEU DIRETÓRIO DE DOCUMENTOS" pelo caminho absoluto do diretório em sua máquina.

```csharp
// caminho para o diretório de documentos.
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
```

## Etapa 3: Criando um objeto de pasta de trabalho

Para começar, precisamos criar um objeto Workbook que represente nosso arquivo Excel. Isso pode ser conseguido usando a classe Workbook fornecida por Aspose.Cells.

```csharp
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
```

## Etapa 4: adicionar uma quebra de página horizontal

Agora vamos adicionar uma quebra de página horizontal à nossa planilha do Excel. No código de exemplo, adicionamos uma quebra de página horizontal à célula “Y30” da primeira planilha.

```csharp
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
```

## Etapa 5: adicionar uma quebra de página vertical

Da mesma forma, podemos adicionar uma quebra de página vertical usando o`VerticalPageBreaks.Add()` método. Em nosso exemplo, estamos adicionando uma quebra de página vertical à célula “Y30” da primeira planilha.

```csharp
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
```

## Etapa 6: Salvando o arquivo Excel

 Agora que adicionamos as quebras de página, precisamos salvar o arquivo Excel final. Use o`Save()` método para especificar o caminho completo do arquivo de saída.

```csharp
// Salve o arquivo Excel.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```
### Exemplo de código-fonte para Excel Adicionar quebras de página usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Adicione uma quebra de página na célula Y30
workbook.Worksheets[0].HorizontalPageBreaks.Add("Y30");
workbook.Worksheets[0].VerticalPageBreaks.Add("Y30");
// Salve o arquivo Excel.
workbook.Save(dataDir + "AddingPageBreaks_out.xls");
```

## Conclusão

Neste tutorial, aprendemos como adicionar quebras de

  página em um arquivo Excel usando Aspose.Cells for .NET. Seguindo as etapas fornecidas, você poderá inserir facilmente quebras de página horizontais e verticais em seus arquivos Excel gerados dinamicamente. Sinta-se à vontade para experimentar mais com a biblioteca Aspose.Cells para descobrir outros recursos poderosos que ela oferece.

### Perguntas frequentes

#### P: O Aspose.Cells for .NET é uma biblioteca gratuita?

R: Aspose.Cells for .NET é uma biblioteca comercial, mas oferece uma versão de teste gratuita que você pode usar para avaliar sua funcionalidade.

#### P: Posso adicionar várias quebras de página em um arquivo Excel?

R: Sim, você pode adicionar quantas quebras de página forem necessárias em diferentes partes da planilha.

#### P: É possível remover uma quebra de página adicionada anteriormente?

R: Sim, Aspose.Cells permite remover quebras de página existentes usando os métodos apropriados do objeto Worksheet.

#### P: Este método também funciona com outros formatos de arquivo Excel, como XLSX ou XLSM?

R: Sim, o método descrito neste tutorial funciona com vários formatos de arquivo Excel suportados pelo Aspose.Cells.

#### P: Posso personalizar a aparência das quebras de página no Excel?

R: Sim, Aspose.Cells oferece uma variedade de recursos para personalizar quebras de página, como estilo, cor e dimensões.
