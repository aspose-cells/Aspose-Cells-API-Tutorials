---
title: Настройка форматов отображения с помощью пользовательских чисел
linktitle: Настройка форматов отображения с помощью пользовательских чисел
second_title: API обработки Excel Aspose.Cells .NET
description: Узнайте, как настроить форматы отображения с помощью Aspose.Cells для .NET. Форматируйте даты, проценты и валюту, используя это пошаговое руководство.
type: docs
weight: 11
url: /ru/net/number-and-display-formats-in-excel/customizing-display-formats-with-user-defined-numbers/
---
## Введение
Работа с файлами Excel часто требует пользовательского форматирования ячеек для представления данных в более осмысленном и удобном для пользователя виде. Представьте, что вы создаете файл Excel для отчета. Вам нужны не просто сырые числа. Вы хотите, чтобы даты, проценты и валюты выглядели гладко и профессионально, верно? Вот где в игру вступают пользовательские форматы отображения. В этом руководстве мы глубоко погружаемся в Aspose.Cells для .NET, чтобы показать вам, как настраивать формат отображения чисел с помощью пользовательских настроек.
## Предпосылки
Прежде чем начать, убедитесь, что у вас все готово для выполнения этого руководства. Вот что вам понадобится:
-  Aspose.Cells для .NET установлен.[Загрузить здесь](https://releases.aspose.com/cells/net/).
- Базовые знания C# и .NET Framework.
-  Действующая лицензия для Aspose.Cells. Если у вас ее нет, возьмите[бесплатная пробная версия](https://releases.aspose.com/) или запросить[временная лицензия](https://purchase.aspose.com/temporary-license/).
- IDE, подобная Visual Studio.
- .NET Framework 4.0 или выше.
 Если вам чего-то не хватает, не волнуйтесь. Вы всегда можете вернуться к этим ссылкам, чтобы загрузить необходимые файлы или обратиться за помощью к[Форум поддержки Aspose](https://forum.aspose.com/c/cells/9).
## Импорт пространств имен
Прежде чем приступить к написанию кода, вам необходимо импортировать требуемые пространства имен для доступа ко всем необходимым функциям Aspose.Cells.
```csharp
using System.IO;
using Aspose.Cells;
using System;
```
Эти два пространства имен будут вашими основными инструментами в этом руководстве. Теперь перейдем к самой интересной части:
## Шаг 1: Настройка каталога проекта
Во-первых, вам нужно место для хранения файлов, верно? Давайте создадим каталог для сохранения выходного файла Excel. На этом этапе мы также убедимся, что каталог существует, прежде чем что-либо сохранять.
```csharp
// Путь к каталогу документов.
string dataDir = "Your Document Directory";
// Создайте каталог, если его еще нет.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
-  Мы определяем`dataDir` переменная для хранения пути, по которому будет сохранен выходной файл Excel.
-  Затем мы проверяем, существует ли каталог, используя`System.IO.Directory.Exists()`.
-  Если каталог не существует, он будет создан с помощью`System.IO.Directory.CreateDirectory()`.
## Шаг 2: Создайте новую рабочую книгу и добавьте рабочий лист
Теперь, когда у нас есть каталог, давайте создадим новую книгу Excel и добавим в нее рабочий лист.
```csharp
// Создание объекта Workbook
Workbook workbook = new Workbook();
// Добавление нового рабочего листа к объекту Excel
int i = workbook.Worksheets.Add();
// Получение ссылки на недавно добавленный рабочий лист путем передачи его индекса листа
Worksheet worksheet = workbook.Worksheets[i];
```
-  Сначала мы создаем новый`Workbook` объект. Подумайте об этом как о вашем файле Excel.
-  Мы добавляем новый рабочий лист в эту книгу с помощью`Add()`метод и сохранить индекс в переменной`i`.
-  Мы ссылаемся на этот рабочий лист, используя`workbook.Worksheets[i]`.
## Шаг 3: Добавление даты в ячейку и настройка ее формата
 Теперь давайте вставим текущую дату в ячейку и отформатируем ее для отображения в пользовательском виде. Вместо формата даты по умолчанию мы установим пользовательский формат, например`d-mmm-yy`.
```csharp
// Добавление текущей системной даты в ячейку «A1»
worksheet.Cells["A1"].PutValue(DateTime.Now);
// Получение стиля ячейки А1
Style style = worksheet.Cells["A1"].GetStyle();
// Установка пользовательского формата отображения для отображения даты в виде «д-ммм-гг»
style.Custom = "d-mmm-yy";
// Применение стиля к ячейке А1
worksheet.Cells["A1"].SetStyle(style);
```
-  Добавляем текущую системную дату в ячейку`A1` с использованием`PutValue(DateTime.Now)`.
-  Мы извлекаем текущий стиль ячейки`A1` с использованием`GetStyle()`.
-  Мы изменяем стиль ячейки, устанавливая`style.Custom = "d-mmm-yy"`, который форматирует дату, отображая день, сокращенный месяц и год.
-  Наконец, мы применяем новый стиль к ячейке с`SetStyle()`.
## Шаг 4: Форматирование ячейки в виде процентов
 Далее, давайте поработаем с числами. Мы добавим числовое значение в другую ячейку, скажем`A2`и отформатируйте его как процент.
```csharp
//Добавление числового значения в ячейку «A2»
worksheet.Cells["A2"].PutValue(20);
// Получение стиля ячейки А2
style = worksheet.Cells["A2"].GetStyle();
// Настройка пользовательского формата отображения для отображения значения в процентах
style.Custom = "0.0%";
// Применение стиля к ячейке А2
worksheet.Cells["A2"].SetStyle(style);
```
-  Мы добавляем ценность`20` в ячейку`A2`.
-  Мы извлекаем стиль ячейки`A2` и установите пользовательский формат`0.0%` для отображения значения в процентах (например, 20%).
-  Наконец, мы применяем стиль к ячейке с помощью`SetStyle()`.
## Шаг 5: Форматирование ячейки как валюты
 Давайте добавим еще одно значение, скажем, в ячейку`A3`, и отформатируем его для отображения в виде валюты. Чтобы сделать вещи более интересными, мы будем использовать формат, который отображает положительные значения как валюту в фунтах, а отрицательные значения в долларах.
```csharp
// Добавление числового значения в ячейку «A3»
worksheet.Cells["A3"].PutValue(2546);
// Получение стиля ячейки А3
style = worksheet.Cells["A3"].GetStyle();
// Настройка пользовательского формата отображения для отображения значения в виде валюты
style.Custom = "£#,##0;[Red]$-#,##0";
// Применение стиля к ячейке А3
worksheet.Cells["A3"].SetStyle(style);
```
-  Мы добавляем ценность`2546` в ячейку`A3`.
-  Мы устанавливаем индивидуальный формат`£#,##0;[Red]$-#,##0`, который отображает положительные значения со знаком решетки, а отрицательные значения — красным со знаком доллара.
- Применяем стиль к ячейке с помощью`SetStyle()`.
## Шаг 6: Сохранение рабочей книги
Последний шаг — сохранить книгу как файл Excel. Для этого урока мы будем использовать формат Excel 97-2003.
```csharp
// Сохранение файла Excel
workbook.Save(dataDir + "book1.out.xls", SaveFormat.Excel97To2003);
```
-  The`Save()` метод сохраняет книгу в указанном каталоге.
-  Мы выбираем`SaveFormat.Excel97To2003` для обеспечения совместимости со старыми версиями Excel.
## Заключение
Вот и все! Мы только что создали файл Excel, добавили пользовательские форматы даты, процентов и валюты в определенные ячейки с помощью Aspose.Cells для .NET и сохранили файл. Пользовательское форматирование делает ваши файлы Excel гораздо более читабельными и профессиональными. Не забудьте изучить другие параметры форматирования в Aspose.Cells, такие как условное форматирование, для еще большего контроля над тем, как выглядят ваши данные.
## Часто задаваемые вопросы
### Как применить более сложные параметры форматирования в Aspose.Cells?
Вы можете комбинировать различные стили форматирования, такие как цвет шрифта, границ и цвета фона, с пользовательскими числовыми форматами.
### Можно ли применить пользовательский числовой формат к диапазону ячеек?
Да, Aspose.Cells позволяет применять стиль к диапазону ячеек с помощью`Range.SetStyle()` метод.
### В каких еще форматах файлов я могу сохранить рабочую книгу?
 Aspose.Cells поддерживает множество форматов, включая XLSX, CSV и PDF. Просто измените`SaveFormat` в`Save()` метод.
### Можно ли форматировать отрицательные числа по-другому?
Конечно! Вы можете использовать пользовательские числовые форматы для отображения отрицательных чисел разными цветами или символами.
### Является ли Aspose.Cells для .NET бесплатным?
 Aspose.Cells предлагает бесплатную пробную версию, но для полной функциональности вам понадобится действующая лицензия. Вы можете получить[временная лицензия здесь](https://purchase.aspose.com/temporary-license/).