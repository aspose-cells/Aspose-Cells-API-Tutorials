---
title: Excel Sayfalarına Sığdır Seçenekleri
linktitle: Excel Sayfalarına Sığdır Seçenekleri
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile bir Excel tablosundaki sayfaları nasıl otomatik olarak sığdıracağınızı öğrenin.
type: docs
weight: 30
url: /tr/net/excel-page-setup/fit-to-excel-pages-options/
---
Bu makalede sizi adım adım aşağıdaki C# kaynak kodunu açıklamaya yönlendireceğiz: Aspose.Cells for .NET kullanarak Excel Sayfalarına Sığdır Seçenekleri. Bu işlemi gerçekleştirmek için .NET için Aspose.Cells kütüphanesini kullanacağız. Excel'de sayfalara sığdırmayı yapılandırmak için aşağıdaki adımları izleyin.

## Adım 1: Çalışma Kitabı Oluşturma
İlk adım bir çalışma kitabı oluşturmaktır. Bir Workbook nesnesini başlatacağız. İşte çalışma kitabı oluşturma kodu:

```csharp
// Belgeler dizininin yolu
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook();
```

## Adım 2: Çalışma sayfasına erişme
Artık çalışma kitabını oluşturduğumuza göre ilk çalışma sayfasına gitmemiz gerekiyor. İlk sayfaya erişmek için 0 indeksini kullanacağız. İşte ona erişmenizi sağlayacak kod:

```csharp
// Çalışma kitabındaki ilk çalışma sayfasına erişim
Worksheet worksheet = workbook.Worksheets[0];
```

## 3. Adım: Sayfalara Sığdır'ı Ayarlama
 Bu adımda çalışma sayfasının sayfalarındaki ayarlamayı yapılandıracağız. kullanacağız`FitToPagesTall` Ve`FitToPagesWide` özellikleri`PageSetup` Çalışma sayfasının yüksekliği ve genişliği için istenen sayfa sayısını belirtmek için nesne. İşte bunun için kod:

```csharp
// Çalışma sayfasının yüksekliğine göre sayfa sayısını yapılandırma
worksheet.PageSetup.FitToPagesTall = 1;

// Çalışma sayfasının genişliğine göre sayfa sayısını yapılandırma
worksheet.PageSetup.FitToPagesWide = 1;
```

## Adım 4: Çalışma Kitabını Kaydetme
 Artık sayfalara sığdırmayı yapılandırdığımıza göre çalışma kitabını kaydedebiliriz. kullanacağız`Save` Bunun için Çalışma Kitabı nesnesinin yöntemi. Çalışma kitabını kaydetme kodu:

```csharp
// Çalışma kitabını kaydet
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Aspose.Cells for .NET kullanan Excel Sayfalarına Sığdır Seçenekleri için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
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
Bu makalede Aspose.Cells for .NET kullanarak Excel'de sayfalara sığdırmayı nasıl yapılandıracağımızı öğrendik. Şu adımları izledik: çalışma kitabını oluşturma, çalışma sayfasına erişme, sayfalara sığdırmayı yapılandırma ve çalışma kitabını kaydetme. Artık bu bilgiyi e-tablolarınızı istediğiniz sayfalara ayarlamak için kullanabilirsiniz.

### SSS

#### S: Aspose.Cells for .NET'i nasıl kurabilirim?

C: Aspose.Cells for .NET'i yüklemek için Visual Studio'daki NuGet paket yöneticisini kullanabilirsiniz. "Aspose.Cells" paketini bulun ve projenize yükleyin.

#### S: Sayfaları hem yüksekliğe hem de genişliğe sığdırabilir miyim?

 C: Evet, çalışma sayfasının hem yüksekliğini hem de genişliğini aşağıdaki düğmeyi kullanarak ayarlayabilirsiniz:`FitToPagesTall` Ve`FitToPagesWide` özellikler. Her boyut için istediğiniz sayfa sayısını belirtebilirsiniz.

#### S: Sayfalara Sığdır seçeneklerini nasıl özelleştirebilirim?

C: Sayfa sayısını belirtmenin yanı sıra, çalışma sayfası ölçeği, kağıt yönü, kenar boşlukları ve daha fazlası gibi diğer sayfalara sığdırma seçeneklerini de özelleştirebilirsiniz. Mevcut özellikleri kullanın`PageSetup` buna itiraz ediyorum.

#### S: Mevcut çalışma kitaplarını işlemek için Aspose.Cells for .NET'i kullanabilir miyim?

C: Evet, mevcut çalışma kitaplarını açmak ve düzenlemek için Aspose.Cells for .NET'i kullanabilirsiniz. Çeşitli işlemleri gerçekleştirmek için çalışma sayfalarına, hücrelere, formüllere, stillere ve diğer çalışma kitabı öğelerine erişebilirsiniz.