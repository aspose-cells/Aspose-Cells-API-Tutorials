---
title: Atur Kualitas Cetak Excel
linktitle: Atur Kualitas Cetak Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mengelola dan mengkustomisasi file Excel, termasuk opsi pencetakan menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 160
url: /id/net/excel-page-setup/set-excel-print-quality/
---
Dalam panduan ini, kami akan menjelaskan cara mengatur kualitas cetak spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Kami akan memandu Anda langkah demi langkah melalui kode sumber C# yang disediakan untuk menyelesaikan tugas ini.

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

## Langkah 5: Akses ke lembar kerja pertama

Navigasikan ke lembar kerja pertama di buku kerja Excel menggunakan kode berikut:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Langkah 6: Mengatur Kualitas Cetak

Untuk mengatur kualitas cetak lembar kerja, gunakan kode berikut:

```csharp
worksheet.PageSetup.PrintQuality = 180;
```

Di sini kami telah mengatur kualitas cetak menjadi 180 dpi, namun Anda dapat menyesuaikan nilai ini sesuai kebutuhan Anda.

## Langkah 7: Menyimpan buku kerja Excel

 Untuk menyimpan buku kerja Excel dengan kualitas cetak yang ditentukan, gunakan`Save` metode objek Buku Kerja:

```csharp
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

Ini akan menyimpan buku kerja Excel dengan nama file "SetPrintQuality_out.xls" di direktori yang ditentukan.

### Contoh kode sumber untuk Mengatur Kualitas Cetak Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Mengatur kualitas cetak lembar kerja menjadi 180 dpi
worksheet.PageSetup.PrintQuality = 180;
// Simpan Buku Kerja.
workbook.Save(dataDir + "SetPrintQuality_out.xls");
```

## Kesimpulan

Selamat! Anda telah mempelajari cara mengatur kualitas cetak spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Anda sekarang dapat menyesuaikan kualitas cetak file Excel Anda sesuai dengan preferensi dan kebutuhan spesifik Anda.

## FAQ


#### 1. Bisakah saya menyesuaikan kualitas cetak berbagai lembar kerja dalam file Excel yang sama?

Ya, Anda dapat menyesuaikan kualitas cetak setiap lembar kerja satu per satu dengan masuk ke objek Lembar Kerja terkait dan mengatur kualitas cetak yang sesuai.

#### 2. Opsi pencetakan apa lagi yang dapat saya sesuaikan dengan Aspose.Cells untuk .NET?

Selain kualitas cetak, Anda dapat menyesuaikan berbagai pilihan pencetakan lainnya seperti margin, orientasi halaman, skala cetak, dll.

#### 3. Apakah Aspose.Cells untuk .NET mendukung format file Excel yang berbeda?

Ya, Aspose.Cells untuk .NET mendukung berbagai format file Excel termasuk XLSX, XLS, CSV, HTML, PDF, dll.