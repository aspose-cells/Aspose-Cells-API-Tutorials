---
title: Menonaktifkan Komentar yang Diungkapkan Downlevel saat Menyimpan ke HTML
linktitle: Menonaktifkan Komentar yang Diungkapkan Downlevel saat Menyimpan ke HTML
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Pelajari cara menonaktifkan komentar yang diungkapkan downlevel saat menyimpan buku kerja Excel ke HTML menggunakan Aspose.Cells untuk .NET dengan panduan langkah demi langkah terperinci ini.
type: docs
weight: 11
url: /id/net/loading-and-saving-excel-files-with-options/disabling-downlevel-revealed-comments/
---
## Perkenalan
Pernahkah Anda perlu mengonversi buku kerja Excel ke HTML dan ingin memastikan bahwa komentar yang tidak perlu atau konten tersembunyi tidak terungkap selama proses berlangsung? Di sinilah menonaktifkan komentar yang terungkap di tingkat bawah menjadi berguna. Jika Anda menggunakan Aspose.Cells untuk .NET, Anda memiliki kendali penuh atas cara buku kerja Excel Anda ditampilkan sebagai file HTML. Dalam tutorial ini, kami akan memandu Anda melalui panduan langkah demi langkah sederhana untuk membantu Anda menonaktifkan komentar yang terungkap di tingkat bawah saat menyimpan buku kerja ke HTML. 
Di akhir artikel ini, Anda akan memiliki pemahaman yang jelas tentang cara menggunakan fitur ini dan memastikan keluaran HTML Anda bersih dan bebas komentar.
## Prasyarat
Sebelum kita menyelami panduan langkah demi langkahnya, mari kita bahas beberapa hal yang perlu Anda persiapkan agar dapat mengikutinya dengan lancar:
1.  Aspose.Cells untuk .NET: Anda harus menginstal pustaka Aspose.Cells. Jika Anda belum menginstalnya, Anda dapat mengunduhnya[Di Sini](https://releases.aspose.com/cells/net/).
2. IDE: Lingkungan pengembangan seperti Visual Studio untuk menulis dan mengeksekusi kode C# Anda.
3. Pengetahuan Dasar C#: Keakraban dengan sintaksis C# dan pemrograman berorientasi objek akan membantu Anda mengikuti kode.
4.  Versi Sementara atau Berlisensi: Anda dapat menggunakan uji coba gratis atau mengajukan lisensi sementara dari[Di Sini](https://purchase.aspose.com/temporary-license/)Ini memastikan perpustakaan berfungsi tanpa batasan apa pun.
Sekarang Anda siap, mari langsung saja mulai!
## Mengimpor Ruang Nama
Sebelum kita masuk ke contoh kode, penting untuk menyertakan namespace yang diperlukan untuk Aspose.Cells. Tanpa namespace ini, kode Anda tidak akan dapat mengakses metode dan properti yang diperlukan untuk memanipulasi file Excel.
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Pastikan untuk menempatkan baris ini di bagian atas berkas C# Anda untuk mengimpor namespace Aspose.Cells.
## Langkah 1: Siapkan Jalur Direktori
Sebelum memulai, kita perlu menyiapkan direktori sumber (tempat penyimpanan berkas Excel) dan direktori keluaran (tempat penyimpanan berkas HTML). Ini penting karena Aspose.Cells memerlukan jalur berkas yang tepat untuk mengakses dan menyimpan berkas.
```csharp
// Direktori sumber tempat file Excel Anda berada
string sourceDir = "Your Document Directory";
// Direktori keluaran tempat file HTML yang dihasilkan akan disimpan
string outputDir = "Your Document Directory";
```
 Pada langkah ini, ganti`"Your Document Directory"` dengan jalur berkas yang sebenarnya pada sistem Anda. Anda juga dapat membuat direktori khusus untuk mengatur berkas masukan dan keluaran dengan lebih baik.
## Langkah 2: Muat Buku Kerja Excel
 Pada langkah ini, kita akan memuat buku kerja Excel ke dalam memori sehingga kita dapat memanipulasinya. Untuk tujuan demonstrasi, kita akan menggunakan file contoh bernama`"sampleDisableDownlevelRevealedComments.xlsx"`Anda dapat menggunakan buku kerja apa pun yang Anda sukai.
```csharp
// Muat buku kerja contoh dari direktori sumber
Workbook wb = new Workbook(sourceDir + "sampleDisableDownlevelRevealedComments.xlsx");
```
Ini menciptakan objek Buku Kerja yang berisi semua data dan struktur berkas Excel Anda. Dari sini, Anda dapat memodifikasinya, menerapkan pengaturan, dan akhirnya menyimpannya dalam format yang berbeda.
## Langkah 3: Siapkan Opsi Penyimpanan HTML
Sekarang, kita perlu mengonfigurasi objek HtmlSaveOptions untuk menonaktifkan komentar yang ditampilkan di tingkat bawah. Opsi ini memastikan bahwa komentar atau konten tersembunyi apa pun tidak akan ditampilkan dalam berkas HTML yang dihasilkan.
```csharp
// Buat objek HtmlSaveOptions baru untuk mengonfigurasi opsi penyimpanan
HtmlSaveOptions opts = new HtmlSaveOptions();
// Nonaktifkan komentar yang diungkapkan level bawah
opts.DisableDownlevelRevealedComments = true;
```
 Dengan pengaturan`DisableDownlevelRevealedComments` ke`true`, Anda memastikan bahwa saat Anda menyimpan buku kerja sebagai berkas HTML, semua komentar tingkat bawah akan dinonaktifkan.
## Langkah 4: Simpan Buku Kerja sebagai HTML
Setelah objek HtmlSaveOptions dikonfigurasi, langkah berikutnya adalah menyimpan buku kerja ke HTML menggunakan opsi yang ditentukan. Di sinilah konversi file sebenarnya terjadi.
```csharp
// Simpan buku kerja sebagai file HTML dengan opsi penyimpanan yang ditentukan
wb.Save(outputDir + "outputDisableDownlevelRevealedComments_true.html", opts);
```
Pada baris kode ini, kita menyimpan buku kerja ke direktori keluaran yang Anda tentukan sebelumnya, dan menerapkan pengaturan DisableDownlevelRevealedComments. Hasilnya akan berupa berkas HTML yang bersih tanpa komentar yang tidak diinginkan.
## Langkah 5: Verifikasi dan Jalankan
Terakhir, untuk memastikan semuanya bekerja seperti yang diharapkan, Anda dapat menampilkan pesan sukses pada konsol.
```csharp
// Keluarkan pesan sukses ke konsol
Console.WriteLine("DisableDownlevelRevealedCommentsWhileSavingToHTML executed successfully.");
```
Ini memberi tahu Anda bahwa operasi telah selesai tanpa kesalahan.
## Kesimpulan
Nah, itu dia! Anda telah berhasil mempelajari cara menonaktifkan komentar yang ditampilkan di tingkat bawah saat menyimpan buku kerja Excel ke HTML menggunakan Aspose.Cells untuk .NET. Dengan fitur ini, Anda sekarang dapat mengontrol bagaimana buku kerja Anda ditampilkan sebagai HTML dan menghindari menampilkan konten yang tidak perlu. Baik Anda sedang mengembangkan aplikasi web atau hanya membutuhkan keluaran HTML yang bersih, metode ini memastikan konversi buku kerja Anda akurat dan aman.
Jika Anda merasa tutorial ini bermanfaat, pertimbangkan untuk menjelajahi fitur Aspose.Cells lainnya untuk lebih meningkatkan kemampuan pemrosesan Excel Anda.
## Pertanyaan yang Sering Diajukan
### Apa itu komentar yang terungkap ke tingkat bawah?
Komentar yang ditampilkan di tingkat bawah biasanya digunakan dalam pengembangan web untuk memberikan informasi tambahan bagi peramban lama yang tidak mendukung fitur HTML tertentu. Dalam konversi Excel ke HTML, komentar tersebut terkadang dapat menampilkan konten atau komentar tersembunyi, oleh karena itu menonaktifkannya dapat bermanfaat.
### Bisakah saya mengaktifkan komentar downlevel jika saya membutuhkannya?
 Ya, cukup atur`DisableDownlevelRevealedComments` properti untuk`false` jika Anda ingin mengaktifkan komentar downlevel saat menyimpan buku kerja Anda sebagai HTML.
### Bagaimana cara mendapatkan lisensi sementara untuk Aspose.Cells?
 Anda dapat dengan mudah mengajukan permohonan lisensi sementara dengan mengunjungi[Situs web Aspose](https://purchase.aspose.com/temporary-license/).
### Apakah menonaktifkan komentar downlevel memengaruhi tampilan HTML?
Tidak, menonaktifkan komentar yang ditampilkan di tingkat bawah tidak memengaruhi tampilan visual keluaran HTML. Ini hanya mencegah munculnya informasi tambahan yang ditujukan untuk peramban lama.
### Bisakah saya menyimpan buku kerja dalam format lain selain HTML?
 Ya, Aspose.Cells mendukung berbagai format output seperti PDF, CSV, dan TXT. Anda dapat menjelajahi lebih banyak pilihan di[dokumentasi](https://reference.aspose.com/cells/net/).