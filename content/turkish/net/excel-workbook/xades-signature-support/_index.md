---
title: Xades İmza Desteği
linktitle: Xades İmza Desteği
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel dosyasına nasıl Xades imzası ekleyeceğinizi öğrenin.
type: docs
weight: 190
url: /tr/net/excel-workbook/xades-signature-support/
---
Bu yazıda, Aspose.Cells library for .NET kullanarak Xades imza desteği ile ilgili olan aşağıdaki C# kaynak kodunu adım adım anlatacağız. Bir Excel dosyasına Xades dijital imzası eklemek için bu kütüphaneyi nasıl kullanacağınızı öğreneceksiniz. Ayrıca size imzalama süreci ve yürütülmesi hakkında bir genel bakış sunacağız. Kesin sonuçlar almak için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıktı dizinlerini tanımlayın
Başlamak için, kodumuzda kaynak ve çıktı dizinlerini tanımlamamız gerekiyor. Bu dizinler, kaynak dosyaların nerede olduğunu ve çıktı dosyasının nereye kaydedileceğini gösterir. İşte ilgili kod:

```csharp
// Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

Dizin yollarını gerektiği gibi uyarladığınızdan emin olun.

## 2. Adım: Excel çalışma kitabını yükleme
Bir sonraki adım, Xades dijital imzasını eklemek istediğimiz Excel çalışma kitabını yüklemektir. İşte çalışma kitabını yüklemek için kod:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Kaynak dosya adını kodda doğru şekilde belirttiğinizden emin olun.

## 3. Adım: Dijital imzayı yapılandırma
Şimdi gerekli bilgileri sağlayarak Xades dijital imzasını yapılandıracağız. Dijital sertifikayı içeren PFX dosyasını ve ilişkili şifreyi belirtmeliyiz. İşte ilgili kod:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

"pfxPassword"ü gerçek parolanızla ve "pfxFile"ı PFX dosyasının yolu ile değiştirdiğinizden emin olun.

## 4. Adım: Dijital imzayı ekleme
Artık dijital imzayı yapılandırdığımıza göre, onu Excel çalışma kitabına ekleyebiliriz. İşte ilgili kod:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Bu adım, Xades dijital imzasını Excel çalışma kitabına ekler.

## Adım 5: Çalışma kitabını imzayla kaydetme
Son olarak Excel çalışma kitabını dijital imza eklenmiş olarak kaydediyoruz. İşte ilgili kod:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Çıktı dosyasının adını ihtiyaçlarınıza göre uyarladığınızdan emin olun.

### Aspose.Cells for .NET kullanan Xades Signature Support için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Çözüm
Tebrikler! Bir Excel dosyasına Xades dijital imzası eklemek için Aspose.Cells library for .NET'i nasıl kullanacağınızı öğrendiniz. Bu makalede verilen adımları izleyerek, bu işlevi kendi projelerinizde uygulayabileceksiniz. Kitaplıkla daha fazla deney yapmaktan ve sunduğu diğer güçlü özellikleri keşfetmekten çekinmeyin.

### SSS

#### S: Xades nedir?

Y: Xades, dijital belgelerin bütünlüğünü ve orijinalliğini sağlamak için kullanılan gelişmiş bir elektronik imza standardıdır.

#### S: Aspose.Cells ile diğer dijital imza türlerini kullanabilir miyim?

Y: Evet, Aspose.Cells, XMLDSig imzaları ve PKCS#7 imzaları gibi diğer dijital imza türlerini de destekler.

#### S: Excel dosyaları dışındaki dosya türlerine imza uygulayabilir miyim?
 
C: Evet, Aspose.Cells, Word, PDF ve PowerPoint dosyaları gibi desteklenen diğer dosya türlerine de dijital imzaların uygulanmasına izin verir.