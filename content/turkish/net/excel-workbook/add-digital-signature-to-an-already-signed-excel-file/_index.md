---
title: Zaten İmzalanmış Bir Excel Dosyasına Dijital İmza Ekleme
linktitle: Zaten İmzalanmış Bir Excel Dosyasına Dijital İmza Ekleme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile mevcut Excel dosyalarına kolayca dijital imzalar ekleyin.
type: docs
weight: 30
url: /tr/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Bu adım adım kılavuzda, Aspose.Cells for .NET kullanarak önceden imzalanmış bir Excel dosyasına dijital imza eklemenizi sağlayacak C# kaynak kodunu açıklayacağız. Mevcut bir Excel dosyasına yeni bir dijital imza eklemek için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıkış dizinlerini ayarlayın

```csharp
// kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda mevcut Excel dosyasını yüklemek ve dosyayı yeni dijital imzayla kaydetmek için kullanılacak kaynak ve çıktı dizinlerini tanımlıyoruz.

## 2. Adım: Mevcut Excel dosyasını yükleyin

```csharp
// Zaten imzalanmış Excel çalışma kitabını yükleyin
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Burada zaten imzalanmış Excel dosyasını kullanarak yüklüyoruz.`Workbook` Aspose.Cells sınıfı.

## 3. Adım: Dijital imza koleksiyonunu oluşturun

```csharp
// Dijital imza koleksiyonu oluşturun
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

 Kullanarak yeni bir dijital imza oluşturuyoruz.`DigitalSignature` sınıfa ekleyin ve dijital imza koleksiyonuna ekleyin.

## 6. Adım: Dijital imza koleksiyonunu çalışma kitabına ekleyin

```csharp
//Dijital imza koleksiyonunu çalışma kitabına ekleme
workbook.AddDigitalSignature(dsCollection);
```

 Dijital imza koleksiyonunu mevcut Excel çalışma kitabına şunu kullanarak ekliyoruz:`AddDigitalSignature()` yöntem.

## Adım 7: Çalışma kitabını kaydedin ve kapatın

```csharp
// Çalışma kitabını kaydedin ve kapatın
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Çalışma kitabını yeni dijital imzayla belirtilen çıktı dizinine kaydediyoruz, ardından kapatıyoruz ve ilgili kaynakları serbest bırakıyoruz.

### Aspose.Cells for .NET Kullanarak Zaten İmzalanmış Bir Excel Dosyasına Dijital İmza Eklemek için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Sertifika dosyası ve şifresi
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Yeni dijital imza eklemek için halihazırda dijital olarak imzalanmış olan çalışma kitabını yükleyin
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Dijital imza koleksiyonunu oluşturun
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Yeni sertifika oluştur
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Yeni dijital imza oluşturun ve bunu dijital imza koleksiyonuna ekleyin
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

Tebrikler! Artık Aspose.Cells for .NET kullanarak önceden imzalanmış bir Excel dosyasına nasıl dijital imza ekleyeceğinizi öğrendiniz. Dijital imzalar, Excel dosyalarınıza ekstra bir güvenlik katmanı ekleyerek onların orijinalliğini ve bütünlüğünü sağlar.

### SSS

#### S: Aspose.Cells for .NET nedir?

C: Aspose.Cells for .NET, .NET geliştiricilerinin Excel dosyalarını kolaylıkla oluşturmasına, değiştirmesine, dönüştürmesine ve işlemesine olanak tanıyan güçlü bir sınıf kitaplığıdır.

#### S: Excel dosyasındaki dijital imza nedir?

C: Excel dosyasındaki dijital imza, belgenin orijinalliğini, bütünlüğünü ve kaynağını garanti eden elektronik bir işarettir. Dosyanın imzalandıktan sonra değiştirilmediğini ve güvenilir bir kaynaktan geldiğini doğrulamak için kullanılır.

#### S: Excel dosyasına dijital imza eklemenin faydaları nelerdir?

C: Bir Excel dosyasına dijital imza eklemek, yetkisiz değişikliklere karşı koruma, veri bütünlüğünün sağlanması, belgenin yazarının kimliğinin doğrulanması ve içerdiği bilgilere güven sağlanması gibi çeşitli faydalar sağlar.

#### S: Bir Excel dosyasına birden fazla dijital imza ekleyebilir miyim?

C: Evet, Aspose.Cells bir Excel dosyasına birden fazla dijital imza eklemenizi sağlar. Dijital imzalardan oluşan bir koleksiyon oluşturabilir ve bunları tek bir işlemle dosyaya ekleyebilirsiniz.

#### S: Excel dosyasına dijital imza eklemenin gereksinimleri nelerdir?

C: Bir Excel dosyasına dijital imza eklemek için belgeyi imzalamada kullanılacak geçerli bir dijital sertifikaya ihtiyacınız vardır. Dijital imzayı eklemeden önce doğru sertifikaya ve şifreye sahip olduğunuzdan emin olun.