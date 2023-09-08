---
title: Çalışma Sayfasının Sayfa Sonu Önizlemesi
linktitle: Çalışma Sayfasının Sayfa Sonu Önizlemesi
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak çalışma sayfasının sayfa sonu önizlemesini gösteren adım adım kılavuz.
type: docs
weight: 110
url: /tr/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
Bu derste Aspose.Cells for .NET kullanarak bir çalışma sayfasının sayfa sonu önizlemesinin nasıl gösterileceğini açıklayacağız. İstenilen sonucu elde etmek için şu adımları izleyin:

## 1. Adım: Ortamı ayarlama

Aspose.Cells for .NET'i kurduğunuzdan ve geliştirme ortamınızı kurduğunuzdan emin olun. Ayrıca sayfa sonu önizlemesini görüntülemek istediğiniz Excel dosyasının bir kopyasına sahip olduğunuzdan emin olun.

## 2. Adım: Gerekli bağımlılıkları içe aktarın

Aspose.Cells'teki sınıfları kullanmak için gerekli yönergeleri ekleyin:

```csharp
using Aspose.Cells;
using System.IO;
```

## 3. Adım: Kodun başlatılması

Excel belgelerinizi içeren dizinin yolunu başlatarak başlayın:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Adım 4: Excel dosyasını açma

 Oluşturmak`FileStream` Açılacak Excel dosyasını içeren nesne:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Bir örnek oluştur`Workbook` nesnesini açın ve dosya akışını kullanarak Excel dosyasını açın:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Adım 5: Elektronik Tabloya Erişim

Excel dosyasındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Adım 6: Sayfa bazında önizlemenin görüntülenmesi

E-tablo için sayfa bazında önizlemeyi etkinleştirin:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Adım 7: Değişiklikleri Kaydetme

Excel dosyasına yapılan değişiklikleri kaydedin:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Adım 8: Dosya akışını kapatma

Tüm kaynakları serbest bırakmak için dosya akışını kapatın:

```csharp
fstream.Close();
```

### Aspose.Cells for .NET kullanılarak Çalışma Sayfasının Sayfa Sonu Önizlemesi için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını dosya akışı aracılığıyla açma
Workbook workbook = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Çalışma sayfasını sayfa sonu önizlemesinde görüntüleme
worksheet.IsPageBreakPreview = true;
// Değiştirilen Excel dosyasını kaydetme
workbook.Save(dataDir + "output.xls");
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Bu eğitimde Aspose.Cells for .NET kullanarak bir çalışma sayfasının sayfa sonu önizlemesini nasıl görüntüleyeceğinizi öğrendiniz. Anlatılan adımları takip ederek Excel dosyalarınızın görünümünü ve düzenini kolaylıkla kontrol edebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için kullanılan popüler bir yazılım kütüphanesidir.

#### Çalışma sayfasının tamamı yerine belirli bir çalışma sayfasının sayfa sayfa önizlemesini gösterebilir miyim?

Evet, Aspose.Cells'i kullanarak ilgili Çalışma Sayfası nesnesine erişerek belirli bir çalışma sayfası için sayfa sonu önizlemesini etkinleştirebilirsiniz.

#### Aspose.Cells diğer Excel dosya düzenleme özelliklerini destekliyor mu?

Evet, Aspose.Cells, Excel dosyalarını düzenlemek ve değiştirmek için veri ekleme, biçimlendirme, grafik oluşturma vb. gibi çok çeşitli özellikler sunar.

#### Aspose.Cells yalnızca .xls formatındaki Excel dosyalarıyla mı çalışır?

Hayır, Aspose.Cells .xls ve .xlsx dahil olmak üzere çeşitli Excel dosya formatlarını destekler.
	