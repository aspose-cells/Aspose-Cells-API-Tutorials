---
title: Halihazırda İmzalanmış Bir Excel Dosyasına Dijital İmza Ekleme
linktitle: Halihazırda İmzalanmış Bir Excel Dosyasına Dijital İmza Ekleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile mevcut Excel dosyalarına kolayca dijital imzalar ekleyin.
type: docs
weight: 30
url: /tr/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Bu adım adım kılavuzda, zaten imzalanmış bir Excel dosyasına Aspose.Cells for .NET kullanarak dijital imza eklemenizi sağlayacak, sağlanan C# kaynak kodunu açıklayacağız. Mevcut bir Excel dosyasına yeni bir dijital imza eklemek için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıkış dizinlerini ayarlayın

```csharp
// kaynak dizin
string sourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda, mevcut Excel dosyasını yüklemek ve dosyayı yeni dijital imza ile kaydetmek için kullanılacak kaynak ve çıktı dizinlerini tanımlıyoruz.

## 2. Adım: Mevcut Excel dosyasını yükleyin

```csharp
// Önceden imzalanmış Excel çalışma kitabını yükleyin
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Burada zaten imzalanmış Excel dosyasını kullanarak yüklüyoruz.`Workbook` Aspose.Cells sınıfı.

## 3. Adım: Dijital imza koleksiyonunu oluşturun

```csharp
// Dijital imza koleksiyonunu oluşturun
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 kullanarak yeni bir dijital imza koleksiyonu oluşturuyoruz.`DigitalSignatureCollection` sınıf.

## 4. Adım: Yeni bir sertifika oluşturun

```csharp
// Yeni bir sertifika oluştur
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Burada verilen dosya ve şifreden yeni bir sertifika oluşturuyoruz.

## 5. Adım: Koleksiyona yeni bir dijital imza ekleyin

```csharp
// Yeni bir dijital imza oluşturun
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Dijital imzayı koleksiyona ekleyin
dsCollection.Add(signature);
```

 Kullanarak yeni bir dijital imza oluşturuyoruz.`DigitalSignature` sınıflandırın ve dijital imza koleksiyonuna ekleyin.

## 6. Adım: Dijital imza koleksiyonunu çalışma kitabına ekleyin

```csharp
//Dijital imza koleksiyonunu çalışma kitabına ekleme
workbook.AddDigitalSignature(dsCollection);
```

 Kullanarak dijital imza koleksiyonunu mevcut Excel çalışma kitabına ekliyoruz.`AddDigitalSignature()` yöntem.

## 7. Adım: Çalışma kitabını kaydedin ve kapatın

```csharp
// Çalışma kitabını kaydedin ve kapatın
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Çalışma kitabını yeni dijital imzayla belirtilen çıktı dizinine kaydediyoruz, ardından kapatıyoruz ve ilgili kaynakları serbest bırakıyoruz.

### Aspose.Cells for .NET kullanarak Halihazırda İmzalanmış Bir Excel Dosyasına Dijital İmza Eklemek için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Sertifika dosyası ve şifresi
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Yeni dijital imza eklemek için zaten dijital olarak imzalanmış olan çalışma kitabını yükleyin
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Dijital imza koleksiyonunu oluşturun
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Yeni sertifika oluştur
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Yeni dijital imza oluşturun ve dijital imza koleksiyonuna ekleyin
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Çalışma kitabının içine dijital imza koleksiyonu ekleme
workbook.AddDigitalSignature(dsCollection);
//Çalışma kitabını kaydedin ve atın.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak zaten imzalanmış bir Excel dosyasına nasıl dijital imza ekleyeceğinizi öğrendiniz. Dijital imzalar, Excel dosyalarınıza ekstra bir güvenlik katmanı ekleyerek orijinalliklerini ve bütünlüklerini sağlar.

### SSS

#### S: Aspose.Cells for .NET nedir?

Y: Aspose.Cells for .NET, .NET geliştiricilerinin Excel dosyalarını kolaylıkla oluşturmasına, değiştirmesine, dönüştürmesine ve işlemesine olanak sağlayan güçlü bir sınıf kitaplığıdır.

#### S: Bir Excel dosyasındaki dijital imza nedir?

Y: Bir Excel dosyasındaki dijital imza, belgenin gerçekliğini, bütünlüğünü ve kaynağını garanti eden elektronik bir işarettir. Dosyanın imzalandığından beri değiştirilmediğini ve güvenilir bir kaynaktan geldiğini doğrulamak için kullanılır.

#### S: Bir Excel dosyasına dijital imza eklemenin faydaları nelerdir?

C: Bir Excel dosyasına dijital imza eklemek, yetkisiz değişikliklere karşı koruma, veri bütünlüğünü sağlama, belgenin yazarının kimliğini doğrulama ve içerdiği bilgilere güven duyma gibi çeşitli avantajlar sağlar.

#### S: Bir Excel dosyasına birden çok dijital imza ekleyebilir miyim?

C: Evet, Aspose.Cells, bir Excel dosyasına birden çok dijital imza eklemenizi sağlar. Bir dijital imza koleksiyonu oluşturabilir ve bunları tek bir işlemle dosyaya ekleyebilirsiniz.

#### S: Bir Excel dosyasına dijital imza eklemek için gereksinimler nelerdir?

Y: Bir Excel dosyasına dijital imza eklemek için belgeyi imzalamak üzere kullanılacak geçerli bir dijital sertifikaya ihtiyacınız vardır. Dijital imzayı eklemeden önce doğru sertifika ve parolaya sahip olduğunuzdan emin olun.