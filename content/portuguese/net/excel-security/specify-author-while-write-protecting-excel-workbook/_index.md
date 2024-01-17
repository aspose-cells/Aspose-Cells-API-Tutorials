---
title: Especifique o autor ao proteger a pasta de trabalho do Excel contra gravação
linktitle: Especifique o autor ao proteger a pasta de trabalho do Excel contra gravação
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como proteger e personalizar suas pastas de trabalho do Excel usando Aspose.Cells for .NET. Tutorial passo a passo em C#.
type: docs
weight: 30
url: /pt/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Neste tutorial, mostraremos como especificar o autor ao proteger uma pasta de trabalho do Excel contra gravação usando a biblioteca Aspose.Cells para .NET.

## Passo 1: Preparando o ambiente

Antes de começar, certifique-se de ter o Aspose.Cells for .NET instalado em sua máquina. Baixe a biblioteca do site oficial do Aspose e siga as instruções de instalação fornecidas.

## Etapa 2: configurar diretórios de origem e saída

No código-fonte fornecido, você deve especificar os diretórios de origem e de saída. Modifique o`sourceDir` e`outputDir` variáveis substituindo "SEU DIRETÓRIO DE ORIGEM" e "SEU DIRETÓRIO DE SAÍDA" pelos respectivos caminhos absolutos em sua máquina.

```csharp
// Diretório de origem
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Diretório de saída
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Etapa 3: Criando uma pasta de trabalho vazia do Excel

Para começar, criamos um objeto Workbook que representa uma pasta de trabalho vazia do Excel.

```csharp
// Crie uma pasta de trabalho vazia.
Workbook wb = new Workbook();
```

## Passo 4: Proteção contra gravação com senha

 A seguir, especificamos uma senha para proteger a pasta de trabalho do Excel contra gravação usando o`WriteProtection.Password` propriedade do objeto Workbook.

```csharp
// Escreva proteger pasta de trabalho com senha.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Etapa 5: especificação do autor

 Agora especificamos o autor da pasta de trabalho do Excel usando o`WriteProtection.Author` propriedade do objeto Workbook.

```csharp
// Especifique o autor ao proteger a pasta de trabalho contra gravação.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Etapa 6: Backup da pasta de trabalho protegida do Excel

 Depois que a proteção contra gravação e o autor forem especificados, podemos salvar a pasta de trabalho do Excel no formato XLSX usando o`Save()` método.

```csharp
// Salve a pasta de trabalho no formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Exemplo de código-fonte para Especificar autor durante a proteção contra gravação da pasta de trabalho do Excel usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = "YOUR SOURCE DIRECTORY";

//Diretório de saída
string outputDir = "YOUR OUTPUT DIRECTORY";

// Crie uma pasta de trabalho vazia.
Workbook wb = new Workbook();

// Escreva proteger pasta de trabalho com senha.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Especifique o autor ao proteger a pasta de trabalho contra gravação.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Salve a pasta de trabalho no formato XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Conclusão

Parabéns! Agora você aprendeu como especificar o autor ao proteger uma pasta de trabalho do Excel contra gravação com Aspose.Cells for .NET. Você pode aplicar essas etapas aos seus próprios projetos para proteger e personalizar suas pastas de trabalho do Excel.

Sinta-se à vontade para explorar ainda mais os recursos do Aspose.Cells for .NET para operações mais avançadas em arquivos Excel.

## Perguntas frequentes

#### P: Posso proteger uma pasta de trabalho do Excel contra gravação sem especificar uma senha?

 R: Sim, você pode usar o objeto Workbook`WriteProtect()` método sem especificar uma senha para proteger contra gravação uma pasta de trabalho do Excel. Isso restringirá as alterações na pasta de trabalho sem exigir uma senha.

#### P: Como removo a proteção contra gravação de uma pasta de trabalho do Excel?

 R: Para remover a proteção contra gravação de uma pasta de trabalho do Excel, você pode usar o`Unprotect()` método do objeto Worksheet ou o método`RemoveWriteProtection()` método do objeto Workbook, dependendo do seu caso de uso específico. .

#### P: Esqueci a senha para proteger minha pasta de trabalho do Excel. O que posso fazer ?

R: Se você esqueceu a senha para proteger sua pasta de trabalho do Excel, não poderá removê-la diretamente. No entanto, você pode tentar usar ferramentas especializadas de terceiros que fornecem recursos de recuperação de senha para arquivos Excel protegidos.

#### P: É possível especificar vários autores ao proteger uma pasta de trabalho do Excel contra gravação?

R: Não, a biblioteca Aspose.Cells for .NET permite especificar um único autor ao proteger uma pasta de trabalho do Excel contra gravação. Se quiser especificar vários autores, você precisará considerar soluções personalizadas manipulando diretamente o arquivo Excel.