---
title: Конвертировать диаграмму в PDF
linktitle: Конвертировать диаграмму в PDF
second_title: API обработки Excel Aspose.Cells .NET
description: Научитесь конвертировать диаграммы Excel в PDF с помощью Aspose.Cells для .NET с помощью этого простого пошагового руководства. Изучите основные советы и примеры кодирования.
type: docs
weight: 11
url: /ru/net/chart-rendering-and-conversion/convert-chart-to-pdf/
---
## Введение

Когда дело доходит до работы с электронными таблицами, диаграммы часто играют решающую роль в эффективной визуализации данных. Независимо от того, готовите ли вы отчет, проводите презентацию или просто облегчаете анализ данных, преобразование этих диаграмм в PDF придает профессиональный вид. Здесь мы проведем вас через шаги по преобразованию диаграммы Excel в формат PDF с помощью Aspose.Cells for .NET, мощной библиотеки, разработанной для упрощения манипуляций с Excel.

## Предпосылки

Прежде чем погрузиться в учебник, вам нужно убедиться, что у вас есть правильная настройка. Вот что вам нужно:

### .NET Framework
Убедитесь, что на вашем компьютере установлен .NET Framework. Aspose.Cells совместим с различными версиями, но лучше всего работает с последней.

### Библиотека Aspose.Cells
 Вам понадобится библиотека Aspose.Cells for .NET. Вы можете скачать ее здесь[здесь](https://releases.aspose.com/cells/net/). Библиотека поставляется с богатым API, который инкапсулирует все функции, которые вам могут понадобиться для работы с Excel.

### Визуальная Студия
Наличие установленной Visual Studio имеет решающее значение, поскольку это отличная среда IDE для удобного написания кода .NET.

### Базовые знания C#
Некоторое знакомство с языком программирования C# поможет вам лучше понять сегменты кода.

## Импортные пакеты

Для успешного использования Aspose.Cells в вашем проекте вам необходимо импортировать необходимые пакеты. Вот как это можно сделать:

### Создать новый проект

Начните с создания нового проекта C# в Visual Studio:

1. Откройте Visual Studio.
2. Нажмите «Создать новый проект».
3. Выберите «Консольное приложение (.NET Core)» или «Консольное приложение (.NET Framework)» в зависимости от ваших требований.
4. Назовите свой проект и нажмите «Создать».

### Добавить ссылку Aspose.Cells

После создания проекта необходимо добавить ссылку на библиотеку Aspose.Cells:

1. В обозревателе решений щелкните правой кнопкой мыши свой проект.
2. Выберите «Управление пакетами NuGet».
3. Найдите «Aspose.Cells» и установите его.

После включения библиотеки в проект вы готовы перейти к коду.

### Импорт требуемых пространств имен

 В верхней части вашего`Program.cs` файл, добавьте следующие пространства имен:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using Aspose.Cells.Charts;
using System.IO;
```

Вот как систематически преобразовать диаграмму Excel в PDF. Следуйте пошаговым инструкциям!

## Шаг 1: Настройка выходных и исходных каталогов

Чтобы начать писать код, вам сначала нужно указать, где вы будете сохранять выходные данные и где находится исходный документ.

```csharp
// Выходной каталог
string outputDir = "Your Output Directory";

// Исходный каталог
string sourceDir = "Your Document Directory";
```

 Обязательно замените`"Your Output Directory"` и`"Your Document Directory"` с фактическим путем расположения ваших файлов.

## Шаг 2: Загрузите книгу Excel

Теперь давайте загрузим файл Excel, содержащий диаграммы, которые вы хотите преобразовать. Это довольно просто:

```csharp
// Загрузить файл Excel, содержащий диаграммы
Workbook workbook = new Workbook(sourceDir + "sampleChartToPdf.xlsx");
```

Этот код инициализирует новый объект рабочей книги и загружает указанный файл Excel. Убедитесь, что имя файла совпадает с тем, которое у вас есть в исходном каталоге.

## Шаг 3: Доступ к рабочему листу

Далее вам нужно получить доступ к рабочему листу, содержащему диаграмму, которую вы хотите преобразовать. Вот как это сделать:

```csharp
// Доступ к первому рабочему листу
Worksheet worksheet = workbook.Worksheets[0];
```

Этот код получает доступ к первому листу в вашей книге, позволяя вам работать с ним.

## Шаг 4: Доступ к диаграмме 

После того, как у вас есть рабочий лист, пришло время получить доступ к конкретной диаграмме, которую вы хотите преобразовать:

```csharp
// Доступ к первой диаграмме на рабочем листе
Chart chart = worksheet.Charts[0];
```

Эта строка захватывает первую диаграмму, содержащуюся в рабочем листе. Если на вашем рабочем листе есть несколько диаграмм и вам нужно выбрать определенную, настройте индекс соответствующим образом.

## Шаг 5: Преобразуйте диаграмму в PDF

Теперь самое интересное — конвертация диаграммы в формат PDF. Вы можете сохранить ее в файл или в поток памяти.

### Вариант 1: Сохранить диаграмму в файл

Чтобы сохранить диаграмму непосредственно в файл PDF, используйте следующий код:

```csharp
// Сохранить диаграмму в формате PDF
chart.ToPdf(outputDir + "outputChartToPdf.pdf");
```

Просто убедитесь, что выходной каталог действительно существует, чтобы избежать ошибок.

### Вариант 2: Сохранить диаграмму в потоке памяти

Если вы хотите в дальнейшем обрабатывать PDF-файл или хотите немедленно использовать его в своем приложении, лучшим выбором может быть сохранение его в потоке памяти:

```csharp
// Сохраните диаграмму в формате PDF в потоке
MemoryStream ms = new MemoryStream();
chart.ToPdf(ms);
```

Здесь вы сохраняете PDF-файл в потоке памяти, который можно использовать в соответствии с потребностями вашего приложения.

## Шаг 6: Отображение сообщения об успешном завершении

Наконец, всегда приятно указать, что ваша операция прошла успешно. Вы можете просто вывести сообщение об успешном завершении на консоль:

```csharp
Console.WriteLine("ChartToPdf executed successfully.");
```

## Заключение

И вот оно! Используя Aspose.Cells для .NET, преобразование диаграмм Excel в форматы PDF становится прогулкой в парке. Независимо от того, выберете ли вы сохранение в файл или поток памяти, библиотека обещает гибкость и простоту использования. Так почему бы не попробовать? Ваши отчеты будут выглядеть намного четче с профессионально отформатированными диаграммами PDF!

## Часто задаваемые вопросы

### Может ли Aspose.Cells конвертировать несколько диаграмм одновременно?
 Да, вы можете выполнить цикл`worksheet.Charts` коллекция для преобразования каждой диаграммы по отдельности.

### Подходит ли Aspose.Cells для больших файлов Excel?
Конечно! Aspose.Cells оптимизирован для производительности и может эффективно обрабатывать большие файлы Excel.

### Какие версии .NET поддерживает Aspose.Cells?
Aspose.Cells поддерживает различные версии .NET, включая .NET Framework и .NET Core.

### Где я могу найти подробную документацию?
 Посетите[Документация Aspose.Cells](https://reference.aspose.com/cells/net/) для получения подробной информации и примеров.

### Есть ли бесплатная пробная версия?
 Да! Вы можете загрузить бесплатную пробную версию с[здесь](https://releases.aspose.com/).