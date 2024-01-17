---
title: Filter Nama yang Ditentukan Saat Memuat Buku Kerja
linktitle: Filter Nama yang Ditentukan Saat Memuat Buku Kerja
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara memfilter nama yang ditentukan saat memuat buku kerja Excel dengan Aspose.Cells untuk .NET.
type: docs
weight: 100
url: /id/net/excel-workbook/filter-defined-names-while-loading-workbook/
---
Saat bekerja dengan buku kerja Excel dalam aplikasi .NET, sering kali perlu memfilter data yang dimuat. Aspose.Cells for .NET adalah perpustakaan yang kuat untuk memanipulasi buku kerja Excel dengan mudah. Dalam panduan ini, kami akan memperlihatkan kepada Anda cara memfilter nama yang ditentukan saat memuat buku kerja menggunakan Aspose.Cells untuk .NET. Ikuti langkah-langkah sederhana ini untuk mendapatkan hasil yang diinginkan:

## Langkah 1: Tentukan opsi pemuatan

Pertama, Anda perlu menentukan opsi pemuatan untuk menentukan perilaku pemuatan buku kerja. Dalam kasus kami, kami ingin mengabaikan nama yang disetel saat dimuat. Berikut cara melakukannya menggunakan Aspose.Cells:

```csharp
// Menentukan opsi pemuatan
LoadOptions opts = new LoadOptions();

// Jangan memuat nama yang ditentukan
opts. LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
```

## Langkah 2: Muat buku kerja

Setelah opsi pemuatan dikonfigurasi, Anda bisa memuat buku kerja Excel dari file sumber. Pastikan untuk menentukan jalur file yang benar. Berikut ini contoh kodenya:

```csharp
// Muat buku kerja
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
```

## Langkah 3: Simpan buku kerja yang difilter

Setelah memuat buku kerja, Anda bisa melakukan operasi atau pengeditan lain sesuai kebutuhan. Kemudian Anda bisa menyimpan buku kerja yang difilter ke file output. Begini caranya:

```csharp
// Simpan buku kerja Excel yang difilter
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
```

### Contoh kode sumber untuk Memfilter Nama yang Ditentukan Saat Memuat Buku Kerja menggunakan Aspose.Cells untuk .NET 
```csharp
//Tentukan opsi pemuatan
LoadOptions opts = new LoadOptions();
//Kami tidak ingin memuat nama yang ditentukan
opts.LoadFilter = new LoadFilter(~LoadDataFilterOptions.DefinedNames);
//Muat buku kerja
Workbook wb = new Workbook(sourceDir + "sampleFilterDefinedNamesWhileLoadingWorkbook.xlsx", opts);
//Simpan file keluaran Excel, itu akan merusak rumus di C1
wb.Save(outputDir + "outputFilterDefinedNamesWhileLoadingWorkbook.xlsx");
Console.WriteLine("FilterDefinedNamesWhileLoadingWorkbook executed successfully.");
```

## Kesimpulan

Memfilter nama yang ditentukan saat memuat buku kerja Excel bisa menjadi hal yang penting untuk banyak aplikasi. Aspose.Cells untuk .NET membuat tugas ini lebih mudah dengan menyediakan opsi fleksibel untuk memuat dan memfilter data. Dengan mengikuti langkah-langkah dalam panduan ini, Anda akan dapat memfilter nama yang ditentukan secara efektif dan mencapai hasil yang diinginkan di buku kerja Excel Anda.


### FAQ

#### T: Apakah Aspose.Cells mendukung bahasa pemrograman lain selain C#?
    
A: Ya, Aspose.Cells adalah perpustakaan lintas platform yang mendukung banyak bahasa pemrograman seperti Java, Python, C++dan masih banyak lagi.

#### T: Bisakah saya memfilter tipe data lain saat memuat buku kerja dengan Aspose.Cells?
    
J: Ya, Aspose.Cells menawarkan serangkaian opsi pemfilteran untuk data termasuk rumus, gaya, makro, dll.

#### T: Apakah Aspose.Cells mempertahankan format dan properti buku kerja asli?
    
J: Ya, Aspose.Cells mempertahankan pemformatan, gaya, rumus, dan properti lain dari buku kerja asli saat bekerja dengan file Excel.