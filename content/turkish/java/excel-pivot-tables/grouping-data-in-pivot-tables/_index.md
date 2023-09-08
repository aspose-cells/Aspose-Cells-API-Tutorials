---
title: Pivot Tablolarda Verileri Gruplama
linktitle: Pivot Tablolarda Verileri Gruplama
second_title: Aspose.Cells Java Excel İşleme API'si
description: Aspose.Cells for Java'yı kullanarak Excel'de pivot tabloları nasıl oluşturacağınızı öğrenin. Kaynak kodu örnekleriyle veri gruplandırmasını ve analizini otomatikleştirin.
type: docs
weight: 14
url: /tr/java/excel-pivot-tables/grouping-data-in-pivot-tables/
---

Pivot tablolar, elektronik tablolardaki verileri analiz etmek ve özetlemek için güçlü bir araçtır. Değerli bilgiler elde etmek için verileri gruplandırmanıza ve kategorilere ayırmanıza olanak tanır. Bu makalede, kaynak kod örnekleriyle birlikte Aspose.Cells for Java kullanarak pivot tablolardaki verileri etkili bir şekilde nasıl gruplandıracağımızı inceleyeceğiz.

## giriiş

Pivot tablolar, büyük veri kümelerindeki verileri düzenlemek ve özetlemek için esnek bir yol sağlar. Verilerinizi kategorilere veya hiyerarşilere göre gruplandırarak özel görünümler oluşturmanıza olanak tanır. Bu, verilerinizdeki eğilimleri, kalıpları ve aykırı değerleri daha kolay belirlemenize yardımcı olabilir.

## Adım 1: Pivot Tablo Oluşturun

Aspose.Cells for Java'yı kullanarak bir pivot tablo oluşturarak başlayalım. Aşağıda örnek bir Excel dosyasından pivot tablonun nasıl oluşturulacağına ilişkin bir örnek verilmiştir.

```java
// Excel dosyasını yükleyin
Workbook workbook = new Workbook("sample.xlsx");

// Verileri içeren çalışma sayfasına erişin
Worksheet worksheet = workbook.getWorksheets().get(0);

// Veri aralığını belirtin
CellArea sourceData = new CellArea();
sourceData.startRow = 0;
sourceData.endRow = 19; // 20 satırlık veri varsayalım
sourceData.startColumn = 0;
sourceData.endColumn = 3; // 4 sütunluk veri varsayarsak

// Veri aralığına göre bir pivot tablo oluşturun
int index = worksheet.getPivotTables().add(sourceData, "A1", "PivotTable1");

// Pivot tabloyu dizine göre alın
PivotTable pivotTable = worksheet.getPivotTables().get(index);

// Satırlara ve sütunlara alan ekleme
pivotTable.addFieldToArea("Product", PivotFieldType.ROW);
pivotTable.addFieldToArea("Region", PivotFieldType.COLUMN);

// Değer ekleyin ve toplamayı uygulayın
pivotTable.addFieldToArea("Sales", PivotFieldType.DATA);
pivotTable.getDataFields().get(0).setFunction(PivotFieldFunction.SUM);

// Değiştirilen Excel dosyasını kaydedin
workbook.save("output.xlsx");
```

## Adım 2: Verileri Gruplandırın

 Aspose.Cells for Java'da, pivot tablodaki verileri aşağıdaki komutu kullanarak gruplandırabilirsiniz:`PivotField` sınıf. Pivot tablodaki bir alanın nasıl gruplandırılacağına ilişkin bir örneği burada bulabilirsiniz:

```java
// Pivot tablodaki "Ürün" alanına erişin
PivotField productField = pivotTable.getPivotFields().get("Product");

//"Ürün" alanını belirli bir kritere göre, örneğin başlangıç harfine göre gruplandırın
productField.setIsAutoSubtotals(false);
productField.setBaseField("Product");
productField.setAutoSort(true);
productField.setAutoShow(true);

// Değiştirilen Excel dosyasını gruplandırılmış verilerle kaydedin
workbook.save("output_grouped.xlsx");
```

## 3. Adım: Gruplandırmayı Özelleştirin

Tarihe dayalı gruplama aralıkları veya özel gruplama kuralları belirlemek gibi gruplama ayarlarını daha da özelleştirebilirsiniz. Tarihe dayalı gruplamayı özelleştirmenin bir örneğini burada bulabilirsiniz:

```java
// Pivot tablodaki "Tarih" alanına erişin (bunun bir tarih alanı olduğu varsayılarak)
PivotField dateField = pivotTable.getPivotFields().get("Date");

// Tarihleri aylara göre gruplandır
dateField.setIsAutoSubtotals(false);
dateField.setIsDateGroup(true);
dateField.setDateGroupingType(PivotFieldDateGroupingType.MONTHS);

// Değiştirilen Excel dosyasını özel tarih gruplandırmasıyla kaydedin
workbook.save("output_custom_grouping.xlsx");
```

## Çözüm

Verileri pivot tablolarda gruplamak, Excel'de verileri analiz etmek ve özetlemek için değerli bir tekniktir ve Aspose.Cells for Java, bu sürecin otomatikleştirilmesini kolaylaştırır. Sağlanan kaynak kodu örnekleriyle pivot tablolar oluşturabilir, gruplamayı özelleştirebilir ve verilerinizden verimli bir şekilde öngörüler elde edebilirsiniz.

## SSS

### 1. Excel'deki pivot tabloların amacı nedir?

Excel'deki pivot tablolar, büyük veri kümelerini özetlemek ve analiz etmek için kullanılır. Verilerinizin özel görünümlerini oluşturmanıza olanak tanıyarak kalıpları ve eğilimleri tanımlamayı kolaylaştırır.

### 2. Pivot tablodaki verilerin gruplandırılmasını nasıl özelleştirebilirim?

 Pivot tablodaki verilerin gruplandırılmasını aşağıdakileri kullanarak özelleştirebilirsiniz:`PivotField` Aspose.Cells for Java'daki sınıf. Bu, tarihe dayalı aralıklar veya özel kurallar gibi gruplandırma ölçütlerini belirtmenize olanak tanır.

### 3. Aspose.Cells for Java'yı kullanarak pivot tabloların oluşturulmasını otomatikleştirebilir miyim?

Evet, sağlanan kaynak kodu örneklerinde gösterildiği gibi Aspose.Cells for Java'yı kullanarak Excel'de pivot tabloların oluşturulmasını otomatikleştirebilirsiniz.