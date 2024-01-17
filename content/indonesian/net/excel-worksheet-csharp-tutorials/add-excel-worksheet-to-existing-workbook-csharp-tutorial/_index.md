---
title: Tambahkan Lembar Kerja Excel ke Tutorial C# Buku Kerja yang Ada
linktitle: Tambahkan Lembar Kerja Excel ke Buku Kerja yang Ada
second_title: Aspose.Cells untuk Referensi .NET API
description: Tambahkan lembar baru dengan mudah ke buku kerja Excel yang sudah ada menggunakan Aspose.Cells untuk .NET. Tutorial langkah demi langkah dengan contoh kode.
type: docs
weight: 10
url: /id/net/excel-worksheet-csharp-tutorials/add-excel-worksheet-to-existing-workbook-csharp-tutorial/
---
Dalam tutorial ini, kami akan membawa Anda langkah demi langkah untuk menjelaskan kode sumber C# di bawah ini, yang membantu menambahkan lembar baru ke buku kerja Excel yang sudah ada menggunakan Aspose.Cells untuk .NET. Kami akan menyertakan kode contoh untuk setiap langkah untuk membantu Anda memahami prosesnya secara detail.

## Langkah 1: Tentukan Direktori Dokumen

Untuk memulai, Anda perlu mengatur jalur direktori tempat file Excel Anda berada. Ganti "DIREKTORI DOKUMEN ANDA" dalam kode dengan jalur sebenarnya dari file Excel Anda.

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Langkah 2: Buat File Stream dan Buka File Excel

 Selanjutnya, Anda perlu membuat aliran file dan membuka file Excel menggunakan`FileStream` kelas.

```csharp
// Buat aliran file yang berisi file Excel untuk dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
```

## Langkah 3: Buat Instansiasi Objek Buku Kerja

 Setelah membuka file Excel, Anda perlu membuat instance a`Workbook`obyek. Objek ini mewakili buku kerja Excel dan menawarkan berbagai metode dan properti untuk memanipulasi buku kerja.

```csharp
// Membuat instance objek Buku Kerja
// Buka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
```

## Langkah 4: Tambahkan Lembar Baru ke Buku Kerja

 Untuk menambahkan lembar kerja baru ke buku kerja, Anda bisa menggunakan`Worksheets.Add()` metode`Workbook` obyek. Metode ini mengembalikan indeks sheet yang baru ditambahkan.

```csharp
// Tambahkan lembar baru ke buku kerja Buku Kerja
int i = workbook. Worksheets. Add();
```

## Langkah 5: Tetapkan Nama Lembar Baru

 Anda dapat mengatur nama sheet yang baru ditambahkan menggunakan`Name` properti dari`Worksheet` obyek.

```csharp
// Dapatkan referensi sheet baru yang ditambahkan dengan meneruskan indeks sheetnya
Worksheet worksheet = workbook.Worksheets[i];
// Tentukan nama sheet baru
worksheet.Name = "My Worksheet";
```

## Langkah 6: Simpan File Excel

 Setelah Anda menambahkan lembar baru dan menetapkan namanya, Anda dapat menyimpan file Excel yang dimodifikasi menggunakan`Save()` metode`Workbook` obyek.

```csharp
// Simpan file Excelnya
workbook.Save(dataDir + "output.out.xls");
```

## Langkah 7: Tutup File Stream dan Rilis Sumber Daya

Terakhir, penting untuk menutup aliran file untuk melepaskan semua sumber daya yang terkait dengannya.

```csharp
// Tutup aliran file untuk melepaskan semua sumber daya
fstream.Close();
```

### Contoh kode sumber untuk Menambahkan Lembar Kerja Excel ke Buku Kerja yang Ada Tutorial C# menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(dataDir + "book1.xls", FileMode.Open);
// Membuat instance objek Buku Kerja
// Membuka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
// Menambahkan lembar kerja baru ke objek Buku Kerja
int i = workbook.Worksheets.Add();
// Mendapatkan referensi lembar kerja yang baru ditambahkan dengan meneruskan indeks lembarnya
Worksheet worksheet = workbook.Worksheets[i];
// Mengatur nama lembar kerja yang baru ditambahkan
worksheet.Name = "My Worksheet";
// Menyimpan file Excel
workbook.Save(dataDir + "output.out.xls");
// Menutup aliran file untuk mengosongkan semua sumber daya
fstream.Close();
```

## Kesimpulan

Dalam tutorial ini kita telah membahas proses langkah demi langkah menambahkan api baru Sambungkan ke buku kerja Excel yang sudah ada menggunakan Aspose.Cells untuk .NET. Dengan mengikuti contoh kode dan penjelasan yang diberikan, Anda sekarang seharusnya memiliki pemahaman yang baik tentang cara melakukan tugas ini di aplikasi C# Anda. Aspose.Cells for .NET menawarkan serangkaian fitur lengkap untuk bekerja dengan file Excel, memungkinkan Anda mengotomatiskan berbagai tugas terkait Excel secara efisien.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah pustaka .NET canggih yang memungkinkan pengembang membuat, memanipulasi, dan mengonversi file Excel dalam aplikasi mereka. Ini menawarkan berbagai fitur untuk bekerja dengan spreadsheet, sel, rumus, gaya, dan banyak lagi.

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

Untuk menginstal Aspose.Cells untuk .NET, Anda dapat mengunduh paket instalasi dari Aspose Releases (https://releases.aspose.com/cells/net) dan ikuti petunjuk instalasi yang diberikan. Anda juga memerlukan lisensi yang valid untuk menggunakan perpustakaan di aplikasi Anda.

#### Bisakah saya menambahkan beberapa spreadsheet menggunakan Aspose.Cells untuk .NET?

 Ya, Anda bisa menambahkan beberapa lembar kerja ke satu file Excel menggunakan Aspose.Cells untuk .NET. Anda dapat menggunakan`Worksheets.Add()` metode`Workbook` objek untuk menambahkan lembar kerja baru pada posisi berbeda di buku kerja.

#### Bagaimana cara memformat sel di file Excel?

Aspose.Cells untuk .NET menawarkan metode dan properti berbeda untuk memformat sel dalam file Excel. Anda dapat mengatur nilai sel, menerapkan opsi pemformatan seperti gaya font, warna, perataan, batas, dan lainnya. Lihat dokumentasi dan contoh kode yang disediakan oleh Aspose.Cells untuk informasi lebih detail tentang pemformatan sel.

#### Apakah Aspose.Cells untuk .NET kompatibel dengan versi Excel yang berbeda?

Ya, Aspose.Cells untuk .NET kompatibel dengan berbagai versi Excel termasuk Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, Excel 2019, dan Excel untuk Office 365. Mendukung format .xls dan yang lebih baru. format xlsx.