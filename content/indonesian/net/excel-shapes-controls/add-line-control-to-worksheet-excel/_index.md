---
title: Tambahkan Kontrol Garis ke Lembar Kerja di Excel
linktitle: Tambahkan Kontrol Garis ke Lembar Kerja di Excel
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Pelajari cara menambahkan dan menyesuaikan kontrol garis dalam lembar kerja Excel menggunakan Aspose.Cells untuk .NET dalam tutorial komprehensif ini.
type: docs
weight: 26
url: /id/net/excel-shapes-controls/add-line-control-to-worksheet-excel/
---
## Perkenalan
Lembar kerja Excel tidak hanya berisi baris dan kolom data; lembar kerja tersebut juga merupakan kanvas untuk visualisasi. Menambahkan kontrol garis dapat meningkatkan cara informasi direpresentasikan dalam lembar kerja Anda, membuat hubungan dan tren menjadi jauh lebih jelas. Gunakan Aspose.Cells untuk .NET, pustaka canggih yang menyederhanakan proses pembuatan dan manipulasi file Excel secara terprogram. Dalam panduan ini, kami akan memandu Anda melalui langkah-langkah untuk menambahkan kontrol garis ke lembar kerja menggunakan Aspose.Cells. Jika Anda siap untuk meningkatkan kemampuan Excel Anda, mari kita mulai!
## Prasyarat
Sebelum Anda mulai menambahkan baris ke lembar kerja Excel Anda, berikut beberapa hal yang Anda perlukan:
1.  Visual Studio: Pastikan Anda telah menginstal Visual Studio di komputer Anda. Jika belum, Anda dapat mengunduhnya dari[situs web](https://visualstudio.microsoft.com/).
2.  Aspose.Cells untuk .NET: Pustaka ini harus dirujuk dalam proyek Anda. Anda dapat menemukan dokumentasi terperinci[Di Sini](https://reference.aspose.com/cells/net/) dan unduh perpustakaannya[Di Sini](https://releases.aspose.com/cells/net/).
3. Pengetahuan Dasar C#: Keakraban dengan pemrograman C# akan membantu Anda memahami kode yang akan kita lihat.
4. Lingkungan Windows: Karena Aspose.Cells dirancang untuk aplikasi .NET, lingkungan Windows lebih disukai.
## Paket Impor
Mari kita siapkan lingkungan pengkodean kita sebelum kita mulai menambahkan beberapa baris ke lembar kerja Excel Anda. Berikut cara mengimpor paket Aspose.Cells yang diperlukan ke dalam proyek Anda.
### Buat Proyek Baru
- Buka Visual Studio.
- Buat proyek Aplikasi Konsol baru. Anda dapat menamainya apa pun yang Anda suka—mungkin "ExcelLineDemo" agar lebih jelas.
### Instal Aspose.Cells
- Buka NuGet Package Manager di Visual Studio (`Tools` ->`NuGet Package Manager` ->`Manage NuGet Packages for Solution`).
-  Pencarian untuk`Aspose.Cells` dan menginstalnya. Tindakan ini akan menambahkan pustaka yang diperlukan ke proyek Anda.
### Impor Namespace
Di bagian atas file program Utama Anda, tambahkan perintah berikut untuk membuat Aspose.Cells dapat diakses:
```csharp
using System.IO;
using Aspose.Cells;
using Aspose.Cells.Drawing;
```
Dengan melakukan ini, Anda sekarang dapat menggunakan semua fungsi dari pustaka Aspose.Cells tanpa menambahkan awalan.
Setelah semuanya siap, saatnya menambahkan beberapa baris ke lembar kerja kita. Kita akan membahas setiap langkah secara terperinci.
## Langkah 1: Siapkan Direktori Dokumen
Sebelum Anda mulai bekerja dengan berkas Excel, Anda perlu menentukan di mana berkas tersebut akan disimpan. Berikut ini cara melakukannya:
```csharp
// Jalur ke direktori dokumen.
string dataDir = "Your Document Directory";
```
 Mengganti`"Your Document Directory"` dengan jalur yang valid pada sistem Anda tempat Anda ingin menyimpan berkas keluaran.
## Langkah 2: Buat Direktori
Merupakan praktik yang baik untuk memastikan direktori tersebut ada. Jika tidak ada, Anda dapat membuatnya dengan kode berikut:
```csharp
//Buat direktori jika belum ada.
bool IsExists = System.IO.Directory.Exists(dataDir);
if (!IsExists)
    System.IO.Directory.CreateDirectory(dataDir);
```
Potongan kode ini memeriksa apakah direktori yang ditentukan ada dan membuatnya jika tidak ada. Ini seperti memeriksa ransel Anda sebelum berangkat mendaki—Anda ingin memastikan Anda memiliki semua yang Anda butuhkan!
## Langkah 3: Buat Buku Kerja Baru
Sekarang, mari buat buku kerja Excel baru. Ini adalah kanvas tempat Anda akan menggambar garis.
```csharp
// Buat Buku Kerja baru.
Workbook workbook = new Workbook();
```
 Membuat contoh baru dari`Workbook` memberi Anda berkas Excel baru dan kosong untuk digunakan.
## Langkah 4: Akses Lembar Kerja Pertama
Setiap buku kerja memiliki setidaknya satu lembar kerja, dan kita akan menggunakan lembar pertama untuk baris kita.
```csharp
// Dapatkan lembar kerja pertama dalam buku.
Worksheet worksheet = workbook.Worksheets[0];
```
Di sini, kami memilih lembar kerja pertama dengan mengaksesnya melalui`Worksheets` koleksi dari`Workbook`.
## Langkah 5: Tambahkan Baris Pertama
Mari kita mulai menambahkan beberapa baris. Baris pertama akan bergaya solid.
```csharp
// Tambahkan baris baru ke lembar kerja.
Aspose.Cells.Drawing.LineShape line1 = worksheet.Shapes.AddLine(5, 0, 1, 0, 0, 250);
```
Dalam pernyataan ini:
- `AddLine` metode menambahkan garis yang dimulai pada koordinat`(5, 0)` dan berakhir di`(1, 0)` memanjang hingga ketinggian`250`.
-  Koordinat`(5, 0)` mewakili posisi awal pada lembar kerja, sementara`(1, 0, 0, 250)` menunjukkan jarak akhir.
## Langkah 6: Tetapkan Properti Garis
Sekarang, mari kita personalisasikan garisnya sedikit—atur gaya dan penempatan tanda hubungnya.
```csharp
// Mengatur gaya garis putus-putus
line1.Line.DashStyle = MsoLineDashStyle.Solid;
// Atur penempatannya.
line1.Placement = PlacementType.FreeFloating;
```
 Di sini, kami memberi tahu garis untuk tetap berada di satu tempat terlepas dari perubahan dalam struktur lembar kerja dengan menggunakan`PlacementType.FreeFloating`.
## Langkah 7: Tambahkan Baris Tambahan
Mari tambahkan baris kedua dengan gaya yang berbeda, menggunakan gaya putus-putus.
```csharp
// Tambahkan baris lain ke lembar kerja.
Aspose.Cells.Drawing.LineShape line2 = worksheet.Shapes.AddLine(7, 0, 1, 0, 85, 250);
// Mengatur gaya garis putus-putus.
line2.Line.DashStyle = MsoLineDashStyle.DashLongDash;
// Tetapkan bobot garisnya.
line2.Line.Weight = 4;
// Atur penempatannya.
line2.Placement = PlacementType.FreeFloating;
```
 Perhatikan bagaimana kami menyesuaikan penempatan dan mengubah gaya tanda hubung menjadi`DashLongDash`Properti berat memungkinkan Anda mengontrol ketebalan garis.
## Langkah 8: Tambahkan Baris Ketiga
Satu garis lagi! Mari tambahkan garis utuh untuk melengkapi gambar kita.
```csharp
// Tambahkan baris ketiga ke lembar kerja.
Aspose.Cells.Drawing.LineShape line3 = worksheet.Shapes.AddLine(13, 0, 1, 0, 0, 250);
```
Sekali lagi, kita mengonfigurasikan propertinya mirip dengan cara kita mengatur baris sebelumnya.
## Langkah 9: Sembunyikan Garis Kisi
Untuk memberi gambar kita tampilan yang lebih bersih, mari sembunyikan garis kisi pada lembar kerja.
```csharp
// Buat garis kisi tidak terlihat pada lembar kerja pertama.
workbook.Worksheets[0].IsGridlinesVisible = false;
```
Menyembunyikan garis kisi membantu pengguna lebih fokus pada garis sebenarnya yang Anda tambahkan, mirip seperti cara seorang pelukis membersihkan area di sekitar kanvasnya untuk menghindari gangguan.
## Langkah 10: Simpan Buku Kerja
Terakhir, mari kita simpan buku kerja kita agar kerja keras kita tidak sia-sia!
```csharp
// Simpan berkas excel.
workbook.Save(dataDir + "book1.out.xls");
```
 Anda dapat memberi nama file output apa pun yang Anda suka—pastikan diakhiri dengan`.xls` atau ekstensi file Excel lain yang didukung.
## Kesimpulan
Selamat! Anda telah berhasil mempelajari cara menambahkan kontrol baris ke lembar kerja Excel menggunakan Aspose.Cells untuk .NET. Hanya dengan beberapa baris kode, Anda dapat menyempurnakan file Excel Anda, menawarkan representasi visual data Anda yang dapat membantu mengomunikasikan wawasan secara lebih efektif. Baik Anda ingin membuat laporan, presentasi, atau alat analitis, menguasai pustaka seperti Aspose.Cells dapat membuat alur kerja Anda jauh lebih lancar dan lebih efisien.
## Pertanyaan yang Sering Diajukan
### Apa itu Aspose.Cells untuk .NET?
Aspose.Cells untuk .NET adalah pustaka yang memungkinkan pengembang untuk membuat, memanipulasi, dan mengonversi file Excel tanpa perlu menggunakan Microsoft Excel.
### Bisakah saya menambahkan bentuk selain garis?
Ya, Aspose.Cells menawarkan berbagai bentuk seperti persegi panjang, elips, dan banyak lagi. Anda dapat membuatnya dengan mudah menggunakan metode serupa.
### Apakah Aspose.Cells gratis untuk digunakan?
 Aspose.Cells adalah pustaka berbayar, tetapi Anda dapat memulai dengan[uji coba gratis](https://releases.aspose.com/) untuk menjelajahi fitur-fiturnya.
### Bisakah saya menyesuaikan warna garis?
 Tentu saja! Anda dapat mengatur properti warna garis menggunakan garis`LineColor` milik.
### Di mana saya dapat meminta dukungan teknis?
 Anda bisa mendapatkan dukungan dari[Forum Aspose](https://forum.aspose.com/c/cells/9) tempat anggota komunitas dan anggota tim Aspose membantu pengguna.