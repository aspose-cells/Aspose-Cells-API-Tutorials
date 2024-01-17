---
title: Kelola Ukuran Kertas Excel
linktitle: Kelola Ukuran Kertas Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengelola ukuran kertas di Excel dengan Aspose.Cells untuk .NET. Tutorial langkah demi langkah dengan kode sumber di C#.
type: docs
weight: 70
url: /id/net/excel-page-setup/manage-excel-paper-size/
---
Dalam tutorial ini, kami akan memandu Anda langkah demi langkah tentang cara mengatur ukuran kertas di dokumen Excel menggunakan Aspose.Cells untuk .NET. Kami akan menunjukkan cara mengonfigurasi ukuran kertas menggunakan kode sumber C#.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET di mesin Anda. Buat juga proyek baru di lingkungan pengembangan pilihan Anda.

## Langkah 2: Impor perpustakaan yang diperlukan

Dalam file kode Anda, impor pustaka yang diperlukan untuk bekerja dengan Aspose.Cells. Ini kode yang sesuai:

```csharp
using Aspose.Cells;
```

## Langkah 3: Atur Direktori Dokumen

Atur direktori tempat dokumen Excel yang ingin Anda kerjakan berada. Gunakan kode berikut untuk mengatur direktori:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Pastikan untuk menentukan jalur direktori lengkap.

## Langkah 4: Membuat Objek Buku Kerja

Objek Buku Kerja mewakili dokumen Excel yang akan Anda gunakan untuk bekerja. Anda dapat membuatnya menggunakan kode berikut:

```csharp
Workbook workbook = new Workbook();
```

Ini menciptakan objek Buku Kerja kosong yang baru.

## Langkah 5: Akses ke lembar kerja pertama

Untuk mengakses spreadsheet pertama dari dokumen Excel, gunakan kode berikut:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

Ini akan memungkinkan Anda untuk bekerja dengan lembar kerja pertama di buku kerja.

## Langkah 6: Pengaturan Ukuran Kertas

Gunakan properti PageSetup.PaperSize pada objek Lembar Kerja untuk mengatur ukuran kertas. Pada contoh ini, kita akan mengatur ukuran kertas menjadi A4. Ini kode yang sesuai:

```csharp
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
```

Ini mengatur ukuran kertas spreadsheet menjadi A4.

## Langkah 7: Menyimpan buku kerja

Untuk menyimpan perubahan pada buku kerja, gunakan metode Save() pada objek Buku Kerja. Ini kode yang sesuai:

```csharp
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```

Ini akan menyimpan buku kerja dengan perubahan pada direktori yang ditentukan.

### Contoh kode sumber untuk Kelola Ukuran Kertas Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Mengatur ukuran kertas menjadi A4
worksheet.PageSetup.PaperSize = PaperSizeType.PaperA4;
// Simpan Buku Kerja.
workbook.Save(dataDir + "ManagePaperSize_out.xls");
```
## Kesimpulan

Anda sekarang telah mempelajari cara mengatur ukuran kertas dalam dokumen Excel menggunakan Aspose.Cells untuk .NET. Tutorial ini memandu Anda melalui setiap langkah proses, mulai dari menyiapkan lingkungan hingga menyimpan perubahan. Anda sekarang dapat menggunakan pengetahuan ini untuk menyesuaikan ukuran kertas dokumen Excel Anda.

### FAQ

#### Q1: Bisakah saya mengatur ukuran kertas khusus selain A4?

A1: Ya, Aspose.Cells mendukung berbagai ukuran kertas yang telah ditentukan sebelumnya serta kemampuan untuk mengatur ukuran kertas khusus dengan menentukan dimensi yang diinginkan.

#### Q2: Bagaimana cara mengetahui ukuran kertas saat ini di dokumen Excel?

 A2: Anda dapat menggunakan`PageSetup.PaperSize` properti dari`Worksheet` objek untuk mendapatkan ukuran kertas yang disetel saat ini.

#### Q3: Apakah mungkin untuk mengatur margin halaman tambahan dengan ukuran kertas?

 A3: Ya, Anda bisa menggunakannya`PageSetup.LeftMargin`, `PageSetup.RightMargin`, `PageSetup.TopMargin` Dan`PageSetup.BottomMargin` properti untuk mengatur margin halaman tambahan selain ukuran kertas.

#### Q4: Apakah metode ini berfungsi untuk semua format file Excel, seperti .xls dan .xlsx?

A4: Ya, metode ini berfungsi untuk format file .xls dan .xlsx.

#### Q5: Bisakah saya menerapkan ukuran kertas berbeda ke lembar kerja berbeda di buku kerja yang sama?

 A5: Ya, Anda bisa menerapkan ukuran kertas berbeda ke lembar kerja berbeda di buku kerja yang sama dengan menggunakan`PageSetup.PaperSize` properti setiap lembar kerja.