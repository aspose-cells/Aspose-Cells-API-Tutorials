---
title: Salin Lembar Kerja Excel Dari Buku Kerja Lain
linktitle: Salin Lembar Kerja Excel Dari Buku Kerja Lain
second_title: Aspose.Cells untuk Referensi .NET API
description: Salin lembar kerja Excel dengan mudah dari satu buku kerja ke buku kerja lainnya menggunakan Aspose.Cells untuk .NET.
type: docs
weight: 10
url: /id/net/excel-copy-worksheet/excel-copy-worksheet-from-other-workbook/
---
Dalam tutorial ini, kami akan memandu Anda melalui langkah-langkah untuk menyalin lembar kerja Excel dari buku kerja lain menggunakan perpustakaan Aspose.Cells untuk .NET. Ikuti petunjuk di bawah ini untuk menyelesaikan tugas ini.

## Langkah 1: Persiapan

Sebelum memulai, pastikan Anda telah menginstal Aspose.Cells untuk .NET dan membuat proyek C# di lingkungan pengembangan terintegrasi (IDE) pilihan Anda.

## Langkah 2: Tetapkan jalur direktori dokumen

 Nyatakan a`dataDir` variabel dan inisialisasi dengan jalur ke direktori dokumen Anda. Misalnya :

```csharp
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";
```

 Pastikan untuk mengganti`"YOUR_DOCUMENTS_DIRECTORY"` dengan jalur sebenarnya ke direktori Anda.

## Langkah 3: Buat buku kerja Excel baru

 Menggunakan`Workbook` kelas dari Aspose.Cells untuk membuat buku kerja Excel baru:

```csharp
Workbook excelWorkbook0 = new Workbook();
```

## Langkah 4: Dapatkan lembar kerja pertama di buku kerja

Navigasikan ke lembar kerja pertama di buku kerja menggunakan indeks 0:

```csharp
Worksheet ws0 = excelWorkbook0.Worksheets[0];
```

## Langkah 5: Tambahkan data ke baris header (A1:A4)

 Gunakan`for` loop untuk menambahkan data ke baris header (A1:A4):

```csharp
for (int i = 0; i < 5; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Header row {0}", i));
}
```

## Langkah 6: Tambahkan data detail (A5:A999)

 Gunakan yang lain`for` loop untuk menambahkan data detail (A5:A999):

```csharp
for (int i = 5; i < 1000; i++)
{
     ws0.Cells[i, 0].PutValue(string.Format("Detail row {0}", i));
}
```

## Langkah 7: Tetapkan opsi tata letak

 Atur opsi pengaturan halaman untuk lembar kerja menggunakan`PageSetup` obyek:

```csharp
PageSetup pagesetup = ws0.PageSetup;
pagesetup.PrintTitleRows = "$1:$5";
```

## Langkah 8: Buat buku kerja Excel lainnya

Buat buku kerja Excel lainnya:

```csharp
Workbook excelWorkbook1 = new Workbook();
```

## Langkah 9: Dapatkan lembar kerja pertama dari buku kerja kedua

Navigasikan ke lembar kerja pertama di buku kerja kedua:

```csharp
Worksheet ws1 = excelWorkbook1.Worksheets[0];
```

## Langkah 10: Beri nama lembar kerja

beri nama apinya

pulau perhitungan:

```csharp
ws1.Name = "MySheet";
```

## Langkah 11: Salin data dari lembar kerja pertama dari buku kerja pertama ke lembar kerja pertama dari buku kerja kedua

Salin data dari lembar kerja pertama dari buku kerja pertama ke lembar kerja pertama dari buku kerja kedua:

```csharp
ws1.Copy(ws0);
```

## Langkah 12: Simpan file Excel

Simpan file Excelnya:

```csharp
excelWorkbook1.Save(dataDir + "CopyWorkbookSheetToOther_out.xls");
```

Pastikan untuk menentukan jalur dan nama file yang diinginkan untuk file keluaran.

### Contoh kode sumber untuk Excel Salin Lembar Kerja Dari Buku Kerja Lain menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Buat Buku Kerja baru.
Workbook excelWorkbook0 = new Workbook();
// Dapatkan lembar kerja pertama di buku.
Worksheet ws0 = excelWorkbook0.Worksheets[0];
// Masukkan beberapa data ke dalam baris header (A1:A4)
for (int i = 0; i < 5; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Header Row {0}", i));
}
// Masukkan beberapa data detail (A5:A999)
for (int i = 5; i < 1000; i++)
{
	ws0.Cells[i, 0].PutValue(string.Format("Detail Row {0}", i));
}
// Tentukan objek pagesetup berdasarkan lembar kerja pertama.
PageSetup pagesetup = ws0.PageSetup;
// Lima baris pertama diulangi di setiap halaman...
// Hal ini dapat dilihat pada print preview.
pagesetup.PrintTitleRows = "$1:$5";
// Buat Buku Kerja lain.
Workbook excelWorkbook1 = new Workbook();
// Dapatkan lembar kerja pertama di buku.
Worksheet ws1 = excelWorkbook1.Worksheets[0];
// Beri nama lembar kerja.
ws1.Name = "MySheet";
// Salin data dari lembar kerja pertama dari buku kerja pertama ke dalam
// lembar kerja pertama dari buku kerja kedua.
ws1.Copy(ws0);
// Simpan file excelnya.
excelWorkbook1.Save(dataDir + "CopyWorksheetFromWorkbookToOther_out.xls");
```

## Kesimpulan

Selamat! Anda sekarang telah mempelajari cara menyalin lembar kerja Excel dari buku kerja lain menggunakan Aspose.Cells untuk .NET. Jangan ragu untuk menggunakan metode ini dalam proyek Anda sendiri untuk memanipulasi file Excel secara efisien.

### FAQ

#### T. Pustaka apa yang diperlukan untuk menggunakan Aspose.Cells untuk .NET?

A. Untuk menggunakan Aspose.Cells untuk .NET, Anda harus menyertakan perpustakaan Aspose.Cells dalam proyek Anda. Pastikan Anda telah mereferensikan perpustakaan ini dengan benar di lingkungan pengembangan terintegrasi (IDE) Anda.

#### T. Apakah Aspose.Cells mendukung format file Excel lainnya, seperti XLSX?

A. Ya, Aspose.Cells mendukung berbagai format file Excel termasuk XLSX, XLS, CSV, HTML, dan masih banyak lagi. Anda dapat memanipulasi format file ini menggunakan fitur Aspose.Cells untuk .NET.

#### T. Bisakah saya mengkustomisasi opsi tata letak saat menyalin lembar kerja?

A.  Ya, Anda bisa mengkustomisasi opsi pengaturan halaman saat menyalin lembar kerja menggunakan properti`PageSetup` obyek. Anda dapat menentukan header halaman, footer, margin, orientasi, dll.