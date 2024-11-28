---
title: Psdブレンディングオプション操作
weight: 100
type: docs
description: Aspose.PSD for Javaを使用して、簡単なコードスニペットでブレンディングオプションを調整することができます。
keywords: [blend options、blending、add effects、change opacity、change color of shadow、add shadow、psd api、java、code sample]
url: /ja/java/blending-options/
---

## **概要**
Aspose.PSD for Javaを使用すると、PSD画像内のレイヤーの外観を向上させるためにブレンディングオプションを変更することができます。以下は、ブレンディングオプションを利用する様々な方法を示すJavaコード例です。

まず、コードはPSD画像を読み込んで元のPNGファイルとして保存します。その後、特定のレイヤーの不透明度やブレンディングモードを変更します。たとえば、2番目のレイヤーの不透明度を100に設定し、5番目のレイヤーのブレンディングモードをHueに変更します。

さらに、コードは指定されたレイヤーにブレンディング効果を組み込みます。`addDropShadow()`メソッドを使用して、第7レイヤーに30度の影角とRGB(255, 0, 0)の影色を指定してドロップシャドウ効果を導入します。

さらに、コードは第9レイヤーのブレンディングモードをLightenに調整します。さらに、5番目のレイヤーに`addColorOverlay()`メソッドを介してカラーオーバーレイ効果を適用し、カラーオーバーレイをRGB(30, 50, 0)に設定し、不透明度を150にします。

最後に、コードは変更された画像を更新されたPNGファイルとして保存します。

基本的に、Aspose.PSD for Javaは、PSD画像内のレイヤーの外観を操作するためのさまざまなブレンディングオプションを提供しています。これらのオプションには、不透明度の変更、ブレンディングモードの変更、ドロップシャドウやカラーオーバーレイなど様々なブレンディングエフェクトの実装が含まれます。

## **例**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-Psd-blending-options.java" >}}
