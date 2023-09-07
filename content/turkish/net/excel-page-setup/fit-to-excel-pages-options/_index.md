---
title: Excel Sayfalarına Sığdır Seçenekleri
linktitle: Excel Sayfalarına Sığdır Seçenekleri
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile sayfaları bir Excel elektronik tablosuna otomatik sığdırmayı öğrenin.
type: docs
weight: 30
url: /tr/net/excel-page-setup/fit-to-excel-pages-options/
---
Bu yazıda, aşağıdaki C# kaynak kodunu açıklamak için size adım adım yol göstereceğiz: Aspose.Cells for .NET kullanarak Excel Sayfalarına Sığdırma Seçenekleri. Bu işlemi gerçekleştirmek için .NET için Aspose.Cells kütüphanesini kullanacağız. Excel'de sayfalara sığdırmayı yapılandırmak için aşağıdaki adımları izleyin.

## 1. Adım: Çalışma Kitabı Oluşturma
İlk adım bir çalışma kitabı oluşturmaktır. Bir Workbook nesnesini somutlaştıracağız. İşte bir çalışma kitabı oluşturmak için kod:

```csharp
// Belgeler dizinine giden yol
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Bir Çalışma Kitabı nesnesinin örneğini oluşturun
Workbook workbook = new Workbook();
```

## 2. Adım: Çalışma sayfasına erişme
Artık çalışma kitabını oluşturduğumuza göre, ilk çalışma sayfasına gitmemiz gerekiyor. İlk sayfaya erişmek için 0 indeksini kullanacağız. İşte ona erişmek için kod:

```csharp
// Çalışma kitabındaki ilk çalışma sayfasına erişim
Worksheet worksheet = workbook.Worksheets[0];
```

## 3. Adım: Sayfalara Sığdır Ayarı
 Bu adımda, çalışma sayfasının sayfalarına ayarlamayı yapılandıracağız. biz kullanacağız`FitToPagesTall` Ve`FitToPagesWide` özellikleri`PageSetup` Çalışma sayfasının yüksekliği ve genişliği için istenen sayfa sayısını belirtmek için nesne. İşte bunun için kod:

```csharp
// Çalışma sayfasının yüksekliği için sayfa sayısını yapılandırın
worksheet.PageSetup.FitToPagesTall = 1;

// Çalışma sayfasının genişliği için sayfa sayısını yapılandırın
worksheet.PageSetup.FitToPagesWide = 1;
```

## 4. Adım: Çalışma Kitabını Kaydetme
 Artık sayfalara sığdır ayarını yaptığımıza göre çalışma kitabını kaydedebiliriz. biz kullanacağız`Save` Bunun için Çalışma Kitabı nesnesinin yöntemi. İşte çalışma kitabını kaydetmek için kod:

```csharp
// çalışma kitabını kaydet
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Aspose.Cells for .NET kullanan Excel Sayfalarına Sığdırma Seçenekleri için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook();
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Çalışma sayfasının uzunluğunun yayılacağı sayfa sayısını ayarlama
worksheet.PageSetup.FitToPagesTall = 1;
//Çalışma sayfasının genişliğinin yayılacağı sayfa sayısını ayarlama
worksheet.PageSetup.FitToPagesWide = 1;
// Çalışma kitabını kaydedin.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Çözüm
Bu yazıda, Aspose.Cells for .NET kullanarak Excel'de sayfalara sığdırmayı nasıl yapılandıracağımızı öğrendik. Çalışma kitabını oluşturma, çalışma sayfasına erişme, sayfalara sığdırma ve çalışma kitabını kaydetme adımlarından geçtik. Artık elektronik tablolarınızı istediğiniz sayfalara göre ayarlamak için bu bilgiyi kullanabilirsiniz.

### SSS

#### S: Aspose.Cells for .NET'i nasıl kurabilirim?

C: Aspose.Cells for .NET'i kurmak için Visual Studio'da NuGet paket yöneticisini kullanabilirsiniz. "Aspose.Cells" paketini bulun ve projenize kurun.

#### S: Sayfaları hem yüksekliğe hem de genişliğe sığdırabilir miyim?

 C: Evet, çalışma sayfasının hem yüksekliğini hem de genişliğini ayarlayabilirsiniz.`FitToPagesTall` Ve`FitToPagesWide` özellikler. Her boyut için istediğiniz sayfa sayısını belirleyebilirsiniz.

#### S: Sayfalara Sığdır seçeneklerini nasıl özelleştirebilirim?

C: Sayfa sayısını belirtmenin yanı sıra, çalışma sayfası ölçeği, kağıt yönü, kenar boşlukları ve daha fazlası gibi diğer sayfalara sığdır seçeneklerini de özelleştirebilirsiniz. içinde bulunan özellikleri kullanın.`PageSetup` bunun için itiraz edin.

#### S: Mevcut çalışma kitaplarını işlemek için Aspose.Cells for .NET'i kullanabilir miyim?

C: Evet, mevcut çalışma kitaplarını açmak ve düzenlemek için Aspose.Cells for .NET'i kullanabilirsiniz. Çeşitli işlemleri gerçekleştirmek için çalışma sayfalarına, hücrelere, formüllere, stillere ve diğer çalışma kitabı öğelerine erişebilirsiniz.