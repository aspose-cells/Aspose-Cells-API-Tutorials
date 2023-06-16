---
title: Çalışma Sayfalarının Mevcut Yazıcı Ayarlarını Kaldırma
linktitle: Çalışma Sayfalarının Mevcut Yazıcı Ayarlarını Kaldırma
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel elektronik tablolarından mevcut yazıcı ayarlarını nasıl kaldıracağınızı öğrenin.
type: docs
weight: 80
url: /tr/net/excel-page-setup/remove-existing-printer-settings-of-worksheets/
---
Bu öğreticide, Aspose.Cells for .NET kullanarak Excel'deki çalışma sayfalarından mevcut yazıcı ayarlarının nasıl kaldırılacağını adım adım anlatacağız. Süreci göstermek için C# kaynak kodunu kullanacağız.

## 1. Adım: Ortamı ayarlama

Makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Kod dosyanızda, Aspose.Cells ile çalışmak için gereken kütüphaneleri içe aktarın. İşte ilgili kod:

```csharp
using Aspose.Cells;
```

## 3. Adım: Kaynak ve çıkış dizinlerini ayarlayın

Sırasıyla orijinal Excel dosyasının bulunduğu ve değiştirilen dosyayı nereye kaydetmek istediğinizi kaynak ve çıktı dizinlerini ayarlayın. Aşağıdaki kodu kullanın:

```csharp
string sourceDir = "SOURCE DIRECTORY PATH";
string outputDir = "OUTPUT DIRECTORY PATH";
```

Tam dizin yollarını belirttiğinizden emin olun.

## 4. Adım: Kaynak Excel Dosyasını Yükleme

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

## 6. Adım: Mevcut Yazıcı Ayarlarını Silin

Her çalışma sayfası için yazıcı ayarlarının olup olmadığını kontrol edin ve gerekirse silin. Aşağıdaki kodu kullanın:

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

## 7. Adım: Değiştirilmiş Çalışma Kitabını Kaydetme

Değiştirilen çalışma kitabını aşağıdaki kodu kullanarak kaydedin:

```csharp
wb.Save(outputDir + "modifiedFilename.xlsx");
```

Bu, değiştirilen çalışma kitabını belirtilen çıktı dizinine kaydedecektir.

### Aspose.Cells for .NET kullanarak Çalışma Sayfalarının Mevcut Yazıcı Ayarlarını Kaldır için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Kaynak Excel dosyasını yükle
Workbook wb = new Workbook(sourceDir + "sampleRemoveExistingPrinterSettingsOfWorksheets.xlsx");
//Çalışma kitabının sayfa sayısını alın
int sheetCount = wb.Worksheets.Count;
//Tüm sayfaları yinele
for (int i = 0; i < sheetCount; i++)
{
    //i'nci çalışma sayfasına erişin
    Worksheet ws = wb.Worksheets[i];
    //Çalışma sayfası sayfası kurulumuna erişin
    PageSetup ps = ws.PageSetup;
    //Bu çalışma sayfası için yazıcı ayarlarının mevcut olup olmadığını kontrol edin
    if (ps.PrinterSettings != null)
    {
        //Aşağıdaki mesajı yazdır
        Console.WriteLine("PrinterSettings of this worksheet exist.");
        //Yazdırma sayfası adı ve kağıt boyutu
        Console.WriteLine("Sheet Name: " + ws.Name);
        Console.WriteLine("Paper Size: " + ps.PaperSize);
        //Yazıcı ayarlarını boş ayarlayarak kaldırın
        ps.PrinterSettings = null;
        Console.WriteLine("Printer settings of this worksheet are now removed by setting it null.");
        Console.WriteLine("");
    }//eğer
}//için
//çalışma kitabını kaydet
wb.Save(outputDir + "outputRemoveExistingPrinterSettingsOfWorksheets.xlsx");
```

## Çözüm

Artık Aspose.Cells for .NET kullanarak Excel'deki çalışma sayfalarından mevcut yazıcı ayarlarını nasıl kaldıracağınızı öğrendiniz. Bu eğitim, ortamı ayarlamaktan elektronik tablolar arasında gezinmeye ve yazıcı ayarlarını temizlemeye kadar sürecin her adımında size yol gösterdi. Artık bu bilgiyi Excel dosyalarınızdaki yazıcı ayarlarını yönetmek için kullanabilirsiniz.

### SSS

#### S1: Bir e-tablonun mevcut yazıcı ayarları olup olmadığını nasıl anlarım?

 A1: Bir çalışma sayfası için yazıcı ayarlarının mevcut olup olmadığını kontrol edebilirsiniz.`PrinterSettings` mülkiyeti`PageSetup` nesne. Değer boş değilse, mevcut yazıcı ayarları var demektir.

#### S2: Yalnızca belirli bir elektronik tablo için yazıcı ayarlarını silebilir miyim?

 Y2: Evet, belirli bir çalışma sayfasının yazıcı ayarlarını kaldırmak için aynı yaklaşımı o çalışma sayfasının ayarlarına erişerek kullanabilirsiniz.`PageSetup` nesne.

#### S3: Bu yöntem diğer düzen ayarlarını da kaldırır mı?

A3: Hayır, bu yöntem yalnızca yazıcı ayarlarını siler. Kenar boşlukları, kağıt yönü vb. gibi diğer düzen ayarları değişmeden kalır.

#### S4: Bu yöntem, .xls ve .xlsx gibi tüm Excel dosya biçimleri için çalışıyor mu?

C4: Evet, bu yöntem .xls ve .xlsx dahil Aspose.Cells tarafından desteklenen tüm Excel dosya formatlarında çalışır.

#### S5: Düzenlenen Excel dosyasında yazıcı ayarlarında yapılan değişiklikler kalıcı mı?

A5: Evet, yazıcı ayarlarında yapılan değişiklikler düzenlenen Excel dosyasına kalıcı olarak kaydedilir.