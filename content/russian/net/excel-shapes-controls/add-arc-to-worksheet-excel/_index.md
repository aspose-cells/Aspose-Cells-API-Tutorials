---
title: Добавить дугу на рабочий лист в Excel
linktitle: Добавить дугу на рабочий лист в Excel
second_title: API обработки Excel Aspose.Cells .NET
description: Научитесь добавлять дуги в листы Excel с помощью Aspose.Cells для .NET. Следуйте нашему пошаговому руководству, чтобы улучшить дизайн ваших электронных таблиц.
type: docs
weight: 16
url: /ru/net/excel-shapes-controls/add-arc-to-worksheet-excel/
---
## Введение
Создание визуально привлекательных таблиц Excel имеет решающее значение для представления данных, и библиотека Aspose.Cells предоставляет разработчикам надежные инструменты для выполнения этой задачи. Одна интересная функция, которую вы, возможно, захотите включить в свои документы Excel, — это возможность добавлять фигуры, такие как дуги. В этом руководстве мы шаг за шагом рассмотрим, как добавлять дуги на лист Excel с помощью Aspose.Cells для .NET. К концу этой статьи вы не только узнаете, как добавлять дуги, но и получите представление об управлении фигурами в целом.
## Предпосылки
Прежде чем мы погрузимся в тонкости добавления дуг на ваш рабочий лист, важно убедиться, что у вас есть несколько вещей на месте. Вот предварительные условия, которые вам понадобятся для начала:
1. Visual Studio: на вашем компьютере должна быть установлена Visual Studio, поскольку в качестве языка программирования мы будем использовать C#.
2. .NET Framework: Убедитесь, что у вас установлен .NET Framework или .NET Core. Aspose.Cells поддерживает оба.
3. Aspose.Cells для .NET: У вас должна быть библиотека Aspose.Cells. Вы можете загрузить ее с[Загрузки Aspose.Cells](https://releases.aspose.com/cells/net/) страница.
4. Базовые знания C#: знакомство с C# поможет вам без особых затруднений разобраться в фрагментах кода.
## Импортные пакеты
Чтобы начать работать с Aspose.Cells в вашем проекте, вам нужно импортировать необходимые пакеты. Вот как это сделать:
### Создать новый проект
- Откройте Visual Studio.
- Выберите «Создать новый проект».
- Выберите шаблон, работающий с .NET (например, консольное приложение).
  
### Добавить ссылки Aspose.Cells
- Щелкните правой кнопкой мыши по вашему проекту в обозревателе решений.
- Выберите «Управление пакетами NuGet».
- Найдите «Aspose.Cells» и установите его.
Теперь вы готовы приступить к кодированию добавления дуги.
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
Ниже приведен пошаговый разбор кода, демонстрирующий, как добавлять дуги на лист в Excel.
## Шаг 1: Настройка каталога
Первый шаг — настроить каталог, в котором вы сохраните свой файл Excel. Это поможет вам легко управлять выходными файлами.
```csharp
string dataDir = "Your Document Directory";
//Создайте каталог, если его еще нет.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
В этом фрагменте кода мы указываем путь к каталогу документов. Мы также проверяем, существует ли каталог; если нет, мы его создаем. Это закладывает основу для нашего вывода.
## Шаг 2: Создание рабочей книги
Далее давайте создадим новый экземпляр рабочей книги.
```csharp
// Создайте новую рабочую книгу.
Workbook excelbook = new Workbook();
```
Эта строка создает новую книгу Excel. Думайте об этом как о чистом холсте, куда мы можем добавлять фигуры, данные и многое другое.
## Шаг 3: Добавьте первую дуговую форму
Теперь давайте добавим на рабочий лист нашу первую дуговую фигуру.
```csharp
// Добавьте форму дуги.
Aspose.Cells.Drawing.ArcShape arc1 = excelbook.Worksheets[0].Shapes.AddArc(2, 0, 2, 0, 130, 130);
```
 Здесь мы добавляем дугу на первый рабочий лист. Параметры определяют положение и размер дуги:`(left, top, width, height, startAngle, endAngle)`. Это как нарисовать сегмент круга!
## Шаг 4: Настройте первую дугу
После добавления дуги вы, возможно, захотите настроить ее внешний вид.
```csharp
// Установите цвет заливки фигуры
arc1.Fill.FillType = FillType.Solid;
arc1.Fill.SolidFill.Color = Color.Blue;
// Установите расположение дуги.
arc1.Placement = PlacementType.FreeFloating;           
// Установите толщину линии.
arc1.Line.Weight = 1;      
// Установите стиль штриховки дуги.
arc1.Line.DashStyle = MsoLineDashStyle.Solid;
```
В этом разделе мы настраиваем дугу. Мы устанавливаем для нее тип заливки сплошным цветом (в данном случае синим), определяем, как она будет размещена, устанавливаем толщину линии и выбираем стиль штриха. По сути, мы наряжаем нашу дугу, чтобы она стала визуально привлекательной!
## Шаг 5: Добавьте вторую дугообразную форму
Давайте добавим еще одну дугообразную форму, чтобы обеспечить больше контекста.
```csharp
// Добавьте еще одну дугообразную форму.
Aspose.Cells.Drawing.ArcShape arc2 = excelbook.Worksheets[0].Shapes.AddArc(9, 0, 2, 0, 130, 130);
```
Подобно первой дуге, мы добавляем вторую дугу на тот же рабочий лист. Координаты здесь немного смещены, чтобы расположить ее по-другому.
## Шаг 6: Настройте вторую дугу
Так же, как мы сделали с первой дугой, мы настроим и вторую.
```csharp
// Установить цвет линии
arc2.Line.FillType = FillType.Solid;
arc2.Line.SolidFill.Color = Color.Blue;
// Установите расположение дуги.
arc2.Placement = PlacementType.FreeFloating;          
// Установите толщину линии.
arc2.Line.Weight = 1;           
// Установите стиль штриховки дуги.
arc2.Line.DashStyle = MsoLineDashStyle.Solid;
```
Здесь мы даем второй дуге тот же стиль, что и первой. Вы можете изменить цвет или стиль по желанию для уникальности или тематических целей.
## Шаг 7: Сохраните рабочую книгу
Наконец, пришло время сохранить вашу новую рабочую книгу с дугами.
```csharp
// Сохраните файл Excel.
excelbook.Save(dataDir + "book1.out.xls");
```
Эта строка работает как нажатие кнопки сохранения. Мы сохраняем нашу работу в указанном месте с указанным именем файла. Обязательно проверьте свой каталог, чтобы увидеть свой шедевр в формате Excel!
## Заключение
В этом уроке мы изучили процесс добавления дуговых фигур на лист Excel с помощью Aspose.Cells for .NET. С помощью простого пошагового руководства вы узнали, как создать новую книгу, добавить дуги, настроить их внешний вид и сохранить документ. Эта возможность не только повышает визуальную привлекательность ваших электронных таблиц, но и делает ваши презентации данных более информативными. Независимо от того, создаете ли вы диаграммы, отчеты или просто экспериментируете, использование таких фигур, как дуги, может добавить творческий поворот в ваши проекты.
## Часто задаваемые вопросы
### Что такое Aspose.Cells?
Aspose.Cells — это мощная библиотека, которая позволяет разработчикам создавать, обрабатывать и конвертировать файлы Excel программным способом без необходимости использования Microsoft Excel.
### Нужно ли мне устанавливать Microsoft Excel для использования Aspose.Cells?
Нет, Aspose.Cells полностью независим и не требует установки Microsoft Excel.
### Могу ли я попробовать Aspose.Cells бесплатно?
Да, вы можете попробовать Aspose.Cells, используя их[Бесплатная пробная версия](https://releases.aspose.com/).
### Какие языки программирования поддерживает Aspose.Cells?
Aspose.Cells поддерживает несколько языков, включая C#, VB.NET и другие.
### Где я могу получить поддержку по Aspose.Cells?
 Вы можете получить поддержку через[Форум Aspose](https://forum.aspose.com/c/cells/9).