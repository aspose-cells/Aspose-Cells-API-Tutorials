---
title: Отрегулируйте уровень сжатия
linktitle: Отрегулируйте уровень сжатия
second_title: Справочник по Aspose.Cells для .NET API
description: Уменьшите размер своих книг Excel, настроив уровень сжатия с помощью Aspose.Cells для .NET.
type: docs
weight: 50
url: /ru/net/excel-workbook/adjust-compression-level/
---
В этом пошаговом руководстве мы объясним предоставленный исходный код C#, который позволит вам настроить уровень сжатия с помощью Aspose.Cells для .NET. Выполните следующие действия, чтобы настроить уровень сжатия в книге Excel.

## Шаг 1: Установите исходный и выходной каталоги

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
// Выходной каталог
string outDir = RunExamples.Get_OutputDirectory();
```

На этом первом шаге мы определяем исходные и выходные каталоги для файлов Excel.

## Шаг 2. Загрузите книгу Excel

```csharp
//Загрузите книгу Excel
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

 Мы загружаем книгу Excel из указанного файла с помощью`Workbook` класс из Aspose.Cells.

## Шаг 3. Установите параметры резервного копирования

```csharp
// Определить параметры резервного копирования
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Мы создаем экземпляр`XlsbSaveOptions` класс, чтобы установить параметры сохранения.

## Шаг 4: Настройте уровень сжатия (уровень 1)

```csharp
// Отрегулируйте уровень сжатия (Уровень 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Мы регулируем уровень сжатия, установив`CompressionType` к`Level1`. Затем мы сохраняем книгу Excel с указанным параметром сжатия.

## Шаг 5: Отрегулируйте уровень сжатия (уровень 6)

```csharp
// Отрегулируйте уровень сжатия (уровень 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Мы повторяем процесс, чтобы отрегулировать уровень сжатия до`Level6` и сохраните книгу Excel с этой опцией.

## Шаг 6: Отрегулируйте уровень сжатия (уровень 9)

```csharp
// Отрегулируйте уровень сжатия (уровень 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Мы повторяем процесс в последний раз, чтобы отрегулировать уровень сжатия до`Level9` и сохраните книгу Excel с этой опцией.

### Пример исходного кода для настройки уровня сжатия с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
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

## Заключение

Поздравляем! Вы узнали, как настроить уровень сжатия в книге Excel с помощью Aspose.Cells для .NET. Поэкспериментируйте с различными уровнями сжатия, чтобы найти тот, который лучше всего соответствует вашим потребностям.

### Часто задаваемые вопросы

#### В: Что такое сжатие в книге Excel?

О: Сжатие в книге Excel — это процесс уменьшения размера файла с помощью алгоритмов сжатия. Это уменьшает требуемый объем памяти и повышает производительность при загрузке файла и управлении им.

#### В: Какие уровни сжатия доступны в Aspose.Cells?

О: В Aspose.Cells вы можете настроить уровень сжатия от 1 до 9. Чем выше уровень сжатия, тем меньше будет размер файла, но это также может увеличить время обработки.

#### Вопрос. Как выбрать правильный уровень сжатия для книги Excel?

A: Выбор уровня сжатия зависит от ваших конкретных потребностей. Если вы хотите максимальное сжатие и время обработки не является проблемой, вы можете перейти на уровень 9. Если вы предпочитаете компромисс между размером файла и временем обработки, вы можете выбрать промежуточный уровень.

#### Вопрос. Влияет ли сжатие на качество данных в книге Excel?

О: Нет, сжатие не влияет на качество данных в книге Excel. Он просто уменьшает размер файла, используя методы сжатия, без изменения самих данных.

#### В: Могу ли я настроить уровень сжатия после сохранения файла Excel?

О: Нет, после того как вы сохраните файл Excel с определенным уровнем сжатия, вы не сможете изменить уровень сжатия позже. Вам нужно будет снова сохранить файл с новым уровнем сжатия, если вы хотите изменить его.