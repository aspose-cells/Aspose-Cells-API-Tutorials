---
title: Dukungan Tanda Tangan Xades
linktitle: Dukungan Tanda Tangan Xades
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menambahkan tanda tangan Xades ke file Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 190
url: /id/net/excel-workbook/xades-signature-support/
---
Pada artikel ini, kami akan memandu Anda langkah demi langkah untuk menjelaskan kode sumber C# di bawah ini, yaitu tentang dukungan tanda tangan Xades menggunakan pustaka Aspose.Cells untuk .NET. Anda akan mengetahui cara menggunakan perpustakaan ini untuk menambahkan tanda tangan digital Xades ke file Excel. Kami juga akan memberi Anda gambaran umum tentang proses penandatanganan dan pelaksanaannya. Ikuti langkah-langkah di bawah ini untuk mendapatkan hasil yang konklusif.

## Langkah 1: Tentukan direktori sumber dan keluaran
Untuk memulai, kita perlu mendefinisikan direktori sumber dan keluaran dalam kode kita. Direktori ini menunjukkan di mana file sumber berada dan di mana file keluaran akan disimpan. Ini kode yang sesuai:

```csharp
// Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

Pastikan untuk menyesuaikan jalur direktori sesuai kebutuhan.

## Langkah 2: Memuat buku kerja Excel
Langkah selanjutnya adalah memuat buku kerja Excel yang ingin kita tambahkan tanda tangan digital Xades. Berikut ini kode untuk memuat buku kerja:

```csharp
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
```

Pastikan untuk menentukan nama file sumber dengan benar dalam kode.

## Langkah 3: Mengonfigurasi tanda tangan digital
Sekarang kita akan mengkonfigurasi tanda tangan digital Xades dengan memberikan informasi yang diperlukan. Kita harus menentukan file PFX yang berisi sertifikat digital, serta kata sandi terkait. Ini kode yang sesuai:

```csharp
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
```

Pastikan untuk mengganti "pfxPassword" dengan kata sandi Anda yang sebenarnya dan "pfxFile" dengan jalur ke file PFX.

## Langkah 4: Menambahkan tanda tangan digital
Sekarang kita telah mengkonfigurasi tanda tangan digital, kita bisa menambahkannya ke buku kerja Excel. Ini kode yang sesuai:

```csharp
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
```

Langkah ini menambahkan tanda tangan digital Xades ke buku kerja Excel.

## Langkah 5: Menyimpan buku kerja dengan tanda tangan
Terakhir, kami menyimpan buku kerja Excel dengan tambahan tanda tangan digital. Ini kode yang sesuai:

```csharp
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
```

Pastikan untuk menyesuaikan nama file keluaran sesuai dengan kebutuhan Anda.

### Contoh kode sumber untuk Dukungan Tanda Tangan Xades menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
//Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
Workbook workbook = new Workbook(sourceDir + "sourceFile.xlsx");
string password = "pfxPassword";
string pfx = "pfxFile";
DigitalSignature signature = new DigitalSignature(File.ReadAllBytes(pfx), password, "testXAdES", DateTime.Now);
signature.XAdESType = XAdESType.XAdES;
DigitalSignatureCollection dsCollection = new DigitalSignatureCollection();
dsCollection.Add(signature);
workbook.SetDigitalSignature(dsCollection);
workbook.Save(outputDir + "XAdESSignatureSupport_out.xlsx");
Console.WriteLine("XAdESSignatureSupport executed successfully.");
```

## Kesimpulan
Selamat! Anda telah mempelajari cara menggunakan perpustakaan Aspose.Cells untuk .NET guna menambahkan tanda tangan digital Xades ke file Excel. Dengan mengikuti langkah-langkah yang disediakan dalam artikel ini, Anda akan dapat mengimplementasikan fungsi ini di proyek Anda sendiri. Jangan ragu untuk bereksperimen lebih banyak dengan perpustakaan dan temukan fitur canggih lainnya yang ditawarkannya.

### FAQ

#### Q: Apa itu Xades?

J: Xades adalah standar tanda tangan elektronik canggih yang digunakan untuk memastikan integritas dan keaslian dokumen digital.

#### T: Bisakah saya menggunakan tanda tangan digital jenis lain dengan Aspose.Cells?

J: Ya, Aspose.Cells juga mendukung jenis tanda tangan digital lainnya, seperti tanda tangan XMLDSig dan tanda tangan PKCS#7.

#### T: Bisakah saya menerapkan tanda tangan ke tipe file lain selain file Excel?
 
J: Ya, Aspose.Cells juga memungkinkan penerapan tanda tangan digital ke jenis file lain yang didukung seperti file Word, PDF, dan PowerPoint.