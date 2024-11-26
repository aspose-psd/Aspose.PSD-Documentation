---
title: 圧縮された画像上に描画する際のパフォーマンスの低下を回避する方法
type: docs
weight: 10
url: /ja/net/avoid-performance-degradation-when-drawing-over-compressed-images/
---

## **圧縮された画像上に描画する際のパフォーマンスの低下を回避する方法**
圧縮された画像上で非常に膨大なグラフィック操作を実行したい場合があります。Aspose.PSDが画像をリアルタイムで圧縮および解凍する必要があると、パフォーマンスの低下が発生する場合があります。圧縮された画像上に描画することもパフォーマンスのペナルティを伴う可能性があります。

### **解決策**
パフォーマンスの低下を回避するために、グラフィック操作を実行する前に画像を非圧縮または生の形式に変換することをお勧めします。

### **ファイルパスを使用**
以下の例では、PSD画像を生の形式（圧縮なし）に変換してディスクに保存し、グラフィック操作を実行する前に非圧縮画像を再び読み込みます。同様のテクニックは、BMPおよびGIFファイルにも適用されます。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageUsingFile-UncompressedImageUsingFile.cs" >}}

### **Streamオブジェクトを使用**
以下のコードスニペットは、PSD画像をMemoryStreamを使用して生の形式に変換し、ディスクに保存する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Examples-CSharp-Aspose-ModifyingAndConvertingImages-PSD-UncompressedImageStreamObject-UncompressedImageStreamObject.cs" >}}
