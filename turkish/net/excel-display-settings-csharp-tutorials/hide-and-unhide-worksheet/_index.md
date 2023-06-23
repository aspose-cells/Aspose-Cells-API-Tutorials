---
title: Çalışma Sayfasını Gizle ve Göster
linktitle: Çalışma Sayfasını Gizle ve Göster
second_title: Aspose.Cells for .NET API Referansı
description: Veri oluşturma, değiştirme ve işleme dahil olmak üzere Excel dosyalarıyla çalışmak için güçlü bir kitaplık.
type: docs
weight: 90
url: /tr/net/excel-display-settings-csharp-tutorials/hide-and-unhide-worksheet/
---
Bu öğreticide, Aspose.Cells for .NET kullanarak bir çalışma sayfasını gizlemek ve göstermek için kullanılan aşağıdaki C# kaynak kodunu adım adım açıklayacağız. Aşağıdaki adımları takip et:

## 1. Adım: Ortamı hazırlamak

Başlamadan önce Aspose.Cells for .NET'in sisteminizde kurulu olduğundan emin olun. Henüz yüklemediyseniz, Aspose'un resmi web sitesinden indirebilirsiniz. Kurulduktan sonra, tercih ettiğiniz tümleşik geliştirme ortamında (IDE) yeni bir proje oluşturabilirsiniz.

## 2. Adım: Gerekli ad alanlarını içe aktarın

Aspose.Cells'in özelliklerini kullanmak için C# kaynak dosyanıza gerekli ad alanlarını ekleyin. Dosyanızın başına aşağıdaki satırları ekleyin:

```csharp
using Aspose.Cells;
using System.IO;
```

## 3. Adım: Excel dosyasını yükleyin

Bir çalışma sayfasını gizlemeden veya göstermeden önce Excel dosyasını uygulamanıza yüklemeniz gerekir. Kullanmak istediğiniz Excel dosyasının projenizle aynı dizinde olduğundan emin olun. Excel dosyasını yüklemek için aşağıdaki kodu kullanın:

```csharp
string dataDir = "PATH TO YOUR DOCUMENTS DIRECTORY";
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
Workbook workbook = new Workbook(fstream);
```

"BELGELER DİZİNİNİZİN YOLU"nu Excel dosyanızı içeren dizinin gerçek yolu ile değiştirdiğinizden emin olun.

## 4. Adım: Elektronik tabloya erişin

Excel dosyası yüklendikten sonra, gizlemek veya göstermek istediğiniz çalışma sayfasına gidebilirsiniz. Dosyadaki ilk çalışma sayfasına erişmek için aşağıdaki kodu kullanın:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## 5. Adım: Çalışma sayfasını gizleyin

 Artık çalışma sayfasına eriştiğinize göre, onu kullanarak gizleyebilirsiniz.`IsVisible` mülk. Dosyadaki ilk çalışma sayfasını gizlemek için aşağıdaki kodu kullanın:

```csharp
worksheet. IsVisible = false;
```

## 6. Adım: Çalışma sayfasını yeniden görüntüleyin

Daha önce gizlenen çalışma sayfasını yeniden görüntülemek isterseniz, aynı kodu, değerini değiştirerek kullanabilirsiniz.`IsVisible` mülk. İlk çalışma sayfasını yeniden görüntülemek için aşağıdaki kodu kullanın:

```csharp
worksheet. IsVisible = true;
```

## 7. Adım: Değişiklikleri Kaydet

bir kez sen

  çalışma sayfasını gerektiği gibi gizlediyseniz veya gösterdiyseniz, değişiklikleri Excel dosyasına kaydetmeniz gerekir. Değişiklikleri kaydetmek için aşağıdaki kodu kullanın:

```csharp
workbook.Save(dataDir + "output.out.xls");
fstream.Close();
```

Değiştirilen Excel dosyasını kaydetmek için doğru çıktı yolunu belirttiğinizden emin olun.

### Aspose.Cells for .NET kullanan Hide And Unhide Worksheet için örnek kaynak kodu 

```csharp
// Belgeler dizininin yolu.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Açılacak Excel dosyasını içeren bir dosya akışı oluşturma
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Excel dosyasını dosya akışı aracılığıyla açarak bir Çalışma Kitabı nesnesini somutlaştırma
Workbook workbook = new Workbook(fstream);
// Excel dosyasındaki ilk çalışma sayfasına erişme
Worksheet worksheet = workbook.Worksheets[0];
// Excel dosyasının ilk çalışma sayfasını gizleme
worksheet.IsVisible = false;
// Excel dosyasının ilk çalışma sayfasını gösterir
//Worksheet.IsVisible = true;
// Değiştirilen Excel dosyasını varsayılan (yani Excel 2003) biçiminde kaydetme
workbook.Save(dataDir + "output.out.xls");
// Tüm kaynakları serbest bırakmak için dosya akışını kapatma
fstream.Close();
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak bir elektronik tabloyu nasıl gizleyeceğinizi ve göstereceğinizi öğrendiniz. Artık elektronik tablolarınızın Excel dosyalarınızdaki görünürlüğünü kontrol etmek için bu özelliği kullanabilirsiniz.

### Sık Sorulan Sorular (SSS)

#### Aspose.Cells for .NET'i nasıl kurabilirim?

 Aspose.Cells for .NET'i ilgili NuGet paketini adresinden indirerek kurabilirsiniz.[Bültenler](https://releases/aspose.com/cells/net/) ve onu Visual Studio projenize eklemek.

#### Aspose.Cells for .NET'i kullanmak için gereken minimum .NET Framework sürümü nedir?

Aspose.Cells for .NET, .NET Framework 2.0 ve sonrasını destekler.

#### Aspose.Cells for .NET ile mevcut Excel dosyalarını açıp düzenleyebilir miyim?

Evet, Aspose.Cells for .NET'i kullanarak mevcut Excel dosyalarını açabilir ve düzenleyebilirsiniz. Excel dosyasının çalışma sayfalarına, hücrelerine, formüllerine ve diğer öğelerine erişebilirsiniz.

#### Aspose.Cells for .NET raporlamayı ve diğer dosya biçimlerine aktarımı destekliyor mu?

Evet, Aspose.Cells for .NET, rapor oluşturmayı ve PDF, HTML, CSV, TXT, vb. formatlara aktarmayı destekler.

#### Excel dosyasındaki değişiklik kalıcı mı?

Evet, kaydettiğinizde Excel dosyası düzenlemesi kalıcıdır. Orijinal dosyada herhangi bir değişiklik yapmadan önce bir yedek kopya kaydettiğinizden emin olun.