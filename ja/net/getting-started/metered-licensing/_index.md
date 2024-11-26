---
title: メーター課金
type: docs
weight: 80
url: /ja/net/metered-licensing/
description: PSD Photoshop C# ライブラリを使用すると、新しいライセンスメカニズムであるメーターキーを適用し、既存のライセンスメソッドと併用することができます。
---

{{% alert color="primary" %}}

Aspose.PSD を使用すると、開発者はメーターキーを適用できます。これは新しいライセンスメカニズムです。新しいライセンスメカニズムは、既存のライセンスメソッドと併用されます。API 機能の使用に応じて請求される顧客は、メーター課金を使用できます。詳細については、[メーター課金 FAQ](https://purchase.aspose.com/faqs/licensing/metered) セクションを参照してください。

{{% /alert %}}
## **メーター課金**
以下は、Metered クラスを使用するための簡単な手順です。

1. Metered クラスのインスタンスを作成します。
1. setMeteredKey メソッドに公開鍵と秘密鍵を渡します。
1. 処理を行います（タスクを実行します）。
1. Metered クラスの getConsumptionQuantity メソッドを呼び出します。
1. これにより、これまでに消費した API リクエストの量が返されます。

以下は、メーターの公開鍵と秘密鍵を設定する方法を示すサンプルコードです。

{{< highlight java >}}

// PSD メータークラスのインスタンスを作成

Aspose.PSD.Metered metered = new Aspose.PSD.Metered();



// setMeteredKey プロパティにアクセスし、パラメーターとして公開鍵と秘密鍵を渡す

metered.SetMeteredKey("*****", "*****");



// API を呼び出す前のメーターデータ量を取得

decimal amountbefore = Aspose.PSD.Metered.GetConsumptionQuantity();



// 情報を表示

Console.WriteLine("消費前の量: " + amountbefore.ToString());

// API を呼び出した後のメーターデータ量を取得

decimal amountafter = Aspose.PSD.Metered.GetConsumptionQuantity();



// 情報を表示

Console.WriteLine("消費後の量: " + amountafter.ToString());

{{< /highlight >}}
