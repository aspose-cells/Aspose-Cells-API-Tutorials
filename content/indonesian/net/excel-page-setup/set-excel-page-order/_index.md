---
title: Atur Urutan Halaman Excel
linktitle: Atur Urutan Halaman Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Panduan langkah demi langkah untuk mengatur urutan halaman di Excel menggunakan Aspose.Cells untuk .NET. Instruksi terperinci dan kode sumber disertakan.
type: docs
weight: 120
url: /id/net/excel-page-setup/set-excel-page-order/
---
Pada artikel ini, kami akan memandu Anda langkah demi langkah untuk menjelaskan kode sumber C# berikut untuk mengatur urutan halaman Excel menggunakan Aspose.Cells untuk .NET. Kami akan menunjukkan cara menyiapkan direktori dokumen, membuat instance objek Buku Kerja, mendapatkan referensi PageSetup, mengatur urutan pencetakan halaman, dan menyimpan buku kerja.

## Langkah 1: Pengaturan Direktori Dokumen

 Sebelum memulai, Anda perlu mengkonfigurasi direktori dokumen tempat Anda ingin menyimpan file Excel. Anda dapat menentukan jalur direktori dengan mengganti nilai`dataDir` variabel dengan jalur Anda sendiri.

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

## Langkah 2: Membuat Instansiasi Objek Buku Kerja

Langkah pertama adalah membuat instance objek Workbook. Ini mewakili buku kerja Excel yang akan kita kerjakan.

```csharp
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
```

## Langkah 3: Mendapatkan referensi PageSetup

Selanjutnya, kita perlu mendapatkan referensi objek PageSetup dari lembar kerja yang ingin kita atur urutan halamannya.

```csharp
// Dapatkan referensi PageSetup lembar kerja
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
```

## Langkah 4: Mengatur Urutan Cetak Halaman

Sekarang kita dapat mengatur urutan pencetakan halaman. Dalam contoh ini, kami menggunakan opsi "OverThenDown", yang berarti halaman akan dicetak dari kiri ke kanan, lalu dari atas ke bawah.

```csharp
// Atur urutan pencetakan halaman ke "OverThenDown"
pageSetup.Order = PrintOrderType.OverThenDown;
```

## Langkah 5: Menyimpan buku kerja

Terakhir, kami menyimpan buku kerja Excel dengan perubahan urutan halaman.

```csharp
// Simpan buku kerja
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

### Contoh kode sumber untuk Mengatur Urutan Halaman Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mendapatkan referensi PageSetup lembar kerja
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Mengatur urutan pencetakan halaman ke atas dan ke bawah
pageSetup.Order = PrintOrderType.OverThenDown;
// Simpan buku kerja.
workbook.Save(dataDir + "SetPageOrder_out.xls");
```

## Kesimpulan

Dalam tutorial ini, kami menjelaskan cara mengatur urutan halaman dalam file Excel menggunakan Aspose.Cells untuk .NET. Dengan mengikuti langkah-langkah yang disediakan, Anda bisa dengan mudah mengonfigurasi direktori dokumen, membuat instance objek Buku Kerja, mendapatkan referensi PageSetup, mengatur urutan pencetakan halaman, dan menyimpan buku kerja.

### FAQ

#### Q1: Mengapa penting untuk mengatur urutan halaman dalam file Excel?

Menentukan urutan halaman dalam file Excel penting karena menentukan bagaimana halaman akan dicetak atau ditampilkan. Dengan menentukan urutan tertentu, Anda dapat mengatur data secara logis dan membuat file lebih mudah dibaca atau dicetak.

#### Q2: Bisakah saya menggunakan pesanan pencetakan halaman lain dengan Aspose.Cells untuk .NET?

Ya, Aspose.Cells untuk .NET mendukung perintah pencetakan beberapa halaman seperti "DownThenOver", "OverThenDown", "DownThenOverThenDownAgain", dll. Anda dapat memilih salah satu yang paling sesuai dengan kebutuhan Anda.

#### Q3: Dapatkah saya mengatur opsi tambahan untuk mencetak halaman dengan Aspose.Cells untuk .NET?

Ya, Anda dapat mengatur berbagai opsi pencetakan halaman seperti skala, orientasi, margin, dll., menggunakan properti objek PageSetup di Aspose.Cells untuk .NET.

#### Q4: Apakah Aspose.Cells untuk .NET mendukung format file Excel lainnya?

Ya, Aspose.Cells untuk .NET mendukung berbagai format file Excel seperti XLSX, XLS, CSV, HTML, PDF, dll. Anda dapat dengan mudah mengkonversi antara format ini menggunakan fitur yang disediakan oleh perpustakaan.