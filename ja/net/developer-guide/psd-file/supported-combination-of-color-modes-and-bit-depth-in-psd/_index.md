---
title: PSDでサポートされているカラーモードとビット深度の組み合わせ
type: ドキュメント
weight: 80
url: /ja/net/supported-combination-of-color-modes-and-bit-depth-in-psd/
---

## **説明**
Aspose.PSDは、Adobe Photoshop PSDファイルの任意のカラーモードとビット深度の組み合わせを開くことをサポートしています。これらのファイルを開いて、ローレベルAPIを使用してファイルの内容を変更できます。ただし、一部の人気のない組み合わせには、カラーモード制限に関連する特定の問題がある場合があります。

## **PSDで読み取り専用モードでサポートされているカラーモードとビット深度のエクスポート組み合わせ**

| | ビットマップ | グレースケール | インデックスカラー | RGB | CMYK | マルチチャンネル | デュオトーン | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| 深度1 | はい[](https://issue.kharkov.dynabic.com/issues/PSDNET-283) | - | - | - | - | - | - | - |
| 深度8 | - | はい | はい | はい | はい | いいえ Q3-Q4 | いいえ Q3-Q4 | はい[](https://issue.kharkov.dynabic.com/issues/PSDNET-290) |
| 深度16 | - | はい | - | はい | はい | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-287) | - | いいえ (Q3-Q4) |
| 深度32 | - | はい*[](https://issue.kharkov.dynabic.com/issues/PSDNET-125) | - | はい* | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-285) | -[](https://issue.kharkov.dynabic.com/issues/PSDNET-288) | - | - |
\* 一部の場合における軽微な問題

## **PSDで編集可能モードでサポートされているカラーモードとビット深度のエクスポート組み合わせ**

| | ビットマップ | グレースケール | インデックスカラー | RGB | CMYK | マルチチャンネル | デュオトーン | Lab |
| :- | :- | :- | :- | :- | :- | :- | :- | :- |
| 深度1 | はい | - | - | - | - | - | - | - |
| 深度8 | - | はい | いいえ | はい | はい | いいえ Q3-Q4 | いいえ Q3-Q4 | はい* |
| 深度16 | - | はい | - | はい | はい* | - | - | いいえ (Q3-Q4) |
| 深度32 | - | いいえ (Q3-Q4) | - | いいえ (Q3-Q4) | - | - | - | - |
\* 一部の場合における軽微な問題

特定のカラーモード/ビット深度の組み合わせのサポートが必要な場合は、[Asposeフォーラム](https://forum.aspose.com/c/psd)に投稿することができます。
