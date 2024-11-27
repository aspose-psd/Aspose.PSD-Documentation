---
title: Layer Vector Mask
type: docs
weight: 10
url: /id/net/layer-vector-mask/
---

## **Ikhtisar Layer Vector Mask**
Masker vektor adalah jalur yang independen resolusi yang memotong konten dari layer. Masker vektor biasanya lebih akurat daripada yang dibuat dengan alat berbasis piksel. Anda membuat masker vektor dengan alat pena atau bentuk.

Aspose.PSD mendukung render dan penerapan masker vektor. Anda dapat mengedit masker vektor melalui pengeditan Jalur Vektor.

## **Jalur vektor di Aspose.PSD**
Akses ke jalur vektor di Aspose.PSD disediakan melalui [VsmsResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vsmsresource) dan [VmskResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vmskresource) yang merupakan kelas anak dari [VectorPathDataResource](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.layers.layerresources/vectorpathdataresource).

![todo:image_alt_text](layer-vector-mask_0.png)

## **Bagaimana cara mengedit jalur vektor?**
### **Struktur jalur vektor**
Struktur dasar untuk memanipulasi jalur adalah [VectorPathRecord](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/vectorpathrecord). Namun, untuk kenyamanan Anda, solusi berikut disarankan.

Untuk mengedit jalur vektor dengan mudah, Anda harus menggunakan kelas [VectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), yang berisi metode untuk pengeditan data vektor yang nyaman dalam sumber daya yang berasal dari VectorPathDataResource.

Mulailah dengan membuat objek bertipe VectorPath. 

Untuk kenyamanan, Anda dapat menggunakan metode statis [VectorDataProvider.CreateVectorPathForLayer](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), yang akan menemukan sumber daya vektor dalam layer masukan dan membuat objek VectorPath berdasarkan itu.

Setelah semua pengeditan, Anda dapat menerapkan objek VectorPath dengan perubahan kembali ke layer menggunakan metode statis [VectorDataProvider.UpdateLayerFromVectorPath](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-1.cs" >}}

Tipe VectorPath berisi daftar elemen [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) dan menggambarkan gambar vektor lengkap yang dapat terdiri dari satu atau lebih bentuk.

![todo:image_alt_text](layer-vector-mask_1.png)

Setiap PathShape adalah figur vektor yang terdiri dari sekumpulan titik bezier yang terpisah.

Titik adalah objek bertipe [BezierKnot](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) yang pada dasarnya merupakan titik-titik dari mana bentuknya dibangun.

![todo:image_alt_text](layer-vector-mask_2.png)

Contoh kode berikut menunjukkan bagaimana mengakses sebuah figur dan titik-titiknya.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-2.cs" >}}
### **Bagaimana cara membuat sebuah bentuk?**
Untuk mengedit sebuah bentuk, Anda perlu mendapatkan yang sudah ada dari daftar [VectorPath.Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs), atau menambahkan bentuk baru dengan membuat instance [PathShape](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs) dan menambahkannya ke daftar [Shapes](https://gist.github.com/aspose-com-gists/8a4c9d34ce856d1642fc7c0ce974175c#file-examples-csharp-aspose-workingwithvectorpaths-classestomanipulatevectorpathobjects-classestomanipulatevectorpathobjects-cs).

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-3.cs" >}}
### **Bagaimana cara menambahkan titik-titik?**
Anda dapat memanipulasi titik-titik dari bentuk sebagai elemen-elemen List reguler menggunakan properti PathShape.Points, misalnya, Anda dapat menambahkan titik-titik bentuk:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-4.cs" >}}

BezierKnot berisi titik Anchor dan dua titik Control.

![todo:image_alt_text](layer-vector-mask_3.png)

Jika titik anchor dan control memiliki nilai yang sama, maka node tersebut akan memiliki sudut tajam.

Untuk mengubah posisi titik anchor beserta titik kontrol (serupa dengan apa yang terjadi di Photoshop), BezierKnot memiliki metode Shift.

Contoh kode berikut menunjukkan memindahkan keseluruhan bezier knot secara vertikal ke atas berdasarkan koordinat Y:

Anda dapat memanipulasi titik-titik dari bentuk sebagai elemen-elemen List reguler menggunakan properti PathShape.Points, misalnya, Anda dapat menambahkan titik-titik bentuk:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-5.cs" >}}

## **Properti PathShape**
Pengeditan PathShape tidak terbatas pada mengedit node, tipe ini juga memiliki properti lain.
### **Operasi Path (Operasi Boolean)**
Properti [PathOperations](https://reference.aspose.com/psd/net/aspose.psd.fileformats.core.vectorpaths/pathoperations) adalah operasi boolean, mengubah nilai yang menentukan bagaimana beberapa bentuk dicampur.

Berikut adalah nilai-nilai yang mungkin:

- 0 = ExcludeOverlappingShapes (operasi XOR).
- 1 = CombineShapes (operasi OR).
- 2 = SubtractFrontShape (operasi NOT).
- 3 = IntersectShapeAreas (operasi AND).

![todo:image_alt_text](layer-vector-mask_4.png)
### **Properti IsClosed**
Juga, menggunakan properti PathShape.IsClosed, kita dapat menentukan apakah titik pertama dan terakhir dari sebuah bentuk terhubung.

|**Bentuk Tertutup**|**Bentuk Terbuka**|
| :- | :- |
|![todo:image_alt_text](layer-vector-mask_5.png)|![todo:image_alt_text](layer-vector-mask_6.png)|
### **Properti FillColor**
Tidak ada figur yang dapat memiliki warna sendiri, jadi Anda dapat mengubah warna jalur vektor keseluruhan dengan properti VectorPath.FillColor.

Anda dapat memanipulasi titik-titik dari bentuk sebagai elemen-elemen List reguler menggunakan properti PathShape.Points, misalnya, Anda dapat menambahkan titik-titik bentuk:

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-CSharp-Aspose-WorkingWithVectorPaths-Snippet-6.cs" >}}

## **Di sini Anda akan menemukan kode sumber VectorDataProvider dan kelas terkait:**
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-WorkingWithVectorPaths-ClassesToManipulateVectorPathObjects-ClassesToManipulateVectorPathObjects.cs" >}}
