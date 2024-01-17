---
title: Ajustar o nível de compressão
linktitle: Ajustar o nível de compressão
second_title: Referência da API Aspose.Cells para .NET
description: Reduza o tamanho de suas pastas de trabalho do Excel ajustando o nível de compactação com Aspose.Cells for .NET.
type: docs
weight: 50
url: /pt/net/excel-workbook/adjust-compression-level/
---
Neste tutorial passo a passo, explicaremos o código-fonte C# fornecido que permitirá ajustar o nível de compactação usando Aspose.Cells for .NET. Siga as etapas abaixo para ajustar o nível de compactação em sua pasta de trabalho do Excel.

## Etapa 1: definir diretórios de origem e saída

```csharp
// diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
// Diretório de saída
string outDir = RunExamples.Get_OutputDirectory();
```

Nesta primeira etapa, definimos os diretórios de origem e saída dos arquivos Excel.

## Etapa 2: carregar a pasta de trabalho do Excel

```csharp
// Carregar a pasta de trabalho do Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Carregamos a pasta de trabalho do Excel do arquivo especificado usando o`Workbook` classe de Aspose.Cells.

## Etapa 3: definir opções de backup

```csharp
// Definir opções de backup
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Criamos uma instância do`XlsbSaveOptions` class para definir opções de salvamento.

## Etapa 4: ajuste o nível de compactação (Nível 1)

```csharp
// Ajuste o nível de compressão (Nível 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Ajustamos o nível de compressão definindo`CompressionType` para`Level1`. Em seguida, salvamos a pasta de trabalho do Excel com esta opção de compactação especificada.

## Etapa 5: ajuste o nível de compactação (nível 6)

```csharp
// Ajuste o nível de compressão (Nível 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Repetimos o processo para ajustar o nível de compressão para`Level6` e salve a pasta de trabalho do Excel com esta opção.

## Passo 6: Ajustar o nível de compressão (Nível 9)

```csharp
// Ajuste o nível de compressão (Nível 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Repetimos o processo uma última vez para ajustar o nível de compressão para`Level9` e salve a pasta de trabalho do Excel com esta opção.

### Exemplo de código-fonte para ajustar o nível de compactação usando Aspose.Cells for .NET 
```csharp
//Diretório de origem
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Conclusão

Parabéns! Você aprendeu como ajustar o nível de compactação em uma pasta de trabalho do Excel usando Aspose.Cells for .NET. Experimente diferentes níveis de compactação para encontrar aquele que melhor atende às suas necessidades.

### Perguntas frequentes

#### P: O que é compactação em uma pasta de trabalho do Excel?

R: A compactação em uma pasta de trabalho do Excel é um processo de redução do tamanho do arquivo usando algoritmos de compactação. Isso reduz o espaço de armazenamento necessário e melhora o desempenho ao carregar e manipular o arquivo.

#### P: Quais níveis de compactação estão disponíveis com Aspose.Cells?

R: Com Aspose.Cells, você pode ajustar o nível de compactação de 1 a 9. Quanto maior o nível de compactação, menor será o tamanho do arquivo, mas também pode aumentar o tempo de processamento.

#### P: Como escolho o nível de compactação correto para minha pasta de trabalho do Excel?

R: A escolha do nível de compactação depende de suas necessidades específicas. Se você deseja compactação máxima e o tempo de processamento não é um problema, você pode optar pelo nível 9. Se preferir um compromisso entre o tamanho do arquivo e o tempo de processamento, você pode escolher um nível intermediário.

#### P: A compactação afeta a qualidade dos dados na pasta de trabalho do Excel?

R: Não, a compactação não afeta a qualidade dos dados na pasta de trabalho do Excel. Simplesmente reduz o tamanho do arquivo usando técnicas de compactação sem alterar os dados em si.

#### P: Posso ajustar o nível de compactação depois de salvar o arquivo Excel?

R: Não, depois de salvar o arquivo Excel com um nível de compactação específico, você não poderá ajustar o nível de compactação posteriormente. Você precisará salvar o arquivo novamente com o novo nível de compactação se desejar modificá-lo.