---
title: Regex'i Değiştir
linktitle: Regex'i Değiştir
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel dosyalarında Regex değişimini nasıl gerçekleştireceğinizi öğrenin.
type: docs
weight: 140
url: /tr/net/excel-workbook/regex-replace/
---
Normal ifadelere (Regex) dayalı metin değiştirme, Excel dosyalarındaki verileri değiştirirken yaygın olarak yapılan bir görevdir. Aspose.Cells for .NET ile aşağıdaki adımları izleyerek kolayca Regex değişimi gerçekleştirebilirsiniz:

## Adım 1: Kaynak dizini ve çıktı dizinini belirtin

Öncelikle değiştirilecek verileri içeren Excel dosyasının bulunduğu kaynak dizini ve değiştirilen dosyayı kaydetmek istediğiniz çıktı dizinini belirtmeniz gerekir. Aspose.Cells'i kullanarak bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// kaynak dizini
string sourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. Adım: Kaynak Excel dosyasını yükleyin

Daha sonra, Regex değişimini gerçekleştirmek istediğiniz kaynak Excel dosyasını yüklemeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Kaynak Excel dosyasını yükleyin
Workbook workbook = new Workbook(sourceDir + "SampleRegexReplace.xlsx");
```

## 3. Adım: Regex Değiştirme işlemini gerçekleştirin

Dosyayı yükledikten sonra, büyük/küçük harf duyarlılığı ve tam hücre içeriği eşleşmesi dahil değiştirme seçeneklerini ayarlayabilirsiniz. Regex değişimini gerçekleştirmek için örnek kod:

```csharp
// Değiştirme seçeneklerini ayarlayın
ReplaceOptions replace = new ReplaceOptions();
replace.CaseSensitive = false;
replace.MatchEntireCellContents = false;

// Arama anahtarının normal bir ifade olduğunu tanımlayın
replace. RegexKey = true;

// Regex değişimini gerçekleştir
workbook. Replace("\\bKIM\\b", "^^^TIM^^^", replace);
```

## Adım 4: Çıktı Excel dosyasını kaydedin

Regex değişimi tamamlandıktan sonra, değiştirilen Excel dosyasını belirtilen çıktı dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel dosyasını kaydedin
workbook.Save(outputDir + "RegexReplace_out.xlsx");
Console.WriteLine("RegexReplace executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak Regex Değiştirme için örnek kaynak kodu 
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

Regex değiştirme, bir Excel dosyasındaki verileri dinamik olarak değiştirmek için güçlü bir tekniktir. Aspose.Cells for .NET ile yukarıda özetlenen adımları izleyerek Regex değişimini kolayca gerçekleştirebilirsiniz. Kendi düzenli ifadelerinizi deneyin ve Aspose.Cells'in sunduğu esneklikten yararlanın.

### SSS

#### S: Regex Değiştirme nedir?
    
C: Regex değiştirme, bir Excel dosyasındaki normal ifadelere dayalı metin kalıplarını değiştirmek için kullanılan bir tekniktir. Bu, verilerde hızlı ve doğru değişiklikler yapılmasına olanak tanır.

#### S: Regex değişimi büyük/küçük harfe duyarlı mıdır?
    
C: Hayır, Aspose.Cells ile Regex değişiminin büyük/küçük harfe duyarlı olup olmayacağını belirleyebilirsiniz. Bu özellik üzerinde tam kontrole sahipsiniz.

#### S: Regex'i değiştirirken hücre içeriğinin tam eşleşmesini nasıl belirleyebilirim?
    
C: Aspose.Cells, Regex değişiminin hücre içeriğiyle tam olarak eşleşip eşleşmeyeceğini tanımlamanıza olanak tanır. Bu seçeneği ihtiyaçlarınıza göre ayarlayabilirsiniz.

#### S: Regex'i Aspose.Cells ile değiştirirken gelişmiş normal ifadeleri kullanabilir miyim?
    
C: Evet, Aspose.Cells gelişmiş düzenli ifadeleri destekleyerek Excel dosyalarınızda karmaşık ve kapsamlı değişiklikler yapmanıza olanak tanır.

#### S: Regex değişiminin başarılı olup olmadığını nasıl kontrol edebilirim?
    
C: Regex değişimini gerçekleştirdikten sonra çıkışı kontrol ederek ve çıkış Excel dosyasının doğru şekilde oluşturulduğundan emin olarak işlemin başarılı olup olmadığını doğrulayabilirsiniz.
	