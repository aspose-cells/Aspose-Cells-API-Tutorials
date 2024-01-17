---
title: Opsi Cocok Untuk Halaman Excel
linktitle: Opsi Cocok Untuk Halaman Excel
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menyesuaikan halaman secara otomatis di spreadsheet Excel dengan Aspose.Cells untuk .NET.
type: docs
weight: 30
url: /id/net/excel-page-setup/fit-to-excel-pages-options/
---
Pada artikel ini, kami akan membawa Anda langkah demi langkah untuk menjelaskan kode sumber C# berikut: Opsi Halaman Fit to Excel menggunakan Aspose.Cells untuk .NET. Kami akan menggunakan perpustakaan Aspose.Cells untuk .NET untuk melakukan operasi ini. Ikuti langkah-langkah di bawah ini untuk mengonfigurasi kesesuaian dengan halaman di Excel.

## Langkah 1: Membuat Buku Kerja
Langkah pertama adalah membuat buku kerja. Kita akan membuat instance objek Workbook. Berikut ini kode untuk membuat buku kerja:

```csharp
// Jalur ke direktori dokumen
string dataDir = "YOUR_DIRECTORY_OF_DOCUMENTS";

// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
```

## Langkah 2: Mengakses lembar kerja
Sekarang kita telah membuat buku kerja, kita perlu menavigasi ke lembar kerja pertama. Kami akan menggunakan indeks 0 untuk mengakses lembar pertama. Berikut kode untuk mengaksesnya:

```csharp
// Akses ke lembar kerja pertama di buku kerja
Worksheet worksheet = workbook.Worksheets[0];
```

## Langkah 3: Mengatur Kesesuaian dengan Halaman
 Pada langkah ini, kita akan mengkonfigurasi penyesuaian pada halaman lembar kerja. Kami akan menggunakan`FitToPagesTall` Dan`FitToPagesWide` properti dari`PageSetup` objek untuk menentukan jumlah halaman yang diinginkan untuk tinggi dan lebar lembar kerja. Ini kode untuk itu:

```csharp
// Konfigurasikan jumlah halaman untuk tinggi lembar kerja
worksheet.PageSetup.FitToPagesTall = 1;

// Konfigurasikan jumlah halaman untuk lebar lembar kerja
worksheet.PageSetup.FitToPagesWide = 1;
```

## Langkah 4: Menyimpan Buku Kerja
 Sekarang kita telah mengonfigurasi kesesuaian dengan halaman, kita dapat menyimpan buku kerja. Kami akan menggunakan`Save` metode objek Buku Kerja untuk ini. Berikut ini kode untuk menyimpan buku kerja:

```csharp
// Simpan buku kerja
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

### Contoh kode sumber untuk Opsi Halaman Fit To Excel menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
// Mengakses lembar kerja pertama di file Excel
Worksheet worksheet = workbook.Worksheets[0];
// Mengatur jumlah halaman yang akan dibentangkan sepanjang lembar kerja
worksheet.PageSetup.FitToPagesTall = 1;
//Mengatur jumlah halaman yang akan dibentangkan lebar lembar kerja
worksheet.PageSetup.FitToPagesWide = 1;
// Simpan buku kerja.
workbook.Save(dataDir + "FitToPagesOptions_out.xls");
```

## Kesimpulan
Dalam artikel ini, kita mempelajari cara mengonfigurasi kesesuaian halaman di Excel menggunakan Aspose.Cells untuk .NET. Kami melakukan langkah-langkah berikut: membuat buku kerja, mengakses lembar kerja, mengonfigurasi kesesuaian halaman, dan menyimpan buku kerja. Sekarang Anda dapat menggunakan pengetahuan ini untuk menyesuaikan spreadsheet Anda ke halaman yang diinginkan.

### FAQ

#### T: Bagaimana cara menginstal Aspose.Cells untuk .NET?

J: Untuk menginstal Aspose.Cells untuk .NET, Anda dapat menggunakan manajer paket NuGet di Visual Studio. Temukan paket "Aspose.Cells" dan instal di proyek Anda.

#### T: Bisakah saya memuat halaman dengan tinggi dan lebar?

 A: Ya, Anda dapat mengatur tinggi dan lebar lembar kerja menggunakan`FitToPagesTall` Dan`FitToPagesWide` properti. Anda dapat menentukan jumlah halaman yang diinginkan untuk setiap dimensi.

#### T: Bagaimana cara menyesuaikan opsi Sesuaikan dengan Halaman?

J: Selain menentukan jumlah halaman, Anda juga dapat mengkustomisasi opsi penyesuaian halaman lainnya seperti skala lembar kerja, orientasi kertas, margin, dan lainnya. Gunakan properti yang tersedia di`PageSetup` keberatan untuk ini.

#### T: Dapatkah saya menggunakan Aspose.Cells untuk .NET untuk memproses buku kerja yang ada?

J: Ya, Anda bisa menggunakan Aspose.Cells untuk .NET untuk membuka dan mengedit buku kerja yang ada. Anda bisa mengakses lembar kerja, sel, rumus, gaya, dan item buku kerja lainnya untuk melakukan berbagai operasi.