---
title: Сохранение рабочей книги в строгом формате Open XML в .NET
linktitle: Сохранение рабочей книги в строгом формате Open XML в .NET
second_title: API обработки Excel Aspose.Cells .NET
description: В этом подробном руководстве вы узнаете, как сохранить книгу в формате Strict Open XML Spreadsheet с помощью Aspose.Cells для .NET.
type: docs
weight: 19
url: /ru/net/converting-excel-files-to-other-formats/saving-workbook-to-strict-open-xml-spreadsheet-format/
---
## Введение
Привет! Если вы погружаетесь в мир обработки файлов Excel с помощью .NET, вы попали по адресу. Сегодня мы рассмотрим, как сохранить книгу в формате Strict Open XML Spreadsheet с помощью Aspose.Cells для .NET. Этот формат необходим, если вы хотите обеспечить максимальную совместимость и соответствие стандартам в ваших файлах Excel. Думайте об этом как о создании красиво оформленного, высококачественного документа, который может оценить каждый!
Итак, что это вам даст? Ну, к концу этого руководства вы не только будете знать, как сохранить книгу в этом формате, но и будете иметь четкое представление о том, как манипулировать файлами Excel с помощью Aspose.Cells. Готовы к работе? Давайте начнем!
## Предпосылки
Прежде чем мы перейдем к коду, давайте убедимся, что у вас есть все необходимое. Вот что вам понадобится:
1.  Visual Studio: Убедитесь, что Visual Studio установлена на вашем компьютере. Если у вас ее еще нет, вы можете скачать ее[здесь](https://visualstudio.microsoft.com/).
2.  Aspose.Cells для .NET: Вам нужно будет добавить Aspose.Cells в свой проект. Вы можете загрузить его с сайта или использовать NuGet Package Manager в Visual Studio. Вы можете найти пакет[здесь](https://releases.aspose.com/cells/net/).
3. Базовые знания C#: Вы должны быть знакомы с базовыми концепциями программирования на C#. Если вы раньше занимались кодированием, то вы готовы!
4. Выходной каталог: Решите, где вы хотите сохранить файл Excel. Создайте папку на своем компьютере, чтобы все было организовано.
Теперь, когда вы выполнили все необходимые предварительные требования, давайте перейдем к написанию кода!
## Импортные пакеты
Сначала самое главное: нам нужно импортировать необходимые пакеты. Вот как вы сообщаете коду, какие библиотеки использовать. Вот как это сделать:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Эта простая строка кода — ваш шлюз для доступа ко всем мощным функциям, которые предлагает Aspose.Cells. Обязательно поместите ее в начало вашего файла C#. 
Давайте разобьем процесс на управляемые шаги, ладно? Мы вместе пройдемся по каждой части кода.
## Шаг 1: Настройте выходной каталог
Прежде чем что-либо делать, вам нужно настроить выходной каталог. Это место, где будет сохранен ваш файл Excel. Вот как это можно сделать:
```csharp
// Выходной каталог
string outputDir = "Your Document Directory";
```
 Заменять`"Your Document Directory"` с фактическим путем, по которому вы хотите сохранить файл. Например, если вы хотите сохранить его в папке «ExcelFiles» на рабочем столе, вы должны написать:
```csharp
string outputDir = @"C:\Users\YourUsername\Desktop\ExcelFiles\";
```
## Шаг 2: Создайте рабочую книгу
Теперь, когда вы задали выходной каталог, пришло время создать новую рабочую книгу. Рабочая книга — это, по сути, файл Excel, который может содержать несколько рабочих листов. Вот как ее создать:
```csharp
// Создать рабочую тетрадь.
Workbook wb = new Workbook();
```
 Эта строка кода инициализирует новый экземпляр`Workbook` класс. Вы можете представить это как открытие нового пустого файла Excel, готового для заполнения данными!
## Шаг 3: Укажите параметры соответствия
Далее нам нужно указать, что мы хотим сохранить нашу книгу в формате Strict Open XML Spreadsheet. Это важный шаг для обеспечения совместимости с другими программами Excel. Вот как это сделать:
```csharp
// Укажите - Строгая электронная таблица Open XML - Формат.
wb.Settings.Compliance = OoxmlCompliance.Iso29500_2008_Strict;
```
 Установив соответствие`OoxmlCompliance.Iso29500_2008_Strict`, вы сообщаете Aspose.Cells, что хотите, чтобы ваша рабочая книга строго соответствовала стандартам Open XML.
## Шаг 4: Добавьте данные на рабочий лист
А теперь самое интересное! Давайте добавим немного данных на наш рабочий лист. Мы напишем сообщение в ячейке B4, чтобы указать, что наш файл находится в формате Strict Open XML. Вот как:
```csharp
// Добавьте сообщение в ячейку B4 первого рабочего листа.
Cell b4 = wb.Worksheets[0].Cells["B4"];
b4.PutValue("This Excel file has Strict Open XML Spreadsheet format.");
```
На этом этапе мы получаем доступ к первому рабочему листу (рабочие листы индексируются с нуля) и вставляем наше сообщение в ячейку B4. Это как прикрепить записку в файл Excel!
## Шаг 5: Сохраните рабочую книгу
Мы почти у цели! Последний шаг — сохранить вашу рабочую книгу в выходной каталог, который мы указали ранее. Вот код для этого:
```csharp
// Сохранить в выходной файл Excel.
wb.Save(outputDir + "outputSaveWorkbookToStrictOpenXMLSpreadsheetFormat.xlsx", SaveFormat.Xlsx);
```
 Эта строка кода берет вашу рабочую книгу и сохраняет ее как`.xlsx` файл в указанном каталоге. Вы можете назвать свой файл как угодно; просто убедитесь, что вы сохранили`.xlsx` расширение.
## Шаг 6: Подтвердите успех
В завершение давайте добавим небольшое подтверждающее сообщение, которое сообщит нам, что все выполнено успешно:
```csharp
Console.WriteLine("SaveWorkbookToStrictOpenXMLSpreadsheetFormat executed successfully.");
```
Это простой способ проверить, что ваш код работает без сбоев. Если при запуске программы вы видите это сообщение в консоли, значит, вы это сделали!
## Заключение
И вот оно! Вы только что узнали, как сохранить книгу в формате Strict Open XML Spreadsheet с помощью Aspose.Cells для .NET. Это как освоить новый рецепт на кухне — теперь у вас есть инструменты и знания для создания красивых файлов Excel, совместимых и соответствующих отраслевым стандартам.
Независимо от того, управляете ли вы данными для своего бизнеса или составляете отчеты для школы, этот навык вам пригодится. Так что вперед, экспериментируйте с различными функциями в Aspose.Cells и смотрите, что вы можете создать!
## Часто задаваемые вопросы
### Что такое формат Strict Open XML Spreadsheet?
Формат Strict Open XML Spreadsheet строго соответствует стандартам Open XML, обеспечивая совместимость с различными приложениями.
### Могу ли я использовать Aspose.Cells бесплатно?
 Да! Вы можете начать с бесплатной пробной версии Aspose.Cells, чтобы изучить ее возможности. Загрузить ее[здесь](https://releases.aspose.com/).
### Где я могу найти более подробную информацию об Aspose.Cells?
 Подробные руководства и ссылки на API можно найти в документации.[здесь](https://reference.aspose.com/cells/net/).
### Как получить поддержку по Aspose.Cells?
 Если у вас есть вопросы или вам нужна помощь, вы можете посетить форум поддержки.[здесь](https://forum.aspose.com/c/cells/9).
### Могу ли я сохранить рабочую книгу в разных форматах?
Конечно! Aspose.Cells позволяет вам сохранять вашу рабочую книгу в различных форматах, таких как PDF, CSV и других, в зависимости от ваших потребностей.