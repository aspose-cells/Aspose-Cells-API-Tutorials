---
title: Buat Bookmark PDF untuk Lembar Bagan di Aspose.Cells
linktitle: Buat Bookmark PDF untuk Lembar Bagan di Aspose.Cells
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Pelajari cara membuat penanda PDF untuk lembar bagan di Aspose.Cells untuk .NET dengan panduan langkah demi langkah yang komprehensif ini.
type: docs
weight: 13
url: /id/net/rendering-and-export/create-pdf-bookmark-entry-for-chart-sheet/
---
## Perkenalan
Aspose.Cells untuk .NET memungkinkan pengembang untuk memanipulasi file Excel secara terprogram. Salah satu fiturnya yang praktis adalah kemampuan untuk membuat penanda PDF untuk lembar bagan individual. Tutorial ini akan memandu Anda melalui proses ini langkah demi langkah, sehingga mudah diikuti, terlepas dari pengalaman pemrograman Anda. Ambil editor kode Anda, dan mari kita mulai!
## Prasyarat
Sebelum kita mulai, mari pastikan Anda memiliki semua yang perlu diikuti:
1.  Aspose.Cells untuk .NET: Anda memerlukan pustaka Aspose.Cells. Jika Anda belum memilikinya, Anda dapat mengunduhnya dari[Di Sini](https://releases.aspose.com/cells/net/).
2. Visual Studio atau IDE .NET apa pun: Anda memerlukan lingkungan pengembangan tempat Anda dapat menulis dan mengeksekusi kode C#.
3. Pemahaman Dasar tentang C#: Sementara kami akan memandu Anda melalui setiap langkah, pengetahuan dasar tentang pengkodean C# akan berguna.
4. Contoh Berkas Excel: Dapatkan contoh berkas Excel yang berisi bagan. Anda dapat membuatnya sendiri atau menggunakan contoh berkas untuk latihan ini.
Jika prasyarat ini terpenuhi, Anda siap membuat penanda PDF untuk lembar bagan dengan mudah!
## Paket Impor
Sekarang setelah kita menyiapkan semua prasyarat, mari kita mulai kodenya. Sebelum Anda dapat mulai memanipulasi file Excel, Anda perlu mengimpor paket yang diperlukan. Berikut cara melakukannya:
### Siapkan Lingkungan Pengembangan Anda
1. Buat Proyek Baru: Buka Visual Studio dan buat aplikasi konsol C# baru. Sebut saja “AsposePDFBookmarkExample”.
2. Tambahkan Referensi Aspose.Cells: Klik kanan pada proyek Anda di Solution Explorer, pilih "Manage NuGet Packages," dan cari "Aspose.Cells". Instal versi terbaru.
3. Tambahkan Petunjuk Penggunaan:
 Di dalam kamu`Program.cs` file, tambahkan baris berikut di bagian atas:
```csharp
using System;
using System.Collections;
using System.Linq;
using System.Text;
using Aspose.Cells;
using Aspose.Cells.Rendering;
```
Paket-paket ini memungkinkan Anda bekerja dengan berkas Excel dan mengolahnya menjadi PDF dengan penanda halaman.
Mari kita bahas kode untuk membuat bookmark PDF. Kita akan bahas setiap bagian langkah demi langkah.
## Langkah 1: Tentukan Jalur Direktori Anda
Untuk mengatur kode Anda, mari tentukan di mana file kita berada.
```csharp
string sourceDir = "Your Document Directory"; // misalnya, @"C:\Documents\"
string outputDir = "Your Document Directory"; // misalnya, @"C:\Documents\Output\"
```
 Mengganti`Your Document Directory` dengan jalur sebenarnya tempat file Excel contoh Anda disimpan dan tempat Anda ingin menyimpan PDF keluaran.
## Langkah 2: Muat Buku Kerja Excel
Berikutnya, kita perlu memuat buku kerja Excel yang ingin Anda manipulasi.
```csharp
Workbook wb = new Workbook(sourceDir + "sampleCreatePdfBookmarkEntryForChartSheet.xlsx");
```
 Di sini kita membuat sebuah instance dari`Workbook` kelas, memuat contoh berkas Excel kami. Pastikan nama berkas sesuai dengan berkas Anda yang sebenarnya.
## Langkah 3: Akses Lembar Kerja
Setelah buku kerja dimuat, Anda dapat mengakses lembar kerjanya. 
```csharp
Worksheet sheet1 = wb.Worksheets[0];
Worksheet sheet2 = wb.Worksheets[1];
Worksheet sheet3 = wb.Worksheets[2];
Worksheet sheet4 = wb.Worksheets[3];
```
Kode tersebut merujuk pada empat lembar kerja dalam buku kerja. Pastikan berkas Excel Anda memiliki setidaknya empat lembar.
## Langkah 4: Buat Entri Bookmark PDF
Di sinilah keajaiban terjadi! Kami akan membuat entri penanda buku untuk setiap lembar.
```csharp
PdfBookmarkEntry ent1 = new PdfBookmarkEntry {
    Destination = sheet1.Cells["A1"],
    Text = "Bookmark-I"
};
PdfBookmarkEntry ent2 = new PdfBookmarkEntry {
    Destination = sheet2.Cells["A1"],
    Text = "Bookmark-II-Chart1"
};
PdfBookmarkEntry ent3 = new PdfBookmarkEntry {
    Destination = sheet3.Cells["A1"],
    Text = "Bookmark-III"
};
PdfBookmarkEntry ent4 = new PdfBookmarkEntry {
    Destination = sheet4.Cells["A1"],
    Text = "Bookmark-IV-Chart2"
};
```
 Setiap`PdfBookmarkEntry`Objek memiliki sel tujuan dan label teks. Pengaturan ini akan membuat penanda dalam PDF yang sesuai dengan area dalam lembar Excel.
## Langkah 5: Atur Entri Bookmark
Untuk membuat struktur hierarki penanda buku, kita perlu mengaturnya.
```csharp
ArrayList lst = new ArrayList();
ent1.SubEntry = lst;
lst.Add(ent2);
lst.Add(ent3);
lst.Add(ent4);
```
Kode ini menambahkan penanda kedua, ketiga, dan keempat sebagai sub-entri di bawah penanda pertama. Sekarang, saat Anda mengklik "Bookmark-I" di PDF, Anda akan diarahkan ke penanda lainnya.
## Langkah 6: Buat Opsi Penyimpanan PDF dengan Entri Bookmark
Sekarang, mari kita persiapkan pilihan penyimpanan PDF dengan bookmark kita.
```csharp
PdfSaveOptions opts = new PdfSaveOptions();
opts.Bookmark = ent1;
```
 Itu`PdfSaveOptions` konfigurasi memungkinkan kita untuk menyertakan penanda saat PDF disimpan.
## Langkah 7: Simpan PDF Output
Akhirnya, waktunya menyimpan pekerjaan Anda!
```csharp
wb.Save(outputDir + "outputCreatePdfBookmarkEntryForChartSheet.pdf", opts);
```
Perintah ini menyimpan buku kerja ke dalam berkas PDF di jalur keluaran yang ditentukan, lengkap dengan penanda halaman yang praktis.
## Langkah 8: Konfirmasi Eksekusi
Terakhir, mari kita cetak pesan sukses untuk mengonfirmasi semuanya berjalan lancar.
```csharp
Console.WriteLine("CreatePdfBookmarkEntryForChartSheet executed successfully.");
```
## Kesimpulan 
Membuat penanda PDF untuk lembar bagan menggunakan Aspose.Cells for .NET adalah proses mudah yang dapat meningkatkan kegunaan dokumen Excel Anda. Hanya dengan beberapa baris kode, Anda dapat menavigasi PDF dengan mudah, menghemat waktu yang berharga, dan meningkatkan alur kerja Anda.
Baik Anda membuat laporan atau mengelola kumpulan data yang kompleks, penanda ini membuat akses informasi menjadi jauh lebih mudah. Jadi, lanjutkan, kendalikan dokumen Anda dan perkaya dengan fitur fantastis ini!
## Pertanyaan yang Sering Diajukan
### Apa itu Aspose.Cells?
Aspose.Cells adalah pustaka .NET canggih yang dirancang untuk menangani manipulasi file Excel, termasuk membaca, menulis, dan mengonversi lembar kerja.
### Bisakah saya membuat penanda untuk sel tertentu saja?
Ya, Anda dapat mengatur tujuan penanda buku ke sel mana saja di lembar kerja Anda.
### Apakah saya memerlukan lisensi untuk menggunakan Aspose.Cells?
Sementara Aspose.Cells menawarkan uji coba gratis, lisensi berbayar diperlukan untuk fungsionalitas penuh untuk penggunaan produksi.
### Bisakah saya membuat penanda halaman untuk lebih dari empat lembar?
Tentu saja! Anda dapat membuat penanda halaman untuk sebanyak mungkin lembar sesuai keinginan dengan mengikuti struktur kode yang serupa.
### Di mana saya dapat menemukan bantuan lebih lanjut?
 Anda dapat memeriksa[Forum dukungan komunitas Aspose](https://forum.aspose.com/c/cells/9) untuk masalah atau pertanyaan apa pun.