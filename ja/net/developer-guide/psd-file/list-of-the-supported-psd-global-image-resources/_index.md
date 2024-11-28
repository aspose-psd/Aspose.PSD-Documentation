---
title: サポートされるPSDグローバルイメージリソースのリスト
type: ドキュメント
weight: 30
url: /ja/net/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSDは画像リソースのローレベル編集をサポートしています。**
Aspose.PSD .Net [APIリファレンス](https://reference.aspose.com/psd/net) で使用できる完全にサポートされている画像リソースのリストを見つけることができます。

Adobe® Photoshop®フォーマット仕様によると、画像リソースは複数の標準ID番号を使用します。すべてのファイル形式がすべてのIDを使用するわけではありません。一部の情報はファイルの他のセクションに保存されることがあります。

Photoshop 3.0以降に追加されたリソースIDについては、導入されたバージョンが示されます（例：(*Photoshop 6.0)*）。

画像リソースID。

| **ID** | **説明** |
| :- | :- |
| **Decimal** | |
| 1000 | *(非推奨--Photoshop 2.0限定)* チャネル数、行数、列数、深度、およびモード |
| 1001 | Macintoshプリントマネージャープリント情報レコード |
| 1002 | Macintoshページフォーマット情報。Photoshopによって読み取られなくなりました。 *(非推奨)* |
| 1003 | *(非推奨--Photoshop 2.0限定)* インデックスカラーテーブル |
| 1005 | [ResolutionInfo構造](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource) |
| 1006 | アルファチャネルの名前（Pascal文字列のシリーズ） |
| 1007 | *(非推奨) ID 1077表示情報* 構造 |
| 1008 | キャプション（Pascal文字列） |
| 1009 | [境界情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource)。境界の幅に固定された数値（2バイトの実数、2バイトの分数）、および境界の単位の2バイト（1 = インチ、2 = cm、3 = ポイント、4 = ピカ、5 = カラム）を含む。 |
| 1010 | [背景色](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index) |
| 1011 | プリントフラグ。1バイトのブール値のシリーズ：ラベル、切り取りマーク、カラーバー、登録マーク、ネガティブ、反転、補間、キャプション、プリントフラグ。 |
| 1012 | グレースケールおよびマルチチャンネルハーフトーン情報 |
| 1013 | [カラーハーフトーン情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource) |
| 1014 | デュオトーンハーフトーン情報 |
| 1015 | グレースケールおよびマルチチャンネル転送関数 |
| 1016 | [カラー転送関数](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188) |
| 1017 | デュオトーン転送関数 |
| 1018 | デュオトーン画像情報 |
| 1019 | ドット範囲の有効な黒と白の値用の2バイト |
| 1020 | *(非推奨)* |
| 1021 | EPSオプション |
| 1022 | [Quick Mask情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource)。Quick MaskチャネルID；最初にマスクが空であるかどうかを示す1バイトのブール値。 |
| 1023 | *(非推奨)* |
| 1024 | [レイヤー状態情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource) |
| 1025 | ワーキングパス（保存されません）。パスリソースフォーマット |
| 1026 | [レイヤーグループ情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource)。 ドラッググループ用のレイヤーごとに2バイトを含むグループID。グループ内のレイヤーは同じグループIDを持つ。 |
| 1027 | *(非推奨)* |
| 1028 | IPTC-NAAレコード。*ファイル情報*情報が含まれています。 |
| 1029 | 生の形式ファイルの画像モード |
| 1030 | JPEG品質。プライベート。 |
| 1032 | *(Photoshop 4.0)* [グリッドとガイド情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)* |
| 1033 | *(Photoshop 4.0)* [Photoshop 4.0用のサムネールリソース](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* のみ |
| 1034 | *(Photoshop 4.0)* 著作権フラグ。画像が著作権保護されているかどうかを示すブール値。 |
| 1035 | *(Photoshop 4.0)* URL。一様リソースロケータのテキスト文字列ハンドル。 |
| 1036 | *(Photoshop 5.0)* [サムネールリソース](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)*（リソース1033を置き換える）。 |
| 1037 | *(Photoshop 5.0)* [グローバルアングル](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*。エフェクトレイヤーのグローバル照明角を示す0から359までの整数を含む4バイト。存在しない場合、30と想定されます。 |
| 1038 | *(非推奨) ID 1073を参照してください。 (Photoshop 5.0)* カラーサンプラーリソース。 |
| 1039 | *(Photoshop 5.0)* [ICCプロファイル](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*。ICC（International Color Consortium）形式プロファイルの生のバイト。 |
| 1040 | *(Photoshop 5.0)* [ウォーターマーク](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*。 |
| 1041 | *(Photoshop 5.0)* [ICC未タグプロファイル](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*。ファイルを開くときに前提される任意のプロファイル処理を無効にする1バイト。1 = 意図的に未タグ付け。 |
| 1042 | *(Photoshop 5.0)* エフェクト可視。すべてのエフェクトレイヤーを表示/非表示にする1バイトのグローバルフラグ。非表示の場合のみ表示されます。 |
| 1043 | *(Photoshop 5.0)* スポットハーフトーン。バージョン用の4バイト、長さ用の4バイト、および可変長データ用の4バイト。 |
| 1044 | *(Photoshop 5.0)* [ドキュメント固有のID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)* シード番号。4バイト：層IDを生成する基本値（または既存のIDが既にそれを超える場合はより大きな値）。この目的は、レイヤーを追加して平坦化し、保存して開き、最初のセットと同じIDになるようにさらにレイヤーを追加した場合の例外を回避することです。 |
| 1045 | *(Photoshop 5.0)* [Unicode Alpha Names](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*。 |
| 1046 | *(Photoshop 6.0)* インデックスカラーテーブル数。実際に定義されているテーブル内の色の数のための2バイト |
| 1047 | *(Photoshop 6.0)* [透明度インデックス](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource)。 |
| 1049 | *(Photoshop 6.0)* [グローバル高度](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)。 |
| 1050 | *(Photoshop 6.0)* スライス。 |
| 1051 | *(Photoshop 6.0)* ワークフローURL。 |
| 1052 | *(Photoshop 6.0)* Jump To XPEP。2バイトのメジャーバージョン、2バイトのマイナーバージョン、4バイトの数。count分繰り返される。4バイトのブロックサイズ、キーが*'jtDd'*である場合、次に最初のバイトがdirtyフラグのブール値；それ以外の場合は、モディファイデートのエントリになります。 |
| 1053 | *(Photoshop 6.0)* アルファ識別子。 |
| 1054 | *(Photoshop 6.0)* [URLリスト](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*。 |
| 1057 | *(Photoshop 6.0)* [バージョン情報](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/versioninforesource)。 |
| 1058 | *(Photoshop 7.0)* EXIFデータ1。 |
| 1059 | *(Photoshop 7.0)* EXIFデータ3。 |
| 1060 | *(Photoshop 7.0)* [XMPメタデータ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource)。 XML記述としてのファイル情報。 |
| 1061 | *(Photoshop 7.0)* [キャプションダイジェスト](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)。 16バイト：RSA Data Security、MD5メッセージダイジェストアルゴリズム |
| 1062 | *(Photoshop 7.0)* [印刷スケール](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)。 (0 = 中央寄せ、1 = サイズに合わせる、2 = ユーザー定義)。4バイトx座標（浮動小数点数）。4バイトy座標（浮動小数点数）。4バイトスケール（浮動小数点数） |
| 1064 | *(Photoshop CS)* [ピクセルアスペクト比](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource)。 |
| 1065 | *(Photoshop CS)* レイヤー構成。 |
| 1066 | *(Photoshop CS)* 代替デュオトーンカラー。このリソースはPhotoshopによって読み取られたり使用されたりしません。 |
| 1067 | *(Photoshop CS)* 代替スポットカラー。このリソースはPhotoshopによって読み取られたり使用されたりしません。 |
| 1069 | *(Photoshop CS2)* [レイヤー選択ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource)。2バイトカウント、次にカウントごとに繰り返される：4バイトレイヤーID |
| 1070 | *(Photoshop CS2)* HDR調整情報。 |
| 1071 | *(Photoshop CS2)* 印刷情報。 |
| 1072 | *(Photoshop CS2)* [レイヤーグループ有効ID](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource)。 ドキュメント内の各レイヤーに1バイト、リソースの長さで繰り返します。注：レイヤーグループには開始および終了マーカーがあります。 |
| 1073 | *(Photoshop CS3)* カラーサンプラーリソース。古い形式のためにID 1038も参照してください。 |
| 1074 | *(Photoshop CS3)* 測定スケール。 |
| 1075 | *(Photoshop CS3)* タイムライン情報。 |
| 1076 | *(Photoshop CS3)* シートディスクロージャ。 |
| 1077 | *(Photoshop CS3)表示情報* 構造。浮動小数点カラーをサポート。ID 1007も参照してください。 |
| 1078 | *(Photoshop CS3)* オニオンスキン。 |
| 1080 | *(Photoshop CS4)* カウント情報。 |
| 1082 | *(Photoshop CS5)* 印刷情報。 |
| 1083 | *(Photoshop CS5)* 印刷スタイル。印刷マーク、ラベル、飾り物など。 |
| 1084 | *(Photoshop CS5)* Macintosh NSPrintInfo。Macintosh用の可変OS固有情報。 |
| 1085 | *(Photoshop CS5)* Windows DEVMODE。Windows用の可変OS固有情報。 |
| 1086 | *(Photoshop CS6)* 自動保存ファイルパス。 |
| 1087 | *(Photoshop CS6)* 自動保存形式。 |
| 1088 | *(Photoshop CC)* パス選択状態。 |
| 2000-2997 | パス情報（保存されたパス）。 |
| 2999 | クリッピングパスの名前。 |
| 3000 | *(Photoshop CC)* 生成元パス情報 |
| 4000-4999 | プラグインリソース。プラグインによって追加されたリソース。 |
| 7000 | Image Ready変数。変数定