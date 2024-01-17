---
title: Membuat Validasi Data Khusus
linktitle: Membuat Validasi Data Khusus
second_title: API Pemrosesan Java Excel Aspose.Cells
description: Pelajari cara membuat validasi data khusus menggunakan Aspose.Cells untuk Java. Panduan langkah demi langkah dengan kode sumber.
type: docs
weight: 10
url: /id/java/data-validation-rules/creating-custom-data-validation/
---

## Perkenalan

Validasi data membantu menjaga integritas data dengan mencegah pengguna memasukkan data yang salah atau tidak valid ke dalam spreadsheet Excel. Meskipun Excel menawarkan opsi validasi data bawaan, ada skenario di mana Anda perlu menentukan aturan validasi kustom. Aspose.Cells untuk Java memberdayakan Anda untuk mencapai hal ini secara efisien.

## Prasyarat

Sebelum mendalami kode, pastikan Anda memiliki prasyarat berikut:

-  Aspose.Cells untuk Java: Unduh dan instal perpustakaan dari[Di Sini](https://releases.aspose.com/cells/java/).

## Langkah 1: Menyiapkan Proyek Java Anda

Untuk memulai, buat proyek Java baru di Lingkungan Pengembangan Terpadu (IDE) pilihan Anda. Tambahkan perpustakaan Aspose.Cells untuk Java ke jalur kelas proyek Anda.

## Langkah 2: Membuat Buku Kerja Excel

Mari kita mulai dengan membuat buku kerja Excel baru menggunakan Aspose.Cells for Java.

```java
// Kode Java untuk membuat buku kerja Excel baru
Workbook workbook = new Workbook();
```

## Langkah 3: Menambahkan Lembar Kerja

Sekarang, mari tambahkan lembar kerja ke buku kerja tempat kita akan menerapkan validasi data khusus.

```java
// Kode Java untuk menambahkan lembar kerja
Worksheet worksheet = workbook.getWorksheets().get(0);
```

## Langkah 4: Menentukan Kriteria Validasi Kustom

Pada langkah ini, kita akan menentukan kriteria validasi khusus yang harus dipatuhi oleh data kita. Katakanlah kita ingin membatasi usia yang dimasukkan dalam sel antara 18 dan 60.

```java
// Kode Java untuk menentukan kriteria validasi khusus
Validation validation = worksheet.getValidations().add();
validation.setType(ValidationType.WHOLE);
validation.setOperator(OperatorType.BETWEEN);
validation.setFormula1("18");
validation.setFormula2("60");
validation.setShowError(true);
validation.setAlertStyle(ValidationAlertType.STOP);
validation.setErrorTitle("Invalid Age");
validation.setErrorMessage("Age must be between 18 and 60.");
```

## Langkah 5: Menerapkan Validasi Data ke suatu Rentang

Sekarang kita telah menentukan kriteria validasi khusus, mari terapkan ke rentang sel tertentu.

```java
// Kode Java untuk menerapkan validasi data ke suatu rentang
CellArea area = new CellArea();
area.startRow = 0;
area.startColumn = 0;
area.endRow = 9; // Terapkan validasi ke sepuluh baris pertama
area.endColumn = 0;

validation.addArea(area);
```

## Langkah 6: Menyimpan File Excel

Terakhir, simpan file Excel dengan menerapkan aturan validasi data khusus.

```java
// Kode Java untuk menyimpan file Excel
workbook.save("CustomDataValidation.xlsx");
```

## Kesimpulan

Dalam tutorial ini, kita telah menjelajahi cara membuat aturan validasi data kustom menggunakan Aspose.Cells untuk Java. Dengan mengikuti langkah-langkah ini, Anda dapat memastikan bahwa data Excel Anda mematuhi kriteria tertentu, sehingga meningkatkan integritas dan akurasi data.

## FAQ

### Bagaimana cara mengunduh Aspose.Cells untuk Java?

 Anda dapat mengunduh Aspose.Cells untuk Java dari situs web di[Di Sini](https://releases.aspose.com/cells/java/).

### Bisakah saya menerapkan validasi data khusus ke beberapa rentang di lembar kerja yang sama?

Ya, Anda bisa menerapkan validasi data khusus ke beberapa rentang dalam lembar kerja yang sama dengan mengulangi Langkah 5 untuk setiap rentang yang diinginkan.

### Apakah ada jenis validasi data lain yang didukung oleh Aspose.Cells untuk Java?

Ya, Aspose.Cells untuk Java mendukung berbagai jenis validasi data, termasuk bilangan bulat, desimal, tanggal, waktu, panjang teks, dan banyak lagi.

### Bagaimana cara menyesuaikan pesan kesalahan yang ditampilkan ketika validasi data gagal?

 Anda dapat menyesuaikan pesan kesalahan dengan memodifikasi`setErrorMessage` metode di Langkah 4, tempat Anda menentukan kriteria validasi.

### Apakah Aspose.Cells untuk Java berfungsi dengan file Excel dalam format berbeda?

Ya, Aspose.Cells untuk Java mendukung berbagai format file Excel, termasuk XLS, XLSX, XLSM, dan banyak lagi.