---
title: Lembar Kerja Pemindahan Excel
linktitle: Lembar Kerja Pemindahan Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pindahkan lembar kerja ke buku kerja Excel dengan mudah menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 40
url: /id/net/excel-copy-worksheet/excel-move-worksheet/
---
Dalam tutorial ini, kami akan memandu Anda melalui langkah-langkah untuk memindahkan lembar kerja ke buku kerja Excel menggunakan perpustakaan Aspose.Cells untuk .NET. Ikuti petunjuk di bawah ini untuk menyelesaikan tugas ini.


## Langkah 1: Persiapan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET dan membuat proyek C# di lingkungan pengembangan terintegrasi (IDE) pilihan Anda.

## Langkah 2: Tetapkan jalur direktori dokumen

 Nyatakan a`dataDir` variabel dan inisialisasi dengan jalur ke direktori dokumen Anda. Misalnya :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENTS_DIRECTORY"` dengan jalur sebenarnya ke direktori Anda.

## Langkah 3: Tentukan jalur file masukan

 Nyatakan sebuah`InputPath` variabel dan inisialisasi dengan path lengkap file Excel yang ada yang ingin Anda modifikasi. Misalnya :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Pastikan Anda memiliki file Excelnya`book1.xls` di direktori dokumen Anda atau tentukan nama file dan lokasi yang benar.

## Langkah 4: Buka file Excelnya

 Menggunakan`Workbook` kelas Aspose.Cells untuk membuka file Excel yang ditentukan:

```csharp
Workbook wb = new Workbook(InputPath);
```

## Langkah 5: Dapatkan koleksi spreadsheet

 Membuat`WorksheetCollection` objek untuk merujuk ke lembar kerja di buku kerja:

```csharp
WorksheetCollection sheets = wb.Worksheets;
```

## Langkah 6: Dapatkan lembar kerja pertama

Dapatkan lembar kerja pertama di buku kerja:

```csharp
Worksheet worksheet = sheets[0];
```

## Langkah 7: Pindahkan lembar kerja

 Menggunakan`MoveTo` cara memindahkan lembar kerja pertama ke posisi ketiga di buku kerja:

```csharp
worksheet.MoveTo(2);
```

## Langkah 8: Simpan file Excel yang dimodifikasi

Simpan file Excel dengan lembar kerja yang dipindahkan:

```csharp
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

Pastikan untuk menentukan jalur dan nama file yang diinginkan untuk file keluaran.

### Contoh kode sumber untuk Excel Pindahkan Lembar Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Buka file excel yang ada.
Workbook wb = new Workbook(InputPath);
// Buat objek Lembar Kerja dengan referensi ke
// lembar Buku Kerja.
WorksheetCollection sheets = wb.Worksheets;
// Dapatkan lembar kerja pertama.
Worksheet worksheet = sheets[0];
// Pindahkan lembar pertama ke posisi ketiga di buku kerja.
worksheet.MoveTo(2);
// Simpan file excelnya.
wb.Save(dataDir + "MoveWorksheet_out.xls");
```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara memindahkan lembar kerja ke buku kerja Excel menggunakan Aspose.Cells untuk .NET. Jangan ragu untuk menggunakan metode ini dalam proyek Anda sendiri untuk memanipulasi file Excel secara efisien.

### FAQ

#### Q. Bisakah saya memindahkan lembar kerja ke posisi lain di buku kerja Excel yang sama?

A.  Ya, Anda bisa memindahkan lembar kerja ke posisi lain di buku kerja Excel yang sama menggunakan`MoveTo` metode objek Lembar Kerja. Cukup tentukan indeks posisi tujuan di buku kerja.

#### Q. Bisakah saya memindahkan lembar kerja ke buku kerja Excel lainnya?

A.  Ya, Anda bisa memindahkan lembar kerja ke buku kerja Excel lain menggunakan`MoveTo` metode objek Lembar Kerja. Cukup tentukan indeks posisi tujuan di buku kerja target.

#### T. Apakah kode sumber yang diberikan dapat digunakan dengan format file Excel lainnya, seperti XLSX?

A. Ya, kode sumber yang disediakan dapat digunakan dengan format file Excel lainnya, termasuk XLSX. Aspose.Cells untuk .NET mendukung berbagai format file Excel, memungkinkan Anda memanipulasi dan memindahkan lembar kerja ke jenis file yang berbeda.

#### T. Bagaimana cara menentukan jalur dan nama file keluaran saat menyimpan file Excel yang dimodifikasi?

A.  Saat menyimpan file Excel yang dimodifikasi, gunakan`Save` metode objek Buku Kerja yang menentukan jalur lengkap dan nama file keluaran. Pastikan untuk menentukan ekstensi file yang sesuai, seperti`.xls` atau`.xlsx`, tergantung pada format file yang diinginkan.