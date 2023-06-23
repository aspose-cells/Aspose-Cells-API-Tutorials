---
title: Odata Ayrıntılarını Alın
linktitle: Odata Ayrıntılarını Alın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel çalışma kitabından OData ayrıntılarını nasıl alacağınızı öğrenin.
type: docs
weight: 110
url: /tr/net/excel-workbook/get-odata-details/
---
Dış veri kaynaklarından yapılandırılmış verilerin alınması söz konusu olduğunda OData kullanımı yaygındır. Aspose.Cells for .NET ile OData ayrıntılarını bir Excel çalışma kitabından kolayca alabilirsiniz. İstenen sonuçları elde etmek için aşağıdaki adımları izleyin:

## 1. Adım: Kaynak dizini belirtin

Öncelikle, OData ayrıntılarını içeren Excel dosyasının bulunduğu kaynak dizini belirtmeniz gerekir. Aspose.Cells kullanarak bunu şu şekilde yapabilirsiniz:

```csharp
// kaynak dizin
string SourceDir = RunExamples.Get_SourceDirectory();
```

## 2. Adım: Çalışma kitabını yükleyin

Kaynak dizin belirtildikten sonra, Excel çalışma kitabını dosyadan yükleyebilirsiniz. İşte örnek bir kod:

```csharp
// çalışma kitabını yükle
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## 3. Adım: OData ayrıntılarını alın

Çalışma kitabını yükledikten sonra, PowerQueryFormulas koleksiyonunu kullanarak OData ayrıntılarına erişebilirsiniz. İşte nasıl:

```csharp
// Power Query formüllerinin koleksiyonunu alın
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Her bir Power Query formülünü gözden geçirin
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Power Query formül öğeleri koleksiyonunu alın
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Her bir Power Query formül öğesini yineleyin
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Aspose.Cells for .NET kullanarak Odata Ayrıntılarını Al için örnek kaynak kodu 
```csharp
// kaynak dizin
string SourceDir = RunExamples.Get_SourceDirectory();
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;
foreach (PowerQueryFormula PQF in PQFcoll)
{
	Console.WriteLine("Connection Name: " + PQF.Name);
	PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;
	foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
	{
		Console.WriteLine("Name: " + PQFI.Name);
		Console.WriteLine("Value: " + PQFI.Value);
	}
}
Console.WriteLine("GetOdataDetails executed successfully.");
```

## Çözüm

Aspose.Cells for .NET ile bir Excel çalışma kitabından OData ayrıntılarını almak artık çok kolay. Bu kılavuzda belirtilen adımları izleyerek, OData verilerine verimli bir şekilde erişebilecek ve bunları işleyebileceksiniz. OData ayrıntılarını içeren kendi Excel dosyalarınızla deneyler yapın ve bu güçlü özellikten en iyi şekilde yararlanın.

### SSS

#### S: Aspose.Cells, OData dışında başka veri kaynaklarını da destekliyor mu?
    
C: Evet, Aspose.Cells, SQL veritabanları, CSV dosyaları, web hizmetleri vb. gibi çoklu veri kaynaklarını destekler.

#### S: Uygulamamda alınan OData ayrıntılarını nasıl kullanabilirim?
    
C: Aspose.Cells'i kullanarak OData ayrıntılarını aldıktan sonra, bunları uygulamanızda veri analizi, rapor oluşturma veya diğer herhangi bir manipülasyon için kullanabilirsiniz.

#### S: Aspose.Cells ile alırken OData verilerini filtreleyebilir veya sıralayabilir miyim?
    
C: Evet, Aspose.Cells, özel ihtiyaçlarınızı karşılamak için OData verilerini filtrelemek, sıralamak ve işlemek için gelişmiş işlevsellik sunar.

#### S: OData ayrıntılarını alma sürecini Aspose.Cells ile otomatikleştirebilir miyim?
    
C: Evet, Aspose.Cells'i iş akışlarınıza entegre ederek veya programlama betikleri kullanarak OData ayrıntılarını alma sürecini otomatikleştirebilirsiniz.