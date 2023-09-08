---
title: Çalışma Sayfasının Kılavuz Çizgilerini Görüntüleme ve Gizleme
linktitle: Çalışma Sayfasının Kılavuz Çizgilerini Görüntüleme ve Gizleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile Excel çalışma sayfasındaki kılavuz çizgilerinin görünümünü kontrol edin.
type: docs
weight: 30
url: /tr/net/excel-display-settings-csharp-tutorials/display-and-hide-gridlines-of-worksheet/
---
Bu eğitimde, Aspose.Cells for .NET ile C# kaynak kodunu kullanarak bir Excel çalışma sayfasında kılavuz çizgilerini nasıl gösterip gizleyeceğinizi göstereceğiz. İstediğiniz sonucu elde etmek için aşağıdaki adımları izleyin.

## 1. Adım: Gerekli kitaplıkları içe aktarın

.NET için Aspose.Cells kütüphanesini kurduğunuzdan emin olun ve gerekli kütüphaneleri C# projenize aktarın.

```csharp
using Aspose.Cells;
using System.IO;
```

## Adım 2: Dizin yolunu ayarlayın ve Excel dosyasını açın

 Excel dosyanızı içeren dizinin yolunu ayarlayın, ardından bir dosya akışı oluşturup bir örnek oluşturarak dosyayı açın.`Workbook` nesne.

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

## 3. Adım: İlk çalışma sayfasına gidin ve kılavuz çizgilerini gizleyin

 kullanarak Excel dosyasındaki ilk çalışma sayfasına erişin.`Worksheets` mülkiyeti`Workbook` nesne. Daha sonra şunu kullanın:`IsGridlinesVisible` mülkiyeti`Worksheet` Kılavuz çizgilerini gizlemek için nesne.

```csharp
Worksheet worksheet = workbook.Worksheets[0];
worksheet.IsGridlinesVisible = false;
```

## 4. Adım: Değişiklikleri Kaydet

 Gerekli değişiklikleri yaptıktan sonra, değiştirilen Excel dosyasını kullanarak kaydedin.`Save` yöntemi`Workbook` nesne.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET Kullanarak Çalışma Sayfasının Kılavuz Çizgilerini Görüntülemek ve Gizlemek için örnek kaynak kodu 

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
// Excel dosyasının ilk çalışma sayfasının ızgara çizgilerini gizleme
worksheet.IsGridlinesVisible = false;
// Değiştirilen Excel dosyasını kaydetme
workbook.Save(dataDir + "output.xls");
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Bu adım adım kılavuz, Aspose.Cells for .NET kullanarak bir Excel tablosunda kılavuz çizgilerini nasıl gösterip gizleyeceğinizi gösterdi. Sağlanan C# kaynak kodunu kullanarak, Excel dosyalarınızdaki kılavuz çizgilerinin görünümünü kolayca özelleştirebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için güçlü bir kütüphanedir.

#### Aspose.Cells for .NET'i nasıl kurabilirim?

 Aspose.Cells for .NET'i kurmak için ilgili paketi adresinden indirmeniz gerekmektedir.[Sürümleri Aspose](https://releases/aspose.com/cells/net/) ve bunu .NET projenize ekleyin.

#### Aspose.Cells for .NET ile bir Excel tablosundaki kılavuz çizgilerini nasıl gösterebilir veya gizleyebilirim?

 Şunu kullanabilirsiniz:`IsGridlinesVisible` mülkiyeti`Worksheet` Kılavuz çizgilerini göstermek veya gizlemek için nesne. Şuna ayarla:`true` onlara göstermek ve`false` onları saklamak için.

#### Aspose.Cells for .NET başka hangi Excel dosya formatlarını destekliyor?

Aspose.Cells for .NET, XLS, XLSX, CSV, HTML, PDF ve çok daha fazlası gibi çeşitli Excel dosya formatlarını destekler.

