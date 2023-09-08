---
title: Odata Ayrıntılarını Alın
linktitle: Odata Ayrıntılarını Alın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak bir Excel çalışma kitabından OData ayrıntılarını nasıl alacağınızı öğrenin.
type: docs
weight: 110
url: /tr/net/excel-workbook/get-odata-details/
---
Dış veri kaynaklarından yapılandırılmış verilerin alınması söz konusu olduğunda OData kullanımı yaygındır. Aspose.Cells for .NET ile OData ayrıntılarını bir Excel çalışma kitabından kolayca alabilirsiniz. İstenilen sonuçları elde etmek için aşağıdaki adımları izleyin:

## 1. Adım: Kaynak dizini belirtin

Öncelikle OData detaylarını içeren Excel dosyasının bulunduğu kaynak dizini belirtmeniz gerekiyor. Aspose.Cells'i kullanarak bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// kaynak dizini
string SourceDir = RunExamples.Get_SourceDirectory();
```

## Adım 2: Çalışma kitabını yükleyin

Kaynak dizin belirtildikten sonra Excel çalışma kitabını dosyadan yükleyebilirsiniz. İşte örnek bir kod:

```csharp
// Çalışma kitabını yükle
Workbook workbook = new Workbook(SourceDir + "ODataSample.xlsx");
```

## 3. Adım: OData ayrıntılarını alın

Çalışma kitabını yükledikten sonra PowerQueryFormulas koleksiyonunu kullanarak OData ayrıntılarına erişebilirsiniz. İşte nasıl:

```csharp
// Power Query formüllerinin koleksiyonunu alın
PowerQueryFormulaCollction PQFcoll = workbook.DataMashup.PowerQueryFormulas;

// Her Power Query formülünün üzerinden geçin
foreach(PowerQueryFormula PQF in PQFcoll)
{
Console.WriteLine("Connection name: " + PQF.Name);

// Power Query formül öğelerinin koleksiyonunu alma
PowerQueryFormulaItemCollection PQFIcoll = PQF.PowerQueryFormulaItems;

// Her Power Query formül öğesini yineleyin
foreach (PowerQueryFormulaItem PQFI in PQFIcoll)
{
Console.WriteLine("Name: " + PQFI.Name);
Console.WriteLine("Value: " + PQFI.Value);
}
}

Console.WriteLine("GetOdataDetails executed successfully.");
```

### Aspose.Cells for .NET kullanarak Odata Detaylarını Alma için örnek kaynak kodu 
```csharp
// kaynak dizini
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

Aspose.Cells for .NET ile OData ayrıntılarını Excel çalışma kitabından almak artık çok kolay. Bu kılavuzda özetlenen adımları izleyerek OData verilerine verimli bir şekilde erişebilecek ve bunları işleyebileceksiniz. OData ayrıntılarını içeren kendi Excel dosyalarınızla denemeler yapın ve bu güçlü özellikten en iyi şekilde yararlanın.

### SSS

#### S: Aspose.Cells, OData'nın yanı sıra diğer veri kaynaklarını da destekliyor mu?
    
C: Evet, Aspose.Cells, SQL veritabanları, CSV dosyaları, web hizmetleri vb. gibi birden fazla veri kaynağını destekler.

#### S: Alınan OData ayrıntılarını uygulamamda nasıl kullanabilirim?
    
C: Aspose.Cells'i kullanarak OData ayrıntılarını aldıktan sonra bunları veri analizi, rapor oluşturma veya uygulamanızdaki diğer manipülasyonlar için kullanabilirsiniz.

#### S: Aspose.Cells ile OData verilerini alırken filtreleyebilir veya sıralayabilir miyim?
    
C: Evet, Aspose.Cells, OData verilerini özel ihtiyaçlarınızı karşılayacak şekilde filtrelemek, sıralamak ve değiştirmek için gelişmiş işlevsellik sunar.

#### S: Aspose.Cells ile OData ayrıntılarını alma sürecini otomatikleştirebilir miyim?
    
C: Evet, Aspose.Cells'i iş akışlarınıza entegre ederek veya programlama komut dosyalarını kullanarak OData ayrıntılarını alma sürecini otomatikleştirebilirsiniz.