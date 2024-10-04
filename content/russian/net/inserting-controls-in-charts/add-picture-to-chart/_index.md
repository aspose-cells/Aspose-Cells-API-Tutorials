---
title: Добавить изображение в диаграмму
linktitle: Добавить изображение в диаграмму
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как легко добавлять изображения в диаграммы Excel с помощью Aspose.Cells для .NET. Улучшите свои диаграммы и презентации всего за несколько простых шагов.
type: docs
weight: 11
url: /ru/net/inserting-controls-in-charts/add-picture-to-chart/
---
## Введение

Вам надоели скучные диаграммы, которым не хватает индивидуальности? Хотите узнать, как оживить визуальные эффекты Excel, добавив картинки? Что ж, вам повезло! В этом уроке мы погрузимся в мир Aspose.Cells для .NET и узнаем, как добавлять картинки в диаграммы в Excel. Итак, налейте себе чашечку любимого кофе и начнем!

## Предпосылки

Прежде чем мы перейдем к тонкостям кодирования, необходимо выполнить несколько предварительных условий, чтобы все прошло гладко:

- Visual Studio: Здесь вы будете писать и запускать свой код .NET. Убедитесь, что он у вас установлен.
-  Aspose.Cells for .NET: Эта библиотека вам понадобится для работы с файлами Excel. Вы можете[скачать здесь](https://releases.aspose.com/cells/net/).
- Базовые знания C#: Я покажу вам код, но знание основ C# сделает ситуацию более понятной.

### Этапы установки

1. Установить Aspose.Cells: Вы можете добавить Aspose.Cells в свой проект Visual Studio через NuGet Package Manager. Сделайте это, перейдя в Tools > NuGet Package Manager > Manage NuGet Packages for Solution и выполнив поиск по запросу «Aspose.Cells». Нажмите Install.
2. Настройка проекта: создайте новый проект консольного приложения C# в Visual Studio.

## Импортные пакеты

После того, как вы все настроили, следующим шагом будет импорт необходимых пакетов в ваш проект. Вот как это сделать:

### Импорт требуемых пространств имен

В верхней части файла кода C# вам необходимо импортировать следующие пространства имен:

```csharp
using Aspose.Cells;
using Aspose.Cells.Charts;
using Aspose.Cells.Drawing;
using System.IO;
```

Это говорит вашей программе: «Эй! Я собираюсь использовать эти классные функции из Aspose.Cells».

Теперь, когда у нас есть все необходимые условия, давайте разобьем процесс на небольшие шаги. 

## Шаг 1: Определите свои каталоги

Первым делом нам нужно настроить пути для наших входных и выходных файлов. Этот шаг имеет решающее значение, поскольку нам нужно знать, где найти наш существующий файл Excel и где сохранить измененный файл.

```csharp
//Исходный каталог
string sourceDir = "Your Document Directory/";

//Выходной каталог
string outputDir = "Your Output Directory/";
```

 Заменять`Your Document Directory` и`Your Output Directory`с реальными путями на вашем компьютере. 

## Шаг 2: Загрузите существующую рабочую книгу

Теперь давайте загрузим существующий файл Excel, в который мы хотим добавить нашу картинку на диаграмму.

```csharp
// Откройте существующий файл.
Workbook workbook = new Workbook(sourceDir + "sampleAddingPictureInChart.xls");
```

Этот код открывает книгу, делая ее готовой для редактирования.

## Шаг 3: Подготовка потока изображений

Перед добавлением картинки нам необходимо прочитать изображение, которое мы хотим вставить в диаграмму. 

```csharp
// Загрузите файл изображения в поток.
FileStream stream = new FileStream(sourceDir + "sampleAddingPictureInChart.png", FileMode.Open, FileAccess.Read);
```

Убедитесь, что изображение сохранено в указанном каталоге.

## Шаг 4: Нацельтесь на график

Теперь давайте укажем, в какую диаграмму мы собираемся добавить нашу картинку. В этом примере мы нацелимся на первую диаграмму на первом рабочем листе.

```csharp
// Получите схему дизайнера на втором листе.
Worksheet sheet = workbook.Worksheets[0];
Aspose.Cells.Charts.Chart chart = sheet.Charts[0];
```

Вы можете получить доступ к любому рабочему листу, изменив индекс соответствующим образом.

## Шаг 5: Добавьте изображение на диаграмму

Выбрав диаграмму, пришло время добавить изображение! 

```csharp
// Добавьте новую картинку на диаграмму.
Aspose.Cells.Drawing.Picture pic0 = chart.Shapes.AddPictureInChart(50, 50, stream, 200, 200);
```

 Здесь,`50` и`50` — это координаты X и Y, где будет размещено изображение, и`200`ширина и высота изображения.

## Шаг 6: Настройте формат линий изображения

Хотите добавить изюминку к своей картинке? Вы можете настроить ее рамку! Вот как это сделать:

```csharp
// Получите тип формата линии изображения.
Aspose.Cells.Drawing.LineFormat lineformat = pic0.Line; 

// Установите стиль тире.
lineformat.DashStyle = MsoLineDashStyle.Solid;

// Установите толщину линии.
lineformat.Weight = 4;    
```

Этот фрагмент позволяет вам выбрать, как будет выглядеть граница и насколько она будет толстой. Выберите любой стиль, который соответствует вашей презентации!

## Шаг 7: Сохраните измененную рабочую книгу.

После всей этой тяжелой работы давайте сохраним ваши изменения, выполнив следующую строку кода:

```csharp
// Сохраните файл Excel.
workbook.Save(outputDir + "outputAddingPictureInChart.xls");
```

Теперь ваша фотография успешно интегрирована в диаграмму, и ваш выходной файл готов к просмотру!

## Шаг 8: Укажите успех

Наконец, вы можете добавить простое сообщение, подтверждающее, что ваша операция прошла успешно:

```csharp
Console.WriteLine("AddingPictureInChart executed successfully.");
```

## Заключение

В этом уроке мы изучили, как добавить немного индивидуальности в ваши диаграммы Excel, добавив картинки с помощью Aspose.Cells для .NET. Всего за несколько простых шагов вы можете поднять свои презентации от обыденных до запоминающихся. Так чего же вы ждете? Попробуйте и позвольте вашим диаграммам засиять!

## Часто задаваемые вопросы

### Могу ли я добавить несколько изображений в одну диаграмму?
 Да! Вы можете позвонить`AddPictureInChart` метод несколько раз, чтобы добавить столько изображений, сколько вы хотите.

### Какие форматы изображений поддерживает Aspose.Cells?
Aspose.Cells поддерживает различные форматы изображений, включая PNG, JPEG, BMP и GIF.

### Могу ли я настроить положение изображения?
 Конечно! Координаты X и Y в`AddPictureInChart` Метод позволяет точно позиционировать.

### Можно ли использовать Aspose.Cells бесплатно?
 Aspose.Cells предлагает бесплатную пробную версию, но для полного функционала требуется лицензия. Вы можете найти цены[здесь](https://purchase.aspose.com/buy).

### Где я могу найти больше примеров?
 Проверьте[Документация Aspose.Cells](https://reference.aspose.com/cells/net/) для более подробных примеров и функциональных возможностей.