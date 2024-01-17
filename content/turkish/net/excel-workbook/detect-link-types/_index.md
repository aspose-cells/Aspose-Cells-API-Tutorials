---
title: Bağlantı Türlerini Algıla
linktitle: Bağlantı Türlerini Algıla
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak bir Excel çalışma kitabındaki bağlantı türlerini tespit edin.
type: docs
weight: 80
url: /tr/net/excel-workbook/detect-link-types/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak bir Excel çalışma kitabındaki bağlantı türlerini tespit etmenizi sağlayacak C# kaynak kodunu size adım adım anlatacağız. Bu işlemi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak dizini ayarlayın

```csharp
// kaynak dizini
string SourceDir = RunExamples.Get_SourceDirectory();
```

Bu ilk adımda linklerin bulunduğu Excel çalışma kitabının bulunduğu kaynak dizini tanımlıyoruz.

## Adım 2: Excel Çalışma Kitabını Yükleyin

```csharp
// Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Excel çalışma kitabını kaynak dosya yolunu kullanarak yüklüyoruz.

## 3. Adım: Elektronik Tabloyu Alın

```csharp
// İlk çalışma sayfasını alın (varsayılan)
Worksheet worksheet = workbook.Worksheets[0];
```

 Çalışma kitabının ilk çalışma sayfasını alıyoruz. değiştirebilirsiniz`[0]` Gerekirse belirli bir çalışma sayfasına erişmek için dizin.

## Adım 4: Bir hücre aralığı oluşturun

```csharp
// A1:B3 hücrelerinden oluşan bir aralık oluşturun
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Bu örnekte A1 hücresinden A7 hücresine kadar bir dizi hücre oluşturuyoruz. Hücre referanslarını gerektiği gibi ayarlayabilirsiniz.

## Adım 5: Köprüleri aralık içine alın

```csharp
// Aralıktaki köprüleri alın
Hyperlink[] hyperlinks = range.Hyperlinks;
```

Belirtilen aralıkta bulunan tüm köprüleri alıyoruz.

## Adım 6: Köprülere Göz Atın ve Bağlantı Türlerini Görüntüleyin

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Her bağlantıda döngü yaparız ve ekran metnini ve ilgili bağlantı türünü görüntüleriz.

### Aspose.Cells for .NET kullanarak Bağlantı Türlerini Algılamak için örnek kaynak kodu 
```csharp
//kaynak dizini
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
// İlk (varsayılan) çalışma sayfasını alın
Worksheet worksheet = workbook.Worksheets[0];
// A2:B3 aralığı oluşturun
Range range = worksheet.Cells.CreateRange("A1", "A7");
// Menzildeki Köprüleri Alın
Hyperlink[] hyperlinks = range.Hyperlinks;
foreach (Hyperlink link in hyperlinks)
{
	Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
Console.WriteLine("DetectLinkTypes executed successfully.");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET'i kullanarak bir Excel çalışma kitabındaki bağlantı türlerini nasıl tespit edeceğinizi öğrendiniz. Bu özellik, Excel çalışma kitaplarınızda bulunan köprülerle çalışmanıza olanak tanır. Excel çalışma kitabı işleme yeteneklerinizi genişletmek için Aspose.Cells'in özelliklerini keşfetmeye devam edin.

### SSS

#### S: Aspose.Cells for .NET'i projeme nasıl kurabilirim?

 C: Aspose.Cells for .NET'i NuGet paket yöneticisini kullanarak kurabilirsiniz. Aramak[Sürümleri Aspose](https://releases.aspose.com/cells/net) NuGet Paket Yönetici Konsolu'nda ve en son sürümü yükleyin.

#### S: İlk sayfa yerine belirli çalışma sayfalarındaki bağlantı türlerini algılayabilir miyim?

 C: Evet, değiştirebilirsiniz`workbook.Worksheets[0]` Belirli bir çalışma sayfasına erişmek için dizin. Örneğin, ikinci sayfaya erişmek için şunu kullanın:`workbook.Worksheets[1]`.

#### S: Aralıkta tespit edilen bağlantı türlerini değiştirmek mümkün müdür?

C: Evet, köprülere göz atabilir ve URL'leri güncelleme veya istenmeyen bağlantıları kaldırma gibi düzenleme işlemlerini gerçekleştirebilirsiniz.

#### S: Aspose.Cells for .NET'te ne tür bağlantılar mümkündür?

C: Olası bağlantı türleri arasında köprüler, diğer çalışma sayfalarına bağlantılar, harici dosyalara bağlantılar, web sitelerine bağlantılar vb. yer alır.

#### S: Aspose.Cells for .NET bir e-tabloda yeni bağlantılar oluşturmayı destekliyor mu?

 C: Evet, Aspose.Cells for .NET, aşağıdakileri kullanarak yeni bağlantılar oluşturmayı destekler:`Hyperlink` sınıf ve onunla ilişkili özellikler. Köprüler, URL'lere bağlantılar, diğer e-tablolara bağlantılar vb. ekleyebilirsiniz.

#### S: Aspose.Cells for .NET'i web uygulamalarında kullanabilir miyim?

C: Evet, Aspose.Cells for .NET web uygulamalarında kullanılabilir. Bunu ASP.NET, ASP.NET Core ve diğer .NET tabanlı web çerçevelerine gömebilirsiniz.

#### S: Aspose.Cells for .NET'i kullanırken herhangi bir dosya boyutu sınırı var mı?

C: Aspose.Cells for .NET, büyük Excel çalışma kitaplarını belirli bir sınırlama olmadan işleyebilir. Ancak gerçek dosya boyutu mevcut sistem kaynaklarıyla sınırlı olabilir.