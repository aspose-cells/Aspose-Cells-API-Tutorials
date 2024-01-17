---
title: Definir fator de escala do Excel
linktitle: Definir fator de escala do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda a manipular facilmente arquivos Excel e personalizar o fator de escala usando Aspose.Cells for .NET.
type: docs
weight: 180
url: /pt/net/excel-page-setup/set-excel-scaling-factor/
---
Neste guia, orientaremos você sobre como definir o fator de escala em uma planilha do Excel usando Aspose.Cells for .NET. Siga as etapas abaixo para realizar esta tarefa.

## Passo 1: Configurando o ambiente

Certifique-se de ter configurado seu ambiente de desenvolvimento e instalado o Aspose.Cells for .NET. Você pode baixar a versão mais recente da biblioteca no site oficial do Aspose.

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

## Passo 5: Acesso à primeira planilha

Navegue até a primeira planilha da pasta de trabalho do Excel usando o seguinte código:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Etapa 6: definir o fator de escala

Defina o fator de escala usando o seguinte código:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Aqui definimos o fator de escala para 100, o que significa que a planilha será exibida com 100% do tamanho normal quando impressa.

## Etapa 7: Salvando a pasta de trabalho do Excel

 Para salvar a pasta de trabalho do Excel com o fator de escala definido, use o`Save` método do objeto Workbook:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Isso salvará a pasta de trabalho do Excel com o nome de arquivo "ScalingFactor_out.xls" no diretório especificado.

### Exemplo de código-fonte para definir fator de escala do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Configurando o fator de escala para 100
worksheet.PageSetup.Zoom = 100;
// Salve a pasta de trabalho.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Conclusão

Parabéns! Você aprendeu como definir o fator de escala em uma planilha do Excel usando Aspose.Cells for .NET. O fator de escala permite ajustar o tamanho da planilha durante a impressão para uma exibição ideal.

### Perguntas frequentes

#### 1. Como definir o fator de escala na planilha Excel com Aspose.Cells for .NET?

 Use o`Zoom` propriedade do`PageSetup`objeto para definir o fator de escala. Por exemplo,`worksheet.PageSetup.Zoom = 100;` definirá o fator de escala para 100%.

#### 2. Posso personalizar o fator de escala de acordo com minhas necessidades?

 Sim, você pode ajustar o fator de escala alterando o valor atribuído ao`Zoom` propriedade. Por exemplo,`worksheet.PageSetup.Zoom = 75;` definirá o fator de escala para 75%.

#### 3. É possível salvar a pasta de trabalho do Excel com o fator de escala definido?

 Sim, você pode usar o`Save` método do`Workbook` objeto para salvar a pasta de trabalho do Excel com o fator de escala definido.