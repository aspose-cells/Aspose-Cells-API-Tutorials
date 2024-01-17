---
title: Lembar Kerja Salin Excel
linktitle: Lembar Kerja Salin Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Salin satu lembar kerja Excel ke lembar kerja lainnya dengan Aspose.Cells untuk .NET.
type: docs
weight: 20
url: /id/net/excel-copy-worksheet/excel-copy-worksheet/
---

Dalam panduan ini, kami akan menjelaskan cara menyalin lembar kerja Excel menggunakan perpustakaan Aspose.Cells untuk .NET. Kami akan memberi Anda kode sumber C# dan memandu Anda melalui langkah-langkah yang diperlukan untuk menyelesaikan tugas ini. Pada akhirnya, kami akan menunjukkan kepada Anda hasil yang diharapkan. Ikuti petunjuk di bawah ini untuk memulai.

## Langkah 1: Persiapan

Sebelum memulai, pastikan Anda telah menginstal Aspose.Cells untuk .NET dan membuat proyek C# di lingkungan pengembangan terintegrasi (IDE) pilihan Anda. Pastikan juga Anda memiliki salinan file Excel yang ingin Anda manipulasi.

## Langkah 2: Impor perpustakaan yang diperlukan

 Di file sumber C# Anda, impor pustaka yang diperlukan dari Aspose.Cells menggunakan`using` pengarahan:

```csharp
using Aspose.Cells;
```

## Langkah 3: Tetapkan jalur file

 Nyatakan a`dataDir` variabel dan inisialisasi dengan direktori yang berisi file Excel Anda. Misalnya :

```csharp
string dataDir = "PATH_TO_YOUR_DOCUMENT_DIRECTORY";
```

 Pastikan untuk mengganti`"PATH_TO_YOUR_DOCUMENT_DIRECTORY"` dengan jalur sebenarnya ke direktori Anda.

## Langkah 4: Muat file Excel yang ada

 Menggunakan`Workbook` kelas dari Aspose.Cells untuk membuka file Excel yang ada. Menggunakan`InputPath` variabel untuk menentukan jalur file:

```csharp
string InputPath = dataDir + "book1.xls";
Workbook wb = new Workbook(InputPath);
```

 Pastikan Anda sudah menggantinya`"book1.xls"` dengan nama sebenarnya file Excel Anda.

## Langkah 5: Salin lembar kerja

 Sekarang kita akan menyalin lembar kerja yang ada ke lembar kerja baru. Menggunakan`Worksheets` properti dari`Workbook` objek untuk mengakses koleksi lembar kerja:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

 Kemudian gunakan`AddCopy` metode untuk menyalin lembar kerja yang ditentukan. Misalnya, untuk menyalin "Sheet1":

```csharp
sheets.AddCopy("Sheet1");
```

## Langkah 6: Simpan file Excel

 Menggunakan`Save` metode`Workbook` objek untuk menyimpan perubahan ke file baru:

```csharp
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

Pastikan untuk menentukan jalur dan nama file yang diinginkan untuk file keluaran.

### Contoh kode sumber untuk Lembar Kerja Salin Excel menggunakan Aspose.Cells untuk .NET 

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Buka file Excel yang ada.
Workbook wb = new Workbook(InputPath);
// Buat objek Lembar Kerja dengan referensi ke
// lembar Buku Kerja.
WorksheetCollection sheets = wb.Worksheets;
// Salin data ke lembar baru dari yang sudah ada
// lembar dalam Buku Kerja.
sheets.AddCopy("Sheet1");
// Simpan file Excelnya.
wb.Save(dataDir + "CopyWithinWorkbook_out.xls");
```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara menyalin lembar kerja Excel menggunakan Aspose.Cells untuk .NET. Panduan langkah demi langkah ini menunjukkan cara mengimpor perpustakaan yang diperlukan, memuat file Excel yang ada, menyalin lembar kerja dan menyimpan file yang dimodifikasi. Jangan ragu untuk menggunakan metode ini dalam proyek Anda sendiri untuk memanipulasi file Excel secara efisien.

### FAQ

#### Q. Apakah Aspose.Cells kompatibel dengan bahasa pemrograman lain?

A. Ya, Aspose.Cells mendukung berbagai bahasa pemrograman termasuk C#, Java, Python, dan banyak lagi.

#### T. Bisakah saya menyalin lembar kerja ke buku kerja Excel lainnya?

A.  Ya, Anda dapat menggunakan`AddCopy` metode untuk menyalin lembar kerja ke buku kerja Excel lain.

#### T. Apakah Aspose.Cells mempertahankan rumus dan pemformatan saat menyalin lembar kerja?

A. Ya, Aspose.Cells mempertahankan rumus, pemformatan, dan properti lainnya saat menyalin lembar kerja.

#### T. Apakah Aspose.Cells memerlukan lisensi untuk penggunaan komersial?

A. Ya, Aspose.Cells adalah produk komersial dan memerlukan pembelian lisensi untuk penggunaan komersial. Anda dapat menemukan informasi lisensi lebih lanjut di situs resmi Aspose.