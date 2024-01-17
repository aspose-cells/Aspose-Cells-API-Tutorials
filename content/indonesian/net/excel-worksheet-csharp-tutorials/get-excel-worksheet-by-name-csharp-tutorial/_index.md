---
title: Dapatkan Lembar Kerja Excel Berdasarkan Nama Tutorial C#
linktitle: Dapatkan Lembar Kerja Excel Berdasarkan Nama
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara mendapatkan lembar kerja Excel berdasarkan nama menggunakan Aspose.Cells untuk .NET. Tutorial langkah demi langkah dengan contoh kode.
type: docs
weight: 50
url: /id/net/excel-worksheet-csharp-tutorials/get-excel-worksheet-by-name-csharp-tutorial/
---
Dalam tutorial ini, kami akan memandu Anda langkah demi langkah untuk menjelaskan kode sumber C# di bawah ini yang bisa mendapatkan lembar kerja Excel menggunakan Aspose.Cells untuk .NET menggunakan namanya. Kami akan menyertakan kode contoh untuk setiap langkah untuk membantu Anda memahami prosesnya secara detail.

## Langkah 1: Tentukan Direktori Dokumen

Untuk memulai, Anda perlu mengatur jalur direktori tempat file Excel Anda berada. Ganti "DIREKTORI DOKUMEN ANDA" dalam kode dengan jalur sebenarnya dari file Excel Anda.

```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
```

## Langkah 2: Tetapkan Jalur Input File Excel

Selanjutnya, Anda perlu mengatur jalur input file Excel yang ingin Anda buka. Jalur ini akan digunakan untuk membuat aliran file.

```csharp
// Jalur masukan file Excel
string InputPath = dataDir + "book1.xlsx";
```

## Langkah 3: Buat File Stream dan Buka File Excel

 Selanjutnya, Anda perlu membuat aliran file dan membuka file Excel menggunakan`FileStream` kelas.

```csharp
// Buat aliran file yang berisi file Excel untuk dibuka
FileStream fstream = new FileStream(InputPath, FileMode.Open);
```

## Langkah 4: Buat Instansiasi Objek Buku Kerja

 Setelah membuka file Excel, Anda perlu membuat instance a`Workbook`obyek. Objek ini mewakili buku kerja Excel dan menawarkan berbagai metode dan properti untuk memanipulasi buku kerja.

```csharp
// Membuat instance objek Buku Kerja
// Buka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
```

## Langkah 5: Akses Lembar Kerja berdasarkan Nama

Untuk mengakses lembar kerja tertentu berdasarkan nama, Anda bisa menggunakan`Worksheets` properti dari`Workbook` objek dan indeks nama lembar kerja.

```csharp
// Akses lembar kerja menggunakan nama lembarnya
Worksheet worksheet = workbook.Worksheets["Sheet1"];
```

## Langkah 6: Akses Sel tertentu

 Setelah Anda menavigasi ke lembar kerja yang diinginkan, Anda dapat menavigasi ke sel tertentu menggunakan`Cells` properti dari`Worksheet` objek dan mengindeks referensi sel.

```csharp
// Akses ke sel tertentu
Cell cell = worksheet.Cells["A1"];
```

## Langkah 7: Ambil Nilai Sel

 Terakhir, Anda dapat mengambil nilai sel menggunakan`Value` properti dari`Cell` obyek.

```csharp
// Ambil nilai sel
Console.WriteLine(cell.Value);
```

### Contoh kode sumber untuk Tutorial Mendapatkan Lembar Kerja Excel Berdasarkan Nama C# menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
string InputPath = dataDir + "book1.xlsx";
// Membuat aliran file yang berisi file Excel yang akan dibuka
FileStream fstream = new FileStream(InputPath, FileMode.Open);
// Membuat instance objek Buku Kerja
// Membuka file Excel melalui aliran file
Workbook workbook = new Workbook(fstream);
// Mengakses lembar kerja menggunakan nama lembarnya
Worksheet worksheet = workbook.Worksheets["Sheet1"];
Cell cell = worksheet.Cells["A1"];
Console.WriteLine(cell.Value);
```

## Kesimpulan

Dalam tutorial ini, kita telah membahas proses langkah demi langkah untuk mendapatkan lembar kerja Excel tertentu berdasarkan namanya menggunakan Aspose.Cells untuk .NET. Anda sekarang dapat menggunakan pengetahuan ini untuk memanipulasi dan memproses data dalam file Excel Anda secara efisien dan akurat.

### Pertanyaan yang Sering Diajukan (FAQ)

#### Apa itu Aspose.Cells untuk .NET?

Aspose.Cells for .NET adalah perpustakaan canggih yang memungkinkan pengembang membuat, memanipulasi, dan mengonversi file Excel dalam aplikasi .NET mereka. Ia menawarkan berbagai fitur untuk bekerja dengan lembar kerja, sel, rumus, gaya, dan banyak lagi.

#### Bagaimana cara menginstal Aspose.Cells untuk .NET?

Untuk menginstal Aspose.Cells untuk .NET, Anda dapat mengunduh paket instalasi dari Aspose.Releases (https://releases.aspose.com/cells/net) dan ikuti instruksi yang diberikan. Anda memerlukan lisensi yang valid untuk menggunakan perpustakaan di aplikasi Anda.

#### Bisakah saya mendapatkan lembar kerja Excel menggunakan namanya di Aspose.Cells untuk .NET?

 Ya, Anda bisa mendapatkan lembar kerja Excel menggunakan namanya di Aspose.Cells untuk .NET. Anda dapat menggunakan`Worksheets` properti dari`Workbook` objek dan indeks nama lembar kerja untuk mengaksesnya.

#### Bagaimana jika nama lembar kerja tidak ada di file Excel?

Jika nama lembar kerja yang ditentukan tidak ada di file Excel, pengecualian akan diberikan saat mencoba mengakses lembar kerja tersebut. Pastikan untuk memeriksa apakah nama lembar kerja dimasukkan dengan benar dan ada di file Excel sebelum mengaksesnya.

#### Bisakah saya menggunakan Aspose.Cells for .NET untuk memanipulasi data sel di lembar kerja?

Ya, Aspose.Cells untuk .NET menawarkan banyak fitur untuk memanipulasi data sel di lembar kerja. Anda dapat membaca dan menulis nilai sel, menerapkan format, menambahkan rumus, menggabungkan sel, melakukan operasi matematika, dan banyak lagi. Perpustakaan menyediakan antarmuka yang komprehensif untuk bekerja dengan data sel di Excel.