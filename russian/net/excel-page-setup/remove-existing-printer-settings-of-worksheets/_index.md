---
title: Удалить существующие настройки принтера рабочих листов
linktitle: Удалить существующие настройки принтера рабочих листов
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как удалить существующие настройки принтера из электронных таблиц Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 80
url: /ru/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
В этом руководстве мы шаг за шагом расскажем, как удалить существующие настройки принтера из рабочих листов в Excel с помощью Aspose.Cells для .NET. Мы будем использовать исходный код C#, чтобы проиллюстрировать процесс.

## Шаг 1. Настройка среды

Убедитесь, что на вашем компьютере установлен Aspose.Cells for .NET. Также создайте новый проект в предпочитаемой вами среде разработки.

## Шаг 2: Импортируйте необходимые библиотеки

В файл кода импортируйте библиотеки, необходимые для работы с Aspose.Cells. Вот соответствующий код:

```csharp
using Aspose.Cells;
```

## Шаг 3: Установите исходный и выходной каталоги

Установите исходный и выходной каталоги, в которых находится исходный файл Excel и где вы хотите сохранить измененный файл соответственно. Используйте следующий код:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Не забудьте указать полные пути к каталогам.

## Шаг 4: Загрузка исходного файла Excel

Загрузите исходный файл Excel, используя следующий код:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Это загрузит указанный файл Excel в объект Workbook.

## Шаг 5: Навигация по листам

Перебрать все рабочие листы в книге, используя цикл. Используйте следующий код:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Остальной код будет добавлен на следующем шаге.
}
```

## Шаг 6. Удалите существующие настройки принтера

Проверьте, существуют ли настройки принтера для каждого рабочего листа, и при необходимости удалите их. Используйте следующий код:

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

## Шаг 7: Сохранение измененной книги

Сохраните измененную книгу, используя следующий код:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Это сохранит измененную книгу в указанном выходном каталоге.

### Пример исходного кода для удаления существующих настроек принтера рабочих листов с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
//Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
//Загрузить исходный файл Excel
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Получить количество листов рабочей книги
int sheetCount = wb.Worksheets.Count;
//Перебрать все листы
for (int i = 0; i < sheetCount; i++)
{
    //Доступ к i-му рабочему листу
    Worksheet ws = wb.Worksheets[i];
    //Доступ к настройкам страницы рабочего листа
    PageSetup ps = ws.PageSetup;
    //Проверьте, существуют ли настройки принтера для этого рабочего листа
    if (ps.PrinterSettings != null)
    {
        //Распечатайте следующее сообщение
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Печать имени листа и размера бумаги
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Удалите настройки принтера, установив для них значение null
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//если
}//для
//Сохраните книгу
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Заключение

Теперь вы узнали, как удалить существующие настройки принтера из рабочих листов в Excel с помощью Aspose.Cells для .NET. В этом учебном пособии вы прошли все этапы процесса, от настройки среды до навигации по электронным таблицам и сброса настроек принтера. Теперь вы можете использовать эти знания для управления настройками принтера в файлах Excel.

### Часто задаваемые вопросы

#### Q1: Как узнать, есть ли в электронной таблице существующие настройки принтера?

 A1: Вы можете проверить, существуют ли настройки принтера для рабочего листа, открыв`PrinterSettings` собственность`PageSetup` объект. Если значение не равно нулю, это означает, что существуют существующие настройки принтера.

#### Q2: Могу ли я удалить настройки принтера только для определенной электронной таблицы?

 A2: Да, вы можете использовать тот же подход для удаления настроек принтера для определенного рабочего листа, обратившись к этому рабочему листу.`PageSetup` объект.

#### Q3: Удаляет ли этот метод другие настройки макета?

A3: Нет, этот метод удаляет только настройки принтера. Другие параметры макета, такие как поля, ориентация бумаги и т. д., остаются без изменений.

#### Q4: Этот метод работает для всех форматов файлов Excel, таких как .xls и .xlsx?

A4: Да, этот метод работает для всех форматов файлов Excel, поддерживаемых Aspose.Cells, включая .xls и .xlsx.

#### Q5: Являются ли изменения, внесенные в настройки принтера, постоянными в редактируемом файле Excel?

A5: Да, изменения в настройках принтера постоянно сохраняются в редактируемом файле Excel.