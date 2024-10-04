---
title: Buat Bagan Garis
linktitle: Buat Bagan Garis
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Buat diagram garis yang menakjubkan menggunakan Aspose.Cells for .NET. Ikuti panduan langkah demi langkah kami untuk memvisualisasikan data Anda secara efektif.
type: docs
weight: 11
url: /id/net/manipulating-chart-types/create-line-chart/
---
## Perkenalan

Apakah Anda siap memvisualisasikan data Anda dengan sangat jelas? Bagan garis adalah cara yang fantastis untuk menampilkan tren dari waktu ke waktu atau hubungan antara dua variabel. Baik Anda mengelola data untuk proyek bisnis atau menganalisis metrik pribadi, kemampuan untuk membuat bagan garis secara terprogram dapat menghemat waktu Anda dan memungkinkan fleksibilitas yang lebih besar. Dalam panduan ini, kami akan memandu Anda melalui setiap langkah pembuatan bagan garis menggunakan Aspose.Cells untuk .NET. Siap untuk mencobanya? Mari kita mulai!

## Prasyarat

Sebelum kita masuk ke inti pembuatan diagram garis, mari pastikan Anda siap untuk mengikutinya:

1. Visual Studio: Pastikan Anda telah menginstal Visual Studio di komputer Anda karena ini adalah salah satu IDE paling populer untuk pengembangan .NET.
2.  Pustaka Aspose.Cells untuk .NET: Anda memerlukan pustaka Aspose.Cells, yang dapat Anda unduh dari[Di Sini](https://releases.aspose.com/cells/net/).
3. Pengetahuan Dasar C#: Keakraban dengan bahasa pemrograman C# akan membantu Anda memahami contoh dan cuplikan kode dengan lebih baik.
4. .NET Framework atau .NET Core: Pengaturan dasar dari salah satu framework karena ini akan menjadi fondasi untuk aplikasi kita.

Setelah Anda menyelesaikan prasyarat ini, Anda siap membuat beberapa bagan!

## Paket Impor

Setelah kita menyiapkan lingkungan, kita perlu mengimpor paket yang diperlukan ke dalam kode C#. Sama seperti saat Anda mengumpulkan peralatan sebelum memulai proyek, mengimpor paket sangat penting untuk memastikan Anda memiliki semua yang dibutuhkan.

Berikut cara melakukannya:

```csharp
using System;
using System.IO;

using Aspose.Cells;
using Aspose.Cells.Drawing;
using System.Drawing;
using Aspose.Cells.Charts;
```

 Baris ini mengimpor`Aspose.Cells` namespace, yang berisi semua kelas dan metode yang akan kita gunakan untuk membuat diagram garis.

Sekarang, mari kita uraikan seluruh proses menjadi langkah-langkah yang sederhana dan mudah dipahami. Setiap langkah akan memandu Anda melalui alur logis pembuatan diagram garis menggunakan Aspose.Cells for .NET.

## Langkah 1: Siapkan Direktori Output

Langkah pertama adalah menentukan di mana Anda ingin menyimpan berkas output Anda. Ini seperti menyiapkan ruang kerja Anda sebelum Anda mulai bekerja. 

```csharp
// Direktori keluaran
string outputDir = "Your Output Directory";
```
 Mengganti`"Your Output Directory"`dengan jalur sebenarnya tempat Anda ingin menyimpan file Excel yang dihasilkan.

## Langkah 2: Membuat Instansiasi Objek Buku Kerja

Selanjutnya, kita perlu membuat contoh buku kerja baru. Anggaplah Buku Kerja sebagai kanvas tempat kreativitas Anda mengalir. 

```csharp
// Membuat instance objek Buku Kerja
Workbook workbook = new Workbook();
```
Baris ini menginisialisasi buku kerja baru yang akan menampung semua data dan visual Anda.

## Langkah 3: Akses Lembar Kerja

Dalam buku kerja yang baru kita buat, kita perlu mendapatkan referensi ke lembar kerja tempat kita akan memasukkan data. Jika buku kerja adalah kanvas kita, maka lembar kerja adalah palet kita.

```csharp
// Mendapatkan referensi lembar kerja yang baru ditambahkan dengan meneruskan indeks lembar kerjanya
Worksheet worksheet = workbook.Worksheets[0];
```
 Di sini kita mengakses lembar kerja pertama (indeks`0`).

## Langkah 4: Tambahkan Nilai Sampel ke Sel

Sekarang tibalah bagian yang menyenangkan! Kita akan memasukkan beberapa contoh nilai ke dalam lembar kerja kita. Data ini akan menjadi dasar bagi diagram garis kita. 

```csharp
// Menambahkan nilai sampel ke sel
worksheet.Cells["A1"].PutValue(50);
worksheet.Cells["A2"].PutValue(100);
worksheet.Cells["A3"].PutValue(150);
worksheet.Cells["B1"].PutValue(4);
worksheet.Cells["B2"].PutValue(20);
worksheet.Cells["B3"].PutValue(50);
```
Dalam cuplikan ini, kami menambahkan nilai ke sel di kolom A dan B. Kolom A mewakili nilai sumbu X, sedangkan kolom B mewakili nilai sumbu Y.

## Langkah 5: Tambahkan Bagan Garis ke Lembar Kerja

Selanjutnya, kita akan memperkenalkan diagram garis ke lembar kerja. Di sinilah data Anda akan benar-benar menjadi nyata!

```csharp
// Menambahkan bagan ke lembar kerja
int chartIndex = worksheet.Charts.Add(Aspose.Cells.Charts.ChartType.Line, 5, 0, 25, 10);
```
Di sini, kami menambahkan diagram garis di lokasi yang ditentukan. Parameter (5, 0, 25, 10) menentukan posisi dan ukuran diagram dalam lembar kerja.

## Langkah 6: Akses Instansi Bagan Baru

Setelah kita menambahkan bagan, waktunya untuk mendapatkan objek bagan yang baru dibuat. 

```csharp
// Mengakses contoh grafik yang baru ditambahkan
Aspose.Cells.Charts.Chart chart = worksheet.Charts[chartIndex];
```
Kode ini menghubungkan kita ke bagan sehingga kita dapat memanipulasinya lebih lanjut.

## Langkah 7: Tambahkan SeriesCollection ke Bagan

Sekarang kita perlu memberi tahu diagram kita data apa yang akan ditampilkan. Di sinilah kita menentukan sumber data untuk diagram garis kita dengan menambahkan SeriesCollection.

```csharp
// Menambahkan SeriesCollection (sumber data bagan) ke bagan mulai dari sel "A1" hingga "B3"
chart.NSeries.Add("A1:B3", true);
```
Dalam contoh ini, kami memberi tahu bagan untuk menggunakan nilai dalam sel A1 hingga B3.

## Langkah 8: Simpan File Excel

Akhir yang hebat! Setelah semua kerja keras Anda, saatnya menyimpan file Excel dan melihat diagram garis Anda beraksi.

```csharp
// Menyimpan file Excel
workbook.Save(outputDir + "outputHowToCreateLineChart.xlsx");
```
 Baris ini menyimpan buku kerja Anda di direktori keluaran yang ditentukan dengan nama`outputHowToCreateLineChart.xlsx`.

## Langkah 9: Jalankan dan Verifikasi

Akhirnya, Anda sekarang dapat menjalankan kode dan memverifikasi bahwa diagram garis telah berhasil dibuat di direktori keluaran Anda! 

```csharp
Console.WriteLine("HowToCreateLineChart executed successfully.");
```
Ini akan menampilkan pesan pada konsol Anda, yang memberi tahu Anda bahwa semuanya berjalan lancar.

## Kesimpulan

Membuat diagram garis menggunakan Aspose.Cells untuk .NET adalah cara yang efisien untuk membuat data Anda lebih hidup. Dengan mengikuti panduan langkah demi langkah ini, Anda dapat dengan mudah memvisualisasikan tren dan hubungan dalam kumpulan data Anda. Baik Anda seorang pengembang berpengalaman atau baru memulai, Aspose.Cells memberi Anda fleksibilitas dan kekuatan untuk mengotomatiskan tugas visualisasi data Anda. 

## Pertanyaan yang Sering Diajukan

### Apa itu Aspose.Cells untuk .NET?  
Aspose.Cells untuk .NET adalah pustaka hebat yang dirancang untuk mengelola dan memanipulasi file Excel secara terprogram, memungkinkan pengembang untuk membuat, mengedit, dan mengonversi lembar kerja.

### Apakah Aspose.Cells mendukung grafik?  
Ya, Aspose.Cells menyediakan dukungan luas untuk berbagai jenis bagan, termasuk bagan garis, bagan pai, bagan batang, dan banyak lagi.

### Bisakah saya menggunakan Aspose.Cells secara gratis?  
Ya, Anda dapat mengunduh versi uji coba gratis untuk menjelajahi fitur-fiturnya. Untuk penggunaan jangka panjang, pertimbangkan untuk membeli lisensi.

### Apakah ada forum untuk dukungan?  
 Tentu saja! Anda dapat menemukan jawaban dan mengajukan pertanyaan di[Forum Aspose.Cells](https://forum.aspose.com/c/cells/9).

### Bagaimana cara membeli lisensi?  
 Lisensi dapat dibeli dengan mudah melalui[halaman pembelian](https://purchase.aspose.com/buy).