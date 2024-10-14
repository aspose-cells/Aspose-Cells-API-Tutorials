---
title: Menyalin Rentang Bernama di Excel
linktitle: Menyalin Rentang Bernama di Excel
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Pelajari cara menyalin rentang bernama di Excel menggunakan Aspose.Cells untuk .NET dengan panduan langkah demi langkah terperinci kami. Sempurna untuk pemula.
type: docs
weight: 10
url: /id/net/excel-managing-named-ranges/copy-named-ranges/
---
## Perkenalan
Excel adalah alat canggih yang digunakan oleh jutaan orang di seluruh dunia untuk mengorganisasi dan menganalisis data. Namun, jika menyangkut manipulasi file Excel secara terprogram—seperti menyalin rentang bernama—hal itu bisa jadi agak rumit. Untungnya, Aspose.Cells for .NET membuat tugas ini mudah dan efisien. Artikel ini akan memandu Anda melalui proses menyalin rentang bernama di Excel menggunakan Aspose.Cells for .NET, yang dijelaskan secara bertahap, sehingga Anda dapat mengikutinya dengan mudah.
## Prasyarat
Sebelum menyelami seluk-beluk penyalinan rentang bernama, Anda perlu memastikan bahwa Anda telah menyiapkan beberapa hal. Berikut ini yang Anda perlukan:
1. Lingkungan .NET: Pastikan Anda telah menyiapkan lingkungan pengembangan .NET. Anda dapat menggunakan Visual Studio atau IDE lain pilihan Anda.
2.  Pustaka Aspose.Cells untuk .NET: Ini adalah bintang pertunjukan! Unduh pustaka dari[Situs web Aspose](https://releases.aspose.com/cells/net/) jika Anda belum melakukannya.
3. Pengetahuan Dasar C#: Keakraban dengan pemrograman C# akan bermanfaat karena kita akan membuat kode dalam bahasa ini sepanjang tutorial.
4. Excel Terinstal: Meskipun Anda tidak perlu Excel untuk menulis kode, menginstalnya berguna untuk menguji file keluaran Anda.
5.  Akses ke Dokumentasi: Tandai[Dokumentasi Aspose.Cells](https://reference.aspose.com/cells/net/) untuk referensi. Ini adalah sumber yang bagus untuk memahami metode dan fitur.
Sekarang Anda sudah dilengkapi dengan hal-hal penting, mari selami kodenya!
## Paket Impor
Untuk mulai menggunakan Aspose.Cells, Anda harus mengimpor namespace yang diperlukan ke dalam proyek Anda. Ini akan memungkinkan Anda mengakses kelas-kelas yang disediakan oleh pustaka Aspose.Cells.
### Impor Namespace
Berikut cara mengimpor namespace Aspose.Cells:
```csharp
using System;
using System.IO;
using Aspose.Cells;
using System.Drawing;
```
Kode ini akan memberi Anda akses ke kelas-kelas penting seperti`Workbook`, `Worksheet` , Dan`Range`, yang mana Anda perlu memanipulasi file Excel.

Sekarang setelah prasyarat kita terpenuhi, mari kita uraikan prosesnya menjadi beberapa langkah yang mudah diikuti.
## Langkah 1: Siapkan Direktori Output Anda
Pertama, Anda perlu menentukan di mana file Excel yang dihasilkan akan disimpan. Ini seperti mengatur kotak surat sebelum menerima surat!
```csharp
string outputDir = "Your Document Directory\\"; // Pastikan untuk menggunakan garis miring terbalik ganda untuk jalur direktori
```
## Langkah 2: Buat Buku Kerja Baru
Berikutnya, Anda perlu membuat buku kerja baru, yang seperti membuka lembar kerja baru di Excel. 
```csharp
Workbook workbook = new Workbook();
```
Perintah ini membuat berkas Excel baru yang sekarang dapat kita modifikasi.
## Langkah 3: Akses Lembar Kerja
Setelah Anda memiliki buku kerja, Anda dapat mengakses lembar kerja yang ada di dalamnya. 
```csharp
WorksheetCollection worksheets = workbook.Worksheets;
```
Anggap lembar kerja sebagai halaman-halaman tersendiri dalam buku kerja Anda. Anda dapat memiliki beberapa halaman untuk mengatur data Anda.
## Langkah 4: Pilih Lembar Kerja Pertama
Mari kita ambil lembar kerja pertama dari koleksi kita. Di sinilah kita akan membuat dan memanipulasi rentang.
```csharp
Worksheet worksheet = workbook.Worksheets[0];
```
## Langkah 5: Buat dan Beri Nama Rentang Pertama Anda
Sekarang, saatnya membuat rentang bernama. Anda akan membuatnya dengan menentukan bagian sel dalam lembar kerja.
```csharp
Range range1 = worksheet.Cells.CreateRange("E12", "I12");
range1.Name = "MyRange";
```
Di sini, kami telah membuat rentang dari sel E12 hingga I12 dan memberinya nama "MyRange". Memberi nama rentang sangat penting karena memungkinkan Anda untuk merujuknya dengan mudah nanti.
## Langkah 6: Tetapkan Batas Garis Besar untuk Rentang
Selanjutnya, mari tambahkan beberapa gaya ke rentang kita dengan menetapkan batas garis luar. Ini membuat data Anda menarik secara visual!
```csharp
range1.SetOutlineBorder(BorderType.TopBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
range1.SetOutlineBorder(BorderType.BottomBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
range1.SetOutlineBorder(BorderType.LeftBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
range1.SetOutlineBorder(BorderType.RightBorder, CellBorderType.Medium, Color.FromArgb(0, 0, 128));
```
Dalam cuplikan ini, kami telah menetapkan batas atas, bawah, kiri, dan kanan menjadi sedang dan berwarna biru tua. Organisasi visual sama pentingnya dengan organisasi data!
## Langkah 7: Masukkan Data ke dalam Rentang
Sekarang saatnya mengisi rentang kita dengan beberapa data. 
```csharp
range1[0, 0].PutValue("Test");
range1[0, 4].PutValue("123");
```
Potongan kode ini mengisi sel pertama rentang dengan teks "Test" dan sel terakhir dengan angka "123". Ini seperti mengisi formulir dengan informasi penting.
## Langkah 8: Buat Rentang Lain
Berikutnya, Anda memerlukan rentang lain tempat Anda menyalin data dari rentang pertama Anda.
```csharp
Range range2 = worksheet.Cells.CreateRange("B3", "F3");
range2.Name = "testrange"; // Penamaan rentang kedua
```
Langkah ini membuat rentang dari B3 hingga F3, yang akan kita gunakan untuk menyalin konten "MyRange".
## Langkah 9: Salin Rentang Bernama ke Rentang Kedua
Sekarang tibalah bagian yang menarik—menyalin data dari rentang pertama ke rentang kedua!
```csharp
range2.Copy(range1);
```
Perintah ini secara efektif mentransfer data Anda dari "MyRange" ke "testrange". Ini seperti membuat fotokopi dokumen penting—mudah dan efisien!
## Langkah 10: Simpan Buku Kerja
Terakhir, simpan buku kerja Anda ke direktori keluaran yang ditentukan.
```csharp
workbook.Save(outputDir + "outputCopyNamedRanges.xlsx");
```
Baris ini menyimpan buku kerja, yang memuat semua perubahan Anda, ke dalam file bernama "outputCopyNamedRanges.xlsx". Ini adalah akhir dari usaha pengodean Anda!
## Langkah 11: Konfirmasi Eksekusi
Anda dapat memberikan umpan balik ke konsol untuk mengonfirmasi semuanya berjalan lancar.
```csharp
Console.WriteLine("CopyNamedRanges executed successfully.");
```
Menjalankan baris ini akan menunjukkan bahwa kode Anda dijalankan tanpa hambatan apa pun.
## Kesimpulan
Nah, itu dia! Anda telah berhasil menyalin rentang bernama di Excel menggunakan Aspose.Cells for .NET, langkah demi langkah. Proses ini memungkinkan Anda untuk mengotomatiskan tugas Excel dan mengelola data Anda dengan lebih efektif. Dengan sedikit latihan, Anda akan dapat menjalankan tugas otomatisasi Excel yang lebih canggih dalam waktu singkat.
## Pertanyaan yang Sering Diajukan
### Apa itu Aspose.Cells untuk .NET?
Aspose.Cells adalah pustaka .NET yang memungkinkan pengembang untuk membuat, memanipulasi, dan mengonversi file Excel secara terprogram.
### Apakah saya perlu menginstal Excel untuk menggunakan Aspose.Cells?
Tidak, Aspose.Cells bekerja secara independen dari Excel, meskipun menginstalnya dapat berguna untuk menguji keluaran secara visual.
### Bisakah saya menggunakan Aspose.Cells dengan bahasa pemrograman lain?
Aspose.Cells menawarkan berbagai versi untuk berbagai bahasa, termasuk Java dan Python.
### Bagaimana cara mendapatkan dukungan teknis untuk Aspose.Cells?
 Anda dapat mengunjungi[Forum Dukungan Aspose](https://forum.aspose.com/c/cells/9) untuk bantuan atau mengajukan pertanyaan.
### Di mana saya dapat menemukan dokumentasinya?
 Itu[Dokumentasi Aspose.Cells](https://reference.aspose.com/cells/net/) menyediakan informasi lengkap tentang semua kelas dan metode yang tersedia.