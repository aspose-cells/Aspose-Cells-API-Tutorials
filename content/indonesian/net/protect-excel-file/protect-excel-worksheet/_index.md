---
title: Lindungi Lembar Kerja Excel
linktitle: Lindungi Lembar Kerja Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Temukan dalam tutorial ini cara melindungi spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Panduan langkah demi langkah di C#.
type: docs
weight: 50
url: /id/net/protect-excel-file/protect-excel-worksheet/
---
Dalam tutorial ini, kita akan melihat beberapa kode sumber C# yang menggunakan perpustakaan Aspose.Cells untuk melindungi spreadsheet Excel. Kami akan memandu setiap langkah kode dan menjelaskan cara kerjanya. Pastikan untuk mengikuti instruksi dengan seksama untuk mendapatkan hasil yang diinginkan.

## Langkah 1: Prasyarat

Sebelum memulai, pastikan Anda telah menginstal perpustakaan Aspose.Cells untuk .NET. Anda bisa mendapatkannya dari situs resmi Aspose. Pastikan juga Anda memiliki versi terbaru Visual Studio atau lingkungan pengembangan C# lainnya.

## Langkah 2: Impor namespace yang diperlukan

Untuk menggunakan perpustakaan Aspose.Cells, kita perlu mengimpor namespace yang diperlukan ke dalam kode kita. Tambahkan baris berikut ke bagian atas file sumber C# Anda:

```csharp
using Aspose.Cells;
using System.IO;
```

## Langkah 3: Muat file Excel

Pada langkah ini, kita akan memuat file Excel yang ingin kita proteksi. Pastikan untuk menentukan jalur yang benar ke direktori yang berisi file Excel. Gunakan kode berikut untuk mengunggah file:

```csharp
// Jalur ke direktori dokumen.
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Buat aliran file yang berisi file Excel untuk dibuka.
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);

// Membuat instance objek Buku Kerja.
//Buka file Excel melalui aliran file.
Workbook excel = new Workbook(fstream);
```

 Pastikan untuk mengganti`"YOUR_DOCUMENTS_DIR"` dengan jalur yang sesuai ke direktori dokumen Anda.

## Langkah 4: Akses spreadsheet

Sekarang kita telah memuat file Excel, kita dapat mengakses lembar kerja pertama. Gunakan kode berikut untuk mengakses lembar kerja pertama:

```csharp
// Akses ke lembar kerja pertama di file Excel.
Worksheet worksheet = excel.Worksheets[0];
```

## Langkah 5: Lindungi lembar kerja

Pada langkah ini, kami akan melindungi spreadsheet menggunakan kata sandi. Gunakan kode berikut untuk melindungi spreadsheet:

```csharp
// Lindungi lembar kerja dengan kata sandi.
worksheet.Protect(ProtectionType.All, "YOUR_PASSWORD", null);
```

 Mengganti`"YOUR_PASSWORD"` dengan kata sandi yang ingin Anda gunakan untuk melindungi spreadsheet.

## Langkah 6: Simpan File Excel yang Dimodifikasi Sekarang kita telah memproteksinya

é spreadsheet, kami akan menyimpan file Excel yang dimodifikasi dalam format default. Gunakan kode berikut untuk menyimpan file Excel:

```csharp
// Simpan file Excel yang dimodifikasi dalam format default.
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
```

Pastikan untuk menentukan jalur yang benar untuk menyimpan file Excel yang dimodifikasi.

## Langkah 7: Tutup Aliran File

Untuk melepaskan semua sumber daya, kita perlu menutup aliran file yang digunakan untuk memuat file Excel. Gunakan kode berikut untuk menutup aliran file:

```csharp
// Tutup aliran file untuk melepaskan semua sumber daya.
fstream.Close();
```

Pastikan untuk menyertakan langkah ini di akhir kode Anda.


### Contoh kode sumber untuk Lindungi Lembar Kerja Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Membuat instance objek Buku Kerja
// Membuka file Excel melalui aliran file
Workbook excel = new Workbook(fstream);
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = excel.Worksheets[0];
// Melindungi lembar kerja dengan kata sandi
worksheet.Protect(ProtectionType.All, "aspose", null);
// Menyimpan file Excel yang dimodifikasi dalam format default
excel.Save(dataDir + "output.out.xls", SaveFormat.Excel97To2003);
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Selamat! Anda sekarang memiliki kode sumber C# yang memungkinkan Anda melindungi spreadsheet Excel menggunakan perpustakaan Aspose.Cells untuk .NET. Pastikan untuk mengikuti langkah-langkahnya dengan cermat dan sesuaikan kode dengan kebutuhan spesifik Anda.

### FAQ (Pertanyaan yang Sering Diajukan)

#### Apakah mungkin untuk memproteksi banyak lembar kerja dalam satu file Excel?

J: Ya, Anda bisa memproteksi beberapa lembar kerja dalam satu file Excel dengan mengulangi langkah 4-6 untuk setiap lembar kerja.

#### Bagaimana cara menentukan izin khusus untuk pengguna yang berwenang?

 J: Anda dapat menggunakan opsi tambahan yang disediakan oleh`Protect`metode untuk menentukan izin khusus untuk pengguna yang berwenang. Lihat dokumentasi Aspose.Cells untuk informasi lebih lanjut.

#### Bisakah saya melindungi file Excel itu sendiri dengan kata sandi?

J: Ya, Anda dapat melindungi file Excel itu sendiri dengan kata sandi menggunakan metode lain yang disediakan oleh perpustakaan Aspose.Cells. Silakan merujuk ke dokumentasi untuk contoh spesifik.

#### Apakah perpustakaan Aspose.Cells mendukung format file Excel lainnya?

J: Ya, perpustakaan Aspose.Cells mendukung berbagai format file Excel, termasuk XLSX, XLSM, XLSB, CSV, dll.