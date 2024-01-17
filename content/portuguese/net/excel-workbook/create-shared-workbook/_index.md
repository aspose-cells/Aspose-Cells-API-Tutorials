---
title: Criar pasta de trabalho compartilhada
linktitle: Criar pasta de trabalho compartilhada
second_title: Referência da API Aspose.Cells para .NET
description: Crie uma pasta de trabalho compartilhada do Excel com Aspose.Cells for .NET para permitir a colaboração de dados simultânea.
type: docs
weight: 70
url: /pt/net/excel-workbook/create-shared-workbook/
---
Neste tutorial, orientaremos você no código-fonte C# fornecido que permitirá criar uma pasta de trabalho compartilhada usando Aspose.Cells for .NET. Siga as etapas abaixo para realizar esta operação.

## Etapa 1: definir o diretório de saída

```csharp
// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

Nesta primeira etapa, definimos o diretório de saída onde a pasta de trabalho compartilhada será salva.

## Etapa 2: criar um objeto de pasta de trabalho

```csharp
// Crie um objeto Pasta de trabalho
Workbook wb = new Workbook();
```

Estamos criando um novo objeto Workbook que representará nossa pasta de trabalho do Excel.

## Etapa 3: ativar o compartilhamento da pasta de trabalho

```csharp
// Compartilhe a pasta de trabalho
wb.Settings.Shared = true;
```

 Ativamos o recurso de compartilhamento da pasta de trabalho definindo a opção`Shared` propriedade do objeto Workbook para`true`.

## Etapa 4: salve a pasta de trabalho compartilhada

```csharp
// Salve a pasta de trabalho compartilhada
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
```

Salvamos a pasta de trabalho compartilhada especificando o caminho e o nome do arquivo de saída.

### Exemplo de código-fonte para criar pasta de trabalho compartilhada usando Aspose.Cells for .NET 
```csharp
//Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
//Criar objeto Pasta de Trabalho
Workbook wb = new Workbook();
//Compartilhe a pasta de trabalho
wb.Settings.Shared = true;
//Salvar a pasta de trabalho compartilhada
wb.Save(outputDir + "outputSharedWorkbook.xlsx");
Console.WriteLine("CreateSharedWorkbook executed successfully.\r\n");
```

## Conclusão

Parabéns! Você aprendeu como criar uma pasta de trabalho compartilhada usando Aspose.Cells for .NET. A pasta de trabalho compartilhada pode ser usada por vários usuários simultaneamente para colaborar nos dados. Experimente seus próprios dados e explore ainda mais os recursos do Aspose.Cells para criar pastas de trabalho do Excel poderosas e personalizadas.

### Perguntas frequentes

#### P: O que é uma pasta de trabalho compartilhada?

R: Uma pasta de trabalho compartilhada é uma pasta de trabalho do Excel que pode ser usada simultaneamente por vários usuários para colaborar nos dados. Cada usuário pode fazer alterações na pasta de trabalho e outros usuários verão as atualizações em tempo real.

#### P: Como habilitar o compartilhamento de uma pasta de trabalho no Aspose.Cells for .NET?

 R: Para habilitar o compartilhamento de uma pasta de trabalho no Aspose.Cells for .NET, você deve definir o`Shared` propriedade do objeto Workbook para`true`. Isso permitirá que os usuários trabalhem na pasta de trabalho simultaneamente.

#### P: Posso restringir as permissões de usuário em uma pasta de trabalho compartilhada?

R: Sim, você pode restringir as permissões do usuário em uma pasta de trabalho compartilhada usando os recursos de segurança do Excel. Você pode definir permissões específicas para cada usuário, como capacidade de edição, somente leitura, etc.

#### P: Como posso compartilhar a pasta de trabalho com outros usuários?

R: Depois de criar a pasta de trabalho compartilhada, você poderá compartilhá-la com outros usuários enviando-lhes o arquivo Excel. Outros usuários poderão abrir o arquivo e trabalhar nele simultaneamente.

#### P: Todos os recursos do Excel são suportados em uma pasta de trabalho compartilhada?

R: A maioria dos recursos do Excel tem suporte em uma pasta de trabalho compartilhada. No entanto, alguns recursos avançados, como macros e suplementos, podem ter limitações ou restrições quando usados em uma pasta de trabalho compartilhada.