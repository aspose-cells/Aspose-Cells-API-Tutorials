---
title: Управление коэффициентом масштабирования рабочего листа
linktitle: Управление коэффициентом масштабирования рабочего листа
second_title: Справочник по Aspose.Cells для .NET API
description: Управляйте коэффициентом масштабирования рабочего листа Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 20
url: /ru/net/excel-display-settings-csharp-tutorials/controll-zoom-factor-of-worksheet/
---
Управление коэффициентом масштабирования рабочего листа является важной функцией при работе с файлами Excel с использованием библиотеки Aspose.Cells для .NET. В этом руководстве мы покажем вам, как использовать Aspose.Cells для управления коэффициентом масштабирования рабочего листа с использованием исходного кода C# шаг за шагом.

## Шаг 1. Импортируйте необходимые библиотеки

Прежде чем начать, убедитесь, что у вас установлена библиотека Aspose.Cells для .NET, и импортируйте необходимые библиотеки в свой проект C#.

```csharp
using System;
using System.IO;
using Aspose.Cells;
```

## Шаг 2: Установите путь к каталогу и откройте файл Excel

 Для начала укажите путь к каталогу, содержащему ваш файл Excel, затем откройте его с помощью`FileStream` объект и создать экземпляр`Workbook` объект для представления книги Excel.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## Шаг 3. Получите доступ к электронной таблице и измените коэффициент масштабирования.

На этом шаге мы получаем доступ к первому рабочему листу книги Excel, используя индекс`0` и установите коэффициент масштабирования рабочего листа на`75`.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet. Zoom = 75;
```

## Шаг 4: Сохраните изменения и закройте файл

 Как только мы изменим коэффициент масштабирования рабочего листа, мы сохраним изменения в файле Excel, используя`Save` метод`Workbook` объект. Затем мы закрываем файловый поток, чтобы освободить все используемые ресурсы.

```csharp
workbook.Save(dataDir + "output.xls");
fstream.Close();
```

### Пример исходного кода для Controll Zoom Factor Of Worksheet с использованием Aspose.Cells для .NET 

```csharp
// Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание файлового потока, содержащего открываемый файл Excel
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook workbook = new Workbook(fstream);
// Доступ к первому рабочему листу в файле Excel
Worksheet worksheet = workbook.Worksheets[0];
// Установка коэффициента масштабирования рабочего листа на 75
worksheet.Zoom = 75;
// Сохранение измененного файла Excel
workbook.Save(dataDir + "output.xls");
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

## Заключение

В этом пошаговом руководстве показано, как управлять коэффициентом масштабирования рабочего листа с помощью Aspose.Cells для .NET. Используя предоставленный исходный код C#, вы можете легко настроить коэффициент масштабирования рабочего листа в своих приложениях .NET.

### Часто задаваемые вопросы (FAQ)

#### Что такое Aspose.Cells для .NET?

Aspose.Cells for .NET — это многофункциональная библиотека для работы с файлами Excel в приложениях .NET.

#### Как я могу установить Aspose.Cells для .NET?

 Чтобы установить Aspose.Cells для .NET, вам необходимо загрузить соответствующий пакет NuGet с[Aspose выпускает](https://releases/aspose.com/cells/net/) и добавьте его в свой проект .NET.

#### Какие функции предлагает Aspose.Cells для .NET?

Aspose.Cells для .NET предлагает такие функции, как создание, редактирование, преобразование и расширенное управление файлами Excel.

#### Какие форматы файлов поддерживает Aspose.Cells для .NET?

Aspose.Cells для .NET поддерживает несколько форматов файлов, включая XLSX, XLSM, CSV, HTML, PDF и многие другие.
