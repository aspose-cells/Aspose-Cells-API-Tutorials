---
title: Pratinjau Istirahat Halaman Lembar Kerja
linktitle: Pratinjau Istirahat Halaman Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Panduan langkah demi langkah untuk menampilkan pratinjau hentian halaman lembar kerja menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 110
url: /id/net/excel-display-settings-csharp-tutorials/page-break-preview-of-worksheet/
---
Dalam tutorial ini, kami akan menjelaskan cara menampilkan pratinjau hentian halaman lembar kerja menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah berikut untuk mendapatkan hasil yang diinginkan:

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET dan menyiapkan lingkungan pengembangan Anda. Selain itu, pastikan Anda memiliki salinan file Excel yang ingin Anda tampilkan pratinjau hentian halamannya.

## Langkah 2: Impor dependensi yang diperlukan

Tambahkan arahan yang diperlukan untuk menggunakan kelas dari Aspose.Cells:

```csharp
using Aspose.Cells;
using System.IO;
```

## Langkah 3: Inisialisasi kode

Mulailah dengan menginisialisasi jalur ke direktori yang berisi dokumen Excel Anda:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Langkah 4: Membuka file Excel

 Membuat`FileStream` objek yang berisi file Excel untuk dibuka:

```csharp
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

 Buat contoh a`Workbook` objek dan buka file Excel menggunakan aliran file:

```csharp
Workbook workbook = new Workbook(fstream);
```

## Langkah 5: Mengakses Spreadsheet

Arahkan ke lembar kerja pertama di file Excel:

```csharp
Worksheet worksheet = workbook.Worksheets[0];
```

## Langkah 6: Menampilkan pratinjau halaman demi halaman

Aktifkan pratinjau halaman demi halaman untuk spreadsheet:

```csharp
worksheet. IsPageBreakPreview = true;
```

## Langkah 7: Menyimpan Perubahan

Simpan perubahan yang dilakukan pada file Excel:

```csharp
workbook.Save(dataDir + "output.xls");
```

## Langkah 8: Menutup aliran file

Tutup aliran file untuk melepaskan semua sumber daya:

```csharp
fstream.Close();
```

### Contoh kode sumber untuk Pratinjau Hentian Halaman Lembar Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Membuat instance objek Buku Kerja
// Membuka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Menampilkan lembar kerja di pratinjau hentian halaman
worksheet.IsPageBreakPreview = true;
// Menyimpan file Excel yang dimodifikasi
workbook.Save(dataDir + "output.xls");
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Dalam tutorial ini, Anda mempelajari cara menampilkan pratinjau hentian halaman lembar kerja menggunakan Aspose.Cells untuk .NET. Dengan mengikuti langkah-langkah yang dijelaskan, Anda bisa dengan mudah mengontrol tampilan dan tata letak file Excel Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan perangkat lunak populer untuk memanipulasi file Excel dalam aplikasi .NET.

#### Bisakah saya memperlihatkan pratinjau halaman demi lembar kerja tertentu, bukan keseluruhan lembar kerja?

Ya, menggunakan Aspose.Cells Anda dapat mengaktifkan pratinjau hentian halaman untuk lembar kerja tertentu dengan mengakses objek Lembar Kerja yang sesuai.

#### Apakah Aspose.Cells mendukung fitur pengeditan file Excel lainnya?

Ya, Aspose.Cells menawarkan berbagai fitur untuk mengedit dan memanipulasi file Excel, seperti menambahkan data, memformat, membuat grafik, dll.

#### Apakah Aspose.Cells hanya berfungsi dengan file Excel dalam format .xls?

Tidak, Aspose.Cells mendukung berbagai format file Excel termasuk .xls dan .xlsx.
	