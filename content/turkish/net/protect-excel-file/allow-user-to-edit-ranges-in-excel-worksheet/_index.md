---
title: Kullanıcının Excel Çalışma Sayfasındaki Aralıkları Düzenlemesine İzin Ver
linktitle: Kullanıcının Excel Çalışma Sayfasındaki Aralıkları Düzenlemesine İzin Ver
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak kullanıcıların bir Excel elektronik tablosundaki belirli aralıkları düzenlemesine izin verin. C# dilinde kaynak koduyla adım adım kılavuz.
type: docs
weight: 10
url: /tr/net/protect-excel-file/allow-user-to-edit-ranges-in-excel-worksheet/
---
Bu kılavuzda, kullanıcının bir Excel elektronik tablosunda belirli aralıkları düzenlemesine izin vermek için Aspose.Cells for .NET'i nasıl kullanacağınız konusunda size yol göstereceğiz. Bu görevi gerçekleştirmek için aşağıdaki adımları izleyin.

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

Oluşturmak istediğiniz Excel çalışma kitabını temsil eden yeni bir Çalışma Kitabı nesnesi oluşturun:

```csharp
Workbook book = new Workbook();
```

## Adım 5: İlk çalışma sayfasına erişim

Aşağıdaki kodu kullanarak Excel çalışma kitabındaki ilk çalışma sayfasına gidin:

```csharp
Worksheet sheet = book.Worksheets[0];
```

## 6. Adım: Yetkili değişiklik aralıklarını alma

 kullanarak izin verilen düzenleme aralıklarının koleksiyonunu alın.`AllowEditRanges` mülk:

```csharp
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
```

## 7. Adım: Korumalı Bir Aralık Tanımlayın

 kullanarak korunan bir aralık tanımlayın.`Add` yöntemi`AllowEditRanges` Toplamak:

```csharp
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
protectedRange protectedRange = allowRanges[idx];
```

Burada, A1 hücresinden C3 hücresine kadar uzanan korumalı bir "r2" aralığı oluşturduk.

## 8. Adım: Parolanın belirtilmesi

 kullanarak korunan aralık için bir parola belirleyin.`Password` mülk:

```csharp
protectedRange.Password = "YOUR_PASSWORD";
```

 değiştirdiğinizden emin olun`"YOUR_PASSWORD"` istenilen şifre ile

## 9. Adım: Çalışma sayfasını koruma

 kullanarak çalışma sayfasını koruyun.`Protect` yöntemi`Worksheet` nesne:

```csharp
sheet.Protect(ProtectionType.All);
```

Bu, izin verilen aralıklar dışında herhangi bir değişiklik yapılmasını engelleyerek elektronik tabloyu koruyacaktır.

## Adım 10:

  Excel dosyası

 Oluşturulan Excel dosyasını kullanarak kaydedin.`Save` yöntemi`Workbook` nesne:

```csharp
book.Save(dataDir + "protectedrange.out.xls");
```

İstenen dosya adını ve doğru yolu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Kullanıcının Excel Çalışma Sayfasındaki Aralıkları Düzenlemesine İzin Ver için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Halihazırda mevcut değilse, dizin oluşturun.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
// Yeni bir Çalışma Kitabı oluşturun
Workbook book = new Workbook();
// İlk (varsayılan) çalışma sayfasını alın
Worksheet sheet = book.Worksheets[0];
// Aralıkları Düzenlemeye İzin Ver'i Alın
ProtectedRangeCollection allowRanges = sheet.AllowEditRanges;
// Korumalı Aralığı Tanımla
ProtectedRange proteced_range;
// Aralığı oluştur
int idx = allowRanges.Add("r2", 1, 1, 3, 3);
proteced_range = allowRanges[idx];
// parolayı belirtin
proteced_range.Password = "123";
// Sayfayı koruyun
sheet.Protect(ProtectionType.All);
// Excel dosyasını kaydedin
book.Save(dataDir + "protectedrange.out.xls");
```

## Çözüm

Artık Aspose.Cells for .NET'in, kullanıcının bir Excel elektronik tablosundaki belirli aralıkları düzenlemesine izin vermek için nasıl kullanılacağını öğrendiniz. Özel ihtiyaçlarınızı karşılamak için Aspose.Cells tarafından sunulan özellikleri daha fazla keşfetmekten çekinmeyin.


### SSS

#### 1. Kullanıcının Excel elektronik tablosunda belirli aralıkları düzenlemesine nasıl izin verilir?

 kullanabilirsiniz`ProtectedRangeCollection` izin verilen değişiklik aralıklarını tanımlamak için sınıf. Kullan`Add` İstenen hücrelerle yeni bir korumalı aralık oluşturma yöntemi.

#### 2. Yetkili değişiklik aralıkları için bir şifre belirleyebilir miyim?

 Evet, kullanarak bir şifre belirleyebilirsiniz.`Password` mülkiyeti`ProtectedRange` nesne. Bu, erişimi yalnızca şifreye sahip kullanıcılarla kısıtlayacaktır.

#### 3. İzin verilen aralıklar ayarlandıktan sonra elektronik tabloyu nasıl koruyabilirim?

 Kullan`Protect` yöntemi`Worksheet` çalışma sayfasını korumak için nesne. Bu, izin verilen aralıkların dışında herhangi bir değişikliği önleyecektir ve muhtemelen bir şifre belirlediyseniz şifre sorulacaktır.