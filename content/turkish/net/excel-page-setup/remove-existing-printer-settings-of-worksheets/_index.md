---
title: Çalışma Sayfalarının Mevcut Yazıcı Ayarlarını Kaldır
linktitle: Çalışma Sayfalarının Mevcut Yazıcı Ayarlarını Kaldır
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile mevcut yazıcı ayarlarını Excel elektronik tablolarından nasıl kaldıracağınızı öğrenin.
type: docs
weight: 80
url: /tr/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak mevcut yazıcı ayarlarını Excel'deki çalışma sayfalarından nasıl kaldıracağınızı adım adım anlatacağız. Süreci göstermek için C# kaynak kodunu kullanacağız.

## 1. Adım: Ortamı ayarlama

Aspose.Cells for .NET'in makinenizde kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Aspose.Cells ile çalışmak için gereken kütüphaneleri kod dosyanıza aktarın. İşte ilgili kod:

```csharp
using Aspose.Cells;
```

## 3. Adım: Kaynak ve çıkış dizinlerini ayarlayın

Orijinal Excel dosyasının bulunduğu kaynak ve çıktı dizinlerini ve değiştirilen dosyayı kaydetmek istediğiniz yeri sırasıyla ayarlayın. Aşağıdaki kodu kullanın:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Tam dizin yollarını belirttiğinizden emin olun.

## Adım 4: Kaynak Excel Dosyasını Yükleme

Aşağıdaki kodu kullanarak kaynak Excel dosyasını yükleyin:

```csharp
Workbook wb = new Workbook(sourceDir + "fileName.xlsx");
```

Bu, belirtilen Excel dosyasını Çalışma Kitabı nesnesine yükleyecektir.

## 5. Adım: Çalışma sayfalarında gezinin

Bir döngü kullanarak çalışma kitabındaki tüm çalışma sayfalarını yineleyin. Aşağıdaki kodu kullanın:

```csharp
int sheetCount = wb. Worksheets. Count;

for (int i = 0; i < sheetCount; i++)
{
     Worksheet ws = wb.Worksheets[i];
     // Kodun geri kalanı bir sonraki adımda eklenecektir.
}
```

## Adım 6: Mevcut Yazıcı Ayarlarını Sil

Her çalışma sayfası için yazıcı ayarlarının mevcut olup olmadığını kontrol edin ve gerekirse bunları silin. Aşağıdaki kodu kullanın:

```csharp
PageSetup ps = ws.PageSetup;

if (ps.PrinterSettings != null)
{
     Console.WriteLine("Printer settings for this spreadsheet exist.");
     Console.WriteLine("Sheet name: " + ws.Name);
     Console.WriteLine("Paper size: " + ps.PaperSize);

     ps.PrinterSettings = null;

     Console.WriteLine("Printer settings for this spreadsheet have been removed by setting them to null.");
     Console.WriteLine("");
}
```

## Adım 7: Değiştirilen Çalışma Kitabını Kaydetme

Değiştirilen çalışma kitabını aşağıdaki kodu kullanarak kaydedin:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Bu, değiştirilen çalışma kitabını belirtilen çıktı dizinine kaydedecektir.

### Aspose.Cells for .NET Kullanarak Çalışma Sayfalarının Mevcut Yazıcı Ayarlarını Kaldırmak için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Kaynak Excel dosyasını yükle
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Çalışma kitabının sayfa sayılarını alın
int sheetCount = wb.Worksheets.Count;
//Tüm sayfaları yinele
for (int i = 0; i < sheetCount; i++)
{
    //i. çalışma sayfasına erişme
    Worksheet ws = wb.Worksheets[i];
    //Çalışma sayfası sayfa düzenine erişme
    PageSetup ps = ws.PageSetup;
    //Bu çalışma sayfası için yazıcı ayarlarının mevcut olup olmadığını kontrol edin
    if (ps.PrinterSettings != null)
    {
        //Aşağıdaki mesajı yazdır
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Sayfa adını ve kağıt boyutunu yazdır
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Yazıcı ayarlarını null olarak ayarlayarak kaldırın
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//eğer
}//için
//Çalışma kitabını kaydet
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Çözüm

Artık Aspose.Cells for .NET kullanarak mevcut yazıcı ayarlarını Excel'deki çalışma sayfalarından nasıl kaldıracağınızı öğrendiniz. Bu eğitim, ortamın ayarlanmasından elektronik tablolar arasında gezinmeye ve yazıcı ayarlarının temizlenmesine kadar sürecin her adımında size yol gösterdi. Artık bu bilgiyi Excel dosyalarınızdaki yazıcı ayarlarını yönetmek için kullanabilirsiniz.

### SSS'ler

#### S1: Bir elektronik tablonun mevcut yazıcı ayarlarına sahip olup olmadığını nasıl anlarım?

 Cevap1: Bir çalışma sayfası için yazıcı ayarlarının mevcut olup olmadığını kontrol edebilirsiniz.`PrinterSettings` mülkiyeti`PageSetup` nesne. Değer boş değilse bu, mevcut yazıcı ayarlarının olduğu anlamına gelir.

#### S2: Yalnızca belirli bir e-tablonun yazıcı ayarlarını silebilir miyim?

 C2: Evet, belirli bir çalışma sayfasının yazıcı ayarlarını kaldırmak için o çalışma sayfasının ayarlarına erişerek aynı yaklaşımı kullanabilirsiniz.`PageSetup` nesne.

#### S3: Bu yöntem diğer düzen ayarlarını da kaldırıyor mu?

Cevap3: Hayır, bu yöntem yalnızca yazıcı ayarlarını siler. Kenar boşlukları, kağıt yönü vb. gibi diğer düzen ayarları değişmeden kalır.

#### S4: Bu yöntem .xls ve .xlsx gibi tüm Excel dosya formatlarında işe yarar mı?

Cevap4: Evet, bu yöntem Aspose.Cells tarafından desteklenen .xls ve .xlsx dahil tüm Excel dosya formatlarında işe yarar.

#### S5: Düzenlenen Excel dosyasında yazıcı ayarlarında yapılan değişiklikler kalıcı mı?

Cevap5: Evet, yazıcı ayarlarında yapılan değişiklikler, düzenlenen Excel dosyasına kalıcı olarak kaydedilir.