---
title: Tentukan Penulis Saat Menulis Melindungi Buku Kerja Excel
linktitle: Tentukan Penulis Saat Menulis Melindungi Buku Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memproteksi dan mengkustomisasi buku kerja Excel Anda menggunakan Aspose.Cells untuk .NET. Tutorial langkah demi langkah di C#.
type: docs
weight: 30
url: /id/net/excel-security/specify-author-while-write-protecting-excel-workbook/
---

Dalam tutorial ini, kami akan memperlihatkan kepada Anda cara menentukan penulis saat proteksi penulisan buku kerja Excel menggunakan pustaka Aspose.Cells untuk .NET.

## Langkah 1: Mempersiapkan lingkungan

Sebelum memulai, pastikan Anda telah menginstal Aspose.Cells for .NET di mesin Anda. Unduh perpustakaan dari situs resmi Aspose dan ikuti petunjuk instalasi yang disediakan.

## Langkah 2: Mengonfigurasi direktori sumber dan keluaran

Dalam kode sumber yang disediakan, Anda harus menentukan direktori sumber dan keluaran. Ubah`sourceDir` Dan`outputDir` variabel dengan mengganti "DIREKTORI SUMBER ANDA" dan "DIREKTORI OUTPUT ANDA" dengan jalur absolut masing-masing pada mesin Anda.

```csharp
// Direktori sumber
string sourceDir = "PATH TO YOUR SOURCE DIRECTORY";

// Direktori keluaran
string outputDir = "YOUR OUTPUT DIRECTORY PATH";
```

## Langkah 3: Membuat buku kerja Excel kosong

Untuk memulai, kita membuat objek Buku Kerja yang mewakili buku kerja Excel kosong.

```csharp
// Buat buku kerja kosong.
Workbook wb = new Workbook();
```

## Langkah 4: Tulis proteksi dengan kata sandi

 Selanjutnya, kami menentukan kata sandi untuk menulis proteksi buku kerja Excel menggunakan`WriteProtection.Password` milik objek Buku Kerja.

```csharp
// Tulis proteksi buku kerja dengan kata sandi.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";
```

## Langkah 5: Spesifikasi penulis

 Sekarang kita tentukan penulis buku kerja Excel menggunakan`WriteProtection.Author` milik objek Buku Kerja.

```csharp
// Tentukan penulis saat menulis buku kerja pelindung.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";
```

## Langkah 6: Cadangkan Buku Kerja Excel yang Dilindungi

 Setelah perlindungan penulisan dan pembuatnya ditentukan, kita dapat menyimpan buku kerja Excel dalam format XLSX menggunakan`Save()` metode.

```csharp
// Simpan buku kerja dalam format XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");
```

### Contoh kode sumber untuk Tentukan Penulis Saat Menulis Melindungi Buku Kerja Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Direktori sumber
string sourceDir = "YOUR SOURCE DIRECTORY";

//Direktori keluaran
string outputDir = "YOUR OUTPUT DIRECTORY";

// Buat buku kerja kosong.
Workbook wb = new Workbook();

// Tulis proteksi buku kerja dengan kata sandi.
wb.Settings.WriteProtection.Password = "YOUR_PASSWORD";

// Tentukan penulis saat menulis buku kerja pelindung.
wb.Settings.WriteProtection.Author = "YOUR_AUTHOR";

// Simpan buku kerja dalam format XLSX.
wb.Save(outputDir + "outputSpecifyAuthorWhileWriteProtectingWorkbook.xlsx");

```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara menentukan penulis saat proteksi penulisan buku kerja Excel dengan Aspose.Cells untuk .NET. Anda bisa menerapkan langkah-langkah ini ke proyek Anda sendiri untuk melindungi dan mengkustomisasi buku kerja Excel Anda.

Jangan ragu untuk menjelajahi lebih jauh fitur Aspose.Cells untuk .NET untuk pengoperasian lebih lanjut pada file Excel.

## FAQ

#### T: Bisakah saya menulis proteksi buku kerja Excel tanpa menentukan kata sandi?

 A: Ya, Anda bisa menggunakan objek Workbook`WriteProtect()` metode tanpa menentukan kata sandi untuk melindungi buku kerja Excel. Ini akan membatasi perubahan pada buku kerja tanpa memerlukan kata sandi.

#### T: Bagaimana cara menghapus proteksi penulisan dari buku kerja Excel?

 J: Untuk menghapus proteksi penulisan dari buku kerja Excel, Anda bisa menggunakan`Unprotect()` metode objek Lembar Kerja atau`RemoveWriteProtection()` metode objek Buku Kerja, bergantung pada kasus penggunaan spesifik Anda. .

#### T: Saya lupa kata sandi untuk melindungi buku kerja Excel saya. Apa yang bisa saya lakukan ?

J: Jika Anda lupa kata sandi untuk melindungi buku kerja Excel Anda, Anda tidak bisa menghapusnya secara langsung. Namun, Anda dapat mencoba menggunakan alat pihak ketiga khusus yang menyediakan fitur pemulihan kata sandi untuk file Excel yang dilindungi.

#### T: Apakah mungkin untuk menentukan beberapa penulis saat memproteksi buku kerja Excel?

J: Tidak, pustaka Aspose.Cells untuk .NET memungkinkan penentuan satu penulis saat proteksi penulisan buku kerja Excel. Jika Anda ingin menentukan beberapa penulis, Anda perlu mempertimbangkan solusi khusus dengan memanipulasi file Excel secara langsung.