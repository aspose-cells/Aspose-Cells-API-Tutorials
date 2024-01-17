---
title: Configurações de proteção avançada para planilha do Excel
linktitle: Configurações de proteção avançada para planilha do Excel
second_title: Referência da API Aspose.Cells para .NET
description: Proteja seus arquivos Excel definindo configurações de proteção avançadas com Aspose.Cells for .NET.
type: docs
weight: 10
url: /pt/net/excel-security/advanced-protection-settings-for-excel-worksheet/
---
Neste tutorial, orientaremos você nas etapas para definir configurações de proteção avançadas para uma planilha do Excel usando a biblioteca Aspose.Cells para .NET. Siga as instruções abaixo para concluir esta tarefa.

## Etapa 1: Preparação

Certifique-se de ter instalado o Aspose.Cells for .NET e criado um projeto C# em seu ambiente de desenvolvimento integrado (IDE) preferido.

## Etapa 2: definir o caminho do diretório do documento

 Declarar um`dataDir` variável e inicialize-a com o caminho para o diretório de documentos. Por exemplo :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Certifique-se de substituir`"YOUR_DOCUMENTS_DIRECTORY"` com o caminho real para o seu diretório.

## Etapa 3: crie um fluxo de arquivo para abrir o arquivo Excel

 Criar uma`FileStream` objeto que contém o arquivo Excel a ser aberto:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Certifique-se de ter o arquivo Excel`book1.xls` no diretório de documentos ou especifique o nome e o local corretos do arquivo.

## Etapa 4: instanciar um objeto Workbook e abrir o arquivo Excel

 Use o`Workbook`class de Aspose.Cells para instanciar um objeto Workbook e abrir o arquivo Excel especificado por meio do fluxo de arquivos:

```csharp
Workbook excel = new Workbook(fstream);
```

## Passo 5: Acesse a primeira planilha

Navegue até a primeira planilha do arquivo Excel:

```csharp
Worksheet worksheet = excel.Worksheets[0];
```

## Etapa 6: definir configurações de proteção de planilha

Use as propriedades do objeto Planilha para definir as configurações de proteção da planilha conforme necessário. Por exemplo :

```csharp
worksheet.Protection.AllowDeletingColumn = false;
worksheet.Protection.AllowDeletingRow = false;
worksheet.Protection.AllowEditingContent = false;
worksheet.Protection.AllowEditingObject = false;
// ... Defina outras configurações de proteção conforme necessário...
```

## Etapa 7: salve o arquivo Excel modificado

 Salve o arquivo Excel modificado usando o`Save` método do objeto Workbook:

```csharp
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

Certifique-se de especificar o caminho e o nome de arquivo desejados para o arquivo de saída.

## Etapa 8: feche o fluxo de arquivos

Depois de salvo, feche o fluxo de arquivos para liberar todos os recursos associados:

```csharp
fstream.Close();
```
	
### Exemplo de código-fonte para configurações de proteção avançada para planilha do Excel usando Aspose.Cells for .NET 
```csharp
// caminho para o diretório de documentos.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Criando um fluxo de arquivos contendo o arquivo Excel a ser aberto
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Instanciando um objeto Workbook
// Abrindo o arquivo Excel por meio do fluxo de arquivos
Workbook excel = new Workbook(fstream);
// Acessando a primeira planilha do arquivo Excel
Worksheet worksheet = excel.Worksheets[0];
// Restringindo usuários para excluir colunas da planilha
worksheet.Protection.AllowDeletingColumn = false;
// Restringindo usuários para excluir linha da planilha
worksheet.Protection.AllowDeletingRow = false;
// Restringindo usuários para editar o conteúdo da planilha
worksheet.Protection.AllowEditingContent = false;
// Restringindo usuários para editar objetos da planilha
worksheet.Protection.AllowEditingObject = false;
// Restringindo usuários para editar cenários da planilha
worksheet.Protection.AllowEditingScenario = false;
//Restringindo usuários para filtrar
worksheet.Protection.AllowFiltering = false;
// Permitindo que os usuários formatem células da planilha
worksheet.Protection.AllowFormattingCell = true;
// Permitir que os usuários formatem linhas da planilha
worksheet.Protection.AllowFormattingRow = true;
// Permitindo que os usuários insiram colunas na planilha
worksheet.Protection.AllowFormattingColumn = true;
// Permitir que os usuários insiram hiperlinks na planilha
worksheet.Protection.AllowInsertingHyperlink = true;
// Permitindo que os usuários insiram linhas na planilha
worksheet.Protection.AllowInsertingRow = true;
// Permitindo que os usuários selecionem células bloqueadas da planilha
worksheet.Protection.AllowSelectingLockedCell = true;
// Permitindo que os usuários selecionem células desbloqueadas da planilha
worksheet.Protection.AllowSelectingUnlockedCell = true;
// Permitir que os usuários classifiquem
worksheet.Protection.AllowSorting = true;
// Permitir que os usuários usem tabelas dinâmicas na planilha
worksheet.Protection.AllowUsingPivotTable = true;
// Salvando o arquivo Excel modificado
excel.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
// Fechando o fluxo de arquivos para liberar todos os recursos
fstream.Close();
```

## Conclusão

Parabéns! Agora você aprendeu como definir configurações de proteção avançadas para uma planilha do Excel usando Aspose.Cells for .NET. Use esse conhecimento para proteger seus arquivos Excel e restringir as ações do usuário.

### Perguntas frequentes

#### P: Como posso criar um novo projeto C# em meu IDE?

R: As etapas para criar um novo projeto C# podem variar dependendo do IDE que você está usando. Consulte a documentação do seu IDE para obter instruções detalhadas.

#### P: É possível definir configurações de proteção personalizadas diferentes das mencionadas no tutorial?

R: Sim, Aspose.Cells oferece uma ampla gama de configurações de proteção que você pode personalizar de acordo com suas necessidades específicas. Consulte a documentação do Aspose.Cells para obter mais detalhes.

#### P: Qual é o formato de arquivo usado para salvar o arquivo Excel modificado no código de exemplo?

R: No código de exemplo, o arquivo Excel modificado é salvo no formato Excel 97-2003 (.xls). Você pode escolher outros formatos suportados pelo Aspose.Cells, se necessário.

#### P: Como posso acessar outras planilhas no arquivo Excel?

 R: Você pode acessar outras planilhas usando o índice ou o nome da planilha, por exemplo:`Worksheet worksheet = excel.Worksheets[1];` ou`Worksheet worksheet = excel.Worksheets[" SheetName"];`.