---
title: Adobe Photoshop SDK なぜ選ばないのか
type: docs
weight: 100
url: /ja/net/why-not-adobe-photoshop-sdk/
description: Learn why PSD file format library is better option than Adobe Photoshop SDK, compare the security, stability, scalability, features of both.
---

{{% alert color="primary" %}}

なぜ Aspose コンポーネントが Adobe Photoshop SDK よりも優れているのでしょうか？

Aspose ではよく聞かれる質問がふたつあります:

1. **製品を実行するために Adobe Photoshop がインストールされている必要はありますか？**
   答えは簡単です。 Aspose コンポーネントは完全に独立しており、Adobe Inc. と提携関係にあるわけではなく、承認を受けていません。
1. **Adobe Photoshop SDK を利用する代わりに Aspose 製品を使用すべき理由はなんですか？**
   最も短い答えは、Adobe Photoshop エンドユーザーライセンス契約により、デスクトップ Photoshop をサーバーとして使用するサービスを開発することが許可されていないためです。 類似のトピックがフォーラムで議論されました([https://community.adobe.com/t5/licensing/photoshop-on-my-server/td-p/7520777?page=1](https://community.adobe.com/t5/licensing/photoshop-on-my-server/td-p/7520777?page=1))

{{% /alert %}}
## **Adobe Photoshop SDK なぜ選ばないのか**
Aspose コンポーネントが Adobe Photoshop SDK よりも優れている理由はいくつかあります。主なポイントは以下に説明されています。また、このセクションの最後にリンク先をご確認ください。

### **セキュリティ**
Adobe Photoshop SDK の情報セキュリティが見つけられません

Aspose 製品は非常に安全です。 Aspose コンポーネントはすべての ASP.NET アプリケーションと同じユーザーコンテキストで実行されます。そのため、Aspose コンポーネントは重要なシステムリソースに潜在的なリスクをもたらすことはありません。また、Aspose コンポーネントが [PSD ファイル](/psd/ja/net/psd-file/) を開く際、マクロは自動的に実行されません。 Aspose コンポーネントは開発者が PSD ファイルを作成、操作、保存することを可能にすることを目的として構築されました。 Adobe Photoshop SDK に関連するリスクは、Aspose コンポーネントには内在していません。

Aspose.PSD のリリースごとに SonarQube でテストを行っています。セキュアな製品を提供するために、すべての脆弱性とセキュリティのホットスポットを修正しています。

オープンソースの .Net Core を使用する要件がある場合は、[Aspose.PSD の .Net Standard バージョンがあります。](/psd/ja/net/installation/)

### **安定性**
Adobe Photoshop SDK を使用しているときに例外が発生した後、Adobe Photoshop を再起動する必要がある可能性はありますか？

Aspose コンポーネントは1つの DLL にパッケージ化されているため、機能するために追加のパーツや部品をインストールする必要はありません。 Aspose コンポーネントは .NET アプリケーションのみによって利用され、コンポーネントコードの部分が人間の応答を待つように設計されている部分はありません。 Aspose コンポーネントは徹底的にテストされました。IBM、Hilton、Reader's Digest、Bank of America などの企業によって使用されています。

### **スケーラビリティ/スピード**
Aspose コンポーネントは高度にスケーラブルで非常に高速です。 Adobe Photoshop には優れた機能がありますが、数百人や数千人のユーザーに同時に使用されることを前提とした設計になっていますか？ Aspose コンポーネントはまさにそのために設計されています。当社のコンポーネントは真の .NET ソリューションであり、単一のアプリケーションを実行するための単一のサーバーまたは企業全体のアプリケーションを実行する負荷分散された Web ファームに乗せたりする場合にも、完璧に機能します。

### **価格**
アプリケーションが Adobe Photoshop SDK を使用している場合、そのアプリケーションを実行する各マシンで Adobe Photoshop のコピーを購入する必要があります。アプリケーションが PSD ファイルを作成または操作する場合であっても、ユーザーが Adobe Photoshop を持っている必要がない場合が多々あります。Aspose は非常に[費用対効果の高い](https://purchase.aspose.com/pricing/psd)、ロイヤリティフリーの再配布ライセンスを提供し、製品を無制限のユーザーに展開する際のライセンスについて心配する必要がありません。(http://www.aspose.com/Purchase)

Web ベースのアプリケーションを作成する際には、Adobe Photoshop SDK はサーバーサイドのソリューションには価格設定やライセンス設定がされていないことを知ることが重要です ([https://community.adobe.com/t5/licensing/photoshop-on-my-server/td-p/7520777?page=1](https://community.adobe.com/t5/licensing/photoshop-on-my-server/td-p/7520777?page=1); [Photoshop の変更された UI での使用や Web サイト経由のアクセスを禁止する Adobe EULA](https://www.adobe.com/content/dam/acom/en/legal/licenses-terms/pdf/CS6.pdf) 参照)。

2.1.7 のセクションに特に注目してください。2.1.7.2 では、"ウェブホストワークグループまたは一般に利用可能なウェブホストサービスを有効にする" ことが禁止されています。

CC の世界では、[CC 使用許諾条件](http://www.adobe.com/legal/terms.html) が簡略化され、セクション 5.2 がサーバー使用ケースをカバーしています。5.2.b では他の人がソフトウェアにあなたのアカウント情報を使用するのを許可しないことが規定されています（PS はコンピュータ上にあり、他の人の利益のために CC サブスクリプションを使用して動作していることから、これが必要になります）。 5.2.d は、お客様に公開するための Web インターフェースなど、ソフトウェアへのカスタムインターフェイスを作成することを禁止しています。

Aspose はサーバーベースのアプリケーションに対して非常に費用対効果の高いソリューションを提供しています。
### **機能**
Aspose コンポーネントは PSD ファイルを管理するために必要なすべての機能を提供します。低レベルの API 操作、[PSD のテキストレイヤーの編集](/psd/ja/net/working-with-text-layers/)、ピクセルパーフェクトな ICC プロファイル変換、[PSD を他の形式にエクスポート](/psd/ja/net/converting-psd-image-to-raster-format/)（[Jpg](/psd/ja/net/psd-to-jpg/)、[Png](/psd/ja/net/psd-to-png/)、[Pdf](/psd/ja/net/psd-to-pdf/)、Bmp、Gif、Jpeg2000）、アジャストメントレイヤーのサポート、[PSD でカスタム グラフィックスを使用](/psd/ja/net/drawing-images-using-graphics/)、[マスクの操作](/psd/ja/net/layer-vector-mask/)やレイヤーデータの直接操作、など、Aspose.PSD は[AI を他の形式にエクスポート](/psd/ja/net/converting-ai-image-to-raster-format/)したり、[PDF に変換](/psd/ja/net/ai-to-pdf/)するためのエントリーレベルの機能を提供しています。Aspose.PSD は、開発者が最小限の作業量で最大の結果を達成できるよう設計されています。Office Automation とは異なり、Aspose コンポーネントは多くの強力で時間を節約する機能を提供します。[Aspose ファミリーのすべてのコンポーネント](https://products.aspose.com/total) はそれぞれ独自のユニークで強力な機能を提供します。Aspose.PSD だけが PSD ファイル構造を変更でき、強力なレンダリング機能と最も多様なカラーモード / ビット深度の組み合わせをサポートできます。

Aspose コンポーネントまたはコンポーネントスイートを購入する最大の利点は、開発チームへのアクセス権があることです。弊社の開発チームは、お客様の会社が必要とする機能がある場合、ほとんどの場合、他の企業もそれを必要とする可能性があることを認識しています。すべての要望を追加することはできませんが、製品の提供を行う際には、チームは非常に柔軟で協力的な姿勢を心がけています。この姿勢が Aspose コンポーネントがこれほど強力になるのに役立ちました。PSD フォーマットから追加の機能が必要な場合は、Aspose [PSD フォーラム](https://forum.aspose.com/c/psd) を使用してリクエストできます。

## **結論**


この記事では、Aspose.PSD がどの PSD SDK よりも優れた選択肢である理由について説明しました。すべての異なる Aspose コンポーネントは、リスクフリーで義務なしの[評価版](https://downloads.aspose.com/psd/net)を提供しています。Aspose がお客様のアプリケーションにどのような効果をもたらすかを確認するために、その評価版の活用をお勧めします。

[いいね](https://docs.aspose.com/display/wordsnet/Why+not+Automation) 
