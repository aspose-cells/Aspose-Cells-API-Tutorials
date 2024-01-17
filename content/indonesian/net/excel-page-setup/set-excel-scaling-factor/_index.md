---
title: Tetapkan Faktor Penskalaan Excel
linktitle: Tetapkan Faktor Penskalaan Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memanipulasi file Excel dengan mudah dan menyesuaikan faktor penskalaan menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 180
url: /id/net/excel-page-setup/set-excel-scaling-factor/
---
Dalam panduan ini, kami akan memandu Anda tentang cara mengatur faktor penskalaan dalam spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah di bawah ini untuk menyelesaikan tugas ini.

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menyiapkan lingkungan pengembangan dan menginstal Aspose.Cells untuk .NET. Anda dapat mengunduh perpustakaan versi terbaru dari situs resmi Aspose.

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

## Langkah 6: Tetapkan Faktor Penskalaan

Atur faktor penskalaan menggunakan kode berikut:

```csharp
worksheet.PageSetup.Zoom = 100;
```

Di sini kami telah menetapkan faktor penskalaan ke 100, yang berarti spreadsheet akan ditampilkan pada 100% ukuran normal saat dicetak.

## Langkah 7: Menyimpan buku kerja Excel

 Untuk menyimpan buku kerja Excel dengan faktor penskalaan yang ditentukan, gunakan`Save` metode objek Buku Kerja:

```csharp
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

Ini akan menyimpan buku kerja Excel dengan nama file "ScalingFactor_out.xls" di direktori yang ditentukan.

### Contoh kode sumber untuk Mengatur Faktor Penskalaan Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Mengatur faktor skala ke 100
worksheet.PageSetup.Zoom = 100;
// Simpan buku kerja.
workbook.Save(dataDir + "ScalingFactor_out.xls");
```

## Kesimpulan

Selamat! Anda telah mempelajari cara mengatur faktor penskalaan dalam spreadsheet Excel menggunakan Aspose.Cells untuk .NET. Faktor penskalaan memungkinkan Anda menyesuaikan ukuran spreadsheet saat mencetak untuk tampilan optimal.

### FAQ

#### 1. Bagaimana cara mengatur faktor penskalaan di spreadsheet Excel dengan Aspose.Cells untuk .NET?

 Menggunakan`Zoom` properti dari`PageSetup`objek untuk mengatur faktor skala. Misalnya,`worksheet.PageSetup.Zoom = 100;` akan mengatur faktor penskalaan menjadi 100%.

#### 2. Dapatkah saya menyesuaikan faktor penskalaan sesuai kebutuhan saya?

 Ya, Anda dapat menyesuaikan faktor penskalaan dengan mengubah nilai yang ditetapkan ke`Zoom` Properti. Misalnya,`worksheet.PageSetup.Zoom = 75;` akan mengatur faktor penskalaan menjadi 75%.

#### 3. Apakah mungkin untuk menyimpan buku kerja Excel dengan faktor penskalaan yang ditentukan?

 Ya, Anda dapat menggunakan`Save` metode`Workbook` objek untuk menyimpan buku kerja Excel dengan faktor penskalaan yang ditentukan.