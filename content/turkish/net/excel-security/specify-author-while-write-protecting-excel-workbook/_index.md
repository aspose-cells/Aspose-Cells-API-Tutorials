---
title: Excel Çalışma Kitabını Korumalı Yazarken Yazarı Belirtin
linktitle: Excel Çalışma Kitabını Korumalı Yazarken Yazarı Belirtin
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel çalışma kitaplarınızı nasıl koruyacağınızı ve özelleştireceğinizi öğrenin. C# ile adım adım öğretici.
type: docs
weight: 30
url: /tr/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Bu eğitimde, Aspose.Cells for .NET kitaplığını kullanarak bir Excel çalışma kitabını yazmaya karşı korurken yazarı nasıl belirteceğinizi göstereceğiz.

## 1. Adım: Ortamı hazırlamak

Başlamadan önce makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Aspose resmi web sitesinden kitaplığı indirin ve verilen kurulum talimatlarını izleyin.

## 2. Adım: Kaynak ve çıkış dizinlerini yapılandırma

Sağlanan kaynak kodunda, kaynak ve çıktı dizinlerini belirtmeniz gerekir. Değiştirmek`sourceDir` Ve`outputDir` "KAYNAK DİZİNİNİZ" ve "ÇIKTI DİZİNİNİZ"i makinenizdeki ilgili mutlak yollarla değiştirerek değişkenler.

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

## 4. Adım: Parola ile yazma koruması

 Ardından, kullanarak Excel çalışma kitabını korumak için bir parola belirliyoruz.`WriteProtection.Password` Çalışma Kitabı nesnesinin özelliği.

```csharp
// Koruma çalışma kitabını parola ile yazın.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Adım 5: Yazar belirtimi

 Şimdi Excel çalışma kitabının yazarını kullanarak belirtiyoruz.`WriteProtection.Author` Çalışma Kitabı nesnesinin özelliği.

```csharp
// Çalışma kitabını yazmaya karşı korurken yazarı belirtin.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## 6. Adım: Yedekleme Korumalı Excel Çalışma Kitabı

 Yazma koruması ve yazar belirlendikten sonra, Excel çalışma kitabını XLSX biçiminde kaydedebiliriz.`Save()` yöntem.

```csharp
// Çalışma kitabını XLSX biçiminde kaydedin.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Aspose.Cells for .NET kullanarak Excel Çalışma Kitabını Yazmaya Karşı Korurken Yazarı Belirtin için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = "YOUR SOURCE DIRECTORY";

//Çıkış dizini
string outputDir = "YOUR OUTPUT DIRECTORY";

// Boş çalışma kitabı oluşturun.
Workbook wb = new Workbook();

// Koruma çalışma kitabını parola ile yazın.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Çalışma kitabını yazmaya karşı korurken yazarı belirtin.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Çalışma kitabını XLSX biçiminde kaydedin.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Çözüm

Tebrikler! Artık bir Excel çalışma kitabını Aspose.Cells for .NET ile yazmaya karşı korurken yazarı nasıl belirteceğinizi öğrendiniz. Excel çalışma kitaplarınızı korumak ve özelleştirmek için bu adımları kendi projelerinize uygulayabilirsiniz.

Excel dosyaları üzerinde daha gelişmiş işlemler için Aspose.Cells for .NET'in özelliklerini keşfetmekten çekinmeyin.

## SSS

#### S: Korumalı bir Excel çalışma kitabını parola belirtmeden yazabilir miyim?

 C: Evet, Çalışma Kitabı nesnesinin`WriteProtect()` bir Excel çalışma kitabını yazmaya karşı korumak için bir parola belirlemeden yöntem. Bu, parola gerektirmeden çalışma kitabındaki değişiklikleri kısıtlayacaktır.

#### S: Bir Excel çalışma kitabından yazma korumasını nasıl kaldırırım?

 Y: Bir Excel çalışma kitabından yazma korumasını kaldırmak için,`Unprotect()` Çalışma Sayfası nesnesinin yöntemi veya`RemoveWriteProtection()` Özel kullanım durumunuza bağlı olarak Çalışma Kitabı nesnesinin yöntemi. .

#### S: Excel çalışma kitabımı korumak için parolamı unuttum. Ne yapabilirim ?

A: Excel çalışma kitabınızı korumak için parolayı unuttuysanız, doğrudan kaldıramazsınız. Ancak, korumalı Excel dosyaları için parola kurtarma özellikleri sağlayan üçüncü taraf özel araçları kullanmayı deneyebilirsiniz.

#### S: Bir Excel çalışma kitabını yazmaya karşı korurken birden çok yazar belirtmek mümkün müdür?

C: Hayır, Aspose.Cells for .NET kitaplığı, bir Excel çalışma kitabını yazmaya karşı korurken tek bir yazarın belirtilmesine izin verir. Birden fazla yazar belirtmek istiyorsanız, doğrudan Excel dosyasını değiştirerek özel çözümler düşünmeniz gerekecektir.