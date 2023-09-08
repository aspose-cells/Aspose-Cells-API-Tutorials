---
title: Excel Çalışma Kitabını Yazmaya Karşı Yazarken Belirleyin
linktitle: Excel Çalışma Kitabını Yazmaya Karşı Yazarken Belirleyin
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET'i kullanarak Excel çalışma kitaplarınızı nasıl koruyacağınızı ve özelleştireceğinizi öğrenin. C#'ta adım adım eğitim.
type: docs
weight: 30
url: /tr/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Bu eğitimde, .NET için Aspose.Cells kütüphanesini kullanarak bir Excel çalışma kitabını yazmaya karşı korurken yazarın nasıl belirleneceğini göstereceğiz.

## Adım 1: Ortamın hazırlanması

Başlamadan önce makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Kütüphaneyi Aspose resmi web sitesinden indirin ve verilen kurulum talimatlarını izleyin.

## Adım 2: Kaynak ve çıktı dizinlerini yapılandırma

Sağlanan kaynak kodunda kaynak ve çıktı dizinlerini belirtmeniz gerekir. Değiştirmek`sourceDir` Ve`outputDir` "KAYNAK DİZİNİNİZ" ve "ÇIKTI DİZINİNİZ" i makinenizdeki ilgili mutlak yollarla değiştirerek değişkenleri değiştirin.

```csharp
// Kaynak dizini
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Çıkış dizini
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## 3. Adım: Boş bir Excel çalışma kitabı oluşturma

Başlamak için boş bir Excel çalışma kitabını temsil eden bir Çalışma Kitabı nesnesi oluşturuyoruz.

```csharp
// Boş çalışma kitabı oluşturun.
Workbook wb = new Workbook();
```

## 4. Adım: Şifreyle yazma koruması

 Daha sonra, Excel çalışma kitabını yazma koruması için kullanarak bir parola belirliyoruz.`WriteProtection.Password` Çalışma Kitabı nesnesinin özelliği.

```csharp
// Korumalı çalışma kitabını parolayla yazın.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Adım 5: Yazarın belirtimi

 Şimdi Excel çalışma kitabının yazarını kullanarak belirtiyoruz.`WriteProtection.Author` Çalışma Kitabı nesnesinin özelliği.

```csharp
// Yazma korumalı çalışma kitabını yazarken belirtin.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Adım 6: Yedekleme Korumalı Excel Çalışma Kitabı

 Yazma koruması ve yazar belirtildikten sonra Excel çalışma kitabını aşağıdaki komutu kullanarak XLSX formatında kaydedebiliriz:`Save()` yöntem.

```csharp
// Çalışma kitabını XLSX formatında kaydedin.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Aspose.Cells for .NET kullanarak Excel Çalışma Kitabını Yazarken Yazarken Koruma Koruması için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = "YOUR SOURCE DIRECTORY";

//Çıkış dizini
string outputDir = "YOUR OUTPUT DIRECTORY";

// Boş çalışma kitabı oluşturun.
Workbook wb = new Workbook();

// Korumalı çalışma kitabını parolayla yazın.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Yazma korumalı çalışma kitabını yazarken belirtin.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Çalışma kitabını XLSX formatında kaydedin.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Çözüm

Tebrikler! Artık bir Excel çalışma kitabını Aspose.Cells for .NET ile yazmaya karşı korurken yazarın nasıl belirleneceğini öğrendiniz. Excel çalışma kitaplarınızı korumak ve özelleştirmek için bu adımları kendi projelerinize uygulayabilirsiniz.

Excel dosyalarında daha gelişmiş işlemler için Aspose.Cells for .NET'in özelliklerini daha fazla keşfetmekten çekinmeyin.

## SSS

#### S: Bir Excel çalışma kitabını parola belirtmeden yazma koruması yapabilir miyim?

 C: Evet, Çalışma Kitabı nesnesinin`WriteProtect()` Excel çalışma kitabını yazmaya karşı korumak için parola belirtmeden yöntem. Bu, çalışma kitabında parola gerektirmeden yapılan değişiklikleri kısıtlayacaktır.

#### S: Bir Excel çalışma kitabından yazma korumasını nasıl kaldırabilirim?

 C: Bir Excel çalışma kitabından yazma korumasını kaldırmak için`Unprotect()` Çalışma Sayfası nesnesinin yöntemi veya`RemoveWriteProtection()` Özel kullanım durumunuza bağlı olarak Çalışma Kitabı nesnesinin yöntemini kullanın. .

#### S: Excel çalışma kitabımı korumak için şifreyi unuttum. Ne yapabilirim ?

C: Excel çalışma kitabınızı korumak için gereken şifreyi unuttuysanız, onu doğrudan kaldıramazsınız. Ancak korumalı Excel dosyaları için parola kurtarma özellikleri sağlayan özel üçüncü taraf araçlarını kullanmayı deneyebilirsiniz.

#### S: Bir Excel çalışma kitabını yazmaya karşı korurken birden fazla yazar belirtmek mümkün müdür?

C: Hayır, Aspose.Cells for .NET kitaplığı, bir Excel çalışma kitabını yazmaya karşı korurken tek bir yazarın belirtilmesine olanak tanır. Birden fazla yazar belirtmek istiyorsanız doğrudan Excel dosyasını işleyerek özel çözümleri düşünmeniz gerekecektir.