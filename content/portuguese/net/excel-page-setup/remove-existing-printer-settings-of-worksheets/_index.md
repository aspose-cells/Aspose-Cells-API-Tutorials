---
title: Remover configurações de impressora existentes de planilhas
linktitle: Remover configurações de impressora existentes de planilhas
second_title: Referência da API Aspose.Cells para .NET
description: Aprenda como remover configurações de impressora existentes de planilhas do Excel com Aspose.Cells for .NET.
type: docs
weight: 80
url: /pt/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
Neste tutorial, orientaremos você passo a passo sobre como remover configurações de impressora existentes de planilhas no Excel usando Aspose.Cells for .NET. Usaremos o código-fonte C# para ilustrar o processo.

## Passo 1: Configurando o ambiente

Certifique-se de ter o Aspose.Cells for .NET instalado em sua máquina. Crie também um novo projeto em seu ambiente de desenvolvimento preferido.

## Etapa 2: importe as bibliotecas necessárias

Em seu arquivo de código, importe as bibliotecas necessárias para trabalhar com Aspose.Cells. Aqui está o código correspondente:

```csharp
using Aspose.Cells;
```

## Etapa 3: definir diretórios de origem e saída

Defina os diretórios de origem e de saída onde o arquivo Excel original está localizado e onde você deseja salvar o arquivo modificado, respectivamente. Use o seguinte código:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Certifique-se de especificar caminhos de diretório completos.

## Etapa 4: Carregando o arquivo Excel de origem

Carregue o arquivo Excel de origem usando o seguinte código:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Isso carregará o arquivo Excel especificado no objeto Workbook.

## Etapa 5: navegue nas planilhas

Itere todas as planilhas da pasta de trabalho usando um loop. Use o seguinte código:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // O restante do código será adicionado na próxima etapa.
}
```

## Etapa 6: excluir configurações de impressora existentes

Verifique se existem configurações de impressora para cada planilha e exclua-as se necessário. Use o seguinte código:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Etapa 7: salvando a pasta de trabalho modificada

Salve a pasta de trabalho modificada usando o seguinte código:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Isso salvará a pasta de trabalho modificada no diretório de saída especificado.

### Exemplo de código-fonte para remover configurações de impressora existentes de planilhas usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
//Diretório de saída
string outputDir = RunExamples.Get_OutputDirectory();
//Carregar arquivo Excel de origem
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Obtenha a contagem de folhas da pasta de trabalho
int sheetCount = wb.Worksheets.Count;
//Iterar todas as planilhas
for (int i = 0; i < sheetCount; i++)
{
    //Acesse a i-ésima planilha
    Worksheet ws = wb.Worksheets[i];
    //Acessar a configuração da página da planilha
    PageSetup ps = ws.PageSetup;
    //Verifique se existem configurações de impressora para esta planilha
    if (ps.PrinterSettings != null)
    {
        //Imprima a seguinte mensagem
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Imprima o nome da folha e seu tamanho de papel
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Remova as configurações da impressora definindo-as como nulas
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//se
}//para
//Salve a pasta de trabalho
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Conclusão

Agora você aprendeu como remover configurações de impressora existentes de planilhas no Excel usando Aspose.Cells for .NET. Este tutorial orientou você em todas as etapas do processo, desde a configuração do ambiente até a navegação pelas planilhas e a limpeza das configurações da impressora. Agora você pode usar esse conhecimento para gerenciar as configurações da impressora em seus arquivos Excel.

### Perguntas frequentes

#### P1: Como posso saber se uma planilha possui configurações de impressora existentes?

 A1: Você pode verificar se existem configurações de impressora para uma planilha acessando o`PrinterSettings` propriedade do`PageSetup` objeto. Se o valor não for nulo, significa que existem configurações de impressora existentes.

#### P2: Posso excluir as configurações da impressora apenas para uma planilha específica?

 A2: Sim, você pode usar a mesma abordagem para remover as configurações da impressora de uma planilha específica acessando o arquivo dessa planilha.`PageSetup` objeto.

#### P3: Este método também remove outras configurações de layout?

A3: Não, este método exclui apenas as configurações da impressora. Outras configurações de layout, como margens, orientação do papel, etc., permanecem inalteradas.

#### P4: Este método funciona para todos os formatos de arquivo Excel, como .xls e .xlsx?

A4: Sim, este método funciona para todos os formatos de arquivo Excel suportados pelo Aspose.Cells, incluindo .xls e .xlsx.

#### P5: As alterações feitas nas configurações da impressora são permanentes no arquivo Excel editado?

R5: Sim, as alterações nas configurações da impressora são salvas permanentemente no arquivo Excel editado.