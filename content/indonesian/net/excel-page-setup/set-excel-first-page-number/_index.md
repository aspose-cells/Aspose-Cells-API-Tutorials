---
title: Tetapkan Nomor Halaman Pertama Excel
linktitle: Tetapkan Nomor Halaman Pertama Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengatur nomor halaman pertama di Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 90
url: /id/net/excel-page-setup/set-excel-first-page-number/
---
Dalam tutorial ini, kami akan memandu Anda tentang cara mengatur nomor halaman pertama di Excel menggunakan Aspose.Cells untuk .NET. Kami akan menggunakan kode sumber C# untuk mengilustrasikan prosesnya.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET di mesin Anda. Buat juga proyek baru di lingkungan pengembangan pilihan Anda.

## Langkah 2: Impor perpustakaan yang diperlukan

Dalam file kode Anda, impor pustaka yang diperlukan untuk bekerja dengan Aspose.Cells. Ini kode yang sesuai:

```csharp
using Aspose.Cells;
```

## Langkah 3: Tetapkan Direktori Data

Tetapkan direktori data tempat Anda ingin menyimpan file Excel yang dimodifikasi. Gunakan kode berikut:

```csharp
string dataDir = "YOUR DATA DIRECTORY";
```

Pastikan untuk menentukan jalur direktori lengkap.

## Langkah 4: Membuat buku kerja dan lembar kerja

Buat objek Buku Kerja baru dan navigasikan ke lembar kerja pertama di buku kerja menggunakan kode berikut:

```csharp
Workbook workbook = new Workbook();
Worksheet worksheet = workbook.Worksheets[0];
```

Ini akan membuat buku kerja kosong dengan lembar kerja.

## Langkah 5: Mengatur nomor halaman pertama

Atur nomor halaman pertama halaman lembar kerja menggunakan kode berikut:

```csharp
worksheet.PageSetup.FirstPageNumber = 2;
```

Ini akan mengatur nomor halaman pertama menjadi 2.

## Langkah 6: Menyimpan Buku Kerja yang Dimodifikasi

Simpan buku kerja yang dimodifikasi menggunakan kode berikut:

```csharp
workbook.Save(dataDir + "OutputFileName.xls");
```

Ini akan menyimpan buku kerja yang dimodifikasi ke direktori data yang ditentukan.

### Contoh kode sumber untuk Menetapkan Nomor Halaman Pertama Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Mengatur nomor halaman pertama pada halaman lembar kerja
worksheet.PageSetup.FirstPageNumber = 2;
// Simpan Buku Kerja.
workbook.Save(dataDir + "SetFirstPageNumber_out.xls");
```

## Kesimpulan

Anda sekarang telah mempelajari cara mengatur nomor halaman pertama di Excel menggunakan Aspose.Cells untuk .NET. Tutorial ini memandu Anda melalui setiap langkah proses, mulai dari menyiapkan lingkungan hingga menyetel nomor halaman pertama. Anda sekarang dapat menggunakan pengetahuan ini untuk menyesuaikan penomoran halaman di file Excel Anda.

### FAQ

#### Q1: Dapatkah saya menetapkan nomor halaman pertama yang berbeda untuk setiap lembar kerja?

 A1: Ya, Anda dapat mengatur nomor halaman pertama yang berbeda untuk setiap lembar kerja dengan mengakses`FirstPageNumber`milik masing-masing lembar kerja`PageSetup` obyek.

#### Q2: Bagaimana cara memeriksa nomor halaman pertama dari spreadsheet yang ada?

 A2: Anda dapat memeriksa nomor halaman pertama dari lembar kerja yang ada dengan mengakses`FirstPageNumber` properti dari`PageSetup` objek yang sesuai dengan lembar kerja itu.

#### Q3: Apakah penomoran halaman selalu dimulai dari 1 secara default?

A3: Ya, penomoran halaman dimulai dari 1 secara default di Excel. Namun, Anda dapat menggunakan kode yang ditunjukkan dalam tutorial ini untuk menyetel nomor halaman pertama yang berbeda.

#### Q4: Apakah perubahan nomor halaman pertama bersifat permanen pada file Excel yang diedit?

A4: Ya, perubahan yang dilakukan pada nomor halaman pertama disimpan secara permanen di file Excel yang dimodifikasi.

#### Q5: Apakah metode ini berfungsi untuk semua format file Excel, seperti .xls dan .xlsx?

A5: Ya, metode ini berfungsi untuk semua format file Excel yang didukung oleh Aspose.Cells, termasuk .xls dan .xlsx.