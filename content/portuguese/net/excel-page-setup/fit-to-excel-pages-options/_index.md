---
title: Opções de ajustar às páginas do Excel
linktitle: Opções de ajustar às páginas do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como ajustar páginas automaticamente em uma planilha do Excel com Aspose.Cells for .NET.
type: docs
weight: 30
url: /pt/net/excel-page-setup/fit-to-excel-pages-options/
---
Neste artigo, iremos guiá-lo passo a passo para explicar o seguinte código-fonte C#: Opções de ajuste às páginas do Excel usando Aspose.Cells for .NET. Usaremos a biblioteca Aspose.Cells para .NET para realizar esta operação. Siga as etapas abaixo para configurar o ajuste às páginas no Excel.

## Etapa 1: Criando uma pasta de trabalho
O primeiro passo é criar uma pasta de trabalho. Vamos instanciar um objeto Workbook. Aqui está o código para criar uma pasta de trabalho:

```csharp
// O caminho para o diretório de documentos
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Instanciar um objeto Workbook
Workbook workbook = new Workbook();
```

## Passo 2: Acessando a planilha
Agora que criamos a pasta de trabalho, precisamos navegar até a primeira planilha. Usaremos o índice 0 para acessar a primeira planilha. Aqui está o código para acessá-lo:

```csharp
// Acesso à primeira planilha da pasta de trabalho
Worksheet worksheet = workbook.Worksheets[0];
```

## Etapa 3: definir o ajuste às páginas
 Nesta etapa iremos configurar o ajuste nas páginas da planilha. Usaremos o`FitToPagesTall` e`FitToPagesWide` propriedades do`PageSetup` objeto para especificar o número desejado de páginas para a altura e largura da planilha. Aqui está o código para isso:

```csharp
// Configure o número de páginas para a altura da planilha
worksheet.PageSetup.FitToPagesTall = 1;

// Configure o número de páginas para a largura da planilha
worksheet.PageSetup.FitToPagesWide = 1;
```

## Etapa 4: salvando a pasta de trabalho
 Agora que configuramos o ajuste às páginas, podemos salvar a pasta de trabalho. Usaremos o`Save` método do objeto Workbook para isso. Aqui está o código para salvar a pasta de trabalho:

```csharp
// Salve a pasta de trabalho
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Exemplo de código-fonte para opções de ajuste de páginas do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Instanciando um objeto Workbook
Workbook workbook = new Workbook();
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = workbook.Worksheets[0];
// Definir o número de páginas que o comprimento da planilha será estendido
worksheet.PageSetup.FitToPagesTall = 1;
//Definir o número de páginas que a largura da planilha será estendida
worksheet.PageSetup.FitToPagesWide = 1;
// Salve a pasta de trabalho.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Conclusão
Neste artigo, aprendemos como configurar o ajuste às páginas no Excel usando Aspose.Cells for .NET. Passamos pelas seguintes etapas: criação da apostila, acesso à planilha, configuração do ajuste às páginas e salvamento da apostila. Agora você pode usar esse conhecimento para ajustar suas planilhas às páginas desejadas.

### Perguntas frequentes

#### P: Como posso instalar o Aspose.Cells for .NET?

R: Para instalar o Aspose.Cells for .NET, você pode usar o gerenciador de pacotes NuGet no Visual Studio. Encontre o pacote "Aspose.Cells" e instale-o em seu projeto.

#### P: Posso ajustar a altura e a largura das páginas?

 R: Sim, você pode ajustar a altura e a largura da planilha usando o`FitToPagesTall` e`FitToPagesWide` propriedades. Você pode especificar o número desejado de páginas para cada dimensão.

#### P: Como posso personalizar as opções Ajustar às páginas?

R: Além de especificar o número de páginas, você também pode personalizar outras opções de ajuste às páginas, como escala da planilha, orientação do papel, margens e muito mais. Utilize as propriedades disponíveis no`PageSetup` objeto para isso.

#### P: Posso usar o Aspose.Cells for .NET para processar pastas de trabalho existentes?

R: Sim, você pode usar Aspose.Cells for .NET para abrir e editar pastas de trabalho existentes. Você pode acessar planilhas, células, fórmulas, estilos e outros itens da pasta de trabalho para realizar diversas operações.