---
title: メーター課金
type: ドキュメント
weight: 70
url: /ja/java/metered-licensing/
---

{{% alert color="primary" %}}

Aspose.PSDを使用すると、開発者はメーターキーを適用できます。これは新しいライセンスメカニズムです。新しいライセンスメカニズムは、既存のライセンス方式と併用されます。API機能の使用状況に応じて請求を希望する顧客は、メーター課金を使用できます。詳細については、[メーター課金に関するFAQ](https://purchase.aspose.com/faqs/licensing/metered)セクションを参照してください。

{{% /alert %}}
## **メーター課金**
以下は、Meteredクラスを使用する簡単な手順です。

1. Meteredクラスのインスタンスを作成します。
1. setMeteredKeyメソッドに公開鍵と秘密鍵を渡します。
1. 処理を実行します（タスクを実行します）。
1. MeteredクラスのgetConsumptionQuantityメソッドを呼び出します。
1. これにより、これまでに消費したAPIリクエストの量が返されます。

以下は、メーターの公開鍵と秘密鍵を設定する方法を示すサンプルコードです。

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}
