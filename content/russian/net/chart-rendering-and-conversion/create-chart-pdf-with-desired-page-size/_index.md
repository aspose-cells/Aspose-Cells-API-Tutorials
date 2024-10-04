---
title: Создать диаграмму PDF с желаемым размером страницы
linktitle: Создать диаграмму PDF с желаемым размером страницы
second_title: API обработки Excel Aspose.Cells .NET
description: Создайте PDF с вашей диаграммой Excel с помощью Aspose.Cells для .NET. Узнайте, как это сделать, с помощью этого пошагового руководства.
type: docs
weight: 12
url: /ru/net/chart-rendering-and-conversion/create-chart-pdf-with-desired-page-size/
---
## Введение

Создание визуально привлекательных и информативных диаграмм необходимо для представления данных в различных областях. Независимо от того, имеете ли вы дело с данными о продажах, показателями производительности или любым другим типом информации, возможность создания высококачественных диаграмм придает вашим выводам глубину и ясность. Если вы работаете с приложениями .NET, Aspose.Cells — это мощная библиотека, которая упрощает обработку документов Excel и создание диаграмм. В этом руководстве мы проведем вас через процесс создания PDF-файла диаграммы из файла Excel с желаемым размером страницы.

## Предпосылки

Прежде чем погрузиться в код, необходимо выполнить несколько предварительных условий, чтобы обеспечить бесперебойную работу:

### Базовые знания C# и .NET

Вам понадобится фундаментальное понимание программирования на C# и .NET Framework. Это поможет вам понять структуру кода, с которым вы столкнетесь в этом руководстве.

### Aspose.Cells для .NET

Убедитесь, что у вас установлен Aspose.Cells for .NET. Все подробности вы можете найти на[Документация Aspose.Cells](https://reference.aspose.com/cells/net/). 

### Среда разработки

 Настройте среду разработки. Это может быть Visual Studio или любая другая IDE, поддерживающая C#. Загрузите и установите библиотеку Aspose.Cells из[страница загрузки](https://releases.aspose.com/cells/net/).

### Образец файла Excel

Вам понадобится образец файла Excel, который содержит хотя бы одну диаграмму. Вы можете создать образец файла или загрузить его, чтобы использовать в этом руководстве.

## Импортные пакеты

Чтобы начать работать с Aspose.Cells, вам нужно импортировать необходимые пространства имен в ваше приложение C#. Вот как это сделать:

```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;

using Aspose.Cells.Charts;
```

Эти пространства имен предоставляют вам доступ к классам и методам, необходимым для управления рабочими книгами Excel и их содержимым.

Теперь, когда мы разобрались со всеми предварительными условиями, давайте разберем процесс на подробные шаги.

## Шаг 1: Настройка выходных и исходных каталогов

Для начала вам необходимо определить, где будет сохранен выходной PDF-файл и где находится исходный документ Excel.

```csharp
//Выходной каталог
string outputDir = "Your Output Directory";

//Исходный каталог
string sourceDir = "Your Document Directory";
```

Обязательно замените «Your Output Directory» и «Your Document Directory» на фактические пути в вашей системе. Это определяет, где Aspose сохранит сгенерированный PDF и где он найдет файл Excel.

## Шаг 2: Загрузите образец файла Excel

Далее вам нужно загрузить файл Excel, содержащий диаграмму. Вот как это сделать:

```csharp
//Загрузите пример файла Excel, содержащего диаграмму.
Workbook wb = new Workbook(sourceDir + "sampleCreateChartPDFWithDesiredPageSize.xlsx");
```

 The`Workbook` class играет центральную роль во взаимодействии с вашим документом Excel. Убедитесь, что путь правильно указывает на ваш файл Excel — ошибка здесь не позволит выполнить остальной код.

## Шаг 3: Доступ к первому рабочему листу

После загрузки рабочей книги следующим шагом будет доступ к рабочему листу, содержащему нужную диаграмму.

```csharp
//Откройте первый рабочий лист.
Worksheet ws = wb.Worksheets[0];
```

 В Aspose.Cells рабочие листы индексируются, начиная с нуля, поэтому`Worksheets[0]` относится к первому листу.

## Шаг 4: Получите доступ к первой диаграмме

Теперь давайте перейдем к диаграмме, которую вы хотите экспортировать в PDF. Этот шаг предполагает, что ваш рабочий лист содержит по крайней мере одну диаграмму.

```csharp
//Доступ к первой диаграмме на рабочем листе.
Chart ch = ws.Charts[0];
```

Опять же, это открывает первую диаграмму на рабочем листе; убедитесь, что структура вашего рабочего листа соответствует этому подходу.

## Шаг 5: Создайте PDF-файл с желаемым размером страницы

Наконец, пришло время создать PDF из диаграммы с указанным размером страницы. Вот волшебная строка кода, которая делает все это:

```csharp
//Создайте диаграмму в формате PDF с желаемым размером страницы.
ch.ToPdf(outputDir + "outputCreateChartPDFWithDesiredPageSize.pdf", 7, 7, PageLayoutAlignmentType.Center, PageLayoutAlignmentType.Center);
```

В этом коде:
- PDF-файл будет сохранен в указанном вами ранее выходном каталоге.
-  Цифры`7, 7` представляют собой ширину и высоту желаемого размера страницы соответственно.
- PageLayoutAlignmentType.Center обеспечивает центрирование диаграммы на странице.

## Шаг 6: Подтверждающее сообщение

Чтобы дать себе (и другим) знать, что все прошло гладко, включите в конец кода подтверждающее сообщение:

```csharp
Console.WriteLine("CreateChartPDFWithDesiredPageSize executed successfully.");
```

Это сообщение появится в окне консоли после завершения процесса, сигнализируя о том, что ваш PDF-файл был создан без сбоев.

## Заключение

Поздравляем! Вы только что узнали, как использовать Aspose.Cells для .NET для создания PDF из диаграммы, содержащейся в файле Excel. Эта мощная библиотека упрощает процесс обработки документов Excel и создания визуальных представлений данных, экономя вам часы ручного форматирования. Обязательно изучите множество других функций, которые Aspose.Cells предлагает помимо простого создания PDF — никогда не знаешь, что может еще больше улучшить ваши проекты!

## Часто задаваемые вопросы

### Для чего используется Aspose.Cells для .NET?  
Aspose.Cells для .NET используется для программного создания, редактирования и преобразования документов Excel в приложениях .NET.

### Могу ли я использовать Aspose.Cells бесплатно?  
 Да, Aspose.Cells предлагает[бесплатная пробная версия](https://releases.aspose.com/) для целей оценки.

### Есть ли возможность продлить пробный период сверх первоначального?  
 Вы можете подать заявку на[временная лицензия](https://purchase.aspose.com/temporary-license/) для расширенного тестирования.

### Что делать, если у меня возникнут проблемы или вопросы?  
 Вы можете обратиться за помощью к сообществу Aspose на их сайте[форум поддержки](https://forum.aspose.com/c/cells/9).

### Как я могу приобрести Aspose.Cells?  
 Вы можете купить Aspose.Cells у[страница покупки](https://purchase.aspose.com/buy).