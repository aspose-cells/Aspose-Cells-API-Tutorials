---
title: XLSB Dosyasının Harici Bağlantısını Okuma ve Yazma
linktitle: XLSB Dosyasının Harici Bağlantısını Okuma ve Yazma
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir XLSB dosyasının harici bağlantılarını nasıl okuyacağınızı ve değiştireceğinizi öğrenin.
type: docs
weight: 130
url: /tr/net/excel-workbook/read-and-write-external-connection-of-xlsb-file/
---
Bir XLSB dosyasına harici bağlantıları okumak ve yazmak, Excel çalışma kitaplarınızdaki harici kaynaklardan gelen verileri işlemek için çok önemlidir. Aspose.Cells for .NET ile aşağıdaki adımları kullanarak harici bağlantıları kolayca okuyabilir ve yazabilirsiniz:

## Adım 1: Kaynak dizini ve çıktı dizinini belirtin

Öncelikle, harici bağlantıyı içeren XLSB dosyasının bulunduğu kaynak dizinin yanı sıra, değiştirilen dosyayı kaydetmek istediğiniz çıkış dizinini de belirtmeniz gerekir. Aspose.Cells'i kullanarak bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## Adım 2: Kaynak Excel XLSB dosyasını yükleyin

Daha sonra harici bağlantı okuma ve yazma işlemlerini gerçekleştirmek istediğiniz kaynak Excel XLSB dosyasını yüklemeniz gerekmektedir. İşte örnek bir kod:

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

## Adım 4: Çıktı Excel XLSB dosyasını kaydedin

Gerekli değişiklikleri yaptıktan sonra değiştirilen Excel XLSB dosyasını belirtilen çıktı dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel XLSB dosyasını kaydedin
wb.Save(outputDir + "outputExternalConnection_XLSB.xlsb");
Console.WriteLine("ReadAndWriteExternalConnectionOfXLSBFile executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak XLSB Dosyasının Harici Bağlantısını Okuma ve Yazma için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Kaynak Excel Xlsb dosyasını yükleyin
Workbook wb = new Workbook(sourceDir + "sampleExternalConnection_XLSB.xlsb");
//Aslında bir DB Bağlantısı olan ilk harici bağlantıyı okuyun
Aspose.Cells.ExternalConnections.DBConnection dbCon = wb.DataConnections[0] as Aspose.Cells.ExternalConnections.DBConnection;
//DB Bağlantısının Adını, Komutunu ve Bağlantı Bilgisini Yazdırın
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

XLSB dosyasına harici bağlantıları okumak ve yazmak, Excel çalışma kitaplarınızdaki harici kaynaklardan gelen verileri değiştirmenize olanak tanır. Aspose.Cells for .NET ile harici bağlantılara kolayca erişebilir, bağlantı bilgilerini okuyup değiştirebilir ve değişiklikleri kaydedebilirsiniz. Kendi XLSB dosyalarınızla denemeler yapın ve Excel uygulamalarınızda harici bağlantıların gücünden yararlanın.

### SSS

#### S: XLSB dosyasındaki harici bağlantı nedir?
    
C: XLSB dosyasındaki harici bağlantı, veritabanı gibi harici bir veri kaynağıyla kurulan bağlantıyı ifade eder. Bu harici kaynaktan verileri Excel çalışma kitabına aktarmanıza olanak tanır.

#### S: Bir XLSB dosyasında birden fazla harici bağlantıya sahip olabilir miyim?
     
C: Evet, bir XLSB dosyasında birden fazla harici bağlantınız olabilir. Her bağlantı nesnesine erişerek bunları ayrı ayrı yönetebilirsiniz.

#### S: Aspose.Cells ile XLSB dosyasındaki harici bağlantının ayrıntılarını nasıl okuyabilirim?
     
C: Bağlantı adı, ilişkili komut ve bağlantı bilgileri gibi harici bağlantı özelliklerine erişmek için Aspose.Cells tarafından sağlanan işlevselliği kullanabilirsiniz.

#### S: XLSB dosyasındaki harici bağlantıyı Aspose.Cells ile değiştirmek mümkün müdür?
     
C: Evet, özel ihtiyaçlarınızı karşılamak için harici bir bağlantının bağlantı adı gibi özelliklerini değiştirebilirsiniz. Aspose.Cells bu değişiklikleri yapmak için yöntemler sağlar.

#### S: Harici bağlantıda yapılan değişiklikleri Aspose.Cells ile XLSB dosyasına nasıl kaydedebilirim?
     
C: Harici bağlantıda gerekli değişiklikleri yaptıktan sonra, değiştirilen Excel XLSB dosyasını Aspose.Cells tarafından sağlanan uygun yöntemi kullanarak kaydedebilirsiniz.