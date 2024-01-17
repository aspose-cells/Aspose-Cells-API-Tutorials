---
title: Excel Menyalin Lembar Kerja Antar Buku Kerja
linktitle: Excel Menyalin Lembar Kerja Antar Buku Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Menyalin lembar kerja antar buku kerja Excel dengan mudah menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 30
url: /id/net/excel-copy-worksheet/excel-copy-worksheets-between-workbooks/
---
Dalam tutorial ini, kami akan memandu Anda melalui langkah-langkah untuk menyalin lembar kerja antar buku kerja Excel menggunakan perpustakaan Aspose.Cells untuk .NET. Ikuti petunjuk di bawah ini untuk menyelesaikan tugas ini.

## Langkah 1: Persiapan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET dan membuat proyek C# di lingkungan pengembangan terintegrasi (IDE) pilihan Anda.

## Langkah 2: Tetapkan jalur direktori dokumen

 Nyatakan a`dataDir` variabel dan inisialisasi dengan jalur ke direktori dokumen Anda. Misalnya :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENTS_DIRECTORY"` dengan jalur sebenarnya ke direktori Anda.

## Langkah 3: Tentukan jalur file masukan

 Nyatakan sebuah`InputPath` variabel dan inisialisasi dengan path lengkap file Excel tempat Anda ingin menyalin spreadsheet. Misalnya :

```csharp
string InputPath = dataDir + "book1.xls";
```

 Pastikan Anda memiliki file Excelnya`book1.xls` di direktori dokumen Anda atau tentukan nama file dan lokasi yang benar.

## Langkah 4: Buat buku kerja Excel pertama

 Menggunakan`Workbook` kelas Aspose.Cells untuk membuat buku kerja Excel pertama dan membuka file yang ditentukan:

```csharp
Workbook excelWorkbook0 = new Workbook(InputPath);
```

## Langkah 5: Buat buku kerja Excel kedua

Buat buku kerja Excel kedua:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Langkah 6: Salin lembar kerja dari buku kerja pertama ke buku kerja kedua

 Menggunakan`Copy`cara menyalin lembar kerja pertama dari buku kerja pertama ke buku kerja kedua:

```csharp
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
```

## Langkah 7: Simpan file Excel

Simpan file Excel yang berisi salinan spreadsheet:

```csharp
excelWorkbook1.Save(dataDir + "Copy WorksheetsBetweenWorkbooks_out.xls");
```

Pastikan untuk menentukan jalur dan nama file yang diinginkan untuk file keluaran.

### Contoh kode sumber untuk Excel Menyalin Lembar Kerja Antar Buku Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xls";
// Buat Buku Kerja.
// Buka file ke dalam buku pertama.
Workbook excelWorkbook0 = new Workbook(InputPath);
// Buat Buku Kerja lain.
Workbook excelWorkbook1 = new Workbook();
// Salin lembar pertama buku pertama ke buku kedua.
excelWorkbook1.Worksheets[0].Copy(excelWorkbook0.Worksheets[0]);
// Simpan berkasnya.
excelWorkbook1.Save(dataDir + "CopyWorksheetsBetweenWorkbooks_out.xls");
```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara menyalin lembar kerja antar buku kerja Excel menggunakan Aspose.Cells untuk .NET. Jangan ragu untuk menggunakan metode ini dalam proyek Anda sendiri untuk memanipulasi file Excel secara efisien.

### FAQ

#### T. Pustaka apa yang diperlukan untuk menggunakan Aspose.Cells untuk .NET?

A. Untuk menggunakan Aspose.Cells untuk .NET, Anda harus menyertakan perpustakaan Aspose.Cells dalam proyek Anda. Pastikan Anda telah mereferensikan perpustakaan ini dengan benar di lingkungan pengembangan terintegrasi (IDE) Anda.

#### T. Apakah Aspose.Cells mendukung format file Excel lainnya, seperti XLSX?

A. Ya, Aspose.Cells mendukung berbagai format file Excel termasuk XLSX, XLS, CSV, HTML, dan masih banyak lagi. Anda dapat memanipulasi format file ini menggunakan fitur Aspose.Cells untuk .NET.

#### T. Dapatkah saya menyesuaikan opsi tata letak saat menyalin spreadsheet?

A.  Ya, Anda dapat menyesuaikan opsi pengaturan halaman saat menyalin spreadsheet menggunakan properti`PageSetup` obyek. Anda dapat menentukan header halaman, footer, margin, orientasi, dll.