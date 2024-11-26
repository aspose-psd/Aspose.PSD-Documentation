---
title: Aspose.PSD でワープの使用方法
type: docs
weight: 40
url: /ja/net/how-to-use-warp-in-aspose-psd/
---

## **Part 1 – ワープエフェクトを適用した PSD ファイルのレンダリング**

Photoshop は、ワープエフェクトを適用した後の描画イメージを保存します。当社のライブラリは、ワープエフェクトを適用した画像を再現または再レンダリングすることができます。この機能を有効にするには、PSD ファイルを開く際に設定で AllowWarpRepaint フラグを単純に設定します。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-1.cs" >}}

結果:
![Aspose.PSD for .NET ワープ結果 1](warp1.png)

スマートレイヤーのワープエフェクトをレンダリングするだけでなく、当社のライブラリはテキストレイヤーのワープにも対応しています。実装コードは同一であり、違いはファイル名のみです。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-2.cs" >}}

結果:
![Aspose.PSD for .NET ワープ結果 2](warp2.png)

**! 注意: ** 現在、当社のライブラリは、ユーザーがメッシュポイントを操作するカスタムワープとすべての標準ワープタイプの両方をレンダリングサポートしています。
* - 現在、当社のライブラリは、標準メッシュを使用したカスタムワープをサポートしており、近い将来、すべてのメッシュタイプをサポートするように積極的に取り組んでいます。


## **Part 2 – ワープエフェクトの修正**

当社のライブラリを使用すると、レンダリングだけでなくワープエフェクトを修正（追加）することもできます。
これらの修正は、**WarpParams** クラスの機能を介して容易に行われます。

| **機能**  | **説明**                                                         | 
|:-------------|:----------------------------------------------------------------------------|
| Bounds       | ワープされた画像の境界を返します。                                     |
| MeshPoints   | 各ポイントがワープメッシュの頂点を表すポイントの配列です。 |
| Value        | カスタム以外のワープエフェクトのワープ効果の値。                   |
| WarpRotates  | カスタム以外のワープエフェクトの方向を定義する列挙です。           |
| WarpStyles   | ワープエフェクトのタイプを定義する列挙です。                            |

以下のコード例は、スマートレイヤーのワープエフェクトのタイプを判別し、効果のタイプと歪みの強度を調整する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-3.cs" >}}

結果:
![Aspose.PSD for .NET ワープ結果 3](warp3.png)

## **Part 3 – ワープエフェクトの追加**

以下のコード例は、スマートレイヤーに標準のワープエフェクトを追加する方法を示しています。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-4.cs" >}}

結果:
![Aspose.PSD for .NET ワープ結果 4](warp4.png)

以下のコード例は、スマートレイヤーにカスタムワープエフェクトを追加する方法を示しています。
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

結果:
![Aspose.PSD for .NET ワープ結果 5](warp5.png)

以下のコード例は、テキストレイヤーにワープエフェクトを追加する方法を示しています。 
**! 注意: ** Photoshop の標準に従うと、テキストレイヤーのワープエフェクトは通常、標準タイプに限定されます。ただし、当社のライブラリは2種類のワープエフェクトの使用をサポートしています。このようなファイルは Photoshop と完全に互換性がない可能性があることに注意してください。

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentation-Aspose-PSD-Warp-Rendering-5.cs" >}}

結果:
![Aspose.PSD for .NET ワープ結果 6](warp6.png)

私たちは常に、ワープエフェクトの機能を洗練し拡張し、その速度、品質、サポートされる機能を向上させることに焦点を当てています。最新の進展については、毎月のリリースで最新情報をご確認ください。
あなたの Aspose.PSD チーム
