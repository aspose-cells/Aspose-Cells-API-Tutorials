---
title: Power Query Formül Öğesini Güncelle
linktitle: Power Query Formül Öğesini Güncelle
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel dosyalarındaki Power Query formül öğelerini nasıl güncelleyeceğinizi öğrenin.
type: docs
weight: 160
url: /tr/net/excel-workbook/update-power-query-formula-item/
---
Bir Power Query formül öğesini güncellemek, Excel dosyalarındaki verilerle çalışırken sık yapılan bir işlemdir. Aspose.Cells for .NET ile, aşağıdaki adımları izleyerek bir Power Query formül öğesini kolayca güncelleyebilirsiniz:

## 1. Adım: Kaynak ve çıktı dizinlerini belirtin

Öncelikle, güncellenecek Power Query formüllerini içeren Excel dosyasının bulunduğu kaynak dizini ve değiştirilen dosyayı kaydetmek istediğiniz çıkış dizinini belirtmeniz gerekir. Aspose.Cells kullanarak bunu şu şekilde yapabilirsiniz:

```csharp
// kaynak dizin
string SourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. Adım: Kaynak Excel çalışma kitabını yükleyin

Ardından, Power Query formül öğesini güncellemek istediğiniz kaynak Excel çalışma kitabını yüklemeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Kaynak Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## 3. Adım: Power Query Formül Öğelerine Göz Atın ve Güncelleyin

Çalışma kitabını yükledikten sonra Power Query formül koleksiyonuna gidebilir ve her formüle ve öğelerine göz atabilirsiniz. Bu örnekte, "Kaynak" adlı formül öğesini arıyoruz ve değerini güncelliyoruz. Aşağıda, bir Power Query formül öğesini güncellemek için örnek kod verilmiştir:

```csharp
// Power Query formül koleksiyonuna erişin
DataMashup mashupData = workbook.DataMashup;

// Power Query formülleri ve öğeleri arasında geçiş yapın
foreach(PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
     foreach(PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
     {
         if (item.Name == "Source")
         {
             item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
         }
     }
}
```

## 4. Adım: Çıkış Excel çalışma kitabını kaydedin

Power Query formül öğesini güncelleştirdikten sonra, değiştirilen Excel çalışma kitabını belirtilen çıkış dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel çalışma kitabını kaydedin
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak Power Query Formül Öğesini Güncellemek için örnek kaynak kodu 
```csharp
// Çalışma dizinleri
string SourceDir = RunExamples.Get_SourceDirectory();
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
DataMashup mashupData = workbook.DataMashup;
foreach (PowerQueryFormula formula in mashupData.PowerQueryFormulas)
{
	foreach (PowerQueryFormulaItem item in formula.PowerQueryFormulaItems)
	{
		if (item.Name == "Source")
		{
			item.Value = "Excel.Workbook(File.Contents(\"" + SourceDir + "SamplePowerQueryFormulaSource.xlsx\"), null, true)";
		}
	}
}
// Çıktı çalışma kitabını kaydedin.
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.");
```

## Çözüm

Power Query formül öğelerinin güncellenmesi, Excel dosyalarındaki verileri işlemek ve işlemek için Aspose.Cells kullanırken önemli bir işlemdir. Yukarıda verilen adımları izleyerek formül öğelerini kolayca güncelleyebilirsiniz.

### SSS

#### S: Excel'de Power Query nedir?
     
C: Power Query, farklı kaynaklardan veri toplamaya, dönüştürmeye ve yüklemeye yardımcı olan bir Excel özelliğidir. Verileri Excel'e aktarmadan önce temizlemek, birleştirmek ve yeniden şekillendirmek için güçlü araçlar sunar.

#### S: Bir Power Query formül öğesinin başarıyla güncellenip güncellenmediğini nasıl anlarım?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### S: Birden çok Power Query formül öğesini aynı anda güncelleştirebilir miyim?
    
C: Evet, özel ihtiyaçlarınıza bağlı olarak Power Query formül öğesi koleksiyonunda döngü yapabilir ve birden çok öğeyi tek bir döngüde güncelleyebilirsiniz.

#### S: Aspose.Cells ile Power Query formüllerinde gerçekleştirebileceğim başka işlemler var mı?
    
Y: Evet, Aspose.Cells, bir Excel çalışma kitabında formül oluşturma, silme, kopyalama ve arama dahil olmak üzere Power Query formülleriyle çalışmak için eksiksiz özellikler sunar.