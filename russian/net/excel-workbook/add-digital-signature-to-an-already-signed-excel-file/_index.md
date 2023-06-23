---
title: Добавить цифровую подпись к уже подписанному файлу Excel
linktitle: Добавить цифровую подпись к уже подписанному файлу Excel
second_title: Справочник по Aspose.Cells для .NET API
description: Легко добавляйте цифровые подписи в существующие файлы Excel с помощью Aspose.Cells для .NET.
type: docs
weight: 30
url: /ru/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
В этом пошаговом руководстве мы объясним предоставленный исходный код C#, который позволит вам добавить цифровую подпись в уже подписанный файл Excel с помощью Aspose.Cells для .NET. Выполните следующие действия, чтобы добавить новую цифровую подпись в существующий файл Excel.

## Шаг 1: Установите исходный и выходной каталоги

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();

// Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
```

На этом первом шаге мы определяем исходный и выходной каталоги, которые будут использоваться для загрузки существующего файла Excel и сохранения файла с новой цифровой подписью.

## Шаг 2: Загрузите существующий файл Excel

```csharp
// Загрузите уже подписанную книгу Excel
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Здесь мы загружаем уже подписанный файл Excel с помощью`Workbook` класс Aspose.Cells.

## Шаг 3. Создайте коллекцию цифровых подписей

```csharp
// Создание коллекции цифровых подписей
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Мы создаем новую коллекцию цифровых подписей, используя`DigitalSignatureCollection` сорт.

## Шаг 4: Создайте новый сертификат

```csharp
// Создать новый сертификат
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Здесь мы создаем новый сертификат из предоставленного файла и пароля.

## Шаг 5. Добавьте новую цифровую подпись в коллекцию

```csharp
// Создать новую цифровую подпись
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Добавьте цифровую подпись в коллекцию
dsCollection.Add(signature);
```

 Мы создаем новую цифровую подпись, используя`DigitalSignature` class и добавить его в коллекцию цифровых подписей.

## Шаг 6. Добавьте коллекцию цифровых подписей в книгу

```csharp
//Добавьте коллекцию цифровых подписей в книгу
workbook.AddDigitalSignature(dsCollection);
```

 Мы добавляем коллекцию цифровых подписей в существующую книгу Excel, используя`AddDigitalSignature()` метод.

## Шаг 7: Сохраните и закройте книгу

```csharp
// Сохраните книгу и закройте ее
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Мы сохраняем книгу с новой цифровой подписью в указанный выходной каталог, затем закрываем ее и освобождаем связанные ресурсы.

### Пример исходного кода для добавления цифровой подписи в уже подписанный файл Excel с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
//Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
//Файл сертификата и его пароль
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Загрузите книгу, которая уже имеет цифровую подпись, чтобы добавить новую цифровую подпись.
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Создание коллекции цифровых подписей
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Создать новый сертификат
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Создайте новую цифровую подпись и добавьте ее в коллекцию цифровых подписей.
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Добавить коллекцию цифровых подписей в книгу
workbook.AddDigitalSignature(dsCollection);
//Сохраните книгу и выбросьте ее.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Заключение

Поздравляем! Теперь вы узнали, как добавить цифровую подпись к уже подписанному файлу Excel с помощью Aspose.Cells для .NET. Цифровые подписи добавляют дополнительный уровень безопасности вашим файлам Excel, гарантируя их подлинность и целостность.

### Часто задаваемые вопросы

#### В: Что такое Aspose.Cells для .NET?

A: Aspose.Cells for .NET — это мощная библиотека классов, которая позволяет разработчикам .NET с легкостью создавать, изменять, преобразовывать и манипулировать файлами Excel.

#### В: Что такое цифровая подпись в файле Excel?

О: Цифровая подпись в файле Excel — это электронная метка, гарантирующая подлинность, целостность и происхождение документа. Он используется для проверки того, что файл не был изменен с момента его подписания и получен из надежного источника.

#### В: Каковы преимущества добавления цифровой подписи к файлу Excel?

О: Добавление цифровой подписи к файлу Excel дает ряд преимуществ, включая защиту от несанкционированных изменений, обеспечение целостности данных, аутентификацию автора документа и уверенность в содержащейся в нем информации.

#### Вопрос. Можно ли добавить несколько цифровых подписей в файл Excel?

О: Да, Aspose.Cells позволяет добавлять несколько цифровых подписей в файл Excel. Вы можете создать коллекцию цифровых подписей и добавить их в файл за одну операцию.

#### В: Каковы требования для добавления цифровой подписи в файл Excel?

О: Чтобы добавить цифровую подпись к файлу Excel, вам нужен действующий цифровой сертификат, который будет использоваться для подписи документа. Перед добавлением цифровой подписи убедитесь, что у вас есть правильный сертификат и пароль.