---
title: Предварительный просмотр рабочей книги
linktitle: Предварительный просмотр рабочей книги
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как создать предварительный просмотр книги с помощью Aspose.Cells для .NET.
type: docs
weight: 170
url: /ru/net/excel-workbook/workbook-print-preview/
---
Предварительный просмотр книги при печати является важной функцией при работе с файлами Excel с помощью Aspose.Cells для .NET. Вы можете легко создать предварительный просмотр печати, выполнив следующие действия:

## Шаг 1. Укажите исходный каталог.

Сначала вам необходимо указать исходный каталог, в котором находится файл Excel, который вы хотите просмотреть. Вот как это сделать:

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
```

## Шаг 2. Загрузите книгу

Затем вам необходимо загрузить книгу Workbook из указанного файла Excel. Вот как это сделать:

```csharp
// Загрузите рабочую книгу
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
```

## Шаг 3. Настройте параметры изображения и печати

Перед созданием предварительного просмотра вы можете настроить изображение и параметры печати по мере необходимости. В этом примере мы используем параметры по умолчанию. Вот как это сделать:

```csharp
// Параметры изображения и печати
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
```

## Шаг 4. Создайте предварительный просмотр книги для печати.

Теперь вы можете создать предварительный просмотр книги Workbook с помощью класса WorkbookPrintingPreview. Вот как это сделать:

```csharp
// Предварительный просмотр книги
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
```

## Шаг 5. Создайте предварительный просмотр листа для печати.

Если вы хотите создать предварительный просмотр определенного листа, вы можете использовать класс SheetPrintingPreview. Вот пример:

```csharp
// Предварительный просмотр рабочего листа
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Number of worksheet pages: " + preview2.EvaluatedPageCount);
```

### Пример исходного кода для предварительного просмотра книги с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(sourceDir + "Book1.xlsx");
ImageOrPrintOptions imgOptions = new ImageOrPrintOptions();
WorkbookPrintingPreview preview = new WorkbookPrintingPreview(workbook, imgOptions);
Console.WriteLine("Workbook page count: " + preview.EvaluatedPageCount);
SheetPrintingPreview preview2 = new SheetPrintingPreview(workbook.Worksheets[0], imgOptions);
Console.WriteLine("Worksheet page count: " + preview2.EvaluatedPageCount);
Console.WriteLine("PrintPreview executed successfully.");
```

## Заключение

Создание предварительного просмотра книги для печати — это мощная функция, предлагаемая Aspose.Cells для .NET. Выполнив описанные выше шаги, вы можете легко просмотреть книгу Excel и получить информацию о количестве страниц для печати.

### Часто задаваемые вопросы

#### Вопрос: Как указать другой исходный каталог для загрузки моей книги?
    
 О: Вы можете использовать`Set_SourceDirectory` метод для указания другого исходного каталога. Например:`RunExamples.Set_SourceDirectory("Path_to_the_source_directory")`.

#### Вопрос: Могу ли я настроить изображение и параметры печати при предварительном просмотре?
    
 О: Да, вы можете настроить параметры изображения и печати, изменив свойства`ImageOrPrintOptions` объект. Например, вы можете установить разрешение изображения, формат выходного файла и т. д.

#### Вопрос: Можно ли создать предварительный просмотр для нескольких листов в книге?
    
О: Да, вы можете перебирать различные листы в книге и создавать предварительный просмотр для каждого листа, используя`SheetPrintingPreview` сорт.

#### Вопрос: Как сохранить предварительный просмотр в виде изображения или PDF-файла?
    
 О: Вы можете использовать`ToImage` или`ToPdf` метод`WorkbookPrintingPreview` или`SheetPrintingPreview` объект для сохранения предварительного просмотра в виде изображения или файла PDF.

#### Вопрос: Что я могу делать с созданным предварительным просмотром печати?
    
О: После того как вы создали предварительный просмотр для печати, вы можете просмотреть его на экране, сохранить как изображение или файл PDF или использовать для других операций, таких как отправка по электронной почте или печать.
	