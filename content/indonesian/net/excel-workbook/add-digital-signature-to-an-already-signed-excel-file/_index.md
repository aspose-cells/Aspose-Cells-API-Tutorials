---
title: Tambahkan Tanda Tangan Digital ke File Excel yang Sudah Ditandatangani
linktitle: Tambahkan Tanda Tangan Digital ke File Excel yang Sudah Ditandatangani
second_title: Aspose.Cells untuk Referensi .NET API
description: Tambahkan tanda tangan digital dengan mudah ke file Excel yang ada dengan Aspose.Cells untuk .NET.
type: docs
weight: 30
url: /id/net/excel-workbook/add-digital-signature-to-an-already-signed-excel-file/
---
Dalam panduan langkah demi langkah ini, kami akan menjelaskan kode sumber C# yang disediakan yang memungkinkan Anda menambahkan tanda tangan digital ke file Excel yang sudah ditandatangani menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk menambahkan tanda tangan digital baru ke file Excel yang sudah ada.

## Langkah 1: Tetapkan direktori sumber dan keluaran

```csharp
// direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();

// Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
```

Pada langkah pertama ini, kita menentukan direktori sumber dan keluaran yang akan digunakan untuk memuat file Excel yang ada dan menyimpan file dengan tanda tangan digital baru.

## Langkah 2: Muat file Excel yang ada

```csharp
// Muat buku kerja Excel yang sudah ditandatangani
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
```

 Di sini kita memuat file Excel yang sudah ditandatangani menggunakan`Workbook` kelas Aspose.Cells.

## Langkah 3: Buat kumpulan tanda tangan digital

```csharp
// Buat koleksi tanda tangan digital
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
```

 Kami membuat koleksi tanda tangan digital baru menggunakan`DigitalSignatureCollection` kelas.

## Langkah 4: Buat sertifikat baru

```csharp
// Buat sertifikat baru
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
```

Di sini kita membuat sertifikat baru dari file dan kata sandi yang disediakan.

## Langkah 5: Tambahkan tanda tangan digital baru ke koleksi

```csharp
// Buat tanda tangan digital baru
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added a new digital signature to the already signed workbook.", DateTime.Now);

// Tambahkan tanda tangan digital ke koleksi
dsCollection.Add(signature);
```

 Kami membuat tanda tangan digital baru menggunakan`DigitalSignature` kelas dan menambahkannya ke koleksi tanda tangan digital.

## Langkah 6: Tambahkan koleksi tanda tangan digital ke buku kerja

```csharp
//Tambahkan koleksi tanda tangan digital ke buku kerja
workbook.AddDigitalSignature(dsCollection);
```

 Kami menambahkan koleksi tanda tangan digital ke buku kerja Excel yang ada menggunakan`AddDigitalSignature()` metode.

## Langkah 7: Simpan dan tutup buku kerja

```csharp
// Simpan buku kerja dan tutup
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
```

Kami menyimpan buku kerja dengan tanda tangan digital baru ke direktori keluaran yang ditentukan, lalu menutupnya dan melepaskan sumber daya terkait.

### Contoh kode sumber untuk Menambahkan Tanda Tangan Digital Ke File Excel yang Sudah Ditandatangani menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = RunExamples.Get_SourceDirectory();
//Direktori keluaran
string outputDir = RunExamples.Get_OutputDirectory();
//File sertifikat dan kata sandinya
string certFileName = sourceDir + "AsposeDemo.pfx";
string password = "aspose";
//Muat buku kerja yang sudah ditandatangani secara digital untuk menambahkan tanda tangan digital baru
Aspose.Cells.Workbook workbook = new Aspose.Cells.Workbook(sourceDir + "sampleDigitallySignedByCells.xlsx");
//Buat koleksi tanda tangan digital
Aspose.Cells.DigitalSignatures.DigitalSignatureCollection dsCollection = new Aspose.Cells.DigitalSignatures.DigitalSignatureCollection();
//Buat sertifikat baru
System.Security.Cryptography.X509Certificates.X509Certificate2 certificate = new System.Security.Cryptography.X509Certificates.X509Certificate2(certFileName, password);
//Buat tanda tangan digital baru dan tambahkan dalam koleksi tanda tangan digital
Aspose.Cells.DigitalSignatures.DigitalSignature signature = new Aspose.Cells.DigitalSignatures.DigitalSignature(certificate, "Aspose.Cells added new digital signature in existing digitally signed workbook.", DateTime.Now);
dsCollection.Add(signature);
//Tambahkan koleksi tanda tangan digital di dalam buku kerja
workbook.AddDigitalSignature(dsCollection);
//Simpan buku kerja dan buang.
workbook.Save(outputDir + "outputDigitallySignedByCells.xlsx");
workbook.Dispose();
Console.WriteLine("AddDigitalSignatureToAnAlreadySignedExcelFile executed successfully.\r\n");
```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara menambahkan tanda tangan digital ke file Excel yang sudah ditandatangani menggunakan Aspose.Cells untuk .NET. Tanda tangan digital menambahkan lapisan keamanan ekstra pada file Excel Anda, memastikan keaslian dan integritasnya.

### FAQ

#### T: Apa itu Aspose.Cells untuk .NET?

J: Aspose.Cells for .NET adalah perpustakaan kelas canggih yang memungkinkan pengembang .NET membuat, memodifikasi, mengonversi, dan memanipulasi file Excel dengan mudah.

#### T: Apa yang dimaksud dengan tanda tangan digital dalam file Excel?

J: Tanda tangan digital pada file Excel adalah tanda elektronik yang menjamin keaslian, integritas, dan asal dokumen. Ini digunakan untuk memverifikasi bahwa file tersebut belum diubah sejak ditandatangani dan berasal dari sumber yang dapat dipercaya.

#### T: Apa keuntungan menambahkan tanda tangan digital ke file Excel?

J: Menambahkan tanda tangan digital ke file Excel memberikan beberapa manfaat, termasuk perlindungan terhadap perubahan yang tidak sah, memastikan integritas data, mengautentikasi penulis dokumen, dan memberikan kepercayaan terhadap informasi yang dikandungnya.

#### T: Bisakah saya menambahkan beberapa tanda tangan digital ke file Excel?

J: Ya, Aspose.Cells memungkinkan Anda menambahkan beberapa tanda tangan digital ke file Excel. Anda dapat membuat kumpulan tanda tangan digital dan menambahkannya ke file dalam satu operasi.

#### T: Apa saja persyaratan untuk menambahkan tanda tangan digital ke file Excel?

J: Untuk menambahkan tanda tangan digital ke file Excel, Anda memerlukan sertifikat digital valid yang akan digunakan untuk menandatangani dokumen. Pastikan Anda memiliki sertifikat dan kata sandi yang benar sebelum menambahkan tanda tangan digital.