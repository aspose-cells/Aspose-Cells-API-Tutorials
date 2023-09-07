---
title: XLSB Dosyasının Harici Bağlantısını Okuma ve Yazma
linktitle: XLSB Dosyasının Harici Bağlantısını Okuma ve Yazma
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir XLSB dosyasının harici bağlantılarını nasıl okuyacağınızı ve değiştireceğinizi öğrenin.
type: docs
weight: 130
url: /tr/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Bir XLSB dosyasına dış bağlantıları okumak ve yazmak, Excel çalışma kitaplarınızdaki dış kaynaklardan gelen verileri değiştirmek için çok önemlidir. Aspose.Cells for .NET ile aşağıdaki adımları kullanarak dış bağlantıları kolayca okuyabilir ve yazabilirsiniz:

## Adım 1: Kaynak dizini ve çıktı dizini belirtin

Öncelikle, harici bağlantıyı içeren XLSB dosyasının bulunduğu kaynak dizini ve değiştirilen dosyayı kaydetmek istediğiniz çıkış dizinini belirtmeniz gerekir. Aspose.Cells kullanarak bunu şu şekilde yapabilirsiniz:

```csharp
// kaynak dizin
string sourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. Adım: Kaynak Excel XLSB dosyasını yükleyin

Ardından, harici bağlantı okuma ve yazma işlemlerini gerçekleştirmek istediğiniz kaynak Excel XLSB dosyasını yüklemeniz gerekir. İşte örnek bir kod:

```csharp
// Kaynak Excel XLSB dosyasını yükleyin
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
```

## 3. Adım: Harici bağlantıyı okuyun ve değiştirin

Dosyayı yükledikten sonra, aslında bir veritabanı bağlantısı olan ilk harici bağlantıya erişebilirsiniz. Harici bağlantının çeşitli özelliklerini okuyabilir ve değiştirebilirsiniz. İşte nasıl:

```csharp
// Veritabanı bağlantısı olan ilk harici bağlantıyı okuyun
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;

// Veritabanı bağlantı adını, komutunu ve bağlantı bilgilerini görüntüleyin
Console.WriteLine("Connection name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);

// Bağlantının adını değiştirin
dbCon.Name = "NewCustomer";
```

## 4. Adım: Çıktı Excel XLSB dosyasını kaydedin

Gerekli değişiklikleri yaptıktan sonra, değiştirilen Excel XLSB dosyasını belirtilen çıkış dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel XLSB dosyasını kaydedin
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak XLSB Dosyasının Harici Bağlantısını Okumak ve Yazmak için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Kaynak Excel Xlsb dosyasını yükleyin
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Aslında bir DB Bağlantısı olan ilk harici bağlantıyı okuyun
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//DB-Connection'ın Adını, Komutunu ve Bağlantı Bilgilerini yazdırın
Console.WriteLine("Connection Name: " + dbCon.Name);
Console.WriteLine("Command: " + dbCon.Command);
Console.WriteLine("Connection Info: " + dbCon.ConnectionInfo);
//Bağlantı Adını Değiştirin
dbCon.Name = "NewCust";
//Excel Xlsb dosyasını kaydedin
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

## Çözüm

Dış bağlantıları bir XLSB dosyasına okumak ve yazmak, Excel çalışma kitaplarınızdaki dış kaynaklardan gelen verileri değiştirmenize olanak tanır. Aspose.Cells for .NET ile dış bağlantılara kolayca erişebilir, bağlantı bilgilerini okuyup değiştirebilir ve değişiklikleri kaydedebilirsiniz. Kendi XLSB dosyalarınızla deneyler yapın ve Excel uygulamalarınızda harici bağlantıların gücünden yararlanın.

### SSS

#### S: Bir XLSB dosyasındaki harici bağlantı nedir?
    
Y: Bir XLSB dosyasındaki harici bağlantı, veritabanı gibi harici bir veri kaynağıyla kurulan bağlantıyı ifade eder. Bu dış kaynaktan Excel çalışma kitabına veri aktarmanıza olanak tanır.

#### S: Bir XLSB dosyasında birden çok harici bağlantıya sahip olabilir miyim?
     
C: Evet, bir XLSB dosyasında birden çok harici bağlantınız olabilir. Her bağlantı nesnesine erişerek bunları ayrı ayrı yönetebilirsiniz.

#### S: Bir XLSB dosyasındaki harici bağlantının ayrıntılarını Aspose.Cells ile nasıl okuyabilirim?
     
C: Bağlantı adı, ilişkili komut ve bağlantı bilgileri gibi harici bir bağlantının özelliklerine erişmek için Aspose.Cells tarafından sağlanan işlevselliği kullanabilirsiniz.

#### S: Bir XLSB dosyasındaki harici bir bağlantıyı Aspose.Cells ile değiştirmek mümkün müdür?
     
C: Evet, özel ihtiyaçlarınızı karşılamak için harici bir bağlantının bağlantı adı gibi özelliklerini değiştirebilirsiniz. Aspose.Cells, bu değişiklikleri yapmak için yöntemler sağlar.

#### S: Harici bağlantıda yaptığım değişiklikleri Aspose.Cells ile bir XLSB dosyasına nasıl kaydedebilirim?
     
C: Harici bir bağlantıda gerekli değişiklikleri yaptıktan sonra, Aspose.Cells tarafından sağlanan uygun yöntemi kullanarak değiştirilen Excel XLSB dosyasını kolayca kaydedebilirsiniz.