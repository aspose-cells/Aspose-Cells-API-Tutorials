---
title: Atur Opsi Cetak Excel
linktitle: Atur Opsi Cetak Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memanipulasi file Excel dan menyesuaikan opsi pencetakan dengan mudah menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 150
url: /id/net/excel-page-setup/set-excel-print-options/
---
Dalam panduan ini, kami akan memandu Anda tentang cara mengatur opsi pencetakan untuk buku kerja Excel menggunakan Aspose.Cells untuk .NET. Kami akan memandu Anda langkah demi langkah melalui kode sumber C# yang disediakan untuk menyelesaikan tugas ini.

## Langkah 1: Menyiapkan lingkungan

Sebelum memulai, pastikan Anda telah menyiapkan lingkungan pengembangan dan menginstal Aspose.Cells untuk .NET. Anda dapat mengunduh perpustakaan versi terbaru dari situs resmi Aspose.

## Langkah 2: Impor namespace yang diperlukan

Dalam proyek C# Anda, impor namespace yang diperlukan untuk bekerja dengan Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Langkah 3: Mengatur jalur ke direktori dokumen

 Nyatakan a`dataDir` variabel untuk menentukan jalur ke direktori tempat Anda ingin menyimpan file Excel yang dihasilkan:

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENT_DIRECTORY"` dengan jalur yang benar di sistem Anda.

## Langkah 4: Membuat Objek Buku Kerja

Buat instance objek Buku Kerja yang mewakili buku kerja Excel yang ingin Anda buat:

```csharp
Workbook workbook = new Workbook();
```

## Langkah 5: Mendapatkan referensi PageSetup pada lembar kerja

Untuk mengatur opsi pencetakan, pertama-tama kita perlu mendapatkan referensi PageSetup dari lembar kerja. Gunakan kode berikut untuk mendapatkan referensi:

```csharp
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Langkah 6: Aktifkan Pencetakan Garis Kisi

Untuk mengaktifkan garis kisi untuk dicetak, gunakan kode berikut:

```csharp
pageSetup. PrintGridlines = true;
```

## Langkah 7: Aktifkan Pencetakan Header Baris/Kolom

Untuk mengaktifkan pencetakan header baris dan kolom, gunakan kode berikut:

```csharp
pageSetup.PrintHeadings = true;
```

## Langkah 8: Mengaktifkan Mode Cetak Hitam Putih

Untuk mengaktifkan pencetakan lembar kerja dalam mode hitam putih, gunakan kode berikut:

```csharp
pageSetup.BlackAndWhite = true;
```

## Langkah 9: Mengaktifkan Pencetakan Umpan Balik

Untuk mengizinkan komentar dicetak seperti yang muncul di spreadsheet, gunakan kode berikut:

```csharp
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
```

## Langkah 10: Aktifkan Pencetakan Mode Draf

Untuk mengaktifkan pencetakan spreadsheet dalam mode draf, gunakan kode berikut:

```csharp
pageSetup.PrintDraft = true;
```

## Langkah 11: Aktifkan Kesalahan Sel Pencetakan sebagai N/A

Untuk mengizinkan kesalahan sel dicetak sebagai

  daripada N/A, gunakan kode berikut:

```csharp
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
```

## Langkah 12: Menyimpan buku kerja Excel

 Untuk menyimpan buku kerja Excel dengan kumpulan opsi pencetakan, gunakan`Save` metode objek Buku Kerja:

```csharp
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```

Ini akan menyimpan buku kerja Excel dengan nama file "OtherPrintOptions_out.xls" di direktori yang ditentukan.

### Contoh kode sumber untuk Mengatur Opsi Cetak Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mendapatkan referensi PageSetup lembar kerja
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Memungkinkan untuk mencetak garis kisi
pageSetup.PrintGridlines = true;
// Memungkinkan untuk mencetak judul baris/kolom
pageSetup.PrintHeadings = true;
// Memungkinkan untuk mencetak lembar kerja dalam mode hitam putih
pageSetup.BlackAndWhite = true;
// Memungkinkan untuk mencetak komentar seperti yang ditampilkan pada lembar kerja
pageSetup.PrintComments = PrintCommentsType.PrintInPlace;
// Memungkinkan untuk mencetak lembar kerja dengan kualitas draft
pageSetup.PrintDraft = true;
// Mengizinkan mencetak kesalahan sel sebagai N/A
pageSetup.PrintErrors = PrintErrorsType.PrintErrorsNA;
// Simpan buku kerja.
workbook.Save(dataDir + "OtherPrintOptions_out.xls");
```
## Kesimpulan

Anda sekarang telah mempelajari cara mengatur opsi pencetakan untuk buku kerja Excel menggunakan Aspose.Cells untuk .NET. Pustaka yang kuat dan ramah pengguna ini memungkinkan Anda untuk menyesuaikan pengaturan pencetakan buku kerja Excel Anda dengan cara yang mudah dan efisien.

### FAQ


#### 1. Dapatkah saya menyesuaikan opsi pencetakan lebih lanjut, seperti margin atau orientasi halaman?

Ya, Aspose.Cells untuk .NET menawarkan beragam opsi pencetakan yang dapat disesuaikan, seperti margin, orientasi halaman, skala, dll.

#### 2. Apakah Aspose.Cells untuk .NET mendukung format file Excel lainnya?

Ya, Aspose.Cells untuk .NET mendukung berbagai format file Excel, seperti XLSX, XLS, CSV, HTML, PDF, dll.

#### 3. Apakah Aspose.Cells for .NET kompatibel dengan semua versi .NET Framework?

Aspose.Cells untuk .NET kompatibel dengan .NET Framework 2.0 atau lebih baru, termasuk versi 3.5, 4.0, 4.5, 4.6, dll.