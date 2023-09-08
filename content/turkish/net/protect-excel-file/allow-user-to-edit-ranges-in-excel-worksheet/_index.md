---
title: Kullanıcının Excel Çalışma Sayfasındaki Aralıkları Düzenlemesine İzin Ver
linktitle: Kullanıcının Excel Çalışma Sayfasındaki Aralıkları Düzenlemesine İzin Ver
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak kullanıcıların bir Excel tablosundaki belirli aralıkları düzenlemesine izin verin. C# kaynak koduyla adım adım kılavuz.
type: docs
weight: 10
url: /tr/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Bu kılavuzda, kullanıcının bir Excel elektronik tablosundaki belirli aralıkları düzenlemesine olanak sağlamak için Aspose.Cells for .NET'i nasıl kullanacağınız konusunda size yol göstereceğiz. Bu görevi gerçekleştirmek için aşağıdaki adımları izleyin.

## 1. Adım: Ortamı ayarlama

Geliştirme ortamınızı kurduğunuzdan ve Aspose.Cells for .NET'i kurduğunuzdan emin olun. Kütüphanenin son sürümünü Aspose resmi web sitesinden indirebilirsiniz.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells ile çalışmak için C# projenize gerekli ad alanlarını içe aktarın:

```csharp
using Aspose.Cells;
```

## 3. Adım: Belgeler dizininin yolunu ayarlama

 bir beyan`dataDir` Oluşturulan Excel dosyasını kaydetmek istediğiniz dizinin yolunu belirtmek için değişken:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Değiştirdiğinizden emin olun`"YOUR_DOCUMENT_DIRECTORY"` sisteminizde doğru yolla.

## Adım 4: Çalışma Kitabı Nesnesi Oluşturma

Oluşturmak istediğiniz Excel çalışma kitabını temsil eden yeni bir Çalışma Kitabı nesnesinin örneğini oluşturun:

```csharp
Workbook book = new Workbook();
```

## Adım 5: İlk çalışma sayfasına erişim

Aşağıdaki kodu kullanarak Excel çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 6. Adım: Yetkili değişiklik aralıklarının alınması

 Kullanarak izin verilen düzenleme aralıklarının koleksiyonunu alın`AllowEditRanges` mülk:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## Adım 7: Korunan Bir Aralık Tanımlayın

 kullanarak korumalı bir aralık tanımlayın.`Add` yöntemi`AllowEditRanges` Toplamak:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Burada A1 hücresinden C3 hücresine kadar uzanan korumalı bir "r2" aralığı oluşturduk.

## Adım 8: Şifrenin belirlenmesi

 kullanarak korunan aralık için bir parola belirtin.`Password` mülk:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 Değiştirdiğinizden emin olun`"YOUR_PASSWORD"` İstenilen şifre ile.

## Adım 9: Çalışma sayfasını koruma

 kullanarak çalışma sayfasını koruyun.`Protect` yöntemi`Worksheet` nesne:

```csharp
sheet.Protect(ProtectionType.All);
```

Bu, izin verilen aralıkların dışında herhangi bir değişiklik yapılmasını önleyerek elektronik tabloyu koruyacaktır.

## Adım 10: Kayıt

  Excel dosyası

 Oluşturulan Excel dosyasını kullanarak kaydedin.`Save` yöntemi`Workbook` nesne:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

İstediğiniz dosya adını ve doğru yolu belirttiğinizden emin olun.

### Aspose.Cells for .NET Kullanarak Kullanıcının Excel Çalışma Sayfasındaki Aralıkları Düzenlemesine İzin Ver için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Henüz mevcut değilse dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Yeni bir Çalışma Kitabı örneği oluşturun
Workbook book = new Workbook();
// İlk (varsayılan) çalışma sayfasını alın
Worksheet sheet = book.Worksheets[0];
// İzin Ver Düzenleme Aralıklarını Alma
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Korumalı Aralığı Tanımlayın
ProtectedRange proteced_range;
// Aralığı oluştur
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// Şifreyi belirtin
proteced_range.Password = "123";
// Sayfayı koruyun
sheet.Protect(ProtectionType.All);
// Excel dosyasını kaydedin
book.Save(dataDir + "protectedrange.out.xls");
```

## Çözüm

Artık kullanıcının bir Excel tablosundaki belirli aralıkları düzenlemesine olanak sağlamak için Aspose.Cells for .NET'i nasıl kullanacağınızı öğrendiniz. Özel ihtiyaçlarınızı karşılamak için Aspose.Cells'in sunduğu özellikleri daha fazla keşfetmekten çekinmeyin.


### SSS

#### 1. Kullanıcının Excel elektronik tablosundaki belirli aralıkları düzenlemesine nasıl izin verilir?

 Şunu kullanabilirsiniz:`ProtectedRangeCollection` İzin verilen değişiklik aralıklarını tanımlamak için sınıf. Kullan`Add` İstenilen hücrelerle yeni bir korumalı aralık oluşturma yöntemi.

#### 2. Yetkili değişiklik aralıkları için şifre belirleyebilir miyim?

 Evet, kullanarak bir şifre belirleyebilirsiniz.`Password` mülkiyeti`ProtectedRange` nesne. Bu, erişimi yalnızca şifreye sahip kullanıcılarla kısıtlayacaktır.

#### 3. İzin verilen aralıklar ayarlandıktan sonra e-tabloyu nasıl koruyabilirim?

 Kullan`Protect` yöntemi`Worksheet` Çalışma sayfasını korumak için nesne. Bu, izin verilen aralıkların dışında herhangi bir değişiklik yapılmasını önleyecek ve muhtemelen belirttiyseniz bir parola sorulmasını sağlayacaktır.