---
title: ライセンス
type: docs
weight: 70
url: /ja/net/licensing/
description: NuGetからPSD Photoshop C#ライブラリを評価し、ファイルまたはストリームを使用してライセンスを適用して、インストールされた評価から制限を除去します。
---

## **評価バージョンの制限**
[こちら](https://www.nuget.org/packages/Aspose.psd/)からAspose.PSD for .NETの評価バージョンをダウンロードできます。評価バージョンは、いくつかの制限付きのフルライセンス版と同じ機能を提供します。 Aspose.PSDを購入すると、ライセンスを適用するだけでインストールされた評価から制限が削除されます。 Aspose.PSD for .NETの評価バージョンは、次の2つの制限のみがあります：

- **各画像にウォーターマーク**: 保存、変更、またはエクスポートするすべての画像に、「評価専用。Aspose.PSDで作成。Copyright 2010-2018 Aspose Pty Ltd.」というウォーターマークが表示されます。完全なウォーターマークが収まらない小さい画像では、代わりに画像に2本の対角線が表示されます。
- **コア描画機能のサポートなし**: 評価モードでは、画像ピクセルを画像に読み込んだり保存したりすることができません。画像を描画するには、代わりに高度な描画機能を使用してください。この制限は、コア描画機能に依存する機能に影響します。 Aspose.PSD for .NETを使用して独自のファイル形式を登録することができます。しかし、この機能はコア描画機能に依存しているため、評価モードで使用する意味がないです。そのファイルの内容を変更できないからです。

評価制限のないAspose.PSD for .NETをテストしたい場合は、30日間の一時ライセンスをリクエストしてください。詳細は[一時ライセンスの入手方法](https://purchase.aspose.com/temporary-license)を参照してください。
## **ライセンスファイルについて**
Aspose.PSDの評価を満足できたら、[Asposeのウェブサイト](https://purchase.aspose.com/default.aspx)でライセンスを購入できます。提供される異なるサブスクリプションタイプを理解してください。質問がある場合は、[Asposeの営業チーム](https://company.aspose.com/contact)に連絡を遠慮しないでください。すべてのAsposeライセンスには、ソフトウェアのアップグレードの1年間のサブスクリプションが付属しています。初年度終了後は、最新の機能と修正を継続して入手するためにサブスクリプションを更新してください。テクニカルサポートは無料で無制限で、Asposeの[サポートフォーラム](https://forum.aspose.com/)を介して、有償ユーザーと評価ユーザーの両方に提供されます。ライセンスは、製品名、ライセンス取得開発者の数、サブスクリプション有効期限などの詳細が含まれるXMLファイルです。ファイルはデジタル署名されているため、変更しないでください。例え、誤って改行を追加するとファイルが無効になります。Aspose.PSDを購入したら、画像を作成、編集、またはその他の操作を行う前にライセンスを適用する必要があります。ライセンスを適用しないと、出力画像に評価ウォーターマークが表示されます。ライセンスは、開発するアプリケーションまたはプロセスごとに1回だけ設定する必要があります。
## **アプリケーションでのライセンス適用場所**
ライセンスを適用する場所は、開発中のアプリケーションの種類によって異なります。次のシンプルなルールに従ってください：

- アプリケーションドメインごとにライセンスを1回だけ適用します。 License.SetLicenseを複数回呼び出しても害はありませんが、プロセッサ時間が無駄になります。
- Aspose.PSD for .NETのクラスを使用する前にライセンスを適用します。
- **Windows Formsまたはコンソールアプリケーション**: Aspose.PSD for .NETのクラスを使用する前に、起動コードでLicense.SetLicenseを呼び出します。
- **ASP.NETアプリケーション**: Global.asax.cs（またはGlobal.asax.vb）ファイルのApplication_Start保護メソッドからLicense.SetLicenseを呼び出します。この方法では、アプリケーションが開始されるときに1回だけ呼び出されます。 Page_Loadメソッド内からLicense.SetLicenseを呼び出さないでください。そうすると、ライセンスがWebページが読み込まれるたびにロードされます。
- **Silverlightアプリケーション**: App.xaml.cs（またはApp.xaml.vb）ファイルのApplication_StartupイベントからLicense.SetLicenseを呼び出します。
- **クラスライブラリ**: Aspose.PSDを使用するクラスの静的コンストラクタからLicense.SetLicenseを呼び出します。 静的コンストラクタは、クラスのインスタンスが作成される前に実行されるため、Aspose.PSDライセンスが適切に設定されます。
## **ライセンスの適用**
NuGetのダウンロードページからAspose.PSDの評価バージョンを簡単にダウンロードできます。評価バージョンは、Aspose.PSDのライセンス版と完全に同じ機能を提供します。さらに、ライセンスを購入し、ライセンスを適用するためのコードを数行追加すると、評価バージョンはライセンス認証された状態に変わります。
### **ファイルまたはストリームを使用**
評価制限を回避したい場合は、Aspose.PSDを使用する前にライセンスを設定する必要があります。アプリケーション（またはプロセス）ごとにライセンスを1回だけ設定する必要があります。
### **ファイルからライセンスを適用**
ライセンスを適用する最も簡単な方法は、ライセンスファイルをAspose.PSD.dllと同じフォルダーに配置することです。その後、コードでファイル名をフルパスの代わりに指定できます。



{{< highlight java >}}

 // ライセンスのインスタンスを作成して、フルパスを使用してライセンスを適用します

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense("Aspose.PSD.lic");



{{< /highlight >}}



SetLicenseメソッドを呼び出す際は、ライセンス名はライセンスファイル名と同じである必要があります。 例えば、ライセンスファイル名を「Aspose.PSD.lic.xml」に変更した場合、SetLicenseメソッドにはこのライセンス名を使用する必要があります。
### **ストリームを使用してライセンスを適用**
以下に示すように、ストリームからライセンスをロードすることもできます。



{{< highlight java >}}



// ライセンスのインスタンスを作成して、ストリームを使用してライセンスを適用します

Aspose.PSD.License license = new Aspose.PSD.License();

license.SetLicense(myStream);



{{< /highlight >}}
### **ライセンスの状態を確認**
Aspose.PSD.Licenseクラスには、ライセンスが適切に設定されている場合にtrueを返すIsLicensedプロパティがあります。



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("ライセンスが設定されました！");

}

{{< /highlight >}}
### **埋め込みリソースの使用**
アプリケーションとライセンスをパッケージ化し、なくさないようにするための実用的な方法は、ライセンスをAspose.PSDを呼び出すアセンブリの埋め込みリソースとして含めることです。ライセンスファイルを埋め込みリソースとして含める方法：

1. Visual Studio .NETで、**ファイル**メニューをクリックして**既存の項目の追加**を選択します。
1. プロジェクトにライセンスファイル（拡張子.lic）を含めます。
1. ソリューションエクスプローラーでファイルを選択します。
1. プロパティウィンドウで、**ビルドアクション**を**埋め込みリソース**に設定します。

埋め込みのライセンスにアクセスするために、Microsoft .NET FrameworkでSystem.Reflection.AssemblyのGetExecutingAssemblyまたはGetManifestResourceStreamメソッドを呼び出す必要はありません。代わりに、プロジェクトにリソースとしてファイルを埋め込み、その後、ライセンスファイル名をSetLicenseメソッドに渡します。 Licenseクラスは、埋め込みリソース内のライセンスファイルを自動的に見つけます。以下の例は、埋め込みリソースとしてライセンスを含め、アプリケーションに適用する方法を示しています。



{{< highlight java >}}

 // Licenseクラスをインスタンス化

Aspose.PSD.License license = new Aspose.PSD.License();



// 埋め込みライセンスファイル名を渡します

license.SetLicense("Aspose.PSD.lic");

{{< /highlight >}}


### **ライセンスの状態を確認**
Aspose.PSD.Licenseクラスには、ライセンスが適切に設定されている場合にtrueを返すIsLicensedプロパティがあります。



{{< highlight java >}}

 License license = new License();

license.SetLicense(licensePath);

if (license.IsLicensed)

{

    Console.WriteLine("ライセンスが設定されました！");

}

{{< /highlight >}}
