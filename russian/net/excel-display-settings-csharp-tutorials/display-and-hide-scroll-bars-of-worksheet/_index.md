---
title: Показать и скрыть полосы прокрутки рабочего листа
linktitle: Показать и скрыть полосы прокрутки рабочего листа
second_title: Справочник по Aspose.Cells для .NET API
description: Отображение или скрытие полос прокрутки на листе Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 50
url: /ru/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
В этом руководстве мы покажем вам, как отображать или скрывать вертикальные и горизонтальные полосы прокрутки на листе Excel, используя исходный код C# с Aspose.Cells для .NET. Выполните следующие шаги, чтобы получить желаемый результат.

## Шаг 1. Импортируйте необходимые библиотеки

Убедитесь, что вы установили библиотеку Aspose.Cells для .NET, и импортируйте необходимые библиотеки в свой проект C#.

```csharp
using Aspose.Cells;
using System.IO;
```

## Шаг 2: Установите путь к каталогу и откройте файл Excel

 Задайте путь к каталогу, содержащему ваш файл Excel, затем откройте файл, создав файловый поток и создав экземпляр`Workbook` объект.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Шаг 3. Скройте полосы прокрутки

 Использовать`IsVScrollBarVisible` и`IsHScrollBarVisible` свойства`Workbook.Settings` объект, чтобы скрыть вертикальные и горизонтальные полосы прокрутки рабочего листа.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## Шаг 4: Сохраните изменения

 После внесения необходимых изменений сохраните измененный файл Excel с помощью`Save` метод`Workbook` объект.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Пример исходного кода для отображения и скрытия полос прокрутки рабочего листа с использованием Aspose.Cells для .NET 

```csharp
// Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание файлового потока, содержащего открываемый файл Excel
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook workbook = new Workbook(fstream);
// Скрытие вертикальной полосы прокрутки файла Excel
workbook.Settings.IsVScrollBarVisible = false;
// Скрытие горизонтальной полосы прокрутки файла Excel
workbook.Settings.IsHScrollBarVisible = false;
// Сохранение измененного файла Excel
workbook.Save(dataDir + "output.xls");
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

### Заключение

В этом пошаговом руководстве показано, как отображать или скрывать вертикальные и горизонтальные полосы прокрутки в электронной таблице Excel с помощью Aspose.Cells для .NET. Используя предоставленный исходный код C#, вы можете легко настроить отображение полос прокрутки в файлах Excel.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это мощная библиотека для работы с файлами Excel в приложениях .NET.

#### Как я могу установить Aspose.Cells для .NET?

 Чтобы установить Aspose.Cells для .NET, вам необходимо скачать соответствующий пакет с[Aspose выпускает](https://releases/aspose.com/cells/net/) и добавьте его в свой проект .NET.

#### Как отображать или скрывать полосы прокрутки в электронной таблице Excel с помощью Aspose.Cells для .NET?

 Вы можете использовать`IsVScrollBarVisible` и`IsHScrollBarVisible` свойства`Workbook.Settings`объект, чтобы отобразить или скрыть вертикальную и горизонтальную полосы прокрутки соответственно на листе Excel.

#### Какие еще форматы файлов Excel поддерживает Aspose.Cells для .NET?

Aspose.Cells для .NET поддерживает различные форматы файлов Excel, такие как XLS, XLSX, CSV, HTML, PDF и т. д.