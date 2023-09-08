---
title: Üst Bilgi Alt Bilgiye Resim Ekle
linktitle: Üst Bilgi Alt Bilgiye Resim Ekle
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel belgesinin üstbilgisine veya altbilgisine nasıl resim ekleyeceğinizi öğrenin. C# kaynak koduyla adım adım kılavuz.
type: docs
weight: 60
url: /tr/net/excel-page-setup/insert-image-in-header-footer/
---
Bir Excel belgesinin üstbilgisine veya altbilgisine resim ekleme yeteneği, raporlarınızı özelleştirmek veya şirket logoları eklemek için çok yararlı olabilir. Bu makalede, Aspose.Cells for .NET kullanarak bir Excel belgesinin üstbilgisine veya altbilgisine resim eklemek için size adım adım rehberlik edeceğiz. C# kaynak kodunu kullanarak bunu nasıl başaracağınızı öğreneceksiniz.

## 1. Adım: Ortamı ayarlama

Başlamadan önce makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Aspose.Cells ile çalışmak için gereken kütüphaneleri kod dosyanıza aktarın. İşte ilgili kod:

```csharp
using Aspose.Cells;
```

## 3. Adım: Belge Dizinini Ayarlayın

Çalışmak istediğiniz Excel belgesinin bulunduğu dizini ayarlayın. Dizini ayarlamak için aşağıdaki kodu kullanın:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Tam dizin yolunu belirttiğinizden emin olun.

## Adım 4: Çalışma Kitabı Nesnesi Oluşturma

Çalışma Kitabı nesnesi, çalışacağınız Excel belgesini temsil eder. Aşağıdaki kodu kullanarak oluşturabilirsiniz:

```csharp
Workbook workbook = new Workbook();
```

Bu, yeni bir boş Çalışma Kitabı nesnesi oluşturur.

## 5. Adım: Resim URL'sini Saklama

Üstbilgiye veya altbilgiye eklemek istediğiniz görselin URL'sini veya yolunu tanımlayın. Resim URL'sini saklamak için aşağıdaki kodu kullanın:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Belirtilen yolun doğru olduğundan ve görüntünün bu konumda mevcut olduğundan emin olun.

## Adım 6: Görüntü dosyasını açma

Görüntü dosyasını açmak için bir FileStream nesnesi kullanacağız ve görüntüdeki ikili verileri okuyacağız. İşte ilgili kod:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Resim yolunun doğru olduğundan ve ona erişim için doğru izinlere sahip olduğunuzdan emin olun.

## Adım 7: PageSetup'ı Yapılandırma

PageSetup nesnesi, üstbilgi ve altbilgi dahil olmak üzere Excel belgesi sayfa ayarlarını ayarlamak için kullanılır. İlk çalışma sayfasının PageSetup nesnesini almak için aşağıdaki kodu kullanın:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Bu, çalışma kitabındaki ilk çalışma sayfasının sayfa ayarlarına erişmenizi sağlayacaktır.

## Adım 8: Resmi başlığa ekleme

Görüntüyü sayfa başlığının orta bölümüne ayarlamak için PageSetup nesnesinin SetHeaderPicture() yöntemini kullanın. İşte ilgili kod:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Bu, belirtilen resmi sayfa başlığına ekleyecektir.

## Adım 9: Başlığa bir komut dosyası ekleme

Sayfa başlığına komut dosyası eklemek için PageSetup nesnesinin SetHeader() yöntemini kullanın. İşte ilgili kod:

```csharp
pageSetup.SetHeader(1, "&G");
```

Bu, belirtilen betiği sayfa başlığına ekleyecektir. Bu örnekte "&G" komut dosyası sayfa numarasını görüntüler.

## Adım 10: Başlığa Sayfa Adı Ekleme

Sayfa adını sayfa üstbilgisinde görüntülemek için PageSetup nesnesinin SetHeader() yöntemini yeniden kullanın. İşte ilgili kod:

```csharp
pageSetup.SetHeader(2, "&A");
```

Bu, sayfa adını sayfa başlığına ekleyecektir. "&A" komut dosyası sayfa adını temsil etmek için kullanılır.

## Adım 11: Çalışma kitabını kaydetme

Çalışma kitabındaki değişiklikleri kaydetmek için Workbook nesnesinin Save() yöntemini kullanın. İşte ilgili kod:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Bu, çalışma kitabını değişikliklerle birlikte belirtilen dizine kaydedecektir.

## Adım 12: FileStream'i Kapatma

Görüntüdeki ikili verileri okuduktan sonra kaynakları boşaltmak için FileStream'i kapattığınızdan emin olun. FileStream'i kapatmak için aşağıdaki kodu kullanın:

```csharp
inFile.Close();
```

FileStreams'i kullanmayı bitirdiğinizde her zaman kapattığınızdan emin olun.

### Aspose.Cells for .NET kullanarak Üst Bilgi Alt Bilgisine Resim Ekleme için örnek kaynak kodu 
```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Çalışma Kitabı nesnesi oluşturma
Workbook workbook = new Workbook();
// Logonun/resmin URL'sini saklamak için bir dize değişkeni oluşturma
string logo_url = dataDir + "aspose-logo.jpg";
// FileStream nesnesini bildirme
FileStream inFile;
// Bayt dizisi bildirme
byte[] binaryData;
// Akıştaki logoyu/resmi açmak için FileStream nesnesinin örneğini oluşturma
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// FileStream nesnesinin boyutunun bayt dizisini örneklendirme
binaryData = new Byte[inFile.Length];
// Akıştan bir bayt bloğu okur ve belirli bir bayt dizisi arabelleğine veri yazar.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Çalışma kitabının ilk çalışma sayfasının sayfa ayarlarını almak için PageSetup nesnesi oluşturma
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Logonun/resmin sayfa başlığının orta kısmına yerleştirilmesi
pageSetup.SetHeaderPicture(1, binaryData);
// Logo/resim için komut dosyasını ayarlama
pageSetup.SetHeader(1, "&G");
// Komut dosyasıyla sayfa başlığının sağ bölümünde Sayfanın adını ayarlama
pageSetup.SetHeader(2, "&A");
// Çalışma kitabını kaydetme
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//FileStream nesnesini kapatma
inFile.Close();       
```
## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak bir Excel belgesinin üstbilgisine veya altbilgisine nasıl resim ekleyeceğinizi biliyorsunuz. Bu eğitim, ortamın ayarlanmasından değiştirilen çalışma kitabının kaydedilmesine kadar sürecin her adımında size yol gösterdi. Kişiselleştirilmiş ve profesyonel Excel belgeleri oluşturmak için Aspose.Cells'in özelliklerini daha fazla denemekten çekinmeyin.

### SSS'ler

#### S1: Bir Excel belgesinin üstbilgisine veya altbilgisine birden çok resim eklemek mümkün mü?

Cevap1: Evet, her ek görüntü için 8. ve 9. adımları tekrarlayarak bir Excel belgesinin üstbilgisine veya altbilgisine birden çok görüntü ekleyebilirsiniz.

#### S2: Üstbilgiye veya altbilgiye eklemek için hangi resim biçimleri desteklenir?
Cevap2: Aspose.Cells, JPEG, PNG, GIF, BMP vb. gibi çeşitli yaygın görüntü formatlarını destekler.

#### S3: Üstbilginin veya altbilginin görünümünü daha da özelleştirebilir miyim?

C3: Evet, üstbilgi veya altbilginin görünümünü daha fazla biçimlendirmek ve özelleştirmek için özel komut dosyaları ve kodlar kullanabilirsiniz. Özelleştirme seçenekleri hakkında daha fazla bilgi için Aspose.Cells belgelerine bakın.

#### S4: Aspose.Cells farklı Excel sürümleriyle çalışır mı?

Cevap4: Evet, Aspose.Cells, Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 ve Excel 2019 dahil olmak üzere farklı Excel sürümleriyle uyumludur.

#### S5: Excel belgesinin hücreler veya grafikler gibi diğer bölümlerine resim eklemek mümkün müdür?

Cevap5: Evet, Aspose.Cells, hücreler, grafikler ve çizim nesneleri de dahil olmak üzere Excel belgesinin farklı bölümlerine resim eklemek için kapsamlı işlevsellik sağlar.