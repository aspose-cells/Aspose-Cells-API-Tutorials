---
title: Paylaşılan Çalışma Kitabını Parolayla Koruyun veya Korumayı Kaldırın
linktitle: Paylaşılan Çalışma Kitabını Parolayla Koruyun veya Korumayı Kaldırın
second_title: Aspose.Cells for .NET API Referansı
description: Aspose.Cells for .NET kullanarak paylaşılan bir çalışma kitabını parolayla nasıl koruyacağınızı veya korumasını nasıl kaldıracağınızı öğrenin.
type: docs
weight: 120
url: /tr/net/excel-workbook/password-protect-or-unprotect-shared-workbook/
---
Paylaşılan bir çalışma kitabını parolayla korumak, veri gizliliğini sağlamak açısından önemlidir. Aspose.Cells for .NET ile, paylaşılan bir çalışma kitabını parola kullanarak kolayca koruyabilir veya korumasını kaldırabilirsiniz. İstenilen sonuçları elde etmek için aşağıdaki adımları izleyin:

## 1. Adım: Çıkış dizinini belirtin

Öncelikle korumalı Excel dosyasının kaydedileceği çıktı dizinini belirtmeniz gerekir. Aspose.Cells'i kullanarak bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
```

## Adım 2: Boş bir Excel dosyası oluşturun

Daha sonra koruma veya korumayı kaldırma uygulamak istediğiniz boş bir Excel dosyası oluşturabilirsiniz. İşte örnek bir kod:

```csharp
// Boş bir Excel çalışma kitabı oluşturun
Workbook wb = new Workbook();
```

## 3. Adım: Paylaşılan çalışma kitabını koruyun veya korumasını kaldırın

Çalışma kitabını oluşturduktan sonra uygun parolayı belirterek paylaşılan çalışma kitabını koruyabilir veya korumasını kaldırabilirsiniz. İşte nasıl:

```csharp
// Paylaşılan çalışma kitabını parolayla koruyun
wb.ProtectSharedWorkbook("1234");

// Paylaşılan çalışma kitabının korumasını kaldırmak için bu satırın açıklamasını kaldırın
// wb.UnprotectSharedWorkbook("1234");
```

## Adım 4: Çıktı Excel dosyasını kaydedin

Korumayı veya korumayı kaldırmayı uyguladıktan sonra, korumalı Excel dosyasını belirtilen çıktı dizinine kaydedebilirsiniz. Bunu nasıl yapacağınız aşağıda açıklanmıştır:

```csharp
// Çıktı Excel dosyasını kaydedin
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

### Aspose.Cells for .NET kullanarak Paylaşılan Çalışma Kitabını Parolayla Korumak veya Korumayı Kaldırmak için örnek kaynak kodu 
```csharp
//Çıkış dizini
string outputDir = RunExamples.Get_OutputDirectory();
//Boş Excel dosyası oluştur
Workbook wb = new Workbook();
//Paylaşılan Çalışma Kitabını Parolayla Koruyun
wb.ProtectSharedWorkbook("1234");
//Paylaşılan Çalışma Kitabının Korumasını Kaldırmak için bu satırın açıklamasını kaldırın
//wb.UnprotectSharedWorkbook("1234");
//Çıktı Excel dosyasını kaydedin
wb.Save(outputDir + "outputProtectSharedWorkbook.xlsx");
Console.WriteLine("PasswordProtectOrUnprotectSharedWorkbook executed successfully.\r\n");
```

## Çözüm

Paylaşılan bir çalışma kitabını parolayla korumak veya korumayı kaldırmak, veri güvenliğini sağlamak açısından önemlidir. Aspose.Cells for .NET ile bu işlevselliği Excel dosyalarınıza kolayca ekleyebilirsiniz. Bu kılavuzdaki adımları izleyerek, paylaşılan çalışma kitaplarınızı parola kullanarak etkili bir şekilde koruyabilir veya korumasını kaldırabilirsiniz. Kendi Excel dosyalarınızla denemeler yapın ve hassas verilerinizin güvenliğini koruduğunuzdan emin olun.

### SSS

#### S: Aspose.Cells ile paylaşılan bir çalışma kitabına ne tür koruma uygulayabilirim?
    
C: Aspose.Cells ile, paylaşılan bir çalışma kitabını, verilere yetkisiz erişimi, değiştirilmesini veya silinmesini önlemek için bir parola belirleyerek koruyabilirsiniz.

#### S: Paylaşılan bir çalışma kitabını parola belirtmeden koruyabilir miyim?
    
C: Evet, paylaşılan bir çalışma kitabını parola belirtmeden koruyabilirsiniz. Ancak daha iyi güvenlik için güçlü bir şifre kullanılması tavsiye edilir.

#### S: Aspose.Cells ile paylaşılan bir çalışma kitabının korumasını nasıl kaldırabilirim?
    
C: Paylaşılan bir çalışma kitabının korumasını kaldırmak için, çalışma kitabını korurken kullandığınız parolanın aynısını belirtmeniz gerekir. Bu, korumanın kaldırılmasına ve verilere serbestçe erişilmesine olanak tanır.

#### S: Paylaşılan bir çalışma kitabını korumak, çalışma kitabındaki özellikleri ve formülleri etkiler mi?
    
C: Paylaşılan bir çalışma kitabını koruduğunuzda kullanıcılar çalışma kitabında bulunan özelliklere ve formüllere erişmeye devam edebilir. Koruma yalnızca çalışma kitabındaki yapısal değişiklikleri etkiler.