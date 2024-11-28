---
title: ライセンス
type: ドキュメント
weight: 60
url: /ja/java/licensing/
---

## **評価版の制限事項**
[ダウンロードページ](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/)からAspose.PSD for Javaの評価版をダウンロードできます。評価版は、完全ライセンス版と同じ機能を提供しますが、いくつかの制限があります。Aspose.PSDを購入すると、ライセンスを適用するだけでインストール済みの評価版から制限が解除されます。

Aspose.PSD for Javaの評価版には、次の2つの制限があります。

- **画像に透かし**: 保存、変更、エクスポートした画像には、「評価版専用。Aspose.PSDで作成。Copyright 2018-2019 Aspose Pty Ltd.」という透かし付きが表示されます。フル透かしを適用できない小さい画像では、代わりに斜めの2本の線が表示されます。
- **コア描画機能の非サポート**: 評価版では、画像ピクセルを読み込んだり保存したりできません。画像を描画するには、高度な描画機能を使用してください。この制限はコア描画機能に依存する機能に影響します。Aspose.PSD for Javaは独自のファイル形式を登録できますが、この機能はコア描画機能に依存するため、評価モードで使用する意味はありません。評価モードでは、これらのファイルのコンテンツを変更できないためです。

{{% alert color="primary" %}}

評価版の制限を含まないAspose.PSD for Javaをテストしたい場合は、30日間の一時ライセンスをリクエストしてください。詳細については、[一時ライセンスの取得方法](https://purchase.aspose.com/temporary-license)をご覧ください。

{{% /alert %}}
## **ライセンスファイルについて**
Aspose.PSDの評価が完了したら、[Asposeのウェブサイト](https://purchase.aspose.com/default.aspx)でライセンスを購入できます。提供されている異なるサブスクリプションタイプについて詳しく理解してください。ご質問がある場合は、[Asposeのセールスチーム](https://company.aspose.com/contact)にお問い合わせください。

Asposeライセンスには、ソフトウェアのアップグレードを1年間無料で受けられるサブスクリプションが付属しています。最初の1年後、最新の機能と修正を引き続き受け取るにはサブスクリプションを更新する必要があります。技術サポートは、有償版と評価版の両方のユーザーに無償で無制限に提供され、[サポートフォーラム](https://forum.aspose.com/)を通じて行われます。

ライセンスは、製品名、ライセンス取得者数、サブスクリプションの有効期限などの詳細が含まれたXMLファイルです。ファイルはデジタル署名されているため、変更しないでください。余分な改行を誤って追加するとファイルが無効になります。

Aspose.PSDを購入した後は、画像の作成、編集、またはその他の操作を行う前にライセンスを適用する必要があります。ライセンスを忘れると、出力される画像に評価版の透かしが表示されます。1つのアプリケーションまたはプロセスごとにライセンスを1度だけ設定する必要があります。
## **ライセンスの適用**
[Aspose.PSD](http://maven.aspose.com/repository/simple/ext-release-local/com/aspose/aspose-psd/)のJava用評価版をダウンロードできます。評価版は製品のライセンスされたバージョンとまったく同じ機能を提供します。さらに、ライセンスを購入し、ライセンスを適用するためのコード行を追加すると、評価版は簡単にライセンスされます。

[Aspose.PSD](http://www.aspose.com/Purchase/Components/Default.aspx)の評価が完了したら、Asposeのウェブサイトでライセンスを購入できます。提供されている異なるサブスクリプションタイプについて詳しく理解してください。ご質問がある場合は、Asposeのセールスチームに連絡を取らないでください。

Asposeのライセンスには、1年間の無料アップグレードサブスクリプションが付属しています。技術サポートは、有償版と評価版の両方のユーザーに無償で無制限に提供されます。

{{% alert color="primary" %}}

評価版の制限を含まないAspose.PSDをテストしたい場合は、30日間の一時ライセンスをリクエストしてください。詳細については、[一時ライセンスの取得方法](http://www.aspose.com/corporate/how-to-get-temporary-license.aspx)をご覧ください。

{{% /alert %}}

### **ライセンスの設定**
ライセンスは、製品名、ライセンスされた開発者の数、サブスクリプションの有効期限などの詳細が含まれたプレーンテキストのXMLファイルです。ファイルはデジタル署名されているため、ファイルを変更しないでください。ファイルに余分な改行を追加すると、ファイルが無効になります。

Aspose.PSDの評価版の制限を回避したい場合は、ライセンスを設定する必要があります。アプリケーションまたはプロセスごとに1度だけライセンスを設定する必要があります。

ライセンスは次の場所からストリームまたはファイルから読み込むことができます:

1. 明示的なパス。
1. Aspose.PSD.jarを含むフォルダ。

[License](http://www.aspose.com/api/java/psd/com.aspose.psd/classes/License)クラスのsetLicenseメソッドを使用してコンポーネントにライセンスを付与します。ライセンスを設定する最も簡単な方法は、Aspose.PSD.jarと同じフォルダにライセンスファイルを配置し、パスを指定せずにファイル名のみを指定することです。以下の例のように：
#### **例1**
この例では、Aspose.PSDがアプリケーションのJARを含むフォルダ内でライセンスファイルを見つけようとします。

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense("Aspose.PSD.Java.lic");

{{< /highlight >}}
#### **例2**
ストリームからライセンスを初期化します。

**Java**

{{< highlight csharp >}}

 com.aspose.psd.License license = new com.aspose.psd.License();

license.setLicense(new java.io.FileInputStream("Aspose.PSD.Java.lic"));

{{< /highlight >}}
### **ライセンスの検証**
ライセンスが適切に設定されているかどうかを確認できます。Licenseクラスには、ライセンスが適切に設定されている場合にtrueを返すisLicensedフィールドがあります。

**Java**

{{< highlight csharp >}}

 License license = new License();

license.setLicense("Aspose.PSD.Java.lic");

if (License.isLicensed()) {

    System.out.println("ライセンスが設定されています！");

}

{{< /highlight >}}
## **アプリケーションでライセンスを適用する場所**
ライセンスを適用する場所は、開発中のアプリケーションのタイプによって異なります。以下のシンプルなルールに従ってください：

- 1つのアプリケーションドメインごとにライセンスを1度だけ設定する必要があります。License.setLicenseを複数回呼び出すことは害はありませんが、プロセッサの時間を無駄にします。
- Aspose.PSDクラスの呼び出し前にライセンスを適用してください。
- **Javaアプリケーション**：起動コードでLicense.SetLicenseを呼び出します。
- **クラスライブラリ**：Aspose.PSDを使用するクラスの静的コンストラクタからLicense.setLicenseを呼び出します。静的コンストラクタは、クラスのインスタンスが作成される前に実行されるため、Aspose.PSDライセンスが適切に設定されることを確認します。
## **複数のAspose製品の使用**
アプリケーションで複数のAspose製品（例: Aspose.PSDとAspose.Cells）を使用する場合、次のヒントが役立ちます。

- **各Aspose製品ごとにライセンスを適用する**。すべてのコンポーネントに単一のライセンスファイル（例: 'Aspose.Total.lic'）がある場合でも、アプリケーションで各Aspose製品のために個別にLicense.setLicenseを呼び出す必要があります。
- **完全修飾されたライセンスクラス名を使用する**。各Aspose製品には、それぞれのネームスペースにライセンスクラスがあります。例えば、Aspose.PSDにはcom.aspose.psd.license.License、Aspose.Cellsにはcom.aspose.cells.Licenseがあります。完全修飾クラス名を使用することで、どのライセンスがどの製品に適用されているかについての混乱を避けることができます。
