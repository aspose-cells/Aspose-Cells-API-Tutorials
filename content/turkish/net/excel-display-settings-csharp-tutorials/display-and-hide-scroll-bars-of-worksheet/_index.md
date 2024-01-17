---
title: Çalışma Sayfasının Kaydırma Çubuklarını Görüntüleme ve Gizleme
linktitle: Çalışma Sayfasının Kaydırma Çubuklarını Görüntüleme ve Gizleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel çalışma sayfasındaki kaydırma çubuklarını görüntüleyin veya gizleyin.
type: docs
weight: 50
url: /tr/net/excel-display-settings-csharp-tutorials/display-and-hide-scroll-bars-of-worksheet/
---
Bu eğitimde, Aspose.Cells for .NET ile C# kaynak kodunu kullanarak bir Excel çalışma sayfasında dikey ve yatay kaydırma çubuklarını nasıl görüntüleyeceğinizi veya gizleyeceğinizi göstereceğiz. İstediğiniz sonucu elde etmek için aşağıdaki adımları izleyin.

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

## 3. Adım: Kaydırma Çubuklarını Gizleyin

 Kullan`IsVScrollBarVisible` Ve`IsHScrollBarVisible` özellikleri`Workbook.Settings` Çalışma sayfasının dikey ve yatay kaydırma çubuklarını gizlemek için nesne.

```csharp
workbook.Settings.IsVScrollBarVisible = false;
workbook.Settings.IsHScrollBarVisible = false;
```

## 4. Adım: Değişiklikleri Kaydet

 Gerekli değişiklikleri yaptıktan sonra, değiştirilen Excel dosyasını kullanarak kaydedin.`Save` yöntemi`Workbook` nesne.

```csharp
workbook.Save(dataDir + "output.xls");
```

### Aspose.Cells for .NET Kullanarak Çalışma Sayfasının Kaydırma Çubuklarını Görüntülemek ve Gizlemek için örnek kaynak kodu 

```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
// Excel dosyasını dosya akışı aracılığıyla açma
Workbook workbook = new Workbook(fstream);
// Excel dosyasının dikey kaydırma çubuğunu gizleme
workbook.Settings.IsVScrollBarVisible = false;
// Excel dosyasının yatay kaydırma çubuğunu gizleme
workbook.Settings.IsHScrollBarVisible = false;
// Değiştirilen Excel dosyasını kaydetme
workbook.Save(dataDir + "output.xls");
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

### Çözüm

Bu adım adım kılavuz, Aspose.Cells for .NET kullanarak bir Excel tablosunda dikey ve yatay kaydırma çubuklarının nasıl görüntüleneceği veya gizleneceğini gösterdi. Sağlanan C# kaynak kodunu kullanarak Excel dosyalarınızdaki kaydırma çubuklarının görünümünü kolayca özelleştirebilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET nedir?

Aspose.Cells for .NET, .NET uygulamalarında Excel dosyalarını işlemek için güçlü bir kütüphanedir.

#### Aspose.Cells for .NET'i nasıl kurabilirim?

 Aspose.Cells for .NET'i kurmak için ilgili paketi adresinden indirmeniz gerekmektedir.[Sürümleri Aspose](https://releases/aspose.com/cells/net/) ve bunu .NET projenize ekleyin.

#### Aspose.Cells for .NET ile bir Excel tablosundaki kaydırma çubuklarını nasıl görüntüleyebilir veya gizleyebilirim?

 Şunu kullanabilirsiniz:`IsVScrollBarVisible` Ve`IsHScrollBarVisible` özellikleri`Workbook.Settings` Bir Excel çalışma sayfasında sırasıyla dikey ve yatay kaydırma çubuğunu görüntülemek veya gizlemek için nesne.

#### Aspose.Cells for .NET başka hangi Excel dosya formatlarını destekliyor?

Aspose.Cells for .NET, XLS, XLSX, CSV, HTML, PDF vb. gibi çeşitli Excel dosya formatlarını destekler.