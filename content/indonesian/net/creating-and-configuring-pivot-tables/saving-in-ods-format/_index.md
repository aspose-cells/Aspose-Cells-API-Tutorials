---
title: Menyimpan Tabel Pivot dalam Format ODS Secara Terprogram di .NET
linktitle: Menyimpan Tabel Pivot dalam Format ODS Secara Terprogram di .NET
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Pelajari cara menyimpan Tabel Pivot dalam format ODS menggunakan Aspose.Cells untuk .NET dengan panduan langkah demi langkah ini.
type: docs
weight: 25
url: /id/net/creating-and-configuring-pivot-tables/saving-in-ods-format/
---
## Perkenalan
Dalam hal mengelola data dalam spreadsheet, tidak ada yang dapat menandingi kekuatan Pivot Table. Pivot Table merupakan alat yang tepat untuk meringkas, menganalisis, dan menyajikan kumpulan data yang kompleks. Hari ini, kita akan membahas penggunaan Aspose.Cells untuk .NET guna menyimpan Pivot Table dalam format ODS. Baik Anda seorang pengembang berpengalaman atau baru mulai menggunakan .NET, panduan ini akan sangat mudah dipahami. 
Mari kita mulai!
## Prasyarat
Sebelum kita masuk ke kode, ada beberapa hal penting yang Anda perlukan:
### 1. Pengetahuan Dasar tentang .NET
Memiliki pemahaman dasar tentang .NET dan konsep pemrogramannya akan membantu Anda mengikutinya dengan mudah.
### 2. Aspose.Cells untuk .NET
 Anda perlu menginstal Aspose.Cells untuk .NET. Anda dapat mengunduhnya dari[Aspose merilis halaman](https://releases.aspose.com/cells/net/) Versi uji coba juga tersedia[Di Sini](https://releases.aspose.com/).
### 3. Lingkungan Pengembangan
Pastikan Anda memiliki IDE seperti Visual Studio tempat Anda dapat menulis dan menguji kode .NET Anda.
### 4. Sedikit Kesabaran
Seperti halnya usaha pengkodean apa pun, kesabaran adalah kuncinya. Jangan khawatir jika sesuatu tidak berjalan sempurna pada awalnya; debugging adalah bagian dari prosesnya.
## Paket Impor
Untuk bekerja dengan Aspose.Cells, Anda perlu mengimpor namespace yang diperlukan. Tambahkan perintah using berikut di awal berkas kode Anda:
```csharp
using System;
using Aspose.Cells.Pivot;
```
Baris ini memungkinkan Anda mengakses semua fungsionalitas dalam pustaka Aspose.Cells, sehingga proses pengkodean Anda mudah.
Sekarang, mari kita uraikan proses tersebut menjadi beberapa langkah yang dapat dikelola.
## Langkah 1: Siapkan Direktori Output Anda
Pertama, Anda perlu menentukan di mana Anda ingin menyimpan berkas ODS. Ini adalah penetapan jalur direktori yang sederhana.
```csharp
string outputDir = "Your Document Directory";
```
 Pada baris ini, ganti`"Your Document Directory"` dengan jalur tempat Anda ingin menyimpan berkas.
## Langkah 2: Buat Buku Kerja Baru
Berikutnya, Anda akan membuat objek Buku Kerja baru, yang akan menampung semua data dan struktur Anda, termasuk Tabel Pivot.
```csharp
Workbook workbook = new Workbook();
```
Di sini, Anda pada dasarnya memulai dari awal—anggaplah ini sebagai kanvas kosong tempat Anda akan menciptakan karya agung Anda.
## Langkah 3: Akses Lembar Kerja
Sekarang setelah kita memiliki buku kerja, kita perlu mulai mengerjakan lembar kerja kita. Aspose.Cells memungkinkan Anda mengakses lembar kerja pertama yang tersedia dengan mudah.
```csharp
Worksheet sheet = workbook.Worksheets[0];
```
Baris ini membawa kita ke lembar pertama, siap untuk entri data.
## Langkah 4: Mengisi Sel dengan Data
Sekarang saatnya mengisi lembar kerja kita dengan beberapa data. Kita akan menggunakan contoh sederhana dari data penjualan olahraga. 
Berikut ini cara Anda dapat mengatur nilai di berbagai sel:
```csharp
Cells cells = sheet.Cells;
cells["A1"].PutValue("Sport");
cells["B1"].PutValue("Quarter");
cells["C1"].PutValue("Sales");
cells["A2"].PutValue("Golf");
cells["A3"].PutValue("Golf");
cells["A4"].PutValue("Tennis");
cells["A5"].PutValue("Tennis");
cells["A6"].PutValue("Tennis");
cells["A7"].PutValue("Tennis");
cells["A8"].PutValue("Golf");
cells["B2"].PutValue("Qtr3");
cells["B3"].PutValue("Qtr4");
cells["B4"].PutValue("Qtr3");
cells["B5"].PutValue("Qtr4");
cells["B6"].PutValue("Qtr3");
cells["B7"].PutValue("Qtr4");
cells["B8"].PutValue("Qtr3");
cells["C2"].PutValue(1500);
cells["C3"].PutValue(2000);
cells["C4"].PutValue(600);
cells["C5"].PutValue(1500);
cells["C6"].PutValue(4070);
cells["C7"].PutValue(5000);
cells["C8"].PutValue(6430);
```
Pada baris ini, kita mendefinisikan judul dan mengisi data penjualan. Anggap langkah ini seperti mengisi persediaan di dapur sebelum memasak makanan; semakin baik bahan-bahan (data) yang Anda gunakan, semakin baik pula makanan Anda (analisis).
## Langkah 5: Buat Tabel Pivot
Sekarang tibalah bagian yang menyenangkan—membuat Tabel Pivot! Berikut cara menambahkannya ke lembar kerja Anda:
```csharp
PivotTableCollection pivotTables = sheet.PivotTables;
// Menambahkan PivotTable ke lembar kerja
int index = pivotTables.Add("=A1:C8", "E3", "PivotTable2");
```
 Dalam cuplikan ini, kami menentukan rentang data untuk Tabel Pivot dan tempat untuk meletakkannya di lembar kerja. Rentang data`=A1:C8` mencakup area tempat data kami berada.
## Langkah 6: Sesuaikan Tabel Pivot Anda
Selanjutnya, Anda perlu menyesuaikan Tabel Pivot sesuai kebutuhan. Hal ini meliputi pengaturan apa yang ditampilkan, bagaimana data tersebut dikategorikan, dan bagaimana data tersebut dihitung.
```csharp
PivotTable pivotTable = pivotTables[index];
// Tidak menampilkan total keseluruhan untuk baris.
pivotTable.RowGrand = false;
// Menyeret bidang pertama ke area baris.
pivotTable.AddFieldToArea(PivotFieldType.Row, 0);
// Menyeret bidang kedua ke area kolom.
pivotTable.AddFieldToArea(PivotFieldType.Column, 1);
// Menyeret bidang ketiga ke area data.
pivotTable.AddFieldToArea(PivotFieldType.Data, 2);
pivotTable.CalculateData();
```
Di sini, Anda memutuskan bidang data mana yang akan diringkas dan bagaimana bidang tersebut harus direpresentasikan. Ini seperti menyiapkan meja untuk pesta makan malam Anda; Anda memutuskan apa yang paling cocok dan bagaimana menyajikannya.
## Langkah 7: Simpan Buku Kerja Anda
Akhirnya, Anda siap menyimpan pekerjaan Anda ke dalam format ODS yang diinginkan. Berikut cara melakukannya:
```csharp
workbook.Save(outputDir + "PivotTableSaveInODS_out.ods");
```
Dengan langkah ini, Anda menyelesaikan proyek Anda dan mengamankannya di direktori pilihan Anda—hasil akhir yang memuaskan!
## Langkah 8: Verifikasi Output Anda
Terakhir, sebaiknya periksa apakah prosesnya berhasil diselesaikan. Anda dapat menambahkan pesan konsol sederhana:
```csharp
Console.WriteLine("PivotTableSaveInODS executed successfully.");
```
Pesan ini akan muncul di konsol Anda untuk mengonfirmasi bahwa semuanya berjalan lancar. Seperti seorang koki yang memeriksa apakah semuanya sudah matang sempurna sebelum disajikan!
## Kesimpulan 
Nah, itu dia! Anda tidak hanya membuat Tabel Pivot menggunakan Aspose.Cells, tetapi juga menyimpannya dalam format ODS. Panduan ini memandu Anda melalui setiap langkah, memastikan Anda dibekali dengan pengetahuan dan keyakinan untuk menangani tugas serupa di masa mendatang.
## Pertanyaan yang Sering Diajukan
### Apa itu Aspose.Cells?
Aspose.Cells adalah pustaka canggih yang memungkinkan Anda membuat dan memanipulasi file Excel dalam aplikasi .NET.
### Bisakah saya menggunakan Aspose.Cells secara gratis?
 Ya, Anda dapat mengunduh versi uji coba gratis dari[Situs web Aspose](https://releases.aspose.com/).
### Format apa yang didukung Aspose.Cells?
Mendukung banyak format, termasuk XLSX, XLS, ODS, PDF, dan banyak lainnya.
### Bagaimana cara mendapatkan dukungan untuk Aspose.Cells?
 Anda dapat menemukan bantuan di[Forum Dukungan Aspose](https://forum.aspose.com/c/cells/9).
### Apakah ada lisensi sementara yang tersedia?
 Ya, Anda dapat mengajukan lisensi sementara melalui situs Aspose[Di Sini](https://purchase.aspose.com/temporary-license/).