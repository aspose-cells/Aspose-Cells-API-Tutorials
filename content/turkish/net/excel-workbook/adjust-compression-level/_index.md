---
title: Sıkıştırma Düzeyini Ayarlayın
linktitle: Sıkıştırma Düzeyini Ayarlayın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET ile sıkıştırma düzeyini ayarlayarak Excel çalışma kitaplarınızın boyutunu azaltın.
type: docs
weight: 50
url: /tr/net/excel-workbook/adjust-compression-level/
---
Bu adım adım eğitimde, Aspose.Cells for .NET'i kullanarak sıkıştırma düzeyini ayarlamanıza olanak tanıyan sağlanan C# kaynak kodunu açıklayacağız. Excel çalışma kitabınızdaki sıkıştırma düzeyini ayarlamak için aşağıdaki adımları izleyin.

## 1. Adım: Kaynak ve çıkış dizinlerini ayarlayın

```csharp
// kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
// Çıkış dizini
string outDir = RunExamples.Get_OutputDirectory();
```

Bu ilk adımda Excel dosyalarının kaynak ve çıktı dizinlerini tanımlıyoruz.

## Adım 2: Excel Çalışma Kitabını Yükleyin

```csharp
// Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(sourceDir + "LargeSampleFile.xlsx");
```

Excel çalışma kitabını belirtilen dosyadan kullanarak yüklüyoruz.`Workbook` Aspose.Cells'ten sınıf.

## 3. Adım: Yedekleme seçeneklerini ayarlayın

```csharp
// Yedekleme seçeneklerini tanımlayın
XlsbSaveOptions options = new XlsbSaveOptions();
```

 Bunun bir örneğini oluşturuyoruz`XlsbSaveOptions` Kaydetme seçeneklerini ayarlamak için sınıf.

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

 Sıkıştırma seviyesini ayarlayarak ayarlıyoruz`CompressionType` ile`Level1`. Daha sonra belirtilen bu sıkıştırma seçeneği ile Excel çalışma kitabını kaydediyoruz.

## 5. Adım: Sıkıştırma düzeyini ayarlayın (Seviye 6)

```csharp
// Sıkıştırma seviyesini ayarlayın (Seviye 6)
options.CompressionType = OoxmlCompressionType.Level6;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_6_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 6): " + elapsedMs);
```

 Sıkıştırma seviyesini ayarlamak için işlemi tekrarlıyoruz.`Level6` ve bu seçenekle Excel çalışma kitabını kaydedin.

## 6. Adım: Sıkıştırma düzeyini ayarlayın (Seviye 9)

```csharp
// Sıkıştırma seviyesini ayarlayın (Seviye 9)
options.CompressionType = OoxmlCompressionType.Level9;
watch = System.Diagnostics.Stopwatch.StartNew();
workbook.Save(outDir + "LargeSampleFile_level_9_out.xlsb", options);
watch.Stop();
elapsedMs = watch. ElapsedMilliseconds;
Console.WriteLine("Elapsed time (Level 9): " + elapsedMs);
```

 Sıkıştırma seviyesini ayarlamak için işlemi son bir kez tekrarlıyoruz.`Level9` ve bu seçenekle Excel çalışma kitabını kaydedin.

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

Tebrikler! Aspose.Cells for .NET'i kullanarak bir Excel çalışma kitabındaki sıkıştırma düzeyini nasıl ayarlayacağınızı öğrendiniz. İhtiyaçlarınıza en uygun olanı bulmak için farklı sıkıştırma düzeylerini deneyin.

### SSS

#### S: Excel çalışma kitabında sıkıştırma nedir?

C: Excel çalışma kitabındaki sıkıştırma, sıkıştırma algoritmaları kullanılarak dosya boyutunun küçültülmesi işlemidir. Bu, gereken depolama alanını azaltır ve dosyayı yüklerken ve işlerken performansı artırır.

#### S: Aspose.Cells'te hangi sıkıştırma seviyeleri mevcut?

C: Aspose.Cells ile sıkıştırma seviyesini 1'den 9'a kadar ayarlayabilirsiniz. Sıkıştırma seviyesi ne kadar yüksek olursa dosya boyutu o kadar küçük olur, ancak aynı zamanda işlem süresini de artırabilir.

#### S: Excel çalışma kitabım için doğru sıkıştırma düzeyini nasıl seçerim?

C: Sıkıştırma seviyesinin seçimi özel ihtiyaçlarınıza bağlıdır. Maksimum sıkıştırma istiyorsanız ve işlem süresi sorun değilse, 9. seviyeye geçebilirsiniz. Dosya boyutu ile işlem süresi arasında bir uzlaşma tercih ediyorsanız, orta seviyeyi seçebilirsiniz.

#### S: Sıkıştırma Excel çalışma kitabındaki veri kalitesini etkiler mi?

C: Hayır, sıkıştırma Excel çalışma kitabındaki veri kalitesini etkilemez. Verinin kendisini değiştirmeden sıkıştırma tekniklerini kullanarak dosya boyutunu azaltır.

#### S: Excel dosyasını kaydettikten sonra sıkıştırma düzeyini ayarlayabilir miyim?

C: Hayır, Excel dosyasını belirli bir sıkıştırma düzeyiyle kaydettikten sonra sıkıştırma düzeyini daha sonra ayarlayamazsınız. Değiştirmek isterseniz dosyayı yeni sıkıştırma düzeyiyle yeniden kaydetmeniz gerekecektir.