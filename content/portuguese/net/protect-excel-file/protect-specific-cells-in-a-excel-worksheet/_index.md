---
title: Proteja células específicas em uma planilha do Excel
linktitle: Proteja células específicas em uma planilha do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como proteger células específicas no Excel com Aspose.Cells for .NET. Tutorial passo a passo em C#.
type: docs
weight: 70
url: /pt/net/protect-excel-file/protect-specific-cells-in-a-excel-worksheet/
---
Neste tutorial, veremos o código-fonte C# que usa a biblioteca Aspose.Cells para proteger células específicas em uma planilha do Excel. Examinaremos cada etapa do código e explicaremos como ele funciona. Siga as instruções cuidadosamente para obter os resultados desejados.

## Etapa 1: Pré-requisitos

Antes de começar, certifique-se de ter instalado a biblioteca Aspose.Cells para .NET. Você pode obtê-lo no site oficial do Aspose. Certifique-se também de ter uma versão recente do Visual Studio ou qualquer outro ambiente de desenvolvimento C#.

## Etapa 2: importar namespaces necessários

Para usar a biblioteca Aspose.Cells, precisamos importar os namespaces necessários para nosso código. Adicione as seguintes linhas ao topo do seu arquivo de origem C#:

```csharp
using Aspose.Cells;
```

## Etapa 3: Criando uma pasta de trabalho do Excel

Nesta etapa, criaremos uma nova pasta de trabalho do Excel. Use o seguinte código para criar uma pasta de trabalho do Excel:

```csharp
// Caminho para o diretório de documentos.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Crie uma nova pasta de trabalho.
Workbook wb = new Workbook();
```

 Certifique-se de substituir`"YOUR_DOCUMENTS_DIR"` com o caminho apropriado para o diretório de documentos.

## Passo 4: Criando uma planilha

Agora que criamos a pasta de trabalho do Excel, vamos criar uma planilha e obter a primeira planilha. Use o seguinte código:

```csharp
// Crie um objeto de planilha e obtenha a primeira planilha.
Worksheet sheet = wb.Worksheets[0];
```

## Etapa 5: definindo o estilo

Nesta etapa, definiremos o estilo a ser aplicado a células específicas. Use o seguinte código:

```csharp
// Definição do objeto de estilo.
Styling styling;
```

## Etapa 6: Loop para desbloquear todas as colunas

Agora iremos percorrer todas as colunas da planilha e desbloqueá-las. Use o seguinte código:

```csharp
// Percorra todas as colunas da planilha e desbloqueie-as.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     sheet.Cells.Columns[(byte)i].ApplyStyle(style);
}
```

## Etapa 7: Bloqueio de células específicas

Nesta etapa, bloquearemos células específicas. Use o seguinte código:

```csharp
//Bloqueando todas as três células... ou seja, A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

## Passo 8: Protegendo a planilha

Por fim, protegeremos a planilha para evitar que células específicas sejam modificadas. Use o seguinte código:

```csharp
// Proteja a planilha.
sheet.Protect(ProtectionType.All);
```

## Etapa 9: Salvando o arquivo Excel

Agora salvaremos o arquivo Excel modificado. Use o seguinte código:

```csharp
// Salve o arquivo Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Certifique-se de especificar o caminho correto para salvar o arquivo Excel modificado.

### Exemplo de código-fonte para proteger células específicas em uma planilha do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Crie um diretório se ainda não estiver presente.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Crie uma nova pasta de trabalho.
Workbook wb = new Workbook();
// Crie um objeto de planilha e obtenha a primeira planilha.
Worksheet sheet = wb.Worksheets[0];
// Defina o objeto de estilo.
Style style;
// Defina o objeto styleflag
StyleFlag styleflag;
// Percorra todas as colunas da planilha e desbloqueie-as.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Bloqueie as três células... ou seja, A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Finalmente, proteja a planilha agora.
sheet.Protect(ProtectionType.All);
// Salve o arquivo Excel.
wb.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```


## Conclusão

Parabéns! Agora você tem código-fonte C# que permite proteger células específicas em uma planilha do Excel usando a biblioteca Aspose.Cells para .NET. Sinta-se à vontade para personalizar o código para atender às suas necessidades específicas.

### FAQs (perguntas frequentes)

#### Este código funciona com versões recentes do Excel?

Sim, este código funciona com versões recentes do Excel, incluindo arquivos no formato Excel 2010 e superior.

#### Posso proteger outras células além de A1, B1 e C1?

Sim, você pode modificar o código para bloquear outras células específicas ajustando as referências das células nas linhas de código correspondentes.

#### Como posso desbloquear células bloqueadas novamente?

 Você pode usar`SetStyle` método com`IsLocked` definido como`false` para desbloquear células.

#### Posso adicionar mais planilhas à pasta de trabalho?

 Sim, você pode adicionar outras planilhas à pasta de trabalho usando o`Worksheets.Add()`método e repita as etapas de proteção de células para cada planilha.

#### Como posso alterar o formato de salvamento do arquivo Excel?

 Você pode alterar o formato de salvamento usando o`SaveFormat` método com o formato desejado, por exemplo`SaveFormat.Xlsx` para Excel 2007 e posterior.