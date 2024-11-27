---
title: Manipulasi Data Piksel menggunakan Aspose.PSD untuk Python
weight: 100
type: docs
description: Contoh bagaimana untuk langsung dan dengan cepat mengupdate data piksel mentah menggunakan PSD Python API
keywords: [edit piksel, edit psd, edit layer, manipulasi data mentah, edit data psd, psd api, python, contoh kode]
url: id/python-net/pixel-data-manipulation/
---

## **Pengenalan**
Aspose.PSD adalah perpustakaan yang kuat yang memungkinkan Anda untuk bekerja dengan file Adobe Photoshop (PSD) di Python. Pada artikel ini, kita akan menjelajahi bagaimana untuk memanipulasi data piksel dalam file PSD menggunakan Aspose.PSD.

## **Gambaran**
Kode yang disediakan menunjukkan bagaimana untuk membuat file PSD, menambahkan lapisan baru untuknya dan kemudian memanipulasi data piksel secara langsung, serta menyimpan gambar yang dimodifikasi.

Mengimpor Modul yang Diperlukan: Langkah pertama adalah mengimpor modul-modul yang diperlukan. Kami mengimpor modul BytesIO dari pustaka io, serta kelas PsdImage dan Layer dari modul aspose.psd.fileformats.psd dan aspose.psd.fileformats.psd.layers masing-masing.

Selanjutnya, kami mendefinisikan jalur file input dan output.

Membuka Berkas Masukan sebagai Stream: Kami membuka file masukan sebagai stream menggunakan fungsi open dan mode "rb". Argumen buffering disetel ke 0 untuk menonaktifkan buffering. Konten file dibaca ke dalam stream BytesIO dan stream disetel ke awal menggunakan stream.seek(0).

Kami membuat objek lapisan PSD dengan melewatkan stream ke konstruktor kelas Layer.

Kami membuat gambar PSD baru menggunakan konstruktor kelas PsdImage dan memberikan lebar dan tinggi lapisan sebagai argumen.

Kami menetapkan lapisan ke properti layers dari gambar PSD menggunakan operator penugasan (=).

Untuk memanipulasi data piksel, kami pertama-tama memuat piksel ARGB32 dari lapisan menggunakan metode load_argb_32_pixels. Kami menyimpan hasilnya dalam variabel piksel.

Selanjutnya, kami mendefinisikan rentang indeks (pixelsRange) berdasarkan panjang array piksel. Kami mengulanginya atas indeks dan memeriksa apakah suatu indeks dapat dibagi oleh 5. Jika iya, kami menetapkan nilai piksel pada indeks tersebut menjadi 500000. Jadi, kami hanya ingin membuat beberapa pola berulang. Anda dapat mengubah data piksel sesuai keinginan.

Kemudian kami menyimpan data piksel yang dimodifikasi kembali ke lapisan menggunakan metode save_argb_32_pixels.

Terakhir, kami menyimpan gambar PSD ke file output menggunakan metode save.

Dalam artikel ini, telah dijelaskan bagaimana untuk memanipulasi data piksel dalam file PSD menggunakan Aspose.PSD untuk Python. Dengan memahami kode yang disediakan, Anda dapat melakukan berbagai operasi level piksel, seperti memodifikasi piksel berdasarkan kondisi tertentu. Aspose.PSD menyediakan serangkaian fitur lengkap untuk bekerja dengan file PSD secara programatik, menjadikannya alat berharga untuk tugas manipulasi gambar di Python.

Harap dicatat bahwa kode yang disediakan mengasumsikan bahwa Anda telah menginstall perpustakaan Aspose.PSD dan dependensinya. Anda dapat menemukan informasi lebih lanjut tentang cara menginstall dan menggunakan Aspose.PSD untuk Python di dokumentasi resmi.

Silakan cek contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-pixel-data-manipulation.py" >}}
