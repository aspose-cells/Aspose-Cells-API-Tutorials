---
title: Поддержка подписей Xades
linktitle: Поддержка подписей Xades
second_title: Справочник по API Aspose.Cells для .NET
description: Узнайте, как добавить подпись Xades в файл Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 190
url: /ru/net/excel-workbook/xades-signature-support/
---
В этой статье мы шаг за шагом объясним приведенный ниже исходный код C#, посвященный поддержке подписи Xades с использованием библиотеки Aspose.Cells для .NET. Вы узнаете, как использовать эту библиотеку для добавления цифровой подписи Xades в файл Excel. Мы также предоставим вам обзор процесса подписания и его выполнения. Следуйте инструкциям ниже, чтобы получить окончательные результаты.

## Шаг 1. Определите исходный и выходной каталоги.
Для начала нам нужно определить исходный и выходной каталоги в нашем коде. Эти каталоги указывают, где расположены исходные файлы и где будет сохранен выходной файл. Вот соответствующий код:

```csharp
// Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
// Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
```

Обязательно измените пути к каталогам по мере необходимости.

## Шаг 2. Загрузка книги Excel
Следующий шаг — загрузить книгу Excel, в которую мы хотим добавить цифровую подпись Xades. Вот код для загрузки книги:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Обязательно правильно укажите имя исходного файла в коде.

## Шаг 3. Настройка цифровой подписи
Теперь мы настроим цифровую подпись Xades, предоставив необходимую информацию. Мы должны указать файл PFX, содержащий цифровой сертификат, а также связанный с ним пароль. Вот соответствующий код:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Обязательно замените «pfxPassword» своим действительным паролем, а «pfxFile» — путем к файлу PFX.

## Шаг 4. Добавление цифровой подписи
Теперь, когда мы настроили цифровую подпись, мы можем добавить ее в книгу Excel. Вот соответствующий код:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

На этом шаге цифровая подпись Xades добавляется в книгу Excel.

## Шаг 5. Сохранение книги с подписью
Наконец, мы сохраняем книгу Excel с добавленной цифровой подписью. Вот соответствующий код:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Обязательно адаптируйте имя выходного файла в соответствии с вашими потребностями.

### Пример исходного кода для поддержки подписей Xades с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
//Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Заключение
Поздравляем! Вы узнали, как использовать библиотеку Aspose.Cells для .NET для добавления цифровой подписи Xades в файл Excel. Выполнив действия, описанные в этой статье, вы сможете реализовать эту функциональность в своих собственных проектах. Не стесняйтесь экспериментировать с библиотекой и открывать для себя другие мощные функции, которые она предлагает.

### Часто задаваемые вопросы

#### Вопрос: Что такое Ксадес?

Ответ: Xades — это усовершенствованный стандарт электронной подписи, используемый для обеспечения целостности и подлинности цифровых документов.

#### Вопрос: Могу ли я использовать другие типы цифровых подписей с Aspose.Cells?

О: Да, Aspose.Cells также поддерживает другие типы цифровых подписей, такие как подписи XMLDSig и подписи PKCS#7.

#### Вопрос: Могу ли я применить подпись к файлам других типов, кроме файлов Excel?
 
О: Да, Aspose.Cells также позволяет применять цифровые подписи к другим поддерживаемым типам файлов, таким как файлы Word, PDF и PowerPoint.