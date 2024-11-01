---
title: Mendeteksi Referensi Sirkular di Excel Secara Terprogram
linktitle: Mendeteksi Referensi Sirkular di Excel Secara Terprogram
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Deteksi referensi melingkar dengan mudah di Excel menggunakan Aspose.Cells for .NET. Ikuti panduan langkah demi langkah kami untuk memastikan perhitungan yang akurat di lembar kerja Anda.
type: docs
weight: 13
url: /id/net/excel-formulas-and-calculation-options/detecting-circular-reference/
---
## Perkenalan
Saat bekerja dengan file Excel, salah satu masalah paling menyebalkan yang mungkin Anda temui adalah referensi melingkar. Ini terjadi saat rumus merujuk kembali ke selnya sendiri, baik secara langsung maupun tidak langsung, sehingga menciptakan lingkaran yang dapat membingungkan mesin kalkulasi Excel. Namun, jangan khawatir! Dengan Aspose.Cells for .NET, Anda dapat mendeteksi referensi melingkar yang mengganggu ini secara terprogram, memastikan spreadsheet Anda tetap berfungsi dan akurat. Dalam panduan ini, kami akan memandu Anda melalui proses ini langkah demi langkah, membuatnya semudah membalik telapak tangan.
## Prasyarat
Sebelum kita menyelami seluk-beluk mendeteksi referensi melingkar, mari pastikan Anda memiliki semua yang dibutuhkan untuk memulai:
1. Visual Studio: Pastikan Anda telah menginstal Visual Studio di komputer Anda. Ini akan menjadi lingkungan pengembangan Anda.
2. .NET Framework: Pastikan Anda menggunakan versi .NET Framework yang kompatibel (setidaknya .NET Framework 4.0).
3.  Pustaka Aspose.Cells: Anda perlu memiliki pustaka Aspose.Cells. Anda dapat mengunduhnya dari[Situs web Aspose](https://releases.aspose.com/cells/net/).
4. Pengetahuan Dasar C#: Keakraban dengan pemrograman C# akan bermanfaat, karena kita akan menulis kode dalam bahasa ini.
5. Berkas Excel: Siapkan berkas Excel yang berisi referensi melingkar untuk pengujian. Anda dapat membuat berkas sederhana atau mengunduh contohnya.
Sekarang setelah prasyaratnya terpenuhi, mari kita lanjut ke bagian yang menyenangkan!
## Paket Impor
Sebelum Anda dapat mulai membuat kode, Anda perlu mengimpor paket-paket yang diperlukan. Berikut cara melakukannya:
### Buat Proyek Baru
- Buka Visual Studio dan buat proyek Aplikasi Konsol C# baru.
### Tambahkan Referensi Aspose.Cells
- Klik kanan pada proyek Anda di Solution Explorer.
- Pilih "Kelola Paket NuGet."
- Cari “Aspose.Cells” dan instal versi terbaru.
### Mengimpor Ruang Nama yang Diperlukan
 Di bagian atas Anda`Program.cs` file, impor namespace yang diperlukan:
```csharp
using System;
using System.Collections;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```

Sekarang setelah semuanya disiapkan, mari selami kode untuk mendeteksi referensi melingkar dalam berkas Excel.
## Langkah 1: Tentukan Direktori Input
Pertama, Anda perlu menentukan direktori tempat file Excel Anda berada. Di sinilah Anda akan memuat file Excel Anda.
```csharp
// Direktori masukan
string sourceDir = "Your Document Directory";
```
 Mengganti`"Your Document Directory"` dengan jalur sebenarnya ke berkas Excel Anda.
## Langkah 2: Muat Buku Kerja dengan LoadOptions
Berikutnya, Anda akan memuat buku kerja Excel Anda. Di sinilah keajaiban dimulai!
```csharp
LoadOptions loadOptions = new LoadOptions();
var objWB = new Aspose.Cells.Workbook(sourceDir + "Circular Formulas.xls", loadOptions);
```
 Di sini, kita membuat contoh baru`LoadOptions` dan memuat buku kerja dari jalur yang ditentukan. Pastikan nama berkas Excel Anda cocok!
## Langkah 3: Aktifkan Pengaturan Iterasi
Untuk memungkinkan referensi melingkar, Anda perlu mengaktifkan pengaturan iterasi dalam buku kerja.
```csharp
objWB.Settings.Iteration = true;
```
Ini memberitahu Aspose.Cells untuk mengizinkan referensi melingkar selama perhitungan.
## Langkah 4: Buat Opsi Perhitungan dan Monitor Sirkular
Sekarang, mari kita buat opsi perhitungan dan monitor melingkar khusus kita.
```csharp
CalculationOptions copts = new CalculationOptions();
CircularMonitor cm = new CircularMonitor();
copts.CalculationMonitor = cm;
```
 Di sini, kita membuat sebuah instance dari`CalculationOptions` dan kebiasaan`CircularMonitor`Monitor ini akan membantu melacak referensi melingkar yang ditemukan selama perhitungan.
## Langkah 5: Hitung Rumusnya
Sekarang, saatnya menghitung rumus di buku kerja Anda.
```csharp
objWB.CalculateFormula(copts);
```
Baris ini menjalankan kalkulasi dan memeriksa referensi melingkar.
## Langkah 6: Hitung Referensi Sirkuler
Setelah perhitungan, Anda dapat menghitung berapa banyak referensi melingkar yang ditemukan.
```csharp
long lngCircularRef = cm.circulars.Count;
Console.WriteLine("Circular References found - " + lngCircularRef);
```
Ini akan menampilkan jumlah referensi melingkar yang terdeteksi dalam berkas Excel Anda.
## Langkah 7: Menampilkan Hasil
Terakhir, mari kita tampilkan hasilnya dan pastikan metode kita berhasil dijalankan.
```csharp
Console.WriteLine("DetectCircularReference executed successfully.\r\n");
```
## Langkah 8: Terapkan Kelas CircularMonitor
 Untuk menyelesaikan prosesnya, Anda perlu menerapkan`CircularMonitor` kelas. Kelas ini akan mewarisi dari`AbstractCalculationMonitor` dan menangani deteksi referensi melingkar.
```csharp
public class CircularMonitor : AbstractCalculationMonitor
{
    public ArrayList circulars = new ArrayList();
    public ArrayList Circulars { get { return circulars; } }
    public override bool OnCircular(IEnumerator circularCellsData)
    {
        CalculationCell cc = null;
        ArrayList cur = new ArrayList();
        while (circularCellsData.MoveNext())
        {
            cc = (CalculationCell)circularCellsData.Current;
            cur.Add(cc.Worksheet.Name + "!" + CellsHelper.CellIndexToName(cc.CellRow, cc.CellColumn));
        }
        circulars.Add(cur);
        return true;
    }
}
```
Kelas ini menangkap detail setiap referensi melingkar yang ditemukan, termasuk nama lembar kerja dan indeks sel.
## Kesimpulan
Mendeteksi referensi melingkar di Excel menggunakan Aspose.Cells untuk .NET merupakan proses yang mudah setelah Anda memecahnya menjadi beberapa langkah yang dapat dikelola. Dengan mengikuti panduan ini, Anda dapat dengan mudah mengidentifikasi dan menangani referensi melingkar di lembar kerja Anda, memastikan perhitungan Anda tetap akurat dan andal. Baik Anda seorang pengembang berpengalaman atau baru memulai, Aspose.Cells menyediakan berbagai alat canggih untuk meningkatkan kemampuan manipulasi Excel Anda. 
## Pertanyaan yang Sering Diajukan
### Apa itu referensi melingkar di Excel?
Referensi melingkar terjadi saat rumus merujuk kembali ke selnya sendiri, yang menyebabkan perulangan tak berujung dalam perhitungan.
### Bagaimana cara mendeteksi referensi melingkar secara terprogram?
Anda dapat menggunakan pustaka Aspose.Cells di .NET untuk mendeteksi referensi melingkar secara terprogram dengan menerapkan monitor kalkulasi kustom.
### Apa saja prasyarat untuk menggunakan Aspose.Cells?
Anda perlu menginstal Visual Studio, .NET Framework, dan pustaka Aspose.Cells.
### Bisakah saya menggunakan Aspose.Cells secara gratis?
Ya, Aspose.Cells menawarkan uji coba gratis yang dapat Anda gunakan untuk menjelajahi fitur-fiturnya.
### Di mana saya dapat menemukan informasi lebih lanjut tentang Aspose.Cells?
 Anda dapat mengunjungi[Dokumentasi Aspose.Cells](https://reference.aspose.com/cells/net/) untuk informasi dan contoh terperinci.