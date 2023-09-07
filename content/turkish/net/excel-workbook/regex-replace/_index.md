---
title: Normal İfade Değiştirme
linktitle: Normal İfade Değiştirme
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel dosyalarında Regex değiştirmeyi nasıl yapacağınızı öğrenin.
type: docs
weight: 140
url: /tr/net/excel-workbook/regex-replace/
---
Düzenli ifadelere (Regex) dayalı metin değiştirme, Excel dosyalarındaki verileri işlerken yaygın bir görevdir. Aspose.Cells for .NET ile, aşağıdaki adımları izleyerek kolayca bir Regex değişimi gerçekleştirebilirsiniz:

## Adım 1: Kaynak dizini ve çıktı dizini belirtin

Her şeyden önce, değiştirilecek verileri içeren Excel dosyasının bulunduğu kaynak dizini ve değiştirilen dosyayı kaydetmek istediğiniz çıkış dizinini belirtmeniz gerekir. Aspose.Cells kullanarak bunu şu şekilde yapabilirsiniz:

```csharp
// kaynak dizin
string sourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. Adım: Kaynak Excel dosyasını yükleyin

Ardından, Regex değiştirmeyi gerçekleştirmek istediğiniz kaynak Excel dosyasını yüklemeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Kaynak Excel dosyasını yükleyin
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## 3. Adım: Regex Değişimini Gerçekleştirin

Dosyayı yükledikten sonra, büyük/küçük harf duyarlılığı ve tam hücre içeriği eşleştirme gibi değiştirme seçeneklerini ayarlayabilirsiniz. Regex değişimini gerçekleştirmek için örnek kod aşağıda verilmiştir:

```csharp
// Değiştirme seçeneklerini ayarla
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Arama anahtarının normal bir ifade olduğunu tanımlayın
replace. RegexKey = true;

// Regex değiştirme gerçekleştirin
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## 4. Adım: Çıktı Excel dosyasını kaydedin

Regex değiştirme işlemi tamamlandıktan sonra, değiştirilen Excel dosyasını belirtilen çıkış dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel dosyasını kaydedin
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak Normal İfade Değiştirme için örnek kaynak kodu 
```csharp
//Kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;
// Aranan anahtarın normal ifade olduğunu belirtmek için true olarak ayarlayın
replace.RegexKey = true;
workbook.Replace("\\bKIM\\b", "^^^TIM^^^", replace);
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.");
```

## Çözüm

Normal ifade değiştirme, bir Excel dosyasındaki verileri dinamik olarak değiştirmek için güçlü bir tekniktir. Aspose.Cells for .NET ile yukarıda özetlenen adımları izleyerek kolayca bir Regex değişimi gerçekleştirebilirsiniz. Kendi normal ifadelerinizle deneyler yapın ve Aspose.Cells'in sunduğu esneklikten yararlanın.

### SSS

#### S: Normal İfade Değiştirme nedir?
    
Y: Normal ifade değiştirme, bir Excel dosyasındaki normal ifadelere dayalı metin kalıplarını değiştirmek için kullanılan bir tekniktir. Bu, verilerde hızlı ve doğru değişiklikler yapılmasını sağlar.

#### S: Regex değiştirme büyük/küçük harfe duyarlı mı?
    
C: Hayır, Aspose.Cells ile normal ifade değişiminin büyük/küçük harfe duyarlı olup olmayacağını belirleyebilirsiniz. Bu özellik üzerinde tam kontrole sahipsiniz.

#### S: Regex'i değiştirirken hücre içeriğinin tam eşleşmesini nasıl belirleyebilirim?
    
C: Aspose.Cells, Normal İfade değişiminin hücre içeriğiyle tam olarak eşleşmesi gerekip gerekmediğini tanımlamanıza olanak tanır. Bu seçeneği ihtiyaçlarınıza göre ayarlayabilirsiniz.

#### S: Regex'i Aspose.Cells ile değiştirirken gelişmiş normal ifadeler kullanabilir miyim?
    
C: Evet, Aspose.Cells, gelişmiş normal ifadeleri destekleyerek, Excel dosyalarınızda karmaşık ve sofistike değişiklikler yapmanıza olanak tanır.

#### S: Regex değişiminin başarılı olup olmadığını nasıl kontrol edebilirim?
    
C: Regex değiştirme işlemini gerçekleştirdikten sonra, çıktıyı kontrol ederek ve çıktı Excel dosyasının doğru şekilde oluşturulduğundan emin olarak işlemin başarılı olup olmadığını doğrulayabilirsiniz.
	