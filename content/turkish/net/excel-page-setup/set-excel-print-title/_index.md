---
title: Excel Yazdırma Başlığını Ayarla
linktitle: Excel Yazdırma Başlığını Ayarla
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak Excel dosyalarını kolayca değiştirmeyi ve yazdırma seçeneklerini özelleştirmeyi öğrenin.
type: docs
weight: 170
url: /tr/net/excel-page-setup/set-excel-print-title/
---
Bu kılavuzda, Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunda baskı başlıklarını nasıl ayarlayacağınız konusunda size yol göstereceğiz. Bu görevi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Ortamı ayarlama

Geliştirme ortamınızı kurduğunuzdan ve Aspose.Cells for .NET'i kurduğunuzdan emin olun. Kütüphanenin en son sürümünü Aspose resmi web sitesinden indirebilirsiniz.

## 2. Adım: Gerekli ad alanlarını içe aktarın

C# projenizde, Aspose.Cells ile çalışmak için gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.Cells;
```

## 3. Adım: Belgeler dizinine giden yolu ayarlama

 ilan etmek`dataDir` oluşturulan Excel dosyasını kaydetmek istediğiniz dizinin yolunu belirtmek için değişken:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 değiştirdiğinizden emin olun`"YOUR_DOCUMENT_DIRECTORY"` sisteminizdeki doğru yol ile.

## 4. Adım: Çalışma Kitabı Nesnesi Oluşturma

Oluşturmak istediğiniz Excel çalışma kitabını temsil eden bir Çalışma Kitabı nesnesi örneği oluşturun:

```csharp
Workbook workbook = new Workbook();
```

## Adım 5: İlk çalışma sayfasına erişim

Aşağıdaki kodu kullanarak Excel çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 6. Adım: Başlık Sütunlarını Tanımlama

Aşağıdaki kodu kullanarak başlık sütunlarını tanımlayın:

```csharp
pageSetup.PrintTitleColumns = "$A:$B";
```

Burada A ve B sütunlarını başlık sütunları olarak tanımladık. Bu değeri ihtiyaçlarınıza göre ayarlayabilirsiniz.

## Adım 7: Başlık Satırlarını Tanımlama

Aşağıdaki kodu kullanarak başlık satırlarını tanımlayın:

```csharp
pageSetup.PrintTitleRows = "$1:$2";
```

1. ve 2. satırları başlık satırları olarak tanımladık. Bu değerleri ihtiyaçlarınıza göre ayarlayabilirsiniz.

## 8. Adım: Excel çalışma kitabını kaydetme

 Excel çalışma kitabını tanımlanmış yazdırma başlıkları ile kaydetmek için,`Save` Çalışma Kitabı nesnesinin yöntemi:

```csharp
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

Bu, Excel çalışma kitabını "SetPrintTitle_out.xls" dosya adıyla belirtilen dizine kaydedecektir.

### Aspose.Cells for .NET kullanarak Excel Yazdırma Başlığını Ayarlamak için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook();
// Çalışma sayfasının PageSetup referansını alma
Aspose.Cells.PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// A ve B sütun numaralarını başlık sütunları olarak tanımlama
pageSetup.PrintTitleColumns = "$A:$B";
// 1 ve 2 numaralı satır numaralarını başlık satırları olarak tanımlama
pageSetup.PrintTitleRows = "$1:$2";
// Çalışma kitabını kaydedin.
workbook.Save(dataDir + "SetPrintTitle_out.xls");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak bir Excel elektronik tablosunda yazdırma başlıklarını nasıl ayarlayacağınızı öğrendiniz. Basılı başlıklar, yazdırılan her sayfada belirli satırları ve sütunları görüntülemenizi sağlayarak verilerin okunmasını ve referans alınmasını kolaylaştırır.

### SSS

#### 1. Excel'de belirli sütunlar için yazdırma başlıkları ayarlayabilir miyim?

 Evet, Aspose.Cells for .NET ile belirli sütunları yazdırma başlıkları olarak ayarlayabilirsiniz.`PrintTitleColumns` mülkiyeti`PageSetup` nesne.

#### 2. Hem sütun hem de satır başlıklarını yazdırmak mümkün mü?

 Evet, kullanarak hem sütun hem de satır başlıklarını yazdırabilirsiniz.`PrintTitleColumns` Ve`PrintTitleRows` özellikleri`PageSetup` nesne.

#### 3. Aspose.Cells for .NET ile başka hangi düzen ayarlarını özelleştirebilirim?

Aspose.Cells for .NET ile kenar boşlukları, sayfa yönü, baskı ölçeği ve daha fazlası gibi çeşitli sayfa düzeni ayarlarını özelleştirebilirsiniz.