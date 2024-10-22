---
title: Добавить элемент управления «Прямоугольник» на рабочий лист в Excel
linktitle: Добавить элемент управления «Прямоугольник» на рабочий лист в Excel
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как добавить элемент управления «Прямоугольник» на лист Excel с помощью Aspose.Cells для .NET, воспользовавшись подробным пошаговым руководством.
type: docs
weight: 25
url: /ru/net/excel-shapes-controls/add-rectangle-control-to-worksheet-excel/
---
## Введение
Когда дело доходит до автоматизации задач Excel, Aspose.Cells for .NET — это мощный инструмент, который может помочь вам достичь различных целей, одной из которых является добавление фигур, таких как прямоугольники, на ваши рабочие листы. В этом руководстве мы рассмотрим, как добавить элемент управления прямоугольником на рабочий лист Excel с помощью Aspose.Cells for .NET. К концу вы сможете создавать, настраивать и сохранять рабочий лист со встроенным в него элементом управления прямоугольником.
Но прежде чем приступить к делу, давайте поговорим о необходимых условиях.
## Предпосылки
Чтобы следовать этому руководству, убедитесь, что у вас выполнены следующие предварительные условия:
1.  Библиотека Aspose.Cells для .NET: если вы этого еще не сделали,[скачать библиотеку](https://releases.aspose.com/cells/net/) или установите его с помощью NuGet в Visual Studio.
2. .NET Framework: на вашем компьютере должна быть настроена среда разработки .NET.
3. Базовые знания C#: Хотя мы и будем вести вас шаг за шагом, базовые знания C# и объектно-ориентированного программирования будут полезны.
4.  Лицензия: использование Aspose.Cells в ознакомительном режиме отлично подходит для базовых задач, но для полной функциональности рассмотрите возможность приобретения[временная лицензия](https://purchase.aspose.com/temporary-license/)или купив его у[здесь](https://purchase.aspose.com/buy).
Теперь давайте погрузимся в код!
## Импортные пакеты
Чтобы начать работу с Aspose.Cells, убедитесь, что вы импортировали необходимые пространства имен в свой проект. Эти импорты позволят получить доступ к различным классам и методам, которые вам нужны для взаимодействия с файлами Excel.
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
```
Эти строки гарантируют, что ваш проект сможет взаимодействовать с файловыми каталогами (`System.IO`), книги Excel (`Aspose.Cells`), и рисование фигур (`Aspose.Cells.Drawing`).
Теперь давайте разобьем этот процесс на простые шаги, чтобы вы могли легко его повторить и повторить в своих собственных проектах.
## Шаг 1: Настройка пути к каталогу
Первое, что вам нужно сделать, это определить каталог, в котором будет сохранен ваш файл Excel. Этот шаг гарантирует, что ваш проект будет знать, где создать и сохранить выходной файл.
### Определение каталога данных
```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";
```
 Здесь вы указываете путь к каталогу, где будет сохранен файл Excel. Вы можете заменить`"Your Document Directory"` с фактическим путем на вашем компьютере или динамически создать папку, если она не существует.
### Проверка и создание каталога
```csharp
//Создайте каталог, если его еще нет.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Этот блок проверяет, существует ли каталог. Если нет, он его создает. Думайте об этом как о том, чтобы подготовить картотечный шкаф перед тем, как вы сохраните какие-либо документы.
## Шаг 2: Создание новой рабочей книги
 На этом этапе вы создаете новую книгу Excel, используя`Aspose.Cells.Workbook` класс. Это будет служить контейнером для вашего рабочего листа и фигур.
```csharp
// Создайте новую рабочую книгу.
Workbook excelbook = new Workbook();
```
 Позвонив по номеру`Workbook` конструктор, теперь у вас есть пустая книга Excel, готовая к настройке.
## Шаг 3: Добавление элемента управления «Прямоугольник»
Вот где происходит волшебство. Вы добавите прямоугольную фигуру на первый лист вашей рабочей книги.
```csharp
// Добавьте прямоугольный элемент управления.
Aspose.Cells.Drawing.RectangleShape rectangle = excelbook.Worksheets[0].Shapes.AddRectangle(3, 0, 2, 0, 70, 130);
```
Давайте разберемся:
- `excelbook.Worksheets[0]`: Это открывает доступ к первому листу в вашей рабочей книге.
- `.Shapes.AddRectangle(3, 0, 2, 0, 70, 130)`: Это добавляет прямоугольную форму на рабочий лист. Параметры здесь определяют положение (строка и столбец), а также ширину и высоту прямоугольника.
## Шаг 4: Настройка прямоугольника
Недостаточно просто добавить прямоугольник — вам нужно будет его настроить. На этом этапе мы зададим размещение, толщину линии и стиль штрихов прямоугольника.
### Установка размещения
```csharp
// Задайте расположение прямоугольника.
rectangle.Placement = PlacementType.FreeFloating;
```
Это указывает на то, что прямоугольник является свободно перемещаемым, то есть он не будет ограничен размерами ячейки.
### Установка толщины линии
```csharp
// Установите толщину линии.
rectangle.Line.Weight = 4;
```
Здесь мы устанавливаем толщину линии прямоугольника в 4 пункта. Чем больше число, тем толще линия.
### Настройка стиля тире
```csharp
// Установите стиль штриховки прямоугольника.
rectangle.Line.DashStyle = MsoLineDashStyle.Solid;
```
 Эта строка устанавливает стиль штриха границы прямоугольника на сплошной. Вы можете экспериментировать с различными стилями, например`Dash` или`Dot` в зависимости от Ваших требований.
## Шаг 5: Сохранение рабочей книги
После добавления и настройки прямоугольника последним шагом будет сохранение книги в указанном каталоге.
```csharp
// Сохраните файл Excel.
excelbook.Save(dataDir + "book1.out.xls");
```
 Это сохранит рабочую книгу как`.xls` файл в папке, которую вы определили ранее. Вы можете изменить формат файла, изменив расширение, например`.xlsx` если вы предпочитаете более новый формат Excel.
## Заключение
И вот оно! Добавление элемента управления прямоугольником в лист Excel с помощью Aspose.Cells для .NET — это простой процесс, если вы разобьете его пошагово. Если вам нужно добавить фигуры для визуальной привлекательности, выделить разделы данных или настроить отчеты, Aspose.Cells дает вам гибкость, чтобы сделать это программно.
Это руководство должно было снабдить вас всеми знаниями, необходимыми для начала добавления фигур, таких как прямоугольники, в ваши листы Excel с помощью Aspose.Cells. Теперь пришло время поэкспериментировать и посмотреть, чего еще можно достичь с помощью этой мощной библиотеки!
## Часто задаваемые вопросы
### Могу ли я добавлять другие фигуры, например круги или линии, с помощью Aspose.Cells для .NET?  
Да, Aspose.Cells позволяет добавлять различные фигуры, включая круги, линии, стрелки и многое другое.
### Какие еще свойства можно задать для элемента управления «Прямоугольник»?  
Вы можете настроить цвет заливки, цвет линии, прозрачность и даже добавить текст внутри прямоугольника.
### Совместим ли Aspose.Cells с .NET Core?  
Да, Aspose.Cells поддерживает .NET Core, а также .NET Framework и другие платформы на базе .NET.
### Можно ли расположить прямоугольник относительно определенной ячейки?  
 Да, вы можете поместить прямоугольник в определенные строки и столбцы или использовать`PlacementType` контролировать, как он закреплен.
### Существует ли бесплатная пробная версия Aspose.Cells?  
 Да, вы можете получить[бесплатная пробная версия](https://releases.aspose.com/) с веб-сайта, чтобы протестировать возможности библиотеки перед покупкой.