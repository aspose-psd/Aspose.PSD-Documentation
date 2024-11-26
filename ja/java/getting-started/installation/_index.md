---
title: Installation
type: docs
weight: 40
url: /ja/java/installation/
---

## **MavenリポジトリからAspose.PSD for Javaのインストール**
AsposeはすべてのJava APIを[Mavenリポジトリ](https://releases.aspose.com/java/repo/com/aspose/)でホストしています。簡単な設定で、Mavenプロジェクトで[Aspose.PSD for Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) APIを直接使用できます。
### **Mavenリポジトリの設定を指定**
まずMavenのpom.xmlでAspose Mavenリポジトリの設定/場所を次のように指定する必要があります:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Aspose.PSD for Java APIの依存関係を定義**
その後、pom.xmlでAspose.PSD for Java APIの依存関係を次のように定義します:

{{< highlight java >}}

 <dependencies>
    <dependency>
        <groupId>com.aspose</groupId>
        <artifactId>aspose-psd</artifactId>
        <version>24.2</version>
        <classifier>jdk16</classifier>
    </dependency>
</dependencies>

{{< /highlight >}}

上記の手順を実行すると、Aspose.PSD for Javaの依存関係が最終的にMavenプロジェクトで定義されます。
## **サポートされるプラットフォーム**
Aspose.PSD for Javaは最も人気のある開発および展開プラットフォームをサポートしています。

|**機能**|**説明**|
| :- | :- |
|デスクトップアプリケーション|Aspose.PSD for Javaを使用して、MS Windowsでデスクトップアプリケーションを開発することができます。|
|エンタープライズWebアプリケーション|Aspose.PSD for JavaはWebアプリケーションを完全にサポートしています。|
|Linux/Unix|Aspose.PSD for Javaはプラットフォームに依存しないAPIであり、LinuxおよびUnix環境で動作します。|
## **サポートされているJavaバージョン**
- JDK 1.6以降
