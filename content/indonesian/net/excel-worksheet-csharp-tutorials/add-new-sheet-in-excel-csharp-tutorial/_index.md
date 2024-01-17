---
title: Tambahkan Lembar Baru Dalam Tutorial Excel C#
linktitle: Tambahkan Lembar Baru Di Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menambahkan lembar baru di Excel menggunakan Aspose.Cells untuk .NET. Tutorial langkah demi langkah dengan kode sumber di C#.
type: docs
weight: 20
url: /id/net/excel-worksheet-csharp-tutorials/add-new-sheet-in-excel-csharp-tutorial/
---
Dalam tutorial ini, kami akan menjelaskan langkah demi langkah kode sumber C# untuk menambahkan sheet baru di Excel menggunakan Aspose.Cells untuk .NET. Menambahkan lembar kerja baru ke buku kerja Excel adalah operasi umum saat membuat laporan atau memanipulasi data. Aspose.Cells adalah perpustakaan canggih yang memudahkan manipulasi dan menghasilkan file Excel menggunakan .NET. Ikuti langkah-langkah di bawah ini untuk memahami dan menerapkan kode ini.

## Langkah 1: Pengaturan Direktori Dokumen

Langkah pertama adalah menentukan direktori dokumen tempat file Excel akan disimpan. Jika direktori tidak ada, kita membuatnya menggunakan kode berikut:

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENTS DIRECTORY";
// Buat direktori jika belum ada.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
System.IO.Directory.CreateDirectory(dataDir);
```

Pastikan untuk mengganti "DIREKTORI DOKUMEN ANDA" dengan jalur yang sesuai ke direktori dokumen Anda.

## Langkah 2: Membuat Instansiasi Objek Buku Kerja

Langkah kedua adalah membuat instance objek Buku Kerja, yang mewakili buku kerja Excel. Gunakan kode berikut:

```csharp
Workbook workbook = new Workbook();
```

Objek ini akan digunakan untuk menambahkan lembar kerja baru dan melakukan operasi lain pada buku kerja Excel.

## Langkah 3: Menambahkan lembar kerja baru

Langkah ketiga adalah menambahkan lembar kerja baru pada objek Workbook. Gunakan kode berikut:

```csharp
int index = workbook. Worksheets. Add();
Worksheet worksheet = workbook.Worksheets[index];
```

Ini akan menambahkan lembar kerja baru ke objek Buku Kerja dan Anda akan mendapatkan referensi ke lembar kerja ini menggunakan indeksnya.

## Langkah 4: Mengatur nama lembar kerja baru

Langkah keempat adalah memberi nama pada lembar kerja baru. Anda dapat menggunakan kode berikut untuk mengatur nama lembar kerja:

```csharp
worksheet.Name = "My Worksheet";
```

Ganti "My Spreadsheet" dengan nama yang diinginkan untuk sheet baru.

## Langkah 5: Menyimpan file Excel

Terakhir, langkah terakhir adalah menyimpan file Excel. Gunakan kode berikut:

```csharp
string filePath = dataDir + "output.out.xls";
workbook.Save(filePath);
```

Ini akan menyimpan buku kerja Excel dengan lembar kerja baru ke direktori dokumen yang Anda tentukan.

### Contoh kode sumber untuk Tutorial Menambahkan Lembar Baru Di Excel C# menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Buat direktori jika belum ada.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
	System.IO.Directory.CreateDirectory(dataDir);
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Menambahkan lembar kerja baru ke objek Buku Kerja
int i = workbook.Worksheets.Add();
// Mendapatkan referensi lembar kerja yang baru ditambahkan dengan meneruskan indeks lembarnya
Worksheet worksheet = workbook.Worksheets[i];
// Mengatur nama lembar kerja yang baru ditambahkan
worksheet.Name = "My Worksheet";
// Menyimpan file Excel
workbook.Save(dataDir + "output.out.xls");
```

## Kesimpulan

Anda sekarang telah mempelajari cara menambahkan lembar kerja baru di Excel menggunakan Aspose.Cells untuk .NET. Anda dapat menggunakan metode ini untuk memanipulasi dan menghasilkan file Excel menggunakan C#. Aspose.Cells menawarkan banyak fitur canggih untuk menyederhanakan penanganan file Excel di aplikasi Anda.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Bisakah saya menggunakan Aspose.Cells dengan bahasa pemrograman lain selain C#?

Ya, Aspose.Cells mendukung berbagai bahasa pemrograman seperti Java, Python, Ruby, dan masih banyak lagi.

#### Bisakah saya menambahkan pemformatan ke sel di lembar kerja yang baru dibuat?

Ya, Anda bisa menerapkan pemformatan ke sel menggunakan metode yang disediakan oleh kelas Lembar Kerja Aspose.Cells. Anda dapat mengatur gaya sel, mengubah warna latar belakang, menerapkan batas, dll.

#### Bagaimana cara mengakses data sel dari lembar kerja baru?

Anda dapat mengakses data sel menggunakan properti dan metode yang disediakan oleh kelas Lembar Kerja Aspose.Cells. Misalnya, Anda bisa menggunakan properti Sel untuk mengakses sel tertentu dan mengambil atau mengubah nilainya.

#### Apakah Aspose.Cells mendukung rumus di Excel?

Ya, Aspose.Cells mendukung rumus Excel. Anda bisa mengatur rumus di sel lembar kerja menggunakan metode SetFormula dari kelas Sel.
