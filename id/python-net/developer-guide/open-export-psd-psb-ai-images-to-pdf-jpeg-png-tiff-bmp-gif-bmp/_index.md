---
title: Buka file PSD, PSB, dan AI dan ekspor ke PDF, PNG, TIFF, GIF, BMP, JPEG
weight: 100
type: docs
description: Contoh ekspor file PSD, PSB, dan AI ke format lainnya
keywords: [buka psd, buka ai, buka psb, ekspor ke png, ekspor ke pdf, ekspor ke jpeg, ekspor ke tiff, psd api, python, contoh kode]
url: id/python-net/buka-ekspor-file-psd-psb-ai-ke-pdf-jpeg-png-tiff-bmp-gif-bmp/
---

## **Ikhtisar**
Untuk mengonversi file PSD, PSB, dan AI ke berbagai format, Anda dapat menggunakan perpustakaan Aspose.PSD dalam Python. Perpustakaan ini menyediakan berbagai opsi dan pengaturan untuk menyesuaikan proses konversi.

Pertama, Anda perlu mengimpor kelas-kelas dan modul-modul yang diperlukan dari perpustakaan Aspose.PSD. Pastikan Anda telah menginstal perpustakaan sebelum menjalankan kode.

Dalam kode ini, kita menentukan berbagai opsi untuk format-format yang berbeda, seperti PNG, PDF, TIFF, JPEG, BMP, JPEG2000, GIF, PSB, dan PSD. Opsi-opsi ini memungkinkan Anda menyesuaikan file keluaran sesuai dengan kebutuhan Anda.

Selanjutnya, kita mendefinisikan sebuah kamus formats yang memetakan ekstensi file ke opsi penyimpanannya masing-masing.

Untuk mengonversi file PSD ke format lain, Anda perlu memuat file PSD menggunakan PsdImage.load() dan kemudian melintasi kamus formats. Untuk setiap format, tentukan nama file keluaran dan simpan gambar menggunakan metode image.save().

Demikian pula, untuk mengonversi file AI ke format lain, muat file AI menggunakan AiImage.load() dan lintasi kamus formats. Tentukan nama file keluaran dan simpan gambar menggunakan metode image.save().

Pastikan untuk menyediakan jalur file yang benar untuk file PSD dan AI sumber.

Itu saja! Anda sekarang dapat menggunakan kode ini untuk mengonversi file PSD, PSB, dan AI ke berbagai format menggunakan Aspose.PSD untuk Python.

Silakan cek contoh lengkap.

## **Contoh**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentation-Python-Aspose-Psd-open-export-psd-psb-ai-images-to-pdf-jpeg-png-tiff-bmp-gif-bmp.py" >}}
