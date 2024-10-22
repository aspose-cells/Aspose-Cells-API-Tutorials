---
title: Извлечь объект OLE из Excel
linktitle: Извлечь объект OLE из Excel
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как извлекать объекты OLE из файлов Excel с помощью Aspose.Cells для .NET. Пошаговое руководство для простого извлечения.
type: docs
weight: 10
url: /ru/net/excel-ole-picture-objects/extract-ole-object-from-excel/
---
## Введение
В современном мире, продвинутом в технологиях, работа с файлами Excel является обычной задачей, особенно для тех, кто занимается анализом данных, финансами и управлением проектами. Одним из часто упускаемых из виду аспектов является обработка объектов OLE (Object Linking and Embedding) в электронных таблицах Excel. Это могут быть встроенные документы, изображения или даже сложные типы данных, которые играют решающую роль в улучшении функциональности и насыщенности ваших файлов Excel. Если вы пользователь Aspose.Cells, желающий извлечь эти объекты OLE программным способом с помощью .NET, вы попали по адресу! Это руководство проведет вас через процесс шаг за шагом, гарантируя, что вы поймете не только, как это сделать, но и почему каждая часть процесса важна.
## Предпосылки
Прежде чем мы углубимся в детали извлечения объектов OLE, необходимо выполнить несколько действий:
1. Базовые знания C#: Если вы знакомы с C#, вы уже на правильном пути. Если нет, не волнуйтесь! Мы сделаем все просто.
2.  Aspose.Cells установлен: Вам понадобится библиотека Aspose.Cells. Вы можете скачать ее с сайта[здесь](https://releases.aspose.com/cells/net/).
3. Совместимая среда разработки: убедитесь, что у вас настроена и готова к работе среда разработки .NET, например Visual Studio.
4. Образец файла Excel: для тестирования вам понадобится файл Excel со встроенными объектами OLE. 
Как только вы выполните все эти предварительные условия, мы сможем начать наше путешествие в мир извлечения объектов OLE.
## Импортные пакеты
Сначала импортируем необходимые пакеты, которые мы будем использовать в нашем руководстве. В вашем проекте C# вам нужно будет включить пространство имен Aspose.Cells. Вот как это можно сделать:
```csharp
using System.IO;
using Aspose.Cells;
```
## Шаг 1: Укажите каталог документов
На этом этапе мы определим путь, по которому находится наш файл Excel. Вы можете спросить, почему это важно. Это похоже на подготовку сцены для представления — это помогает сценарию узнать, где найти актеров (в нашем случае файл Excel).
```csharp
string dataDir = "Your Document Directory";
```
 Заменять`"Your Document Directory"` с фактическим путем, где находится ваш файл Excel (`book1.xls`) сохраняется.
## Шаг 2: Откройте файл Excel.
Теперь, когда у нас настроен каталог документов, следующим шагом будет открытие файла Excel. Представьте, что вы открываете книгу, прежде чем начать читать — важно увидеть, что внутри.
```csharp
Workbook workbook = new Workbook(dataDir + "book1.xls");
```
## Шаг 3: Доступ к коллекции объектов OLE
Каждый рабочий лист в книге Excel может содержать различные объекты, включая объекты OLE. Здесь мы получаем доступ к коллекции объектов OLE первого рабочего листа. Это похоже на выбор страницы для проверки встроенных изображений и документов.
```csharp
Aspose.Cells.Drawing.OleObjectCollection oles = workbook.Worksheets[0].OleObjects;
```
## Шаг 4: Цикл по объектам OLE
Теперь начинается самое интересное — цикл по всем объектам OLE в нашей коллекции. Этот шаг имеет решающее значение, поскольку он позволяет нам эффективно обрабатывать несколько объектов OLE. Представьте себе, что вы просматриваете сундук с сокровищами, чтобы найти ценные предметы!
```csharp
for (int i = 0; i < oles.Count; i++)
{
    Aspose.Cells.Drawing.OleObject ole = oles[i];
    //Дальнейшая логика для обработки каждого объекта
}
```
## Шаг 5: Укажите имя выходного файла
По мере того, как мы углубляемся в каждый объект OLE, нам нужно придумать имя файла для извлеченных объектов. Зачем? Потому что после того, как мы их извлечем, мы хотим сохранить все организованным, чтобы мы могли легко найти наши сокровища позже.
```csharp
string fileName = dataDir + "ole_" + i + ".";
```
## Шаг 6: Определите тип формата файла
Каждый объект OLE может быть разных типов (например, документы, электронные таблицы, изображения). Крайне важно определить тип формата, чтобы вы могли правильно его извлечь. Это как знать рецепт блюда — вам нужно знать ингредиенты!
```csharp
switch (ole.FileFormatType)
{
    case FileFormatType.Doc:
        fileName += "doc";
        break;
    case FileFormatType.Xlsx:
        fileName += "xlsx";
        break;
    case FileFormatType.Ppt:
        fileName += "ppt";
        break;
    case FileFormatType.Pdf:
        fileName += "pdf";
        break;
    case FileFormatType.Unknown:
        fileName += "jpg";
        break;
    default:
        // Обработка других форматов файлов
        break;
}
```
## Шаг 7: Сохраните OLE-объект
 Теперь перейдем к сохранению объекта OLE. Если объект — это файл Excel, мы сохраним его с помощью`MemoryStream` что позволяет нам обрабатывать данные в памяти перед их записью. Этот шаг сродни упаковке сокровища перед отправкой его другу.
```csharp
if (ole.FileFormatType == FileFormatType.Xlsx)
{
    MemoryStream ms = new MemoryStream();
    ms.Write(ole.ObjectData, 0, ole.ObjectData.Length);
    Workbook oleBook = new Workbook(ms);
    oleBook.Settings.IsHidden = false;
    oleBook.Save(dataDir + "Excel_File" + i + ".out.xlsx");
}
```
 Для других типов файлов мы будем использовать`FileStream` для создания файла на диске.
```csharp
else
{
    FileStream fs = File.Create(fileName);
    fs.Write(ole.ObjectData, 0, ole.ObjectData.Length);
    fs.Close();
}
```

## Заключение
И вот так вы успешно прошли воды извлечения объектов OLE с Aspose.Cells для .NET! Выполнив эти шаги, вы сможете легко извлекать и управлять встроенными объектами из файлов Excel. Помните, как и любой ценный навык, практика приводит к совершенству. Так что не торопитесь, экспериментируйте с различными файлами Excel, и вскоре вы станете профессионалом в извлечении OLE!
## Часто задаваемые вопросы
### Что такое объекты OLE в Excel?
Объекты OLE — это технология, которая позволяет встраивать документы и данные в других приложениях и связываться с ними на рабочем листе Excel.
### Зачем мне нужно извлекать объекты OLE?
Извлечение объектов OLE позволяет получать доступ к встроенным документам или изображениям и управлять ими независимо от исходного файла Excel.
### Может ли Aspose.Cells обрабатывать все типы встроенных файлов?
Да, Aspose.Cells может управлять различными объектами OLE, включая документы Word, таблицы Excel, презентации PowerPoint и изображения.
### Как установить Aspose.Cells для .NET?
 Вы можете установить Aspose.Cells, загрузив его с их сайта[страница релиза](https://releases.aspose.com/cells/net/).
### Где я могу найти поддержку Aspose.Cells?
Вы можете получить поддержку Aspose.Cells на их сайте[форум поддержки](https://forum.aspose.com/c/cells/9).