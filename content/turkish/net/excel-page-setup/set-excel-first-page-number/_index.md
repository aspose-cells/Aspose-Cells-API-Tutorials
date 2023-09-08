---
title: Excel İlk Sayfa Numarasını Ayarla
linktitle: Excel İlk Sayfa Numarasını Ayarla
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak Excel'de ilk sayfa numarasını nasıl ayarlayacağınızı öğrenin.
type: docs
weight: 90
url: /tr/net/excel-page-setup/set-excel-first-page-number/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak Excel'de ilk sayfa numarasını nasıl ayarlayacağınız konusunda size yol göstereceğiz. Süreci göstermek için C# kaynak kodunu kullanacağız.

## 1. Adım: Ortamı ayarlama

Aspose.Cells for .NET'in makinenizde kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Aspose.Cells ile çalışmak için gereken kütüphaneleri kod dosyanıza aktarın. İşte ilgili kod:

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

Aşağıdaki kodu kullanarak çalışma sayfası sayfalarının ilk sayfasının sayısını ayarlayın:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Bu, ilk sayfa numarasını 2 olarak ayarlayacaktır.

## Adım 6: Değiştirilen Çalışma Kitabını Kaydetme

Değiştirilen çalışma kitabını aşağıdaki kodu kullanarak kaydedin:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Bu, değiştirilen çalışma kitabını belirtilen veri dizinine kaydedecektir.

### Aspose.Cells for .NET kullanarak Excel İlk Sayfa Numarasını Ayarlama için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
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

Artık Aspose.Cells for .NET kullanarak Excel'de ilk sayfa numarasını nasıl ayarlayacağınızı öğrendiniz. Bu eğitim, ortamın ayarlanmasından ilk sayfa numarasının ayarlanmasına kadar sürecin her adımında size yol gösterdi. Artık bu bilgiyi Excel dosyalarınızdaki sayfa numaralandırmasını özelleştirmek için kullanabilirsiniz.

### SSS'ler

#### S1: Her çalışma sayfası için farklı bir ilk sayfa numarası ayarlayabilir miyim?

 Cevap1: Evet, her çalışma sayfası için farklı bir ilk sayfa numarası ayarlayabilirsiniz.`FirstPageNumber`ilgili çalışma sayfasının özelliği`PageSetup` nesne.

#### S2: Mevcut bir e-tablonun ilk sayfa numarasını nasıl kontrol edebilirim?

 Cevap2: Mevcut bir çalışma sayfasının ilk sayfa numarasını şuraya erişerek kontrol edebilirsiniz:`FirstPageNumber` mülkiyeti`PageSetup` bu çalışma sayfasına karşılık gelen nesne.

#### S3: Sayfa numaralandırması varsayılan olarak her zaman 1'den mi başlar?

C3: Evet, Excel'de sayfa numaralandırma varsayılan olarak 1'den başlar. Ancak farklı bir ilk sayfa numarası ayarlamak için bu eğitimde gösterilen kodu kullanabilirsiniz.

#### S4: Düzenlenen Excel dosyasındaki ilk sayfa numarasındaki değişiklikler kalıcı mıdır?

Cevap4: Evet, ilk sayfa numarasında yapılan değişiklikler kalıcı olarak değiştirilen Excel dosyasına kaydedilir.

#### S5: Bu yöntem .xls ve .xlsx gibi tüm Excel dosya formatlarında işe yarar mı?

Cevap5: Evet, bu yöntem Aspose.Cells tarafından desteklenen .xls ve .xlsx dahil tüm Excel dosya formatlarında işe yarar.