---
title: Proteger ou desproteger com senha a pasta de trabalho compartilhada
linktitle: Proteger ou desproteger com senha a pasta de trabalho compartilhada
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como proteger ou desproteger com senha uma pasta de trabalho compartilhada usando Aspose.Cells for .NET.
type: docs
weight: 120
url: /pt/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Proteger uma pasta de trabalho compartilhada com uma senha é importante para garantir a privacidade dos dados. Com Aspose.Cells for .NET, você pode proteger ou desproteger facilmente uma pasta de trabalho compartilhada usando senhas. Siga as etapas abaixo para obter os resultados desejados:

## Etapa 1: especifique o diretório de saída

Primeiro, você precisa especificar o diretório de saída onde o arquivo Excel protegido será salvo. Veja como fazer isso usando Aspose.Cells:

```csharp
// Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
```

## Etapa 2: crie um arquivo Excel vazio

Em seguida, você pode criar um arquivo Excel vazio ao qual deseja aplicar proteção ou desproteção. Aqui está um exemplo de código:

```csharp
// Crie uma pasta de trabalho vazia do Excel
Workbook wb = new Workbook();
```

## Etapa 3: proteger ou desproteger a pasta de trabalho compartilhada

Depois de criar a pasta de trabalho, você poderá proteger ou desproteger a pasta de trabalho compartilhada especificando a senha apropriada. Veja como:

```csharp
// Proteja a pasta de trabalho compartilhada com uma senha
wb.ProtectSharedWorkbook("1234");

// Remova o comentário desta linha para desproteger a pasta de trabalho compartilhada
// wb.UnprotectSharedWorkbook("1234");
```

## Etapa 4: salve o arquivo Excel de saída

Depois de aplicar proteção ou desproteção, você pode salvar o arquivo Excel protegido no diretório de saída especificado. Veja como fazer isso:

```csharp
// Salve o arquivo Excel de saída
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Exemplo de código-fonte para pasta de trabalho compartilhada protegida ou desprotegida por senha usando Aspose.Cells for .NET 
```csharp
//Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
//Crie um arquivo Excel vazio
Workbook wb = new Workbook();
//Proteja a pasta de trabalho compartilhada com senha
wb.ProtectSharedWorkbook("1234");
//Remova o comentário desta linha para desproteger a pasta de trabalho compartilhada
//wb.UnprotectSharedWorkbook("1234");
//Salve o arquivo Excel de saída
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Conclusão

Proteger ou desproteger uma pasta de trabalho compartilhada com senha é essencial para garantir a segurança dos dados. Com Aspose.Cells for .NET você pode facilmente adicionar essa funcionalidade aos seus arquivos Excel. Seguindo as etapas deste guia, você pode proteger ou desproteger com eficácia suas pastas de trabalho compartilhadas usando senhas. Experimente seus próprios arquivos Excel e certifique-se de manter a segurança de seus dados confidenciais.

### Perguntas frequentes

#### P: Que tipos de proteção posso aplicar a uma pasta de trabalho compartilhada com Aspose.Cells?
    
R: Com Aspose.Cells, você pode proteger uma pasta de trabalho compartilhada especificando uma senha para evitar acesso não autorizado, modificação ou exclusão de dados.

#### P: Posso proteger uma pasta de trabalho compartilhada sem especificar uma senha?
    
R: Sim, você pode proteger uma pasta de trabalho compartilhada sem especificar uma senha. Porém, é recomendado usar uma senha forte para melhor segurança.

#### P: Como posso desproteger uma pasta de trabalho compartilhada com Aspose.Cells?
    
R: Para desproteger uma pasta de trabalho compartilhada, você deve especificar a mesma senha usada ao proteger a pasta de trabalho. Isso permite que a proteção seja removida e os dados sejam acessados livremente.

#### P: A proteção de uma pasta de trabalho compartilhada afeta os recursos e as fórmulas da pasta de trabalho?
    
R: Quando você protege uma pasta de trabalho compartilhada, os usuários ainda podem acessar recursos e fórmulas presentes na pasta de trabalho. A proteção afeta apenas alterações estruturais na pasta de trabalho.