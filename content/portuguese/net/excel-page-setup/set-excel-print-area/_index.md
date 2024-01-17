---
title: Definir área de impressão do Excel
linktitle: Definir área de impressão do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Guia passo a passo para definir a área de impressão do Excel usando Aspose.Cells for .NET. Otimize e personalize facilmente suas pastas de trabalho do Excel.
type: docs
weight: 140
url: /pt/net/excel-page-setup/set-excel-print-area/
---
Usar Aspose.Cells for .NET pode facilitar muito o gerenciamento e manipulação de arquivos Excel em aplicativos .NET. Neste guia, mostraremos como definir a área de impressão de uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Iremos guiá-lo passo a passo através do código-fonte C# fornecido para realizar esta tarefa.

## Passo 1: Configurando o ambiente

Antes de começar, certifique-se de ter configurado seu ambiente de desenvolvimento e instalado o Aspose.Cells for .NET. Você pode baixar a versão mais recente da biblioteca no site oficial do Aspose.

## Etapa 2: importar namespaces necessários

No seu projeto C#, importe os namespaces necessários para trabalhar com Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Etapa 3: definir o caminho para o diretório de documentos

 Declarar um`dataDir` variável para especificar o caminho para o diretório onde deseja salvar o arquivo Excel gerado:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENT_DIRECTORY"` com o caminho correto em seu sistema.

## Etapa 4: Criando um objeto de pasta de trabalho

Instancie um objeto Workbook que representa a pasta de trabalho do Excel que você deseja criar:

```csharp
Workbook workbook = new Workbook();
```

## Etapa 5: Obtendo a referência PageSetup da planilha

Para definir a área de impressão, primeiro precisamos obter a referência do PageSetup da planilha. Use o seguinte código para obter a referência:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Etapa 6: Especificar o intervalo de células da área de impressão

Agora que temos a referência PageSetup, podemos especificar o intervalo de células que compõem a área de impressão. Neste exemplo, definiremos o intervalo de células de A1 a T35 como área de impressão. Use o seguinte código:

```csharp
pageSetup.PrintArea = "A1:T35";
```

Você pode ajustar o intervalo de células de acordo com suas necessidades.

## Etapa 7: Salvando a pasta de trabalho do Excel

 Para salvar a pasta de trabalho do Excel com a área de impressão definida, use o`Save` método do objeto Workbook:

```csharp
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

Isso salvará a pasta de trabalho do Excel com o nome de arquivo "SetPrintArea_out.xls" no diretório especificado.

### Exemplo de código-fonte para definir área de impressão do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Obtendo a referência do PageSetup da planilha
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Especificando o intervalo de células (da célula A1 à célula T35) da área de impressão
pageSetup.PrintArea = "A1:T35";
// Salve a pasta de trabalho.
workbook.Save(dataDir + "SetPrintArea_out.xls");
```

## Conclusão

Parabéns! Agora você aprendeu como definir a área de impressão de uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Esta biblioteca poderosa e fácil de usar torna muito mais fácil trabalhar com arquivos Excel em seus aplicativos .NET. Se você tiver dúvidas adicionais ou tiver alguma dificuldade, sinta-se à vontade para verificar a documentação oficial do Aspose.Cells para obter mais informações e recursos.

### Perguntas frequentes

#### 1. Posso personalizar ainda mais o layout da área de impressão, como orientação e margens?

Sim, você pode acessar outras propriedades do PageSetup, como orientação da página, margens, escala, etc. para personalizar ainda mais o layout da área de impressão.

#### 2. O Aspose.Cells for .NET oferece suporte a outros formatos de arquivo Excel, como XLSX e CSV?

Sim, Aspose.Cells for .NET suporta uma variedade de formatos de arquivo Excel, incluindo XLSX, XLS, CSV, HTML, PDF e muitos mais.

#### 3. O Aspose.Cells for .NET é compatível com todas as versões do .NET Framework?

Aspose.Cells for .NET é compatível com .NET Framework 2.0 ou posterior, incluindo versões 3.5, 4.0, 4.5, 4.6, etc.