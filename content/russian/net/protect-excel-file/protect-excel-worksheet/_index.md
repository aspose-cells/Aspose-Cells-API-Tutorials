---
title: Защитить лист Excel
linktitle: Защитить лист Excel
second_title: Справочник по API Aspose.Cells для .NET
description: В этом руководстве вы узнаете, как защитить электронную таблицу Excel с помощью Aspose.Cells для .NET. Пошаговое руководство на C#.
type: docs
weight: 50
url: /ru/net/protect-excel-file/protect-excel-worksheet/
---
В этом уроке мы рассмотрим исходный код C#, который использует библиотеку Aspose.Cells для защиты электронной таблицы Excel. Мы рассмотрим каждый шаг кода и объясним, как он работает. Обязательно внимательно следуйте инструкциям, чтобы получить желаемые результаты.

## Шаг 1: Предварительные условия

Прежде чем начать, убедитесь, что у вас установлена библиотека Aspose.Cells для .NET. Вы можете получить его на официальном сайте Aspose. Также убедитесь, что у вас установлена последняя версия Visual Studio или любой другой среды разработки C#.

## Шаг 2. Импортируйте необходимые пространства имен.

Чтобы использовать библиотеку Aspose.Cells, нам необходимо импортировать необходимые пространства имен в наш код. Добавьте следующие строки в начало исходного файла C#:

```csharp
using Aspose.Cells;
using System.IO;
```

## Шаг 3. Загрузите файл Excel

На этом этапе мы загрузим файл Excel, который хотим защитить. Обязательно укажите правильный путь к каталогу, содержащему файл Excel. Используйте следующий код для загрузки файла:

```csharp
// Путь к каталогу документов.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Создайте поток файлов, содержащий файл Excel, который нужно открыть.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Создайте экземпляр объекта Workbook.
//Откройте файл Excel через файловый поток.
Workbook excel = new Workbook(fstream);
```

 Обязательно замените`"YOUR_DOCUMENTS_DIR"` с соответствующим путем к каталогу ваших документов.

## Шаг 4. Получите доступ к электронной таблице.

Теперь, когда мы загрузили файл Excel, мы можем получить доступ к первому листу. Используйте следующий код для доступа к первому листу:

```csharp
// Доступ к первому листу в файле Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Шаг 5. Защитите лист

На этом этапе мы защитим таблицу паролем. Используйте следующий код для защиты электронной таблицы:

```csharp
// Защитите рабочий лист паролем.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Заменять`"YOUR_PASSWORD"` с паролем, который вы хотите использовать для защиты электронной таблицы.

## Шаг 6. Сохраните измененный файл Excel. Теперь, когда мы защитили

é электронную таблицу, мы сохраним измененный файл Excel в формате по умолчанию. Используйте следующий код, чтобы сохранить файл Excel:

```csharp
// Сохраните измененный файл Excel в формате по умолчанию.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Обязательно укажите правильный путь для сохранения измененного файла Excel.

## Шаг 7: Закройте файловый поток

Чтобы освободить все ресурсы, нам нужно закрыть файловый поток, используемый для загрузки файла Excel. Используйте следующий код, чтобы закрыть файловый поток:

```csharp
// Закройте файловый поток, чтобы освободить все ресурсы.
fstream.Close();
```

Обязательно включите этот шаг в конец вашего кода.


### Пример исходного кода для защиты листа Excel с использованием Aspose.Cells для .NET 
```csharp
//Путь к каталогу документов.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Создание потока файлов, содержащего открываемый файл Excel.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Создание экземпляра объекта Workbook
// Открытие файла Excel через файловый поток
Workbook excel = new Workbook(fstream);
// Доступ к первому листу в файле Excel
Worksheet worksheet = excel.Worksheets[0];
// Защита рабочего листа паролем
worksheet.Protect(ProtectionType.All, "aspose", null);
// Сохранение измененного файла Excel в формате по умолчанию.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Закрытие файлового потока для освобождения всех ресурсов
fstream.Close();
```

## Заключение

Поздравляем! Теперь у вас есть исходный код C#, который позволяет защитить электронную таблицу Excel с помощью библиотеки Aspose.Cells для .NET. Обязательно внимательно следуйте инструкциям и настройте код в соответствии с вашими конкретными потребностями.

### Часто задаваемые вопросы (часто задаваемые вопросы)

#### Можно ли защитить несколько листов в одном файле Excel?

О: Да, вы можете защитить несколько листов в одном файле Excel, повторив шаги 4–6 для каждого листа.

#### Как я могу указать определенные разрешения для авторизованных пользователей?

 О: Вы можете использовать дополнительные возможности, предоставляемые`Protect`метод для указания конкретных разрешений для авторизованных пользователей. Дополнительную информацию см. в документации Aspose.Cells.

#### Могу ли я защитить сам файл Excel паролем?

О: Да, вы можете защитить паролем сам файл Excel, используя другие методы, предоставляемые библиотекой Aspose.Cells. Пожалуйста, обратитесь к документации за конкретными примерами.

#### Поддерживает ли библиотека Aspose.Cells другие форматы файлов Excel?

О: Да, библиотека Aspose.Cells поддерживает широкий спектр форматов файлов Excel, включая XLSX, XLSM, XLSB, CSV и т. д.