---
title: Dropdown Bertingkat di Excel
linktitle: Dropdown Bertingkat di Excel
second_title: API Pemrosesan Java Excel Aspose.Cells
description: Pelajari cara membuat dropdown berjenjang di Excel menggunakan Aspose.Cells untuk Java. Panduan langkah demi langkah ini memberikan kode sumber dan tip ahli untuk manipulasi spreadsheet Excel yang efisien.
type: docs
weight: 13
url: /id/java/data-validation-rules/cascading-dropdowns-in-excel/
---

## Pengantar Cascading Dropdown di Excel

Dalam dunia manipulasi spreadsheet, Aspose.Cells untuk Java berdiri sebagai perangkat canggih yang memberdayakan pengembang untuk bekerja dengan file Excel secara efisien. Salah satu fitur menarik yang ditawarkannya adalah kemampuan untuk membuat dropdown berjenjang di Excel, memungkinkan pengguna memilih opsi secara dinamis berdasarkan pilihan sebelumnya. Dalam panduan langkah demi langkah ini, kita akan mendalami proses penerapan dropdown berjenjang menggunakan Aspose.Cells untuk Java. Jadi, mari kita mulai!

## Prasyarat

Sebelum kita memulai perjalanan ini, pastikan Anda memiliki prasyarat berikut:

-  Aspose.Cells untuk Java: Unduh dan instal dari[Di Sini](https://releases.aspose.com/cells/java/).
- Lingkungan Pengembangan Java: Anda harus menyiapkan lingkungan pengembangan Java di mesin Anda.
- Pemahaman Dasar Excel: Keakraban dengan Excel dan konsep dasarnya akan sangat membantu.

## Menata panggung

Tujuan kami adalah membuat lembar Excel dengan dropdown berjenjang. Bayangkan sebuah skenario di mana Anda memiliki daftar negara, dan ketika Anda memilih suatu negara, daftar kota di negara tersebut akan tersedia untuk dipilih. Mari kita uraikan langkah-langkah untuk mencapai hal ini.

## Langkah 1: Membuat Buku Kerja Excel

Pertama, mari buat buku kerja Excel menggunakan Aspose.Cells for Java. Kami akan menambahkan dua lembar: satu untuk daftar negara dan satu lagi untuk daftar kota.

```java
// Kode Java untuk membuat buku kerja Excel
Workbook workbook = new Workbook();
Worksheet countrySheet = workbook.getWorksheets().get(0);
countrySheet.setName("Countries");
Worksheet citySheet = workbook.getWorksheets().add("Cities");
```

## Langkah 2: Mengisi Data

Sekarang, kita perlu mengisi lembar kerja kita dengan data. Di lembar "Negara", kami akan mencantumkan negaranya, dan di lembar "Kota", pertama-tama kami akan membiarkannya kosong, karena nanti kami akan mengisinya secara dinamis.

```java
//Kode Java untuk mengisi lembar "Negara".
countrySheet.getCells().get("A1").putValue("Country");
countrySheet.getCells().get("A2").putValue("USA");
countrySheet.getCells().get("A3").putValue("Canada");
countrySheet.getCells().get("A4").putValue("UK");
// Tambahkan lebih banyak negara sesuai kebutuhan
```

## Langkah 3: Membuat Dropdown

Selanjutnya, kita akan membuat daftar dropdown untuk kolom negara dan kota. Dropdown ini akan dihubungkan sedemikian rupa sehingga ketika suatu negara dipilih, dropdown kota akan diperbarui sesuai dengan itu.

```java
// Kode Java untuk membuat daftar dropdown
DataValidationCollection validations = countrySheet.getDataValidations();
DataValidation validation = validations.get(validations.add(1, 1, countrySheet.getCells().getMaxDataRow(), 1));
validation.setType(DataValidationType.LIST);
validation.setFormula1("Countries!$A$2:$A$4"); // Referensi ke daftar negara
```

## Langkah 4: Menerapkan Dropdown Berjenjang

Sekarang sampai pada bagian yang menarik: mengimplementasikan dropdown berjenjang. Kami akan menggunakan Aspose.Cells untuk Java untuk memperbarui dropdown kota secara dinamis berdasarkan negara yang dipilih.

```java
// Kode Java untuk mengimplementasikan dropdown berjenjang
countrySheet.getCells().setCellObserver(new ICellObserver() {
    @Override
    public void cellChanged(Cell cell) {
        if (cell.getName().equals("B2")) {
            // Hapus dropdown kota sebelumnya
            citySheet.getCells().get("B2").setValue("");
            
            // Tentukan negara yang dipilih
            String selectedCountry = cell.getStringValue();
            
            // Berdasarkan negara yang dipilih, isi dropdown kota
            switch (selectedCountry) {
                case "USA":
                    validation.setFormula1("Cities!$A$2:$A$4"); // Berpopulasi dengan kota-kota di Amerika
                    break;
                case "Canada":
                    validation.setFormula1("Cities!$B$2:$B$4"); // Berpopulasi dengan kota-kota di Kanada
                    break;
                case "UK":
                    validation.setFormula1("Cities!$C$2:$C$4"); // Berpopulasi dengan kota-kota di Inggris
                    break;
                // Tambahkan lebih banyak kasus untuk negara lain
            }
        }
    }
});
```

## Kesimpulan

Dalam panduan komprehensif ini, kita mempelajari cara membuat dropdown berjenjang di Excel menggunakan Aspose.Cells untuk Java. Kami memulai dengan menyiapkan prasyarat, membuat buku kerja Excel, mengisi data, lalu mempelajari seluk-beluk pembuatan dropdown dan menerapkan perilaku berjenjang dinamis. Sebagai pengembang, kini Anda memiliki pengetahuan dan alat untuk menyempurnakan file Excel Anda dengan dropdown interaktif, sehingga memberikan pengalaman pengguna yang lancar.

## FAQ

### Bagaimana cara menambahkan lebih banyak negara dan kota ke dropdown?

Untuk menambahkan lebih banyak negara dan kota, Anda perlu memperbarui masing-masing lembar di buku kerja Excel Anda. Cukup perluas daftar di lembar "Negara" dan "Kota", dan menu tarik-turun akan secara otomatis menyertakan entri baru.

### Bisakah saya menggunakan teknik ini bersamaan dengan fitur Excel lainnya?

Sangat! Anda dapat menggabungkan dropdown berjenjang dengan berbagai fitur Excel seperti pemformatan bersyarat, rumus, dan bagan untuk membuat spreadsheet canggih dan interaktif yang disesuaikan dengan kebutuhan spesifik Anda.

### Apakah Aspose.Cells untuk Java cocok untuk proyek skala kecil dan besar?

Ya, Aspose.Cells untuk Java serbaguna dan dapat digunakan dalam proyek dengan segala ukuran. Baik Anda sedang mengerjakan utilitas kecil atau aplikasi perusahaan yang kompleks, Aspose.Cells untuk Java dapat menyederhanakan tugas-tugas terkait Excel Anda.

### Apakah saya memerlukan keterampilan pemrograman tingkat lanjut untuk mengimplementasikan dropdown berjenjang dengan Aspose.Cells untuk Java?

Meskipun pemahaman dasar tentang Java sangat membantu, Aspose.Cells untuk Java menyediakan dokumentasi dan contoh ekstensif untuk memandu Anda melalui proses tersebut. Dengan sedikit dedikasi dan latihan, Anda dapat menguasai fitur ini.

### Di mana saya dapat menemukan lebih banyak sumber daya dan dokumentasi untuk Aspose.Cells untuk Java?

 Anda dapat mengakses dokumentasi dan sumber daya komprehensif untuk Aspose.Cells untuk Java di[Di Sini](https://reference.aspose.com/cells/java/).