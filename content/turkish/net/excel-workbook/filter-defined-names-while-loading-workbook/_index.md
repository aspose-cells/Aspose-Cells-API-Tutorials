---
title: Çalışma Kitabını Yüklerken Tanımlı Adları Filtrele
linktitle: Çalışma Kitabını Yüklerken Tanımlı Adları Filtrele
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile bir Excel çalışma kitabını yüklerken tanımlı adları nasıl filtreleyeceğinizi öğrenin.
type: docs
weight: 100
url: /tr/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Bir .NET uygulamasında Excel çalışma kitaplarıyla çalışırken, genellikle yük sırasında verileri filtrelemek gerekir. Aspose.Cells for .NET, Excel çalışma kitaplarını kolayca yönetmenizi sağlayan güçlü bir kütüphanedir. Bu kılavuzda, Aspose.Cells for .NET kullanarak bir çalışma kitabını yüklerken tanımlanan adları nasıl filtreleyeceğinizi göstereceğiz. İstediğiniz sonuçları elde etmek için şu basit adımları izleyin:

## 1. Adım: Yükleme seçeneklerini belirtin

Öncelikle çalışma kitabının yükleme davranışını tanımlamak için yükleme seçeneklerini belirtmeniz gerekir. Bizim durumumuzda yükte ayarlanan isimleri göz ardı etmek istiyoruz. Aspose.Cells'i kullanarak bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Yükleme seçeneklerini belirtir
LoadOptions opts = new LoadOptions();

// Tanımlanmış adları yükleme
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Adım 2: Çalışma kitabını yükleyin

Yükleme seçenekleri yapılandırıldıktan sonra Excel çalışma kitabını kaynak dosyadan yükleyebilirsiniz. Doğru dosya yolunu belirttiğinizden emin olun. İşte örnek bir kod:

```csharp
// Çalışma kitabını yükle
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## 3. Adım: Filtrelenen çalışma kitabını kaydedin

Çalışma kitabını yükledikten sonra gerektiği gibi diğer işlemleri veya düzenlemeleri gerçekleştirebilirsiniz. Daha sonra filtrelenen çalışma kitabını bir çıktı dosyasına kaydedebilirsiniz. İşte nasıl:

```csharp
// Filtrelenen Excel çalışma kitabını kaydedin
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Aspose.Cells for .NET Kullanarak Çalışma Kitabını Yüklerken Tanımlı Adları Filtrelemek için örnek kaynak kodu 
```csharp
//Yükleme seçeneklerini belirtin
LoadOptions opts = new LoadOptions();
//Tanımlanmış adları yüklemek istemiyoruz
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Çalışma kitabını yükle
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Çıktı Excel dosyasını kaydedin, C1'deki formülü bozar
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Çözüm

Excel çalışma kitabını yüklerken tanımlı adların filtrelenmesi birçok uygulama için kritik olabilir. Aspose.Cells for .NET, veri yükleme ve filtreleme için esnek seçenekler sunarak bu görevi kolaylaştırır. Bu kılavuzdaki adımları takip ederek, tanımlanan adları etkili bir şekilde filtreleyebilecek ve Excel çalışma kitaplarınızda istediğiniz sonuçları elde edebileceksiniz.


### SSS

#### S: Aspose.Cells, C#'ın yanı sıra diğer programlama dillerini de destekliyor mu?
    
C: Evet, Aspose.Cells Java, Python, C gibi birçok programlama dilini destekleyen platformlar arası bir kütüphanedir.++ve daha fazlası.

#### S: Aspose.Cells ile bir çalışma kitabını yüklerken diğer veri türlerini filtreleyebilir miyim?
    
C: Evet, Aspose.Cells veriler için formüller, stiller, makrolar vb. gibi çeşitli filtreleme seçenekleri sunar.

#### S: Aspose.Cells orijinal çalışma kitabının formatını ve özelliklerini koruyor mu?
    
C: Evet, Aspose.Cells, Excel dosyalarıyla çalışırken orijinal çalışma kitabının formatını, stillerini, formüllerini ve diğer özelliklerini korur.