---
title: Excel İlk Sayfa Numarasını Ayarla
linktitle: Excel İlk Sayfa Numarasını Ayarla
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel'de ilk sayfa numarasını nasıl ayarlayacağınızı öğrenin.
type: docs
weight: 90
url: /tr/net/excel-page-setup/set-excel-first-page-number/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak Excel'de ilk sayfa numarasını nasıl ayarlayacağınız konusunda size yol göstereceğiz. Süreci göstermek için C# kaynak kodunu kullanacağız.

## 1. Adım: Ortamı ayarlama

Makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Kod dosyanızda, Aspose.Cells ile çalışmak için gereken kütüphaneleri içe aktarın. İşte ilgili kod:

```csharp
using Aspose.Cells;
```

## 3. Adım: Veri Dizinini Ayarlayın

Değiştirilen Excel dosyasını kaydetmek istediğiniz veri dizinini ayarlayın. Aşağıdaki kodu kullanın:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Tam dizin yolunu belirttiğinizden emin olun.

## Adım 4: Çalışma kitabını ve çalışma sayfasını oluşturma

Yeni bir Çalışma Kitabı nesnesi oluşturun ve aşağıdaki kodu kullanarak çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Bu, çalışma sayfası içeren boş bir çalışma kitabı oluşturacaktır.

## Adım 5: İlk sayfanın numarasını ayarlama

Aşağıdaki kodu kullanarak çalışma sayfası sayfalarının ilk sayfasının numarasını ayarlayın:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Bu, ilk sayfa numarasını 2 olarak ayarlayacaktır.

## Adım 6: Değiştirilmiş Çalışma Kitabını Kaydetme

Değiştirilen çalışma kitabını aşağıdaki kodu kullanarak kaydedin:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Bu, değiştirilen çalışma kitabını belirtilen veri dizinine kaydedecektir.

### Aspose.Cells for .NET kullanarak Excel İlk Sayfa Numarasını Ayarlamak için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook();
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Çalışma sayfası sayfalarının ilk sayfa numarasını ayarlama
worksheet.PageSetup.FirstPageNumber = 2;
// Çalışma Kitabını kaydedin.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Çözüm

Artık Aspose.Cells for .NET kullanarak Excel'de ilk sayfa numarasını nasıl ayarlayacağınızı öğrendiniz. Bu öğretici, ortamın ayarlanmasından ilk sayfa numarasının ayarlanmasına kadar sürecin her adımında size yol gösterdi. Artık bu bilgiyi, Excel dosyalarınızdaki sayfa numaralandırmayı özelleştirmek için kullanabilirsiniz.

### SSS

#### S1: Her çalışma sayfası için farklı bir ilk sayfa numarası ayarlayabilir miyim?

 A1: Evet, her çalışma sayfası için farklı bir ilk sayfa numarası belirleyebilirsiniz.`FirstPageNumber`ilgili çalışma sayfasının özelliği`PageSetup` nesne.

#### S2: Mevcut bir e-tablonun ilk sayfa numarasını nasıl kontrol edebilirim?

 A2: Mevcut bir çalışma sayfasının ilk sayfa numarasını şu adrese erişerek kontrol edebilirsiniz:`FirstPageNumber` mülkiyeti`PageSetup` o çalışma sayfasına karşılık gelen nesne.

#### S3: Sayfa numaralandırma varsayılan olarak her zaman 1'den mi başlar?

A3: Evet, sayfa numaralandırma Excel'de varsayılan olarak 1'den başlar. Ancak, farklı bir ilk sayfa numarası ayarlamak için bu eğitimde gösterilen kodu kullanabilirsiniz.

#### S4: Düzenlenen Excel dosyasında ilk sayfa numarasındaki değişiklikler kalıcı mı?

A4: Evet, ilk sayfa numarasında yapılan değişiklikler değiştirilen Excel dosyasına kalıcı olarak kaydedilir.

#### S5: Bu yöntem, .xls ve .xlsx gibi tüm Excel dosya biçimleri için çalışıyor mu?

C5: Evet, bu yöntem .xls ve .xlsx dahil Aspose.Cells tarafından desteklenen tüm Excel dosya formatlarında çalışır.