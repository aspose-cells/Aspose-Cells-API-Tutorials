---
title: Сохранить книгу в текстовом формате CSV
linktitle: Сохранить книгу в текстовом формате CSV
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как легко преобразовать рабочие книги Excel в формат CSV с помощью Aspose.Cells в этом подробном пошаговом руководстве, разработанном для разработчиков .NET.
type: docs
weight: 17
url: /ru/net/saving-files-in-different-formats/save-workbook-to-text-csv-format/
---
## Введение
При работе с данными выбранный вами формат может действительно определить, насколько легко вы сможете с ними работать. Среди наиболее распространенных форматов для обработки табличных данных — CSV (значения, разделенные запятыми). Если вы разработчик, работающий с файлами Excel, и вам нужно преобразовать рабочие книги в формат CSV, Aspose.Cells for .NET — фантастическая библиотека, которая упрощает эту задачу. В этом руководстве мы разберем шаги для бесшовного преобразования рабочей книги Excel в текстовый формат CSV.
## Предпосылки
Прежде чем приступить к работе, давайте убедимся, что у вас все готово для начала работы:
1. Базовые знания C# и .NET: поскольку мы будем писать код на C#, знакомство с языком и платформой .NET имеет важное значение.
2. Библиотека Aspose.Cells: Убедитесь, что в вашей среде разработки установлена библиотека Aspose.Cells for .NET. Вы можете загрузить ее[здесь](https://releases.aspose.com/cells/net/).
3. Visual Studio или любая C# IDE: Вам понадобится интегрированная среда разработки (IDE) для написания и выполнения кода. Visual Studio — популярный выбор.
4. Рабочая книга Excel: подготовьте образец рабочей книги Excel (например, «book1.xls»), содержащий некоторые данные для проверки преобразования.
## Импортные пакеты
Теперь, когда у нас есть все необходимые условия, первым шагом в этом процессе является импорт необходимых пакетов. В вашем проекте C# вам необходимо включить следующее пространство имен в верхней части вашего файла кода:
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
Эти пространства имен предоставят вам доступ к классам и методам, необходимым для работы с файлами Excel и управления потоками памяти.
## Шаг 1: Определите путь к каталогу документов
Первый шаг в нашем процессе — определить, где хранятся наши документы (книги Excel). Это важно, поскольку позволяет нашей программе знать, где найти файлы, которые ей нужно обработать. 
```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";
```
 Обязательно замените`"Your Document Directory"` с фактическим путем, где находится ваш файл "book1.xls". Это может быть каталог на вашем компьютере или путь к серверу.
## Шаг 2: Загрузите исходную рабочую книгу
Далее нам необходимо загрузить книгу Excel, которая будет преобразована в формат CSV.
```csharp
// Загрузите исходную рабочую книгу
Workbook workbook = new Workbook(dataDir + "book1.xls");
```
 The`Workbook` класс из библиотеки Aspose.Cells позволяет манипулировать и получать доступ к книгам Excel. Передавая путь к файлу, мы загружаем указанную книгу для обработки.
## Шаг 3: Инициализация массива байтов для данных рабочей книги
Прежде чем начать преобразование рабочей книги в CSV, нам необходимо инициализировать пустой массив байтов, который в конечном итоге будет содержать все данные рабочего листа.
```csharp
// 0-байтовый массив
byte[] workbookData = new byte[0];
```
Этот массив байтов объединит данные с каждого рабочего листа в единую структуру, которую мы позже сможем записать в файл.
## Шаг 4: Настройте параметры сохранения текста
Теперь давайте настроим параметры того, как мы хотим сохранить текстовый формат. Вы можете выбрать пользовательские разделители или придерживаться табуляции.
```csharp
// Параметры сохранения текста. Можно использовать любой тип разделителя
TxtSaveOptions opts = new TxtSaveOptions();
opts.Separator = '\t'; // Установка табуляции в качестве разделителя
```
 В этом примере мы используем символ табуляции в качестве разделителя. Вы можете заменить`'\t'` любым символом, например запятой (`,`), в зависимости от того, как вы хотите отформатировать свой CSV.
## Шаг 5: Повторите все рабочие листы
 Далее мы пройдемся по всем рабочим листам в рабочей книге, сохраняя каждый из них в нашем`workbookData` массив, но сначала необходимо выбрать, с каким рабочим листом работать.
```csharp
// Скопируйте данные каждого рабочего листа в текстовом формате в массив данных рабочей книги.
for (int idx = 0; idx < workbook.Worksheets.Count; idx++)
{
    // Сохранить активный рабочий лист в текстовом формате
    MemoryStream ms = new MemoryStream();
    workbook.Worksheets.ActiveSheetIndex = idx;
    workbook.Save(ms, opts);
```
 Цикл проходит по каждому рабочему листу в рабочей книге.`ActiveSheetIndex` настроено так, что каждый раз в цикле мы сохраняем текущий рабочий лист. Результаты будут сохранены в памяти с помощью`MemoryStream`.
## Шаг 6: Извлечение данных из рабочего листа
 После сохранения рабочего листа в потоке памяти следующим шагом будет извлечение этих данных и добавление их в наш`workbookData` множество.
```csharp
    // Сохраните данные рабочего листа в массив данных листа
    ms.Position = 0; // Сбросить позицию потока памяти
    byte[] sheetData = ms.ToArray(); // Получить массив байтов
```
`ms.Position = 0;` сбрасывает позицию для чтения после записи. Затем мы используем`ToArray()` для преобразования потока памяти в массив байтов, содержащий данные рабочего листа.
## Шаг 7: Объедините данные рабочего листа
 Теперь мы объединим данные из каждого рабочего листа в один`workbookData` массив инициализирован ранее.
```csharp
    // Объединить данные этого рабочего листа в массив данных рабочей книги.
    byte[] combinedArray = new byte[workbookData.Length + sheetData.Length];
    Array.Copy(workbookData, 0, combinedArray, 0, workbookData.Length);
    Array.Copy(sheetData, 0, combinedArray, workbookData.Length, sheetData.Length);
    workbookData = combinedArray;
}
```
Мы создаем новый массив, достаточно большой для хранения как существующих данных рабочей книги, так и новых данных рабочего листа. Затем мы копируем существующие и новые данные в этот объединенный массив для дальнейшего использования.
## Шаг 8: Сохраните все данные рабочей книги в файл
 Наконец, со всеми данными, объединенными в нашем`workbookData` массив, мы можем сохранить этот массив в указанном файле.
```csharp
//Сохранить все данные рабочей книги в файл
File.WriteAllBytes(dataDir + "out.txt", workbookData);
```
`WriteAllBytes` берет объединенный массив байтов и записывает его в текстовый файл с именем «out.txt» в указанном каталоге.
## Заключение
И вот оно! Вы успешно преобразовали книгу Excel в формат CSV с помощью Aspose.Cells for .NET. Этот процесс не только эффективен, но и позволяет легко манипулировать данными Excel для дальнейшего анализа или составления отчетов. Теперь вы можете автоматизировать задачи по обработке данных или даже интегрировать эту функциональность в более крупные приложения.
## Часто задаваемые вопросы
### Можно ли использовать разные разделители для CSV-файла?
 Да, вы можете изменить`opts.Separator` на любой символ, например запятую или вертикальную черту.
### Можно ли использовать Aspose.Cells бесплатно?
 Aspose.Cells не бесплатен, но вы можете получить бесплатную пробную версию[здесь](https://releases.aspose.com/).
### В каких форматах, помимо CSV, я могу сохранять данные?
Aspose.Cells позволяет сохранять данные в различных форматах, включая XLSX, PDF и другие.
### Могу ли я обрабатывать большие файлы Excel с помощью Aspose.Cells?
Да, Aspose.Cells разработан для эффективной обработки больших файлов, но производительность может зависеть от системных ресурсов.
### Где я могу найти более подробную документацию?
Вы можете найти подробную документацию и примеры на их[справочный сайт](https://reference.aspose.com/cells/net/).