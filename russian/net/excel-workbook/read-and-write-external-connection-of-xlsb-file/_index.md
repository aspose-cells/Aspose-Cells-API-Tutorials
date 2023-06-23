---
title: Чтение и запись внешнего соединения файла XLSB
linktitle: Чтение и запись внешнего соединения файла XLSB
second_title: Справочник по Aspose.Cells для .NET API
description: Узнайте, как читать и изменять внешние соединения файла XLSB с помощью Aspose.Cells для .NET.
type: docs
weight: 130
url: /ru/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Чтение и запись внешних подключений к файлу XLSB необходимы для управления данными из внешних источников в ваших книгах Excel. С Aspose.Cells для .NET вы можете легко читать и записывать внешние соединения, используя следующие шаги:

## Шаг 1: Укажите исходный каталог и выходной каталог

Во-первых, вы должны указать исходный каталог, в котором находится файл XLSB, содержащий внешнее соединение, а также выходной каталог, в котором вы хотите сохранить измененный файл. Вот как это сделать с помощью Aspose.Cells:

```csharp
// исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();

// Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
```

## Шаг 2. Загрузите исходный файл Excel XLSB

Затем вам нужно загрузить исходный файл Excel XLSB, для которого вы хотите выполнять операции чтения и записи внешнего подключения. Вот пример кода:

```csharp
// Загрузите исходный файл Excel XLSB
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## Шаг 3: Прочтите и измените внешнее соединение

После загрузки файла вы можете получить доступ к первому внешнему соединению, которое на самом деле является соединением с базой данных. Вы можете читать и изменять различные свойства внешнего соединения. Вот как:

```csharp
// Прочитайте первое внешнее соединение, которое является соединением с базой данных.
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Отображение имени подключения к базе данных, команды и информации о подключении
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Изменить имя соединения
dbCon.Name = "NewCustomer";
```

## Шаг 4. Сохраните выходной файл Excel XLSB.

После внесения необходимых изменений вы можете сохранить измененный файл Excel XLSB в указанный выходной каталог. Вот как это сделать:

```csharp
// Сохраните выходной файл Excel XLSB
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Пример исходного кода для чтения и записи внешнего подключения файла XLSB с использованием Aspose.Cells для .NET 
```csharp
//Исходный каталог
string sourceDir = RunExamples.Get_SourceDirectory();
//Выходной каталог
string outputDir = RunExamples.Get_OutputDirectory();
//Загрузите исходный файл Excel Xlsb
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Прочитайте первое внешнее соединение, которое на самом деле является соединением с БД.
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//Распечатайте имя, команду и информацию о подключении к базе данных
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Изменить имя подключения
dbCon.Name = "NewCust";
//Сохраните файл Excel Xlsb
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Заключение

Чтение и запись внешних подключений к файлу XLSB позволяет вам манипулировать данными из внешних источников в ваших книгах Excel. С Aspose.Cells для .NET вы можете легко получить доступ к внешним подключениям, прочитать и изменить информацию о подключении и сохранить изменения. Экспериментируйте с собственными файлами XLSB и используйте возможности внешних подключений в приложениях Excel.

### Часто задаваемые вопросы

#### В: Что такое внешнее соединение в файле XLSB?
    
О: Внешнее соединение в файле XLSB — это соединение, установленное с внешним источником данных, таким как база данных. Он позволяет импортировать данные из этого внешнего источника в книгу Excel.

#### В: Могу ли я иметь несколько внешних подключений в файле XLSB?
     
О: Да, в файле XLSB может быть несколько внешних подключений. Вы можете управлять ими по отдельности, обращаясь к каждому объекту подключения.

#### В: Как я могу прочитать информацию о внешнем соединении в файле XLSB с помощью Aspose.Cells?
     
О: Вы можете использовать функциональные возможности, предоставляемые Aspose.Cells, для доступа к свойствам внешнего соединения, таким как имя соединения, связанная команда и информация о соединении.

#### В: Можно ли изменить внешнее соединение в файле XLSB с помощью Aspose.Cells?
     
О: Да, вы можете изменить свойства внешнего подключения, такие как имя подключения, в соответствии с вашими потребностями. Aspose.Cells предоставляет методы для внесения этих изменений.

#### В: Как я могу сохранить изменения, внесенные во внешнее соединение, в файл XLSB с помощью Aspose.Cells?
     
О: После внесения необходимых изменений во внешнее соединение вы можете просто сохранить измененный файл Excel XLSB, используя соответствующий метод, предоставляемый Aspose.Cells.