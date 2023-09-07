---
title: Üstbilgi Altbilgiye Resim Ekle
linktitle: Üstbilgi Altbilgiye Resim Ekle
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel belgesinin üstbilgisine veya altbilgisine nasıl resim ekleyeceğinizi öğrenin. C# dilinde kaynak koduyla adım adım kılavuz.
type: docs
weight: 60
url: /tr/net/excel-page-setup/insert-image-in-header-footer/
---
Bir Excel belgesinin üstbilgisine veya altbilgisine resim ekleme özelliği, raporlarınızı özelleştirmek veya şirket logoları eklemek için çok yararlı olabilir. Bu yazıda, Aspose.Cells for .NET kullanarak bir Excel belgesinin üst bilgisine veya alt bilgisine resim eklemek için adım adım yol göstereceğiz. C# kaynak kodunu kullanarak bunu nasıl başaracağınızı öğreneceksiniz.

## 1. Adım: Ortamı ayarlama

Başlamadan önce makinenizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Ayrıca tercih ettiğiniz geliştirme ortamında yeni bir proje oluşturun.

## 2. Adım: Gerekli kitaplıkları içe aktarın

Kod dosyanızda, Aspose.Cells ile çalışmak için gereken kütüphaneleri içe aktarın. İşte ilgili kod:

```csharp
using Aspose.Cells;
```

## 3. Adım: Belge Dizinini Ayarlayın

Çalışmak istediğiniz Excel belgesinin bulunduğu dizini ayarlayın. Dizini ayarlamak için aşağıdaki kodu kullanın:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Tam dizin yolunu belirttiğinizden emin olun.

## 4. Adım: Çalışma Kitabı Nesnesi Oluşturma

Çalışma Kitabı nesnesi, birlikte çalışacağınız Excel belgesini temsil eder. Aşağıdaki kodu kullanarak oluşturabilirsiniz:

```csharp
Workbook workbook = new Workbook();
```

Bu, yeni bir boş Çalışma Kitabı nesnesi oluşturur.

## 5. Adım: Resim URL'sini Kaydetme

Üstbilgiye veya altbilgiye eklemek istediğiniz görüntünün URL'sini veya yolunu tanımlayın. Resim URL'sini saklamak için aşağıdaki kodu kullanın:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Belirtilen yolun doğru olduğundan ve görüntünün bu konumda bulunduğundan emin olun.

## Adım 6: Görüntü dosyasını açma

Görüntü dosyasını açmak için bir FileStream nesnesi kullanacağız ve ikili verileri görüntüden okuyacağız. İşte ilgili kod:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Görüntü yolunun doğru olduğundan ve ona erişmek için doğru izinlere sahip olduğunuzdan emin olun.

## 7. Adım: PageSetup'ı Yapılandırma

PageSetup nesnesi, üst bilgi ve alt bilgi dahil olmak üzere Excel belge sayfası ayarlarını yapmak için kullanılır. İlk çalışma sayfasının PageSetup nesnesini almak için aşağıdaki kodu kullanın:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Bu, çalışma kitabındaki ilk çalışma sayfası için sayfa ayarlarına erişmenizi sağlar.

## 8. Adım: Görüntüyü başlığa ekleme

Görüntüyü sayfa başlığının orta bölümünde ayarlamak için PageSetup nesnesinin SetHeaderPicture() yöntemini kullanın. İşte ilgili kod:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Bu, belirtilen resmi sayfa başlığına ekleyecektir.

## 9. Adım: Başlığa bir komut dosyası ekleme

Sayfa başlığına komut dosyası eklemek için PageSetup nesnesinin SetHeader() yöntemini kullanın. İşte ilgili kod:

```csharp
pageSetup.SetHeader(1, "&G");
```

Bu, belirtilen komut dosyasını sayfa başlığına ekleyecektir. Bu örnekte, "&G" komut dosyası sayfa numarasını gösterir.

## Adım 10: Başlığa Sayfa Adı Ekleyin

Sayfa adını sayfa başlığında görüntülemek için, PageSetup nesnesinin SetHeader() yöntemini tekrar kullanın. İşte ilgili kod:

```csharp
pageSetup.SetHeader(2, "&A");
```

Bu, sayfa adını sayfa başlığına ekleyecektir. "&A" betiği, sayfa adını temsil etmek için kullanılır.

## Adım 11: Çalışma kitabını kaydetme

Çalışma kitabındaki değişiklikleri kaydetmek için Workbook nesnesinin Save() yöntemini kullanın. İşte ilgili kod:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Bu, çalışma kitabını değişikliklerle birlikte belirtilen dizine kaydeder.

## Adım 12: FileStream'i Kapatma

Görüntüden ikili verileri okuduktan sonra, kaynakları serbest bırakmak için FileStream'i kapattığınızdan emin olun. FileStream'i kapatmak için aşağıdaki kodu kullanın:

```csharp
inFile.Close();
```

Kullanmayı bitirdiğinizde FileStreams'i her zaman kapattığınızdan emin olun.

### Aspose.Cells for .NET kullanarak Üstbilgi Altbilgisine Resim Ekleme için örnek kaynak kodu 
```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Çalışma Kitabı nesnesi oluşturma
Workbook workbook = new Workbook();
// Logonun/resmin URL'sini depolamak için bir dize değişkeni oluşturma
string logo_url = dataDir + "aspose-logo.jpg";
// FileStream nesnesi bildirme
FileStream inFile;
// Bir bayt dizisi bildirme
byte[] binaryData;
// Akışta logoyu/resmi açmak için FileStream nesnesinin örneğini oluşturma
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// FileStream nesnesinin boyutunun bayt dizisini başlatma
binaryData = new Byte[inFile.Length];
// Akıştan bir bayt bloğu okur ve verileri belirli bir bayt dizisi arabelleğine yazar.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Çalışma kitabının ilk çalışma sayfasının sayfa ayarlarını almak için bir PageSetup nesnesi oluşturma
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Sayfa başlığının orta bölümünde logo/resmin ayarlanması
pageSetup.SetHeaderPicture(1, binaryData);
// Logo/resim için komut dosyası ayarlama
pageSetup.SetHeader(1, "&G");
// Sayfa adının sayfa başlığının sağ bölümünde komut dosyasıyla ayarlanması
pageSetup.SetHeader(2, "&A");
// Çalışma kitabını kaydetme
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//FileStream nesnesini kapatma
inFile.Close();       
```
## Çözüm

Tebrikler! Artık Aspose.Cells for .NET kullanarak bir Excel belgesinin üstbilgisine veya altbilgisine nasıl resim ekleyeceğinizi biliyorsunuz. Bu öğretici, ortamın ayarlanmasından değiştirilen çalışma kitabının kaydedilmesine kadar sürecin her adımında size yol gösterdi. Kişiselleştirilmiş ve profesyonel Excel belgeleri oluşturmak için Aspose.Cells'in özelliklerini daha fazla denemekten çekinmeyin.

### SSS

#### S1: Bir Excel belgesinin üstbilgisine veya altbilgisine birden çok resim eklemek mümkün müdür?

Y1: Evet, her ek görüntü için 8. ve 9. adımları tekrarlayarak bir Excel belgesinin üstbilgisine veya altbilgisine birden çok görüntü ekleyebilirsiniz.

#### S2: Üstbilgiye veya altbilgiye eklemek için hangi resim biçimleri desteklenir?
A2: Aspose.Cells, JPEG, PNG, GIF, BMP vb. gibi çeşitli yaygın görüntü formatlarını destekler.

#### S3: Üstbilgi veya altbilginin görünümünü daha da özelleştirebilir miyim?

Y3: Evet, üst bilgi veya alt bilginin görünümünü daha fazla biçimlendirmek ve özelleştirmek için özel komut dosyaları ve kodlar kullanabilirsiniz. Özelleştirme seçenekleri hakkında daha fazla bilgi için Aspose.Cells belgelerine bakın.

#### S4: Aspose.Cells, Excel'in farklı sürümleriyle çalışır mı?

C4: Evet, Aspose.Cells, Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016 ve Excel 2019 dahil olmak üzere farklı Excel sürümleriyle uyumludur.

#### S5: Excel belgesinin hücreler veya grafikler gibi diğer bölümlerine resim eklemek mümkün müdür?

C5: Evet, Aspose.Cells, Excel belgesinin hücreler, grafikler ve çizim nesneleri dahil olmak üzere farklı bölümlerine resim eklemek için kapsamlı işlevsellik sağlar.