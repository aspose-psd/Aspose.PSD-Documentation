---
title: Masalah yang Diketahui
type: docs
weight: 40
url: /id/net/known-issues/
---

## **.NET Compact Framework**
- Diamati bahwa di beberapa versi Windows tertentu seperti Windows Mobile 5.0-6.0, perakitan compact framework yang ditandai dengan sertifikat (atau sertifikat ganda) tidak berfungsi seperti yang diharapkan dan tidak dapat dimuat dengan benar (TypeLoadException dilemparkan). Untuk mengatasi masalah ini, pengguna perlu menghapus semua sertifikat dan kemudian menggunakan perakitan yang diperbarui. Harap dicatat bahwa Anda melakukannya atas risiko sendiri dan kami tidak menjamin kinerja yang valid karena perubahan perakitan tersebut. Kami juga tidak mengirimkan perakitan tanpa tanda tangan karena ini merupakan ancaman keamanan potensial. Sebaliknya, pelanggan seharusnya menghindari menggunakan sistem operasi lama semacam itu, jika memungkinkan, dan/atau meningkatkan sistem operasi ke edisi atau service pack yang lebih baru yang menyelesaikan masalah penandatanganan sertifikat.
