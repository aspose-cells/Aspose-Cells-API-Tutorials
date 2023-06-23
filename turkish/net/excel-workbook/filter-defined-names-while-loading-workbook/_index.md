---
title: Çalışma Kitabını Yüklerken Tanımlı Adları Filtrele
linktitle: Çalışma Kitabını Yüklerken Tanımlı Adları Filtrele
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile bir Excel çalışma kitabı yüklerken tanımlanmış adları nasıl filtreleyeceğinizi öğrenin.
type: docs
weight: 100
url: /tr/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Bir .NET uygulamasında Excel çalışma kitaplarıyla çalışırken, genellikle verileri yük altında filtrelemek gerekir. Aspose.Cells for .NET, Excel çalışma kitaplarını kolayca işlemek için güçlü bir kitaplıktır. Bu kılavuzda, Aspose.Cells for .NET kullanarak bir çalışma kitabı yüklerken tanımlanan adları nasıl filtreleyeceğinizi göstereceğiz. İstenen sonuçları elde etmek için şu basit adımları izleyin:

## 1. Adım: Yükleme seçeneklerini belirtin

Öncelikle, çalışma kitabının yükleme davranışını tanımlamak için yükleme seçeneklerini belirtmeniz gerekir. Bizim durumumuzda, yükte ayarlanan adları yok saymak istiyoruz. Aspose.Cells kullanarak bunu şu şekilde yapabilirsiniz:

```csharp
// yükleme seçeneklerini belirtir
LoadOptions opts = new LoadOptions();

// Tanımlanmış adları yükleme
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## 2. Adım: Çalışma kitabını yükleyin

Yükleme seçenekleri yapılandırıldıktan sonra, Excel çalışma kitabını kaynak dosyadan yükleyebilirsiniz. Doğru dosya yolunu belirttiğinizden emin olun. İşte örnek bir kod:

```csharp
// çalışma kitabını yükle
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## 3. Adım: Filtre uygulanmış çalışma kitabını kaydedin

Çalışma kitabını yükledikten sonra, gereken diğer işlemleri veya düzenlemeleri yapabilirsiniz. Ardından, filtre uygulanmış çalışma kitabını bir çıktı dosyasına kaydedebilirsiniz. İşte nasıl:

```csharp
// Filtre uygulanmış Excel çalışma kitabını kaydedin
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Aspose.Cells for .NET kullanarak Çalışma Kitabını Yüklerken Filtre Tanımlı Adlar için örnek kaynak kodu 
```csharp
//Yükleme seçeneklerini belirtin
LoadOptions opts = new LoadOptions();
//Tanımlanmış isimleri yüklemek istemiyoruz
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//çalışma kitabını yükle
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Çıktı Excel dosyasını kaydedin, formülü C1'de bozacaktır
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Çözüm

Bir Excel çalışma kitabını yüklerken tanımlı adları filtrelemek birçok uygulama için kritik olabilir. Aspose.Cells for .NET, verileri yüklemek ve filtrelemek için esnek seçenekler sunarak bu görevi kolaylaştırır. Bu kılavuzdaki adımları izleyerek, tanımlı adları etkili bir şekilde filtreleyebilecek ve Excel çalışma kitaplarınızda istediğiniz sonuçları elde edebileceksiniz.


### SSS

#### S: Aspose.Cells, C# dışında diğer programlama dillerini destekliyor mu?
    
C: Evet, Aspose.Cells Java, Python, C gibi birçok programlama dilini destekleyen platformlar arası bir kitaplıktır.++, ve daha fazlası.

#### S: Aspose.Cells ile bir çalışma kitabı yüklerken diğer veri türlerini filtreleyebilir miyim?
    
C: Evet, Aspose.Cells formüller, stiller, makrolar vb. dahil olmak üzere veriler için bir dizi filtreleme seçeneği sunar.

#### S: Aspose.Cells orijinal çalışma kitabının biçimlendirme ve özelliklerini koruyor mu?
    
C: Evet, Aspose.Cells, Excel dosyalarıyla çalışırken orijinal çalışma kitabının biçimlendirme, stiller, formüller ve diğer özelliklerini korur.