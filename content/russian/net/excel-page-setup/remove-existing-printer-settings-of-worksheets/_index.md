---
title: Удалить существующие настройки принтера на листах
linktitle: Удалить существующие настройки принтера на листах
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как удалить существующие настройки принтера из электронных таблиц Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 80
url: /ru/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
В этом уроке мы шаг за шагом покажем вам, как удалить существующие настройки принтера из листов в Excel с помощью Aspose.Cells для .NET. Для иллюстрации процесса мы будем использовать исходный код C#.

## Шаг 1. Настройка среды

Убедитесь, что на вашем компьютере установлен Aspose.Cells for .NET. Также создайте новый проект в предпочитаемой вами среде разработки.

## Шаг 2. Импортируйте необходимые библиотеки.

В файл кода импортируйте библиотеки, необходимые для работы с Aspose.Cells. Вот соответствующий код:

```csharp
using Aspose.Cells;
```

## Шаг 3. Установите исходный и выходной каталоги.

Установите исходный и выходной каталоги, в которых находится исходный файл Excel и где вы хотите сохранить измененный файл соответственно. Используйте следующий код:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Обязательно указывайте полные пути к каталогам.

## Шаг 4. Загрузка исходного файла Excel

Загрузите исходный файл Excel, используя следующий код:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Это загрузит указанный файл Excel в объект Workbook.

## Шаг 5. Навигация по листам

Перебрать все листы книги с помощью цикла. Используйте следующий код:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Остальная часть кода будет добавлена на следующем шаге.
}
```

## Шаг 6. Удалите существующие настройки принтера

Проверьте, существуют ли настройки принтера для каждого листа, и при необходимости удалите их. Используйте следующий код:

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

## Шаг 7. Сохранение измененной книги

Сохраните измененную книгу, используя следующий код:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Это позволит сохранить измененную книгу в указанном выходном каталоге.

### Пример исходного кода для удаления существующих настроек принтера из листов с помощью Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
//Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
//Загрузить исходный файл Excel
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Получить количество листов в книге
int sheetCount = wb.Worksheets.Count;
//Перебрать все листы
for (int i = 0; i < sheetCount; i++)
{
    //Доступ к i-му листу
    Worksheet ws = wb.Worksheets[i];
    //Доступ к настройке страницы рабочего листа
    PageSetup ps = ws.PageSetup;
    //Проверьте, существуют ли настройки принтера для этого листа.
    if (ps.PrinterSettings != null)
    {
        //Распечатайте следующее сообщение
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Распечатайте имя листа и его размер бумаги.
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Удалите настройки принтера, установив для них значение null.
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//если
}//для
//Сохраните книгу
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Заключение

Теперь вы узнали, как удалить существующие настройки принтера из листов Excel с помощью Aspose.Cells для .NET. В этом руководстве вы прошли каждый этап процесса: от настройки среды до навигации по электронным таблицам и очистки настроек принтера. Теперь вы можете использовать эти знания для управления настройками принтера в файлах Excel.

### Часто задаваемые вопросы

#### Вопрос 1. Как узнать, имеются ли в электронной таблице настройки принтера?

 A1: Вы можете проверить, существуют ли настройки принтера для листа, открыв`PrinterSettings` собственность`PageSetup` объект. Если значение не равно нулю, это означает, что существуют существующие настройки принтера.

#### Вопрос 2. Могу ли я удалить настройки принтера только для определенной таблицы?

 О2: Да, вы можете использовать тот же подход для удаления настроек принтера для определенного листа, открыв его`PageSetup` объект.

#### Вопрос 3. Удаляет ли этот метод и другие настройки макета?

О3: Нет, этот метод удаляет только настройки принтера. Другие настройки макета, такие как поля, ориентация бумаги и т. д., остаются неизменными.

#### Вопрос 4. Этот метод работает для всех форматов файлов Excel, таких как .xls и .xlsx?

A4: Да, этот метод работает для всех форматов файлов Excel, поддерживаемых Aspose.Cells, включая .xls и .xlsx.

#### Вопрос 5. Являются ли изменения, внесенные в настройки принтера, постоянными в редактируемом файле Excel?

О5: Да, изменения настроек принтера навсегда сохраняются в редактируемом файле Excel.