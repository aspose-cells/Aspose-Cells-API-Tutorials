---
title: Отображать и скрывать заголовки столбцов строк рабочего листа
linktitle: Отображать и скрывать заголовки столбцов строк рабочего листа
second_title: Справочник по API Aspose.Cells для .NET
description: Отобразите или скройте заголовки строк и столбцов на листе Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 40
url: /ru/net/excel-display-settings-csharp-tutorials/display-and-hide-row-column-headers-of-worksheet/
---
В этом уроке мы покажем вам, как отображать или скрывать заголовки строк и столбцов листа Excel, используя исходный код C# с помощью Aspose.Cells для .NET. Следуйте инструкциям ниже, чтобы получить желаемый результат.

## Шаг 1. Импортируйте необходимые библиотеки.

Убедитесь, что вы установили библиотеку Aspose.Cells для .NET и импортировали необходимые библиотеки в свой проект C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Шаг 2. Установите путь к каталогу и откройте файл Excel.

 Задайте путь к каталогу, содержащему файл Excel, затем откройте файл, создав поток файлов и создав экземпляр`Workbook` объект.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Шаг 3. Перейдите на первый лист и скройте заголовки строк и столбцов.

 Получите доступ к первому листу в файле Excel, используя команду`Worksheets` собственность`Workbook` объект. Затем используйте`IsRowColumnHeadersVisible` собственность`Worksheet` объект, чтобы скрыть заголовки строк и столбцов.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. IsRowColumnHeadersVisible = false;
```

## Шаг 4. Сохраните изменения.

 После внесения необходимых изменений сохраните измененный файл Excel, используя`Save` метод`Workbook` объект.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Пример исходного кода для отображения и скрытия заголовков столбцов строк рабочего листа с использованием Aspose.Cells для .NET 
```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание потока файлов, содержащего открываемый файл Excel.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook workbook = new Workbook(fstream);
// Доступ к первому листу в файле Excel
Worksheet worksheet = workbook.Worksheets[0];
// Скрытие заголовков строк и столбцов
worksheet.IsRowColumnHeadersVisible = false;
// Сохранение измененного файла Excel
workbook.Save(dataDir + "output.xls");
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close(); 
```

## Заключение

В этом пошаговом руководстве показано, как отображать или скрывать заголовки строк и столбцов в электронной таблице Excel с помощью Aspose.Cells для .NET. Используя предоставленный исходный код C#, вы можете легко настроить отображение заголовков в файлах Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это мощная библиотека для управления файлами Excel в приложениях .NET.

#### Как мне установить Aspose.Cells для .NET?

 Чтобы установить Aspose.Cells для .NET, вам необходимо скачать соответствующий пакет с сайта[Aspose Релизы](https://releases/aspose.com/cells/net/) и добавьте его в свой проект .NET.

#### Как я могу показать или скрыть заголовки строк и столбцов электронной таблицы Excel с помощью Aspose.Cells для .NET?

 Вы можете использовать`IsRowColumnHeadersVisible` собственность`Worksheet`объект для отображения или скрытия заголовков строк и столбцов. Установите его на`true` показать их и`false` чтобы скрыть их.

#### Какие еще форматы файлов Excel поддерживаются Aspose.Cells для .NET?

Aspose.Cells для .NET поддерживает различные форматы файлов Excel, такие как XLS, XLSX, CSV, HTML, PDF и многие другие.
