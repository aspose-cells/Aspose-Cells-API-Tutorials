---
title: Sıkıştırma Seviyesini Ayarlayın
linktitle: Sıkıştırma Seviyesini Ayarlayın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile sıkıştırma seviyesini ayarlayarak Excel çalışma kitaplarınızın boyutunu küçültün.
type: docs
weight: 50
url: /tr/net/excel-workbook/adjust-compression-level/
---
Bu adım adım eğitimde, Aspose.Cells for .NET'i kullanarak sıkıştırma seviyesini ayarlamanıza izin verecek, sağlanan C# kaynak kodunu açıklayacağız. Excel çalışma kitabınızdaki sıkıştırma düzeyini ayarlamak için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıkış dizinlerini ayarlayın

```csharp
// kaynak dizin
string sourceDir = RunExamples.Get_SourceDirectory();
// Çıkış dizini
string outDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda, Excel dosyaları için kaynak ve çıktı dizinlerini tanımlıyoruz.

## 2. Adım: Excel Çalışma Kitabını Yükleyin

```csharp
//Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

 Excel çalışma kitabını belirtilen dosyadan yükleriz.`Workbook` Aspose.Cells'ten sınıf.

## 3. Adım: Yedekleme seçeneklerini ayarlayın

```csharp
// Yedekleme seçeneklerini tanımlayın
XlsbSaveOptions options = new XlsbSaveOptions();
```

 örneğini oluşturuyoruz`XlsbSaveOptions` kaydetme seçeneklerini ayarlamak için sınıf.

## 4. Adım: Sıkıştırma düzeyini ayarlayın (Seviye 1)

```csharp
// Sıkıştırma düzeyini ayarlayın (Seviye 1)
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
let elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 1): " + elapsedMs);
```

 Sıkıştırma seviyesini ayarlayarak ayarlıyoruz`CompressionType` ile`Level1`. Daha sonra bu sıkıştırma seçeneği belirtilen Excel çalışma kitabını kaydediyoruz.

## Adım 5: Sıkıştırma düzeyini ayarlayın (Seviye 6)

```csharp
// Sıkıştırma düzeyini ayarlayın (Seviye 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Sıkıştırma seviyesini ayarlamak için işlemi tekrarlıyoruz.`Level6` ve Excel çalışma kitabını bu seçenekle kaydedin.

## Adım 6: Sıkıştırma düzeyini ayarlayın (Seviye 9)

```csharp
// Sıkıştırma düzeyini ayarlayın (Seviye 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Sıkıştırma seviyesini ayarlamak için işlemi son bir kez tekrarlıyoruz.`Level9` ve Excel çalışma kitabını bu seçenekle kaydedin.

### Aspose.Cells for .NET kullanarak Sıkıştırma Düzeyini Ayarlamak için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
string outDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
XlsbSaveOptions options = new XlsbSaveOptions();
options.CompressionType = OoxmlCompressionType.Level1;
var watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_1_out.xlsb", options);
watch.Stop();
var elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 1 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level6;
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 6 Elapsed Time: " + elapsedMs);
watch = System.Diagnostics.Stopwatch.StartNew();
options.CompressionType = OoxmlCompressionType.Level9;
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch.ElapsedMilliseconds;
Console.WriteLine("Level 9 Elapsed Time: " + elapsedMs);
Console.WriteLine("AdjustCompressionLevel executed successfully.");
```

## Çözüm

Tebrikler! Aspose.Cells for .NET kullanarak bir Excel çalışma kitabında sıkıştırma düzeyini nasıl ayarlayacağınızı öğrendiniz. İhtiyaçlarınıza en uygun olanı bulmak için farklı sıkıştırma düzeyleriyle denemeler yapın.

### SSS

#### S: Excel çalışma kitabında sıkıştırma nedir?

Y: Bir Excel çalışma kitabında sıkıştırma, sıkıştırma algoritmalarını kullanarak dosya boyutunu küçültme işlemidir. Bu, gereken depolama alanını azaltır ve dosyayı yüklerken ve değiştirirken performansı artırır.

#### S: Aspose.Cells ile hangi sıkıştırma seviyeleri mevcut?

C: Aspose.Cells ile sıkıştırma seviyesini 1'den 9'a ayarlayabilirsiniz.

#### S: Excel çalışma kitabım için doğru sıkıştırma düzeyini nasıl seçerim?

C: Sıkıştırma düzeyi seçimi, özel ihtiyaçlarınıza bağlıdır. Maksimum sıkıştırma istiyorsanız ve işlem süresi sorun değilse, 9. seviyeye gidebilirsiniz. Dosya boyutu ile işlem süresi arasında bir uzlaşmayı tercih ediyorsanız, bir orta seviye seçebilirsiniz.

#### S: Sıkıştırma, Excel çalışma kitabındaki veri kalitesini etkiler mi?

Y: Hayır, sıkıştırma Excel çalışma kitabındaki veri kalitesini etkilemez. Verilerin kendisini değiştirmeden sıkıştırma tekniklerini kullanarak dosya boyutunu küçültür.

#### S: Excel dosyasını kaydettikten sonra sıkıştırma düzeyini ayarlayabilir miyim?

C: Hayır, Excel dosyasını belirli bir sıkıştırma düzeyiyle kaydettikten sonra sıkıştırma düzeyini daha sonra ayarlayamazsınız. Değiştirmek isterseniz, dosyayı yeni sıkıştırma düzeyiyle yeniden kaydetmeniz gerekecektir.