---
title: Доступ к непримитивным формам в Excel
linktitle: Доступ к непримитивным формам в Excel
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как получить доступ к непримитивным фигурам в Excel с помощью Aspose.Cells для .NET. Откройте для себя пошаговые методологии в этом всеобъемлющем руководстве.
type: docs
weight: 19
url: /ru/net/excel-shape-text-modifications/access-non-primitive-shape-excel/
---
## Введение
Вы когда-нибудь натыкались на непримитивную фигуру в файле Excel и задавались вопросом, как получить доступ к сложным деталям, которые с ней связаны? Если вы разработчик, работающий с .NET и ищущий возможности манипулировать листами Excel, вы в правильном месте! В этой статье мы рассмотрим, как эффективно получать доступ и манипулировать непримитивными фигурами в Excel с помощью библиотеки Aspose.Cells. Мы рассмотрим подробное пошаговое руководство, которое подробно разберет процесс, что сделает его простым даже для новичков в платформе. Итак, устраивайтесь поудобнее и давайте погрузимся в увлекательный мир Aspose.Cells!
## Предпосылки
Прежде чем перейти к коду, необходимо выполнить несколько предварительных условий:
1. Базовые знания C#: знакомство с языком программирования C# необходимо для успешного освоения материала.
2. Visual Studio: На вашем компьютере должна быть установлена Visual Studio. Здесь мы будем писать наш код.
3.  Библиотека Aspose.Cells: Вам понадобится установленная библиотека Aspose.Cells. Вы можете загрузить последнюю версию[здесь](https://releases.aspose.com/cells/net/).
4. Файл Excel: Создайте или получите файл Excel, содержащий непримитивные формы для тестирования. Для этого урока мы будем использовать`"NonPrimitiveShape.xlsx"`.
Как только вы выполните все эти предварительные условия, мы можем приступить к самой интересной части!
## Импортные пакеты
Первый шаг, чтобы все заработало, — импортировать необходимые пакеты в ваш проект C#. Вот что вам нужно сделать:
### Создать новый проект
- Откройте Visual Studio и создайте новый проект консольного приложения C#.
-  Выберите подходящее название для вашего проекта, например`AsposeShapeAccess`.
### Установить пакет Aspose.Cells NuGet
- Щелкните правой кнопкой мыши по проекту в обозревателе решений.
- Выберите «Управление пакетами NuGet».
-  Искать`Aspose.Cells` и нажмите «Установить».
### Импорт пространства имен
 В верхней части вашего`Program.cs` импортируйте пространство имен Aspose.Cells, добавив следующую строку:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Collections;
using System;
```
Теперь давайте перейдем к реальному коду, с помощью которого мы получим доступ к непримитивным фигурам в нашем файле Excel.
## Шаг 1: Укажите путь к документу
Прежде чем перейти к доступу к фигурам, нам нужно указать каталог, в котором находится ваш файл Excel. Вот как это сделать:
```csharp
string dataDir = "Your Document Directory";
```
 Заменять`"Your Document Directory"` с фактическим путем, где ваш`NonPrimitiveShape.xlsx` файл сохранен. 
## Шаг 2: Загрузите рабочую книгу
Теперь, когда мы настроили путь к документу, пришло время загрузить книгу. Вот как это можно сделать:
```csharp
Workbook workbook = new Workbook(dataDir + "NonPrimitiveShape.xlsx");
```
 Эта строка создает новый`Workbook`объект, который считывает указанный вами ранее файл Excel.
## Шаг 3: Доступ к рабочему листу
Далее мы перейдем к первому листу в рабочей книге. Давайте сделаем это:
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
Эта строка обращается к первому листу в вашей книге — Excel работает лучше всего, когда мы ограничиваем свое внимание одним листом за раз.
## Шаг 4: Доступ к пользовательской форме
А теперь самое интересное! Мы получим доступ к пользовательской форме (которая может быть не примитивной) на рабочем листе.
```csharp
Shape shape = worksheet.Shapes[0];
```
Здесь мы получаем доступ к первой фигуре на рабочем листе. Вы можете изменить индекс, если у вас несколько фигур.
## Шаг 5: Проверьте, является ли форма непримитивной
Прежде чем приступить к получению доступа к данным о форме, крайне важно убедиться, что она не является примитивной:
```csharp
if (shape.AutoShapeType == AutoShapeType.NotPrimitive)
{
```
Этот блок гарантирует, что мы работаем только с формами, имеющими более сложные детали.
## Шаг 6: Доступ к данным Shape
Теперь, когда мы убедились, что это непримитивная форма, мы можем получить доступ к ее данным.
```csharp
ShapePathCollection shapePathCollection = shape.Paths;
```
Эта строка извлекает набор путей, которые определяют форму. Думайте об этом как о получении чертежа для дизайна формы!
## Шаг 7: Пройдитесь по каждому пути
Для более глубокого понимания структуры фигуры мы пройдемся по каждому пути, связанному с фигурой:
```csharp
foreach (ShapePath shapePath in shapePathCollection)
{
```
Этот цикл позволит нам углубиться в каждый путь и изучить их детали.
## Шаг 8: Сегменты пути доступа
Каждый контур фигуры может иметь несколько сегментов. Давайте получим к ним доступ!
```csharp
ShapeSegmentPathCollection pathSegments = shapePath.PathSegementList;
```
В этой коллекции хранятся сегменты, составляющие контуры фигуры.
## Шаг 9: Пройдитесь по каждому сегменту пути
Здесь мы переберем каждый сегмент в коллекции сегментов пути:
```csharp
foreach (ShapeSegmentPath pathSegment in pathSegments)
{
```
Вот тут-то и начинается самое интересное: мы подробно рассмотрим каждый сегмент!
## Шаг 10: Точки сегмента пути доступа
Теперь давайте перейдем к отдельным точкам на каждом участке пути:
```csharp
ShapePathPointCollection segmentPoints = pathSegment.Points;
```
Думайте об этом как о сборе всех координат, определяющих изгибы и углы фигуры.
## Шаг 11: Распечатайте данные о точках
Наконец, выведем на консоль сведения о каждой точке сегмента пути:
```csharp
foreach (ShapePathPoint pathPoint in segmentPoints)
{
    Console.WriteLine("X: " + pathPoint.X + ", Y: " + pathPoint.Y);
}
```
Благодаря этому мы фактически выводим координаты каждой точки, определяющей нашу непримитивную форму — фантастический способ визуализировать то, что происходит под капотом!
## Заключение
И вот оно! Вы успешно получили доступ и изучили детали непримитивных фигур в Excel с помощью Aspose.Cells для .NET. Эта мощная библиотека открывает целый мир возможностей для работы с файлами Excel, независимо от того, создаете ли вы отчеты, динамические электронные таблицы или обрабатываете сложные фигуры. Если у вас есть вопросы или вам нужна дополнительная помощь, не стесняйтесь обращаться!
## Часто задаваемые вопросы
### Что такое непримитивные фигуры в Excel?
Непримитивные формы — это сложные фигуры, состоящие из множества сегментов и кривых, а не простые геометрические формы.
### Как установить Aspose.Cells для .NET?
 Вы можете установить его через диспетчер пакетов NuGet в Visual Studio или загрузить с их сайта.[сайт](https://releases.aspose.com/cells/net/).
### Могу ли я использовать Aspose.Cells бесплатно?
Да, вы можете получить бесплатную пробную версию на их веб-сайте, чтобы изучить его возможности.[здесь](https://releases.aspose.com/).
### В чем преимущество использования Aspose.Cells?
Aspose.Cells предоставляет мощные функции для программного управления электронными таблицами Excel без необходимости установки Excel на вашем компьютере.
### Где я могу найти поддержку Aspose.Cells?
 Вы можете получить помощь и поддержку на форуме сообщества Aspose.[здесь](https://forum.aspose.com/c/cells/9).