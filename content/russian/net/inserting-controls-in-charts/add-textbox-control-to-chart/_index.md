---
title: Добавить элемент управления TextBox на диаграмму
linktitle: Добавить элемент управления TextBox на диаграмму
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как добавить TextBox в диаграммы в Excel с помощью Aspose.Cells для .NET. Улучшите визуализацию данных без усилий.
type: docs
weight: 12
url: /ru/net/inserting-controls-in-charts/add-textbox-control-to-chart/
---
## Введение

Создание динамических и визуально привлекательных диаграмм в Excel — это фантастический способ эффективного представления данных. Одна из замечательных функций, которую вы можете использовать, — это добавление TextBox в диаграмму. С Aspose.Cells for .NET эта задача становится легкой и увлекательной! В этом руководстве мы шаг за шагом проведем вас через процесс интеграции TextBox в вашу диаграмму. Независимо от того, являетесь ли вы опытным разработчиком или только начинаете, это руководство предоставит вам все инструменты, необходимые для улучшения ваших диаграмм Excel. Итак, вы готовы погрузиться в процесс?

## Предпосылки

Прежде чем приступить к кодированию, вам следует подготовить несколько вещей:

- Базовое понимание C#: Фундаментальное понимание программирования на C# будет полезным. Не волнуйтесь, вам не нужно быть экспертом, просто удобно ориентироваться в синтаксисе.
-  Установленная библиотека Aspose.Cells: Убедитесь, что у вас установлена библиотека Aspose.Cells for .NET. Вы можете загрузить ее с[здесь](https://releases.aspose.com/cells/net/)если вы еще этого не сделали.
- Visual Studio: Обязательное знание Visual Studio или любой IDE, которую вы предпочитаете использовать для .NET Framework.
- Существующий файл Excel: в этом примере мы будем работать с существующим файлом Excel с именем "sampleAddingTextBoxControlInChart.xls". Вы можете создать его или загрузить пример.

Теперь, когда у нас все готово, давайте приступим к написанию кода!

## Импортные пакеты

Первым делом нам нужно импортировать необходимые пространства имен Aspose.Cells в наш проект C#. Вы можете легко это сделать, включив следующие строки в начало вашего файла кода:

```csharp
using System;
using System.IO;

using Aspose.Cells;
using System.Drawing;
```

## Шаг 1: Определите исходные и выходные каталоги

Прежде чем начать работать с файлом Excel, важно определить, где находится ваш входной файл и где вы хотите сохранить выходной файл. Это помогает поддерживать организованность вашего проекта.

```csharp
// Исходный каталог
string sourceDir = "Your Document Directory";

// Выходной каталог
string outputDir = "Your Output Directory";
```
 Заменять`"Your Document Directory"` и`"Your Output Directory"` с реальными путями в вашей системе.

## Шаг 2: Откройте существующий файл Excel.

Далее нам нужно открыть файл Excel, содержащий диаграмму, которую мы хотим изменить. Это позволит нам извлечь диаграмму и внести изменения.

```csharp
// Откройте существующий файл.
Workbook workbook = new Workbook(sourceDir + "sampleAddingTextBoxControlInChart.xls");
```
Эта строка инициализирует новый объект Workbook с указанным нами файлом.

## Шаг 3: Доступ к диаграмме на рабочем листе

Поскольку диаграммы в Excel хранятся на листе, нам нужно сначала получить доступ к листу, а затем получить нужную диаграмму. Для этого примера мы получим доступ к первой диаграмме на первом листе.

```csharp
// Получите схему дизайнера на первом листе.
Worksheet sheet = workbook.Worksheets[0];
Aspose.Cells.Charts.Chart chart = sheet.Charts[0];
```
Изменяя значение индекса, вы можете выбирать другие рабочие листы или диаграммы, если в вашем файле их больше.

## Шаг 4: Добавьте новое текстовое поле в диаграмму.

Теперь мы готовы добавить наш TextBox. Мы укажем его положение и размер при создании.

```csharp
// Добавьте новое текстовое поле в диаграмму.
Aspose.Cells.Drawing.TextBox textbox0 = chart.Shapes.AddTextBoxInChart(400, 1100, 350, 2550);
```
В этой команде параметры определяют местоположение (x, y) и размер (ширина, высота) TextBox в диаграмме. Отрегулируйте эти значения в зависимости от конкретных потребностей макета.

## Шаг 5: Задайте текст для текстового поля

Как только TextBox будет на месте, пора заполнить его содержимым. Вы можете добавить любой текст, который посчитаете необходимым для своей диаграммы.

```csharp
// Введите текст.
textbox0.Text = "Sales By Region";
```
Вы можете заменить «Продажи по регионам» любым текстом, соответствующим вашим данным.

## Шаг 6: Настройте свойства текстового поля

Теперь давайте сделаем наш TextBox красивым! Вы можете настроить различные свойства, такие как цвет шрифта, размер и стиль.

```csharp
// Установите цвет шрифта.
textbox0.Font.Color = Color.Maroon; // Измените на желаемый цвет

// Установите жирный шрифт.
textbox0.Font.IsBold = true;

// Установите размер шрифта.
textbox0.Font.Size = 14;

// Установите атрибут шрифта на курсив.
textbox0.Font.IsItalic = true;
```

Каждая из этих строк изменяет внешний вид текста внутри текстового поля, улучшая его видимость и привлекательность.

## Шаг 7: Отформатируйте внешний вид текстового поля

Также важно отформатировать фон и границу TextBox. Это выделяет его на графике.

```csharp
// Получить формат заполнения текстового поля.
Aspose.Cells.Drawing.FillFormat fillformat = textbox0.Fill;

// Получить тип формата строки текстового поля.
Aspose.Cells.Drawing.LineFormat lineformat = textbox0.Line;

// Установите толщину линии.
lineformat.Weight = 2;

// Установите сплошной стиль штриха.
lineformat.DashStyle = Aspose.Cells.Drawing.MsoLineDashStyle.Solid;
```

Эти параметры позволяют задать фоновую заливку текстового поля и настроить его границу.

## Шаг 8: Сохраните измененный файл Excel.

Последний шаг — сохранить внесенные изменения в новый файл Excel. Это гарантирует, что ваш исходный файл останется нетронутым.

```csharp
// Сохраните файл Excel.
workbook.Save(outputDir + "outputAddingTextBoxControlInChart.xls");
```
 Заменять`"outputAddingTextBoxControlInChart.xls"` с любым именем файла, которое вы предпочитаете.

## Заключение

Поздравляем! Вы успешно добавили элемент управления TextBox в диаграмму с помощью Aspose.Cells для .NET. Это простое, но эффективное изменение может сделать ваши диаграммы более информативными и визуально привлекательными. Представление данных является ключом к эффективной коммуникации, и с такими инструментами, как Aspose, у вас есть возможность улучшить это представление с минимальными усилиями.

## Часто задаваемые вопросы

### Что такое Aspose.Cells для .NET?
Aspose.Cells для .NET — это мощная библиотека для создания, обработки и преобразования файлов Excel без необходимости использования Microsoft Excel.

### Можно ли добавить несколько текстовых полей в одну диаграмму?
Да! Вы можете добавить столько текстовых полей, сколько вам нужно, повторяя шаги создания текстовых полей с разными позициями.

### Можно ли использовать Aspose.Cells бесплатно?
 Aspose.Cells — платная библиотека, но вы можете загрузить бесплатную пробную версию с сайта[здесь](https://releases.aspose.com/).

### Где я могу найти дополнительную документацию по Aspose.Cells?
 Вы можете получить доступ к полной документации[здесь](https://reference.aspose.com/cells/net/).

### Как мне получить поддержку, если у меня возникнут проблемы?
 Вы можете обратиться за помощью через форум поддержки Aspose.[здесь](https://forum.aspose.com/c/cells/9).