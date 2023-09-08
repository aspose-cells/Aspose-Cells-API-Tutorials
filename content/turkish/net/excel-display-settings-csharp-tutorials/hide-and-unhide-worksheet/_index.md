---
title: Çalışma Sayfasını Gizle ve Göster
linktitle: Çalışma Sayfasını Gizle ve Göster
second_title: Aspose.Cells for .NET API Referansı
description: Veri oluşturma, değiştirme ve işleme dahil olmak üzere Excel dosyalarıyla çalışmaya yönelik güçlü bir kitaplık.
type: docs
weight: 90
url: /tr/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
Bu eğitimde, Aspose.Cells for .NET kullanarak bir çalışma sayfasını gizlemek ve göstermek için kullanılan aşağıdaki C# kaynak kodunu adım adım açıklayacağız. Aşağıdaki adımları takip et:

## Adım 1: Ortamın hazırlanması

Başlamadan önce sisteminizde Aspose.Cells for .NET'in kurulu olduğundan emin olun. Henüz yüklemediyseniz Aspose'un resmi web sitesinden indirebilirsiniz. Kurulduktan sonra tercih ettiğiniz entegre geliştirme ortamında (IDE) yeni bir proje oluşturabilirsiniz.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells'in özelliklerini kullanmak için C# kaynak dosyanıza gerekli ad alanlarını ekleyin. Dosyanızın başına aşağıdaki satırları ekleyin:

```csharp
using Aspose.Cells;
using System.IO;
```

## 3. Adım: Excel dosyasını yükleyin

Bir çalışma sayfasını gizlemeden veya göstermeden önce Excel dosyasını uygulamanıza yüklemelisiniz. Kullanmak istediğiniz Excel dosyasının projenizle aynı dizinde olduğundan emin olun. Excel dosyasını yüklemek için aşağıdaki kodu kullanın:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

"BELGELER DİZİNİN YOLU" ifadesini Excel dosyanızı içeren dizinin gerçek yolu ile değiştirdiğinizden emin olun.

## 4. Adım: E-tabloya erişin

Excel dosyası yüklendikten sonra gizlemek veya göstermek istediğiniz çalışma sayfasına gidebilirsiniz. Dosyadaki ilk çalışma sayfasına erişmek için aşağıdaki kodu kullanın:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 5. Adım: Çalışma sayfasını gizleyin

 Artık çalışma sayfasına eriştiğinize göre, onu kullanarak gizleyebilirsiniz.`IsVisible` mülk. Dosyadaki ilk çalışma sayfasını gizlemek için aşağıdaki kodu kullanın:

```csharp
worksheet. IsVisible = false;
```

## 6. Adım: Çalışma sayfasını yeniden görüntüleyin

Daha önce gizlenmiş olan çalışma sayfasını yeniden görüntülemek istiyorsanız, aynı kodu, değerini değiştirerek kullanabilirsiniz.`IsVisible` mülk. İlk çalışma sayfasını yeniden görüntülemek için aşağıdaki kodu kullanın:

```csharp
worksheet. IsVisible = true;
```

## Adım 7: Değişiklikleri Kaydet

Bir kez sen

  Çalışma sayfasını gerektiği gibi gizlediyseniz veya gösterdiyseniz, değişiklikleri Excel dosyasına kaydetmelisiniz. Değişiklikleri kaydetmek için aşağıdaki kodu kullanın:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Değiştirilen Excel dosyasını kaydetmek için doğru çıktı yolunu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanarak Çalışma Sayfasını Gizle ve Göster için örnek kaynak kodu 

```csharp
//Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Excel dosyasını dosya akışı aracılığıyla açarak bir Çalışma Kitabı nesnesinin örneğini oluşturma
Workbook workbook = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Excel dosyasının ilk çalışma sayfasını gizleme
worksheet.IsVisible = false;
// Excel dosyasının ilk çalışma sayfasını gösterir
//Worksheet.IsVisible = true;
// Değiştirilen Excel dosyasını varsayılan (yani Excel 2003) biçimde kaydetme
workbook.Save(dataDir + "output.out.xls");
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Tebrikler! Aspose.Cells for .NET'i kullanarak bir elektronik tabloyu nasıl gizleyeceğinizi ve göstereceğinizi öğrendiniz. Artık bu özelliği Excel dosyalarınızdaki e-tablolarınızın görünürlüğünü kontrol etmek için kullanabilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET'i nasıl kurabilirim?

 Aspose.Cells for .NET'i aşağıdaki adresten ilgili NuGet paketini indirerek kurabilirsiniz.[Sürümleri Aspose](https://releases/aspose.com/cells/net/) ve onu Visual Studio projenize ekleyin.

#### Aspose.Cells for .NET'i kullanmak için gereken minimum .NET Framework sürümü nedir?

Aspose.Cells for .NET, .NET Framework 2.0 ve sonraki sürümlerini destekler.

#### Mevcut Excel dosyalarını Aspose.Cells for .NET ile açıp düzenleyebilir miyim?

Evet, Aspose.Cells for .NET'i kullanarak mevcut Excel dosyalarını açabilir ve düzenleyebilirsiniz. Excel dosyasının çalışma sayfalarına, hücrelerine, formüllerine ve diğer öğelerine erişebilirsiniz.

#### Aspose.Cells for .NET raporlamayı ve diğer dosya formatlarına aktarmayı destekliyor mu?

Evet, Aspose.Cells for .NET, rapor oluşturmayı ve PDF, HTML, CSV, TXT vb. formatlara aktarmayı destekler.

#### Excel dosyasındaki değişiklik kalıcı mıdır?

Evet, Excel dosyasını kaydettiğinizde düzenleme kalıcı olur. Orijinal dosyada herhangi bir değişiklik yapmadan önce yedek kopyayı kaydettiğinizden emin olun.