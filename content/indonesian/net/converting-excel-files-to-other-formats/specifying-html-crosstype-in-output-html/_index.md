---
title: Menentukan HTML CrossType dalam Output HTML Secara Terprogram di .NET
linktitle: Menentukan HTML CrossType dalam Output HTML Secara Terprogram di .NET
second_title: API Pemrosesan Excel Aspose.Cells .NET
description: Pelajari cara menentukan HTML CrossType di Aspose.Cells untuk .NET. Ikuti tutorial langkah demi langkah kami untuk mengonversi file Excel ke HTML dengan tepat.
type: docs
weight: 17
url: /id/net/converting-excel-files-to-other-formats/specifying-html-crosstype-in-output-html/
---
## Perkenalan
Saat mengonversi file Excel ke HTML dalam aplikasi .NET, Anda mungkin perlu menentukan cara penanganan referensi silang dalam output. Kelas HtmlSaveOptions di Aspose.Cells untuk .NET menyediakan berbagai pengaturan untuk mengontrol proses konversi, dan salah satu opsi tersebut adalah HtmlCrossType. Dalam tutorial ini, kami akan membahas cara menentukan tipe silang HTML secara terprogram saat mengekspor file Excel ke format HTML. 
## Prasyarat
Sebelum menyelami kode, pastikan Anda memiliki hal berikut:
-  Aspose.Cells untuk .NET: Pastikan Anda telah menginstal pustaka Aspose.Cells di proyek Anda. Anda dapat mengunduhnya dari[Situs web Aspose](https://releases.aspose.com/cells/net/).
- Visual Studio: Instalasi Visual Studio atau lingkungan pengembangan .NET lainnya yang berfungsi.
- Pengetahuan Dasar C#: Keakraban dengan pemrograman C# akan membantu Anda memahami contoh-contohnya dengan lebih baik.
-  Contoh Berkas Excel: Siapkan contoh berkas Excel yang siap digunakan. Untuk contoh ini, kami akan menggunakan`sampleHtmlCrossStringType.xlsx`.
## Paket Impor
Untuk memulai, Anda perlu mengimpor namespace Aspose.Cells yang diperlukan. Berikut cara melakukannya:
```csharp
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
```
Mari kita uraikan langkah demi langkah, agar mudah bagi Anda untuk mengikuti dan menerapkan fungsi ini dalam proyek Anda sendiri.
## Langkah 1: Tentukan Direktori Sumber dan Output Anda
Pertama, Anda perlu mengatur direktori untuk file Excel sumber Anda dan tempat Anda ingin menyimpan file HTML keluaran.
```csharp
// Direktori sumber
string sourceDir = "Your Document Directory";
// Direktori keluaran
string outputDir = "Your Document Directory";
```
## Langkah 2: Muat File Excel Sampel
 Selanjutnya, muat file Excel contoh Anda ke dalam`Workbook` objek. Di sinilah semua keajaiban dimulai.
```csharp
// Muat file Excel contoh
Workbook wb = new Workbook(sourceDir + "sampleHtmlCrossStringType.xlsx");
```
 Di sini, ganti`"Your Document Directory"` dengan jalur sebenarnya tempat file Excel Anda berada. Baris ini membaca file Excel ke dalam memori sehingga Anda dapat memanipulasinya.
## Langkah 3: Tentukan Opsi Penyimpanan HTML
 Sekarang, kita akan membuat sebuah instance dari`HtmlSaveOptions`, yang memungkinkan Anda mengonfigurasi bagaimana file Excel akan dikonversi ke HTML.
```csharp
// Tentukan Jenis Silang HTML
HtmlSaveOptions opts = new HtmlSaveOptions();
opts.HtmlCrossStringType = HtmlCrossType.Default;
```
 Pada langkah ini, kami telah mengatur`HtmlCrossStringType` ke`HtmlCrossType.Default`, yang merupakan salah satu opsi yang tersedia untuk menangani referensi silang dalam HTML keluaran.
## Langkah 4: Ubah Jenis Salib Sesuai Kebutuhan
 Anda dapat menentukan jenis yang berbeda untuk`HtmlCrossStringType` berdasarkan kebutuhan Anda. Berikut adalah berbagai pilihan yang dapat Anda gunakan:
- `HtmlCrossType.Default`: Jenis silang default.
- `HtmlCrossType.MSExport`: Mengekspor HTML dengan perilaku seperti MS Excel.
- `HtmlCrossType.Cross`: Membuat referensi silang.
- `HtmlCrossType.FitToCell`: Menyesuaikan referensi silang dengan dimensi sel.
 Anda dapat mengubah`HtmlCrossStringType` seperti ini:
```csharp
opts.HtmlCrossStringType = HtmlCrossType.MSExport;
// atau
opts.HtmlCrossStringType = HtmlCrossType.Cross;
// atau
opts.HtmlCrossStringType = HtmlCrossType.FitToCell;
```
## Langkah 5: Simpan File HTML Output
 Setelah Anda mengonfigurasi opsi Anda, saatnya untuk menyimpan file HTML yang dikonversi. Gunakan`Save` metode pada Anda`Workbook` obyek:
```csharp
// Keluaran HTML
wb.Save(outputDir + "out" + opts.HtmlCrossStringType + ".htm", opts);
```
 Di sini, kami memberi nama file output berdasarkan`HtmlCrossStringType` kami telah mengaturnya. Dengan cara ini, Anda dapat dengan mudah mengidentifikasi jenis silang mana yang digunakan dalam konversi.
## Langkah 6: Konfirmasikan Eksekusi yang Berhasil
Terakhir, sebaiknya Anda selalu mengonfirmasi bahwa operasi Anda berhasil. Anda dapat mencetak pesan ke konsol:
```csharp
Console.WriteLine("SpecifyHtmlCrossTypeInOutputHTML executed successfully.\r\n");
```
Ini akan memberi tahu Anda bahwa proses telah selesai tanpa kesalahan apa pun.
## Kesimpulan
Nah, itu dia! Anda telah berhasil menentukan tipe silang HTML untuk ekspor Excel Anda dalam .NET menggunakan Aspose.Cells. Fungsionalitas ini sangat berguna ketika Anda perlu mempertahankan format atau referensi tertentu dalam output HTML Anda, memastikan bahwa dokumen yang dikonversi memenuhi persyaratan Anda.
## Pertanyaan yang Sering Diajukan
### Apa itu HtmlCrossType di Aspose.Cells?  
HtmlCrossType menentukan bagaimana referensi silang dalam berkas Excel ditangani selama konversi HTML. Anda dapat memilih opsi seperti Default, MSExport, Cross, dan FitToCell.
### Bisakah saya menggunakan Aspose.Cells secara gratis?  
 Aspose.Cells menawarkan versi uji coba gratis. Anda dapat mengunduhnya dari situs web mereka[situs web](https://releases.aspose.com/).
### Bagaimana cara menginstal Aspose.Cells di proyek .NET saya?  
 Anda dapat menginstal Aspose.Cells melalui NuGet Package Manager di Visual Studio dengan menjalankan perintah:`Install-Package Aspose.Cells`.
### Di mana saya dapat menemukan dokumentasi untuk Aspose.Cells?  
 Anda dapat menemukan dokumentasi lengkap di Aspose.Cells[Di Sini](https://reference.aspose.com/cells/net/).
### Apa yang harus saya lakukan jika saya menemukan kesalahan saat menyimpan berkas HTML?  
Pastikan jalur direktori sudah benar dan Anda memiliki izin menulis untuk direktori output. Jika masalah masih berlanjut, periksa forum dukungan Aspose untuk mendapatkan bantuan.