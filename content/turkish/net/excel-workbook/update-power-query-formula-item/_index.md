---
title: Power Query Formül Öğesini Güncelle
linktitle: Power Query Formül Öğesini Güncelle
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak Excel dosyalarındaki Power Query formül öğelerini nasıl güncelleyeceğinizi öğrenin.
type: docs
weight: 160
url: /tr/net/excel-workbook/update-power-query-formula-item/
---
Power Query formül öğesini güncellemek, Excel dosyalarındaki verilerle çalışırken sık yapılan bir işlemdir. Aspose.Cells for .NET ile aşağıdaki adımları izleyerek bir Power Query formül öğesini kolayca güncelleyebilirsiniz:

## 1. Adım: Kaynak ve çıktı dizinlerini belirtin

Öncelikle, güncelleştirilecek Power Query formüllerini içeren Excel dosyasının bulunduğu kaynak dizinin yanı sıra, değiştirilen dosyayı kaydetmek istediğiniz çıkış dizinini de belirtmeniz gerekir. Aspose.Cells'i kullanarak bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// kaynak dizini
string SourceDir = RunExamples.Get_SourceDirectory();

// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## 2. Adım: Kaynak Excel çalışma kitabını yükleyin

Daha sonra, Power Query formül öğesini güncelleştirmek istediğiniz kaynak Excel çalışma kitabını yüklemeniz gerekir. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Kaynak Excel çalışma kitabını yükleyin
Workbook workbook = new Workbook(SourceDir + "SamplePowerQueryFormula.xlsx");
```

## 3. Adım: Power Query Formül Öğelerine Göz Atın ve Güncelleyin

Çalışma kitabını yükledikten sonra Power Query formül koleksiyonuna gidebilir ve her formüle ve öğelerine göz atabilirsiniz. Bu örnekte "Kaynak" isimli formül öğesini arıyoruz ve değerini güncelliyoruz. Power Query formül öğesini güncelleştirmek için örnek kod aşağıda verilmiştir:

```csharp
// Power Query formül koleksiyonuna erişme
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

## 4. Adım: Çıktı Excel çalışma kitabını kaydedin

Power Query formül öğesini güncelleştirdikten sonra, değiştirilen Excel çalışma kitabını belirtilen çıktı dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel çalışma kitabını kaydedin
workbook.Save(outputDir + "SamplePowerQueryFormula_out.xlsx");
Console.WriteLine("UpdatePowerQueryFormulaItem executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak Power Query Formül Öğesini Güncelleme için örnek kaynak kodu 
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

Power Query formül öğelerini güncellemek, Excel dosyalarındaki verileri değiştirmek ve işlemek için Aspose.Cells kullanıldığında önemli bir işlemdir. Yukarıda verilen adımları takip ederek formül öğelerini kolayca güncelleyebilirsiniz.

### SSS

#### S: Excel'de Power Query nedir?
     
C: Power Query, farklı kaynaklardan veri toplamaya, dönüştürmeye ve yüklemeye yardımcı olan bir Excel özelliğidir. Verileri Excel'e aktarmadan önce temizlemek, birleştirmek ve yeniden şekillendirmek için güçlü araçlar sunar.

#### S: Power Query formül öğesinin başarıyla güncelleştirilip güncelleştirilmediğini nasıl anlarım?
    A: After running the Power Query Formula Item Update, you can check if the operation was successful by viewing the output and ensuring that the output Excel file was created correctly.

#### S: Birden fazla Power Query formül öğesini aynı anda güncelleştirebilir miyim?
    
C: Evet, Power Query formül öğesi koleksiyonunda dolaşabilir ve özel ihtiyaçlarınıza bağlı olarak birden çok öğeyi tek bir döngüde güncelleştirebilirsiniz.

#### S: Aspose.Cells ile Power Query formülleri üzerinde yapabileceğim başka işlemler var mı?
    
C: Evet, Aspose.Cells, Power Query formülleriyle çalışmak için Excel çalışma kitabındaki formülleri oluşturma, silme, kopyalama ve arama dahil olmak üzere çok çeşitli özellikler sunar.