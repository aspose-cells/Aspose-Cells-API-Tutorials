---
title: Hapus Panel Lembar Kerja
linktitle: Hapus Panel Lembar Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Panduan langkah demi langkah untuk menghapus panel dari lembar kerja Excel menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 120
url: /id/net/excel-display-settings-csharp-tutorials/remove-panes-of-worksheet/
---
Dalam tutorial ini, kami akan menjelaskan cara menghapus panel dari lembar kerja Excel menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah berikut untuk mendapatkan hasil yang diinginkan:

## Langkah 1: Menyiapkan lingkungan

Pastikan Anda telah menginstal Aspose.Cells untuk .NET dan menyiapkan lingkungan pengembangan Anda. Selain itu, pastikan Anda memiliki salinan file Excel yang panelnya ingin Anda hapus.

## Langkah 2: Impor dependensi yang diperlukan

Tambahkan arahan yang diperlukan untuk menggunakan kelas dari Aspose.Cells:

```csharp
using Aspose.Cells;
```

## Langkah 3: Inisialisasi kode

Mulailah dengan menginisialisasi jalur ke direktori yang berisi dokumen Excel Anda:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

## Langkah 4: Membuka file Excel

 Buat instance yang baru`Workbook` objek dan buka file Excel menggunakan`Open` metode:

```csharp
Workbook book = new Workbook(dataDir + "Book1.xls");
```

## Langkah 5: Tentukan sel aktif

 Atur sel aktif lembar kerja menggunakan`ActiveCell` Properti:

```csharp
book.Worksheets[0].ActiveCell = "A20";
```

## Langkah 6: Menghapus panel

 Hapus panel dari jendela lembar kerja menggunakan`RemoveSplit` metode:

```csharp
book.Worksheets[0].RemoveSplit();
```

## Langkah 7: Menyimpan Perubahan

Simpan perubahan yang dilakukan pada file Excel:

```csharp
book.Save(dataDir + "output.xls");
```

### Contoh kode sumber untuk Menghapus Panel Lembar Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Buat instance buku kerja baru dan Buka file templat
Workbook book = new Workbook(dataDir + "Book1.xls");
// Atur sel aktif
book.Worksheets[0].ActiveCell = "A20";
// Pisahkan jendela lembar kerja
book.Worksheets[0].RemoveSplit();
// Simpan file excelnya
book.Save(dataDir + "output.xls");
```

## Kesimpulan

Dalam tutorial ini, Anda mempelajari cara menghapus panel dari lembar kerja Excel menggunakan Aspose.Cells untuk .NET. Dengan mengikuti langkah-langkah yang dijelaskan, Anda bisa dengan mudah mengkustomisasi tampilan dan perilaku file Excel Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan perangkat lunak populer untuk memanipulasi file Excel dalam aplikasi .NET.

#### Bagaimana cara mengatur sel aktif lembar kerja di Aspose.Cells?

 Anda dapat mengatur sel aktif menggunakan`ActiveCell`milik objek Lembar Kerja.

#### Bisakah saya menghapus panel horizontal atau vertikal saja dari jendela lembar kerja?

 Ya, menggunakan Aspose.Cells Anda hanya dapat menghapus panel horizontal atau vertikal menggunakan metode yang sesuai seperti`RemoveHorizontalSplit` atau`RemoveVerticalSplit`.

#### Apakah Aspose.Cells hanya berfungsi dengan file Excel dalam format .xls?

Tidak, Aspose.Cells mendukung berbagai format file Excel termasuk .xls dan .xlsx.
	