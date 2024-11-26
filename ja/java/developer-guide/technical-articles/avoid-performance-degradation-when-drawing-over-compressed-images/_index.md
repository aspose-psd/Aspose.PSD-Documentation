---
title: 圧縮された画像を描画する際のパフォーマンス劣化を回避する
type: ドキュメント
weight: 40
url: /ja/java/%e5%9c%a7%e7%b8%ae%e3%81%95%e3%82%8c%e3%81%9f%e7%94%bb%e5%83%8f%e3%82%92%e6%8f%8f%e7%94%bb%e3%81%99%e3%82%8b%e9%9a%9b%e3%81%ae%e3%83%91%e3%83%95%e3%82%a9%e3%83%bc%e3%83%9e%e3%83%b3%e3%82%b9%e5%8a%a3%e5%8c%96%e3%82%92%e5%9b%9e%e9%81%bf%e3%81%99%e3%82%8b/
---

## **圧縮された画像を描画する際のパフォーマンス劣化を回避する**
圧縮された画像上で非常に複雑なグラフィック操作を行いたいときがあります。Aspose.PSD が画像を圧縮および展開する必要があるとき、パフォーマンスの低下が発生する可能性があります。圧縮された画像上に描画することもパフォーマンスのペナルティを伴う可能性があります。

### **解決策**
パフォーマンスの劣化を回避するためには、グラフィック操作を行う前に画像を非圧縮形式、または生の形式に変換することをお勧めします。

### **ファイルパスを使用**
以下の例では、PSD 画像を非圧縮形式（圧縮なし）に変換してディスクに保存します。非圧縮画像をディスクから読み込み、その後にグラフィック操作を行います。同じ手法が BMP ファイルや GIF ファイルにも適用されます。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.java" >}}

### **ストリームオブジェクトを使用**
以下のコードスニペットは、PSD 画像を非圧縮形式（圧縮なし）に変換してストリームを使用してディスクに保存する方法を示しています。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.java" >}}
