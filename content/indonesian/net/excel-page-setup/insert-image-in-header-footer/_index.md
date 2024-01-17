---
title: Sisipkan Gambar Di Header Footer
linktitle: Sisipkan Gambar Di Header Footer
second_title: Aspose.Cells untuk Referensi .NET API
description: Pelajari cara menyisipkan gambar ke header atau footer dokumen Excel menggunakan Aspose.Cells untuk .NET. Panduan langkah demi langkah dengan kode sumber dalam C#.
type: docs
weight: 60
url: /id/net/excel-page-setup/insert-image-in-header-footer/
---
Kemampuan untuk menyisipkan gambar di header atau footer dokumen Excel bisa sangat berguna untuk menyesuaikan laporan atau menambahkan logo perusahaan. Pada artikel ini, kami akan memandu Anda langkah demi langkah untuk menyisipkan gambar di header atau footer dokumen Excel menggunakan Aspose.Cells untuk .NET. Anda akan mempelajari cara melakukannya menggunakan kode sumber C#.

## Langkah 1: Menyiapkan lingkungan

Sebelum memulai, pastikan Anda telah menginstal Aspose.Cells for .NET di mesin Anda. Buat juga proyek baru di lingkungan pengembangan pilihan Anda.

## Langkah 2: Impor perpustakaan yang diperlukan

Dalam file kode Anda, impor pustaka yang diperlukan untuk bekerja dengan Aspose.Cells. Ini kode yang sesuai:

```csharp
using Aspose.Cells;
```

## Langkah 3: Atur Direktori Dokumen

Atur direktori tempat dokumen Excel yang ingin Anda kerjakan berada. Gunakan kode berikut untuk mengatur direktori:

```csharp
string dataDir = "YOUR DOCUMENTS DIRECTORY";
```

Pastikan untuk menentukan jalur direktori lengkap.

## Langkah 4: Membuat Objek Buku Kerja

Objek Buku Kerja mewakili dokumen Excel yang akan Anda gunakan untuk bekerja. Anda dapat membuatnya menggunakan kode berikut:

```csharp
Workbook workbook = new Workbook();
```

Ini menciptakan objek Buku Kerja kosong yang baru.

## Langkah 5: Menyimpan URL Gambar

Tentukan URL atau jalur gambar yang ingin Anda sisipkan di header atau footer. Gunakan kode berikut untuk menyimpan URL gambar:

```csharp
string logo_url = dataDir + "aspose-logo.jpg";
```

Pastikan jalur yang ditentukan sudah benar dan gambar ada di lokasi tersebut.

## Langkah 6: Membuka file gambar

Untuk membuka file gambar, kita akan menggunakan objek FileStream dan membaca data biner dari gambar. Ini kode yang sesuai:

```csharp
FileStream inFile;
byte[] binaryData;

inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
binaryData = new Byte[inFile.Length];
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
```

Pastikan jalur gambar sudah benar dan Anda memiliki izin yang benar untuk mengaksesnya.

## Langkah 7: Mengonfigurasi PageSetup

Objek PageSetup digunakan untuk mengatur pengaturan halaman dokumen Excel termasuk header dan footer. Gunakan kode berikut untuk mendapatkan objek PageSetup pada lembar kerja pertama:

```csharp
PageSetup pageSetup = workbook. Worksheets

[0].PageSetup;
```

Ini akan memungkinkan Anda mengakses pengaturan halaman untuk lembar kerja pertama di buku kerja.

## Langkah 8: Menambahkan gambar ke header

Gunakan metode SetHeaderPicture() pada objek PageSetup untuk mengatur gambar di bagian tengah header halaman. Ini kode yang sesuai:

```csharp
pageSetup.SetHeaderPicture(1, binaryData);
```

Ini akan menambahkan gambar tertentu ke header halaman.

## Langkah 9: Menambahkan skrip ke header

Untuk menambahkan skrip ke header halaman, gunakan metode SetHeader() pada objek PageSetup. Ini kode yang sesuai:

```csharp
pageSetup.SetHeader(1, "&G");
```

Ini akan menambahkan skrip yang ditentukan ke header halaman. Dalam contoh ini, skrip "&G" menampilkan nomor halaman.

## Langkah 10: Tambahkan Nama Lembar ke Header

Untuk menampilkan nama sheet di header halaman, gunakan kembali metode SetHeader() pada objek PageSetup. Ini kode yang sesuai:

```csharp
pageSetup.SetHeader(2, "&A");
```

Ini akan menambahkan nama sheet ke header halaman. Skrip "&A" digunakan untuk mewakili nama sheet.

## Langkah 11: Menyimpan buku kerja

Untuk menyimpan perubahan pada buku kerja, gunakan metode Save() pada objek Buku Kerja. Ini kode yang sesuai:

```csharp
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
```

Ini akan menyimpan buku kerja dengan perubahan pada direktori yang ditentukan.

## Langkah 12: Menutup FileStream

Setelah membaca data biner dari gambar, pastikan untuk menutup FileStream untuk mengosongkan sumber daya. Gunakan kode berikut untuk menutup FileStream:

```csharp
inFile.Close();
```

Pastikan untuk selalu menutup FileStreams setelah Anda selesai menggunakannya.

### Contoh kode sumber untuk Menyisipkan Gambar Di Header Footer menggunakan Aspose.Cells untuk .NET 
```csharp
//Jalur ke direktori dokumen.
string dataDir = "YOUR DOCUMENT DIRECTORY";
//Membuat objek Buku Kerja
Workbook workbook = new Workbook();
// Membuat variabel string untuk menyimpan url logo/gambar
string logo_url = dataDir + "aspose-logo.jpg";
// Mendeklarasikan objek FileStream
FileStream inFile;
// Mendeklarasikan array byte
byte[] binaryData;
// Membuat instance objek FileStream untuk membuka logo/gambar di aliran
inFile = new System.IO.FileStream(logo_url, System.IO.FileMode.Open, System.IO.FileAccess.Read);
// Membuat instance array byte ukuran objek FileStream
binaryData = new Byte[inFile.Length];
// Membaca satu blok byte dari aliran dan menulis data dalam buffer array byte tertentu.
long bytesRead = inFile.Read(binaryData, 0, (int)inFile.Length);
// Membuat objek PageSetup untuk mendapatkan pengaturan halaman lembar kerja pertama buku kerja
PageSetup pageSetup = workbook.Worksheets[0].PageSetup;
// Mengatur logo/gambar pada bagian tengah header halaman
pageSetup.SetHeaderPicture(1, binaryData);
// Setting script untuk logo/gambar
pageSetup.SetHeader(1, "&G");
// Mengatur nama Sheet di bagian kanan header halaman dengan skrip
pageSetup.SetHeader(2, "&A");
// Menyimpan buku kerja
workbook.Save(dataDir + "InsertImageInHeaderFooter_out.xls");
//Menutup objek FileStream
inFile.Close();       
```
## Kesimpulan

Selamat! Anda sekarang mengetahui cara menyisipkan gambar di header atau footer dokumen Excel menggunakan Aspose.Cells untuk .NET. Tutorial ini memandu Anda melalui setiap langkah proses, mulai dari menyiapkan lingkungan hingga menyimpan buku kerja yang dimodifikasi. Jangan ragu untuk bereksperimen lebih banyak dengan fitur Aspose.Cells untuk membuat dokumen Excel yang dipersonalisasi dan profesional.

### FAQ

#### Q1: Apakah mungkin untuk menyisipkan banyak gambar di header atau footer dokumen Excel?

A1: Ya, Anda bisa menyisipkan beberapa gambar ke header atau footer dokumen Excel dengan mengulangi langkah 8 dan 9 untuk setiap gambar tambahan.

#### Q2: Format gambar apa yang didukung untuk disisipkan di header atau footer?
A2: Aspose.Cells mendukung berbagai format gambar umum seperti JPEG, PNG, GIF, BMP, dll.

#### Q3: Dapatkah saya menyesuaikan tampilan header atau footer lebih lanjut?

A3: Ya, Anda dapat menggunakan skrip dan kode khusus untuk memformat lebih lanjut dan menyesuaikan tampilan header atau footer. Lihat dokumentasi Aspose.Cells untuk informasi selengkapnya tentang opsi penyesuaian.

#### Q4: Apakah Aspose.Cells berfungsi dengan versi Excel yang berbeda?

A4: Ya, Aspose.Cells kompatibel dengan berbagai versi Excel termasuk Excel 2003, Excel 2007, Excel 2010, Excel 2013, Excel 2016, dan Excel 2019.

#### Q5: Apakah mungkin untuk menyisipkan gambar di bagian lain dokumen Excel, seperti sel atau bagan?

A5: Ya, Aspose.Cells menyediakan fungsionalitas ekstensif untuk menyisipkan gambar ke berbagai bagian dokumen Excel, termasuk sel, bagan, dan objek gambar.