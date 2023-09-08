---
title: Çalışma Sayfasının Kağıt Boyutunun Otomatik Olup Olmadığını Belirleme
linktitle: Çalışma Sayfasının Kağıt Boyutunun Otomatik Olup Olmadığını Belirleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile bir elektronik tablonun kağıt boyutunun otomatik olup olmadığını nasıl belirleyeceğinizi öğrenin.
type: docs
weight: 20
url: /tr/net/excel-page-setup/determine-if-paper-size-of-worksheet-is-automatic/
---
Bu makalede sizi adım adım aşağıdaki C# kaynak kodunu açıklamaya yönlendireceğiz: Aspose.Cells for .NET kullanarak bir çalışma sayfasının kağıt boyutunun otomatik olup olmadığını belirleyin. Bu işlemi gerçekleştirmek için .NET için Aspose.Cells kütüphanesini kullanacağız. Bir çalışma sayfasının kağıt boyutunun otomatik olup olmadığını belirlemek için aşağıdaki adımları izleyin.

## 1. Adım: Çalışma kitaplarını yükleme
İlk adım çalışma kitaplarını yüklemektir. İki çalışma kitabımız olacak: biri otomatik kağıt boyutu devre dışı, diğeri ise otomatik kağıt boyutu etkin. Çalışma kitaplarını yüklemek için gereken kod:

```csharp
// kaynak dizini
string sourceDir = "YOUR_SOURCE_DIR";
// Çıkış dizini
string outputDir = "YOUR_OUTPUT_DIRECTORY";

// İlk çalışma kitabını otomatik kağıt boyutu devre dışı bırakılarak yükleyin
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");

// İkinci çalışma kitabını otomatik kağıt boyutu etkin olarak yükleyin
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
```

## Adım 2: E-Tablolara Erişim
Artık çalışma kitaplarını yüklediğimize göre, otomatik kağıt boyutunu kontrol edebilmek için çalışma sayfalarına erişmemiz gerekiyor. İki çalışma kitabının ilk çalışma sayfasına gideceğiz. İşte ona erişmenizi sağlayacak kod:

```csharp
//İlk çalışma kitabının ilk çalışma sayfasına git
Worksheet ws11 = wb1.Worksheets[0];

// İkinci çalışma kitabının ilk çalışma sayfasına git
Worksheet ws12 = wb2.Worksheets[0];
```

## 3. Adım: Otomatik kağıt boyutunu kontrol edin
 Bu adımda çalışma sayfası kağıt boyutunun otomatik olup olmadığını kontrol edeceğiz. kullanacağız`PageSetup.IsAutomaticPaperSize` Bu bilgiyi almak için özellik. Daha sonra sonucu göstereceğiz. İşte bunun için kod:

```csharp
// İlk çalışma kitabındaki ilk çalışma sayfasının IsAutomaticPaperSize özelliğini görüntüleme
Console.WriteLine("First worksheet in first workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);

// İlk çalışma sayfasının IsAutomaticPaperSize özelliğini ikinci çalışma kitabında görüntüleme
Console.WriteLine("First worksheet of second workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);

```

### Aspose.Cells for .NET Kullanarak Çalışma Sayfasının Kağıt Boyutunun Otomatik Olup Olmadığını Belirlemek için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = "YOUR_SOURCE_DIRECTORY";
//Çıkış dizini
string outputDir = "YOUR_OUTPUT_DIRECTORY";
//Otomatik kağıt boyutuna sahip ilk çalışma kitabını yükleyin yanlış
Workbook wb1 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-False.xlsx");
//Otomatik kağıt boyutu doğru olan ikinci çalışma kitabını yükleyin
Workbook wb2 = new Workbook(sourceDir + "samplePageSetupIsAutomaticPaperSize-True.xlsx");
//Her iki çalışma kitabının da ilk çalışma sayfasına erişin
Worksheet ws11 = wb1.Worksheets[0];
Worksheet ws12 = wb2.Worksheets[0];
//Her iki çalışma sayfasının PageSetup.IsAutomaticPaperSize özelliğini yazdırın
Console.WriteLine("First Worksheet of First Workbook - IsAutomaticPaperSize: " + ws11.PageSetup.IsAutomaticPaperSize);
Console.WriteLine("First Worksheet of Second Workbook - IsAutomaticPaperSize: " + ws12.PageSetup.IsAutomaticPaperSize);
Console.WriteLine();
Console.WriteLine("DetermineIfPaperSizeOfWorksheetIsAutomatic executed successfully.\r\n");
```


## Çözüm
Bu makalede Aspose.Cells for .NET kullanarak bir çalışma sayfasının kağıt boyutunun otomatik olup olmadığını nasıl belirleyeceğimizi öğrendik. Şu adımları izledik: çalışma kitaplarını yükleme,

elektronik tablolara erişim ve otomatik kağıt boyutu kontrolü. Artık bu bilgiyi e-tablolarınızın kağıt boyutunun otomatik olup olmadığını belirlemek için kullanabilirsiniz.

### SSS

#### S: Aspose.Cells for .NET ile çalışma kitaplarını nasıl yükleyebilirim?

C: Aspose.Cells kütüphanesindeki Workbook sınıfını kullanarak çalışma kitaplarını yükleyebilirsiniz. Bir dosyadan çalışma kitabı yüklemek için Workbook.Load yöntemini kullanın.

#### S: Diğer elektronik tablolar için otomatik kağıt boyutunu kontrol edebilir miyim?

C: Evet, ilgili Worksheet nesnesinin PageSetup.IsAutomaticPaperSize özelliğine erişerek herhangi bir çalışma sayfasının otomatik kağıt boyutunu kontrol edebilirsiniz.

#### S: Bir e-tablonun otomatik kağıt boyutunu nasıl değiştirebilirim?

C: Bir çalışma sayfasının otomatik kağıt boyutunu değiştirmek için PageSetup.IsAutomaticPaperSize özelliğini kullanabilir ve bunu istediğiniz değere (doğru veya yanlış) ayarlayabilirsiniz.

#### S: Aspose.Cells for .NET başka hangi özellikleri sunuyor?

C: Aspose.Cells for .NET, elektronik tablolarla çalışmak için çalışma kitaplarını oluşturma, değiştirme ve dönüştürmenin yanı sıra verileri, formülleri ve biçimlendirmeyi değiştirme gibi birçok özellik sunar.