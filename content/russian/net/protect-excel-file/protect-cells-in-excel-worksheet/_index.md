---
title: Защитите ячейки на листе Excel
linktitle: Защитите ячейки на листе Excel
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как защитить определенные ячейки в Excel с помощью Aspose.Cells для .NET. Пошаговое руководство по C#.
type: docs
weight: 30
url: /ru/net/protect-excel-file/protect-cells-in-excel-worksheet/
---
Microsoft Excel — широко используемый инструмент для создания электронных таблиц и управления ими. Одной из основных функций Excel является возможность защищать определенные ячейки для сохранения целостности данных. В этом руководстве мы шаг за шагом проведем вас по защите определенных ячеек в электронной таблице Excel с помощью Aspose.Cells для .NET. Aspose.Cells for .NET — это мощная библиотека программирования, которая позволяет легко манипулировать файлами Excel, обеспечивая большую гибкость и расширенные функции. Следуйте инструкциям, чтобы узнать, как защитить важные ячейки и обеспечить безопасность ваших данных.

## Шаг 1. Настройка среды

Убедитесь, что в вашей среде разработки установлен Aspose.Cells for .NET. Загрузите библиотеку с официального сайта Aspose и проверьте документацию на наличие инструкций по установке.

## Шаг 2. Инициализация книги и листа

Для начала нам нужно создать новую книгу и получить ссылку на лист, ячейки которого мы хотим защитить. Используйте следующий код:

```csharp
// Путь к каталогу документов.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Создайте каталог, если он еще не существует.
bool exists = System.IO.Directory.Exists(dataDir);
if (! exists)
     System.IO.Directory.CreateDirectory(dataDir);

// Создать новую книгу
Workbook workbook = new Workbook();

// Получите первый рабочий лист
Worksheet sheet = workbook.Worksheets[0];
```

 В этом фрагменте кода мы сначала определяем путь к каталогу, в котором будет сохранен файл Excel. Далее мы создаем новый экземпляр`Workbook` класс и получите ссылку на первый лист, используя`Worksheets` свойство.

## Шаг 3: Определите стиль ячейки

Теперь нам нужно определить стиль ячеек, которые мы хотим защитить. Используйте следующий код:

```csharp
// Определить объект стиля
Styling styling;

// Перебрать все столбцы на листе и разблокировать их.
for (int i = 0; i <= 255; i++)
{
     style = sheet.Cells.Columns[(byte)i].Style;
     style. IsLocked = false;
     leaf.Cells.Columns[(byte)i].ApplyStyle(style, new StyleFlag { Locked = true });
}
```

 В этом коде мы используем цикл для перебора всех столбцов на листе и разблокировки их ячеек, установив стиль`IsLocked` собственность`false` . Затем мы используем`ApplyStyle` метод для применения стиля к столбцам с помощью`StyleFlag` флаг для блокировки ячеек.

## Шаг 4: Защитите определенные клетки

Теперь мы собираемся защитить конкретные ячейки, которые хотим заблокировать. Используйте следующий код:

```csharp
// Заблокируйте три ячейки: A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style. IsLocked = true;
sheet.Cells["A1"].SetStyle(style);

style = sheet.Cells["B1"].GetStyle();
style. IsLocked = true;
sheet.Cells["B1"].SetStyle(style);

style = sheet.Cells["C1"].GetStyle();
style. IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
```

 В этом коде мы получаем стиль каждой конкретной ячейки, используя метод`GetStyle` метод, а затем мы устанавливаем`IsLocked` свойство стиля`true`чтобы запереть ячейку. Наконец, мы применяем обновленный стиль к каждой ячейке, используя`SetStyle` метод.

## Шаг 5. Защита листа

Теперь, когда мы определили ячейки, которые необходимо защитить, мы можем защитить сам лист. Используйте следующий код:

```csharp
// Защитите рабочий лист
leaf.Protect(ProtectionType.All);
```

 Этот код использует`Protect` метод защиты листа с указанным типом защиты, в данном случае`ProtectionType.All` который защищает все элементы на листе.

## Шаг 6. Сохраните файл Excel.

Наконец, сохраняем файл Excel с внесенными изменениями. Используйте следующий код:

```csharp
// Сохраните файл Excel
workbook.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

 В этом коде мы используем`Save` метод для сохранения книги в указанном каталоге с помощью`Excel97To2003` формат.

### Пример исходного кода для защиты ячеек на листе Excel с использованием Aspose.Cells для .NET 
```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создайте каталог, если он еще не существует.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Создайте новую книгу.
Workbook wb = new Workbook();
// Создайте объект рабочего листа и получите первый лист.
Worksheet sheet = wb.Worksheets[0];
// Определите объект стиля.
Style style;
// Определите объект styleflag
StyleFlag styleflag;
// Просмотрите все столбцы на листе и разблокируйте их.
for (int i = 0; i <= 255; i++)
{
    style = sheet.Cells.Columns[(byte)i].Style;
    style.IsLocked = false;
    styleflag = new StyleFlag();
    styleflag.Locked = true;
    sheet.Cells.Columns[(byte)i].ApplyStyle(style, styleflag);
}
// Заблокируйте три ячейки... т.е. A1, B1, C1.
style = sheet.Cells["A1"].GetStyle();
style.IsLocked = true;
sheet.Cells["A1"].SetStyle(style);
style = sheet.Cells["B1"].GetStyle();
style.IsLocked = true;
sheet.Cells["B1"].SetStyle(style);
style = sheet.Cells["C1"].GetStyle();
style.IsLocked = true;
sheet.Cells["C1"].SetStyle(style);
// Наконец, защитите лист сейчас.
sheet.Protect(ProtectionType.All);
// Сохраните файл Excel.
wb.Save(dataDir + "output.xls", SaveFormat.Excel97To2003);
```

## Заключение

Поздравляем! Вы узнали, как защитить определенные ячейки в электронной таблице Excel с помощью Aspose.Cells для .NET. Теперь вы можете применить эту технику в своих проектах и повысить безопасность файлов Excel.


### Часто задаваемые вопросы

#### Вопрос: Почему мне следует использовать Aspose.Cells for .NET для защиты ячеек в электронной таблице Excel?

О: Aspose.Cells for .NET — это мощная библиотека, упрощающая работу с файлами Excel. Он предлагает расширенные функции для защиты ячеек, разблокировки диапазонов и т. д.

#### Вопрос: Можно ли защитить диапазоны ячеек вместо отдельных ячеек?

 О: Да, вы можете определить определенные диапазоны ячеек для защиты, используя`ApplyStyle` метод с соответствующим`StyleFlag`.

#### Вопрос: Как открыть защищенный файл Excel после его сохранения?

О: Когда вы открываете защищенный файл Excel, вам необходимо будет ввести пароль, указанный при защите листа.

#### Вопрос: Существуют ли другие типы защиты, которые я могу применить к электронной таблице Excel?

О: Да, Aspose.Cells для .NET поддерживает несколько типов защиты, например, защиту структуры, защиту окон и т. д. Вы можете выбрать подходящий тип защиты в соответствии с вашими потребностями.