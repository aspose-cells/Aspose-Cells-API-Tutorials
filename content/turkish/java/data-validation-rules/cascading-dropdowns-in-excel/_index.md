---
title: Excel'de Basamaklı Açılan Menüler
linktitle: Excel'de Basamaklı Açılan Menüler
second_title: Aspose.Cells Java Excel İşleme API'si
description: Aspose.Cells for Java'yı kullanarak Excel'de basamaklı açılır menüleri nasıl oluşturacağınızı öğrenin. Bu adım adım kılavuz, verimli Excel elektronik tablosu manipülasyonu için kaynak kodu ve uzman ipuçları sağlar.
type: docs
weight: 13
url: /tr/java/data-validation-rules/cascading-dropdowns-in-excel/
---

## Excel'de Basamaklı Açılan Menülere Giriş

Elektronik tablo manipülasyonu dünyasında Aspose.Cells for Java, geliştiricilerin Excel dosyalarıyla verimli bir şekilde çalışmasını sağlayan güçlü bir araç seti olarak duruyor. Sunduğu ilgi çekici özelliklerden biri, Excel'de basamaklı açılır menüler oluşturma yeteneğidir; bu, kullanıcıların önceki seçime dayalı olarak seçenekleri dinamik olarak seçmesine olanak tanır. Bu adım adım kılavuzda, Aspose.Cells for Java'yı kullanarak basamaklı açılır menüleri uygulama sürecini ayrıntılı olarak ele alacağız. Öyleyse başlayalım!

## Önkoşullar

Bu yolculuğa çıkmadan önce aşağıdaki önkoşulların mevcut olduğundan emin olun:

-  Aspose.Cells for Java: Şu adresten indirip yükleyin:[Burada](https://releases.aspose.com/cells/java/).
- Java Geliştirme Ortamı: Makinenizde Java geliştirme ortamının kurulu olması gerekir.
- Temel Excel Anlayışı: Excel'e ve temel kavramlarına aşinalık faydalı olacaktır.

## Sahneyi hazırlamak

Amacımız basamaklı açılır menülere sahip bir Excel sayfası oluşturmaktır. Bir ülke listenizin olduğu ve bir ülke seçtiğinizde o ülkedeki şehirlerin bir listesinin seçime açık olması gereken bir senaryo düşünün. Bunu başarmak için adımları inceleyelim.

## Adım 1: Excel Çalışma Kitabının Oluşturulması

Öncelikle Aspose.Cells for Java'yı kullanarak bir Excel çalışma kitabı oluşturalım. İki sayfa ekleyeceğiz: biri ülke listesi için, diğeri şehir listesi için.

```java
// Excel çalışma kitabı oluşturmak için Java kodu
Workbook workbook = new Workbook();
Worksheet countrySheet = workbook.getWorksheets().get(0);
countrySheet.setName("Countries");
Worksheet citySheet = workbook.getWorksheets().add("Cities");
```

## Adım 2: Verileri Doldurma

Şimdi çalışma sayfalarımızı verilerle doldurmamız gerekiyor. "Ülkeler" sayfasında ülkeleri listeleyeceğiz ve "Şehirler" sayfasında daha sonra dinamik olarak dolduracağımız için başlangıçta boş bırakacağız.

```java
//"Ülkeler" sayfasını doldurmak için Java kodu
countrySheet.getCells().get("A1").putValue("Country");
countrySheet.getCells().get("A2").putValue("USA");
countrySheet.getCells().get("A3").putValue("Canada");
countrySheet.getCells().get("A4").putValue("UK");
// Gerektiğinde daha fazla ülke ekleyin
```

## 3. Adım: Açılır Menüleri Oluşturma

Daha sonra ülke ve şehir sütunları için açılır listeler oluşturacağız. Bu açılır menüler, bir ülke seçildiğinde şehir açılır listesinin buna göre güncelleneceği şekilde bağlanacaktır.

```java
// Açılır listeler oluşturmak için Java kodu
DataValidationCollection validations = countrySheet.getDataValidations();
DataValidation validation = validations.get(validations.add(1, 1, countrySheet.getCells().getMaxDataRow(), 1));
validation.setType(DataValidationType.LIST);
validation.setFormula1("Countries!$A$2:$A$4"); // Ülke listesine referans
```

## 4. Adım: Basamaklı Açılır Menüleri Uygulama

Şimdi heyecan verici kısım geliyor: basamaklı açılır menülerin uygulanması. Şehir açılır listesini seçilen ülkeye göre dinamik olarak güncellemek için Aspose.Cells for Java'yı kullanacağız.

```java
// Basamaklı açılır menüleri uygulamak için Java kodu
countrySheet.getCells().setCellObserver(new ICellObserver() {
    @Override
    public void cellChanged(Cell cell) {
        if (cell.getName().equals("B2")) {
            // Önceki şehir açılır listesini temizle
            citySheet.getCells().get("B2").setValue("");
            
            // Seçilen ülkeyi belirle
            String selectedCountry = cell.getStringValue();
            
            // Seçilen ülkeye göre şehir açılır menüsünü doldurun
            switch (selectedCountry) {
                case "USA":
                    validation.setFormula1("Cities!$A$2:$A$4"); // ABD şehirleriyle doldurun
                    break;
                case "Canada":
                    validation.setFormula1("Cities!$B$2:$B$4"); // Kanada şehirleriyle doldurun
                    break;
                case "UK":
                    validation.setFormula1("Cities!$C$2:$C$4"); // Birleşik Krallık şehirleriyle doldurun
                    break;
                // Diğer ülkeler için daha fazla vaka ekleyin
            }
        }
    }
});
```

## Çözüm

Bu kapsamlı kılavuzda Aspose.Cells for Java kullanarak Excel'de basamaklı açılır menülerin nasıl oluşturulacağını araştırdık. Önkoşulları ayarlayarak, Excel çalışma kitabını oluşturarak, verileri doldurarak başladık ve ardından açılır menüler oluşturmanın ve dinamik basamaklandırma davranışını uygulamanın inceliklerini derinlemesine inceledik. Bir geliştirici olarak artık Excel dosyalarınızı etkileşimli açılır menülerle geliştirerek kusursuz bir kullanıcı deneyimi sağlayacak bilgi ve araçlara sahipsiniz.

## SSS'ler

### Açılır menülere nasıl daha fazla ülke ve şehir ekleyebilirim?

Daha fazla ülke ve şehir eklemek için Excel çalışma kitabınızdaki ilgili sayfaları güncellemeniz gerekir. "Ülkeler" ve "Şehirler" sayfalarındaki listeleri genişletmeniz yeterlidir; açılır menüler otomatik olarak yeni girişleri içerecektir.

### Bu tekniği diğer Excel özellikleriyle birlikte kullanabilir miyim?

Kesinlikle! Özel ihtiyaçlarınıza göre tasarlanmış güçlü ve etkileşimli elektronik tablolar oluşturmak için basamaklı açılır menüleri koşullu biçimlendirme, formüller ve grafikler gibi çeşitli Excel özellikleriyle birleştirebilirsiniz.

### Aspose.Cells for Java hem küçük hem de büyük ölçekli projelere uygun mu?

Evet, Aspose.Cells for Java çok yönlüdür ve her boyuttaki projede kullanılabilir. İster küçük bir yardımcı program üzerinde ister karmaşık bir kurumsal uygulama üzerinde çalışıyor olun, Aspose.Cells for Java, Excel ile ilgili görevlerinizi kolaylaştırabilir.

### Aspose.Cells for Java ile basamaklı açılan menüleri uygulamak için ileri düzey programlama becerilerine ihtiyacım var mı?

Java'yı temel düzeyde anlamak yararlı olsa da Aspose.Cells for Java, süreç boyunca size yol gösterecek kapsamlı belgeler ve örnekler sağlar. Biraz özveri ve pratikle bu özelliğe hakim olabilirsiniz.

### Aspose.Cells for Java için daha fazla kaynak ve belgeyi nerede bulabilirim?

 Aspose.Cells for Java ile ilgili kapsamlı belgelere ve kaynaklara şu adresten ulaşabilirsiniz:[Burada](https://reference.aspose.com/cells/java/).