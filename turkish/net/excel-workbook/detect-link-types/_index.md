---
title: Bağlantı Türlerini Algıla
linktitle: Bağlantı Türlerini Algıla
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel çalışma kitabındaki bağlantı tiplerini tespit edin.
type: docs
weight: 80
url: /tr/net/excel-workbook/detect-link-types/
---
Bu öğreticide, Aspose.Cells for .NET kullanarak bir Excel çalışma kitabındaki bağlantı türlerini algılamanıza olanak sağlayacak şekilde sağlanan C# kaynak kodunda adım adım yol göstereceğiz. Bu işlemi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak dizini ayarlayın

```csharp
// kaynak dizin
string SourceDir = RunExamples.Get_SourceDirectory();
```

Bu ilk adımda, bağlantıların bulunduğu Excel çalışma kitabının bulunduğu kaynak dizini tanımlarız.

## 2. Adım: Excel Çalışma Kitabını Yükleyin

```csharp
//Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(SourceDir + "LinkTypes.xlsx");
```

Excel çalışma kitabını kaynak dosya yolunu kullanarak yüklüyoruz.

## 3. Adım: Elektronik Tabloyu Alın

```csharp
// İlk çalışma sayfasını al (varsayılan)
Worksheet worksheet = workbook.Worksheets[0];
```

 Çalışma kitabının ilk çalışma sayfasını alıyoruz. değiştirebilirsiniz`[0]` Gerekirse belirli bir çalışma sayfasına erişmek için dizin.

## 4. Adım: Bir hücre aralığı oluşturun

```csharp
// Bir hücre aralığı oluşturun A1:B3
Range range = worksheet.Cells.CreateRange("A1", "A7");
```

Bu örnekte A1 hücresinden A7 hücresine kadar bir hücre aralığı oluşturuyoruz. Hücre referanslarını gerektiği gibi ayarlayabilirsiniz.

## 5. Adım: Menzildeki köprüleri alın

```csharp
// Aralıktaki köprüleri al
Hyperlink[] hyperlinks = range.Hyperlinks;
```

Belirtilen aralıkta bulunan tüm köprüleri alırız.

## 6. Adım: Köprülere Göz Atın ve Bağlantı Türlerini Görüntüleyin

```csharp
foreach (Hyperlink link in hyperlinks)
{
Console.WriteLine(link.TextToDisplay + ": " + link.LinkType);
}
```

Her bağlantıda döngü halinde dolaşıyoruz ve ekran metnini ve ilgili bağlantı türünü gösteriyoruz.

### Aspose.Cells for .NET kullanarak Bağlantı Türlerini Algılamak için örnek kaynak kodu 
```csharp
//kaynak dizin
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

Tebrikler! Aspose.Cells for .NET kullanarak bir Excel çalışma kitabında bağlantı türlerinin nasıl algılanacağını öğrendiniz. Bu özellik, Excel çalışma kitaplarınızda bulunan köprülerle çalışmanıza olanak tanır. Excel çalışma kitabı işleme becerilerinizi genişletmek için Aspose.Cells'in özelliklerini keşfetmeye devam edin.

### SSS

#### S: Aspose.Cells for .NET'i projeme nasıl kurabilirim?

 C: Aspose.Cells for .NET'i NuGet paket yöneticisini kullanarak kurabilirsiniz. Aramak[Bültenler](https://releases.aspose.com/cells/net) NuGet Paket Yöneticisi Konsolunda ve en son sürümü yükleyin.

#### S: Bağlantı türlerini ilk sayfa yerine belirli çalışma sayfalarında algılayabilir miyim?

 A: Evet, değiştirebilirsiniz`workbook.Worksheets[0]` belirli bir çalışma sayfasına erişmek için dizin. Örneğin, ikinci sayfaya erişmek için şunu kullanın:`workbook.Worksheets[1]`.

#### S: Menzilde tespit edilen bağlantı türlerini değiştirmek mümkün müdür?

C: Evet, köprülere göz atabilir ve URL'leri güncelleme veya istenmeyen bağlantıları kaldırma gibi düzenleme işlemlerini gerçekleştirebilirsiniz.

#### S: Aspose.Cells for .NET'te ne tür bağlantılar mümkündür?

Y: Olası bağlantı türleri arasında köprüler, diğer çalışma sayfalarına bağlantılar, harici dosyalara bağlantılar, web sitelerine bağlantılar vb. yer alır.

#### S: Aspose.Cells for .NET bir hesap tablosunda yeni bağlantılar oluşturmayı destekliyor mu?

 C: Evet, Aspose.Cells for .NET,`Hyperlink` sınıf ve ilişkili özellikleri. Köprüler, URL'lere bağlantılar, diğer e-tablolara bağlantılar vb. ekleyebilirsiniz.

#### S: Aspose.Cells for .NET'i web uygulamalarında kullanabilir miyim?

C: Evet, Aspose.Cells for .NET web uygulamalarında kullanılabilir. ASP.NET, ASP.NET Core ve diğer .NET tabanlı web çerçevelerine katıştırabilirsiniz.

#### S: Aspose.Cells for .NET kullanırken herhangi bir dosya boyutu sınırı var mı?

Y: Aspose.Cells for .NET, büyük Excel çalışma kitaplarını belirli bir sınırlama olmadan işleyebilir. Ancak, gerçek dosya boyutu mevcut sistem kaynaklarıyla sınırlı olabilir.