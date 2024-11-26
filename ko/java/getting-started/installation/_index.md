---
title: 설치
type: 문서
weight: 40
url: /ko/java/installation/
---

## **Maven 저장소에서 Aspose.PSD for Java 설치**
Aspose는 모든 Java API를 [Maven 저장소](https://releases.aspose.com/java/repo/com/aspose/)에 호스팅합니다. 간단한 구성을 사용하여 Maven 프로젝트에서 [Aspose.PSD for Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) API를 직접 사용할 수 있습니다.
### **Maven 저장소 구성 지정**
우선 Maven pom.xml에서 Aspose Maven 저장소 구성/위치를 다음과 같이 지정해야 합니다.

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Aspose.PSD for Java API 종속성 정의**
그런 다음 pom.xml에서 Aspose.PSD for Java API 종속성을 다음과 같이 정의해야 합니다.

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

위 단계를 수행한 후 Maven 프로젝트에서 Aspose.PSD for Java 종속성이 최종적으로 정의됩니다.
## **지원되는 플랫폼**
Aspose.PSD for Java는 가장 인기 있는 개발 및 배포 플랫폼을 지원합니다.

|**기능**|**설명**|
| :- | :- |
|데스크톱 응용 프로그램|Aspose.PSD for Java를 사용하여 MS Windows 용 데스크톱 응용 프로그램을 개발할 수 있습니다.|
|기업 웹 응용 프로그램|Aspose.PSD for Java는 완전히 웹 응용 프로그램을 지원합니다.|
|Linux/Unix|Aspose.PSD for Java는 플랫폼 독립적인 API이며 Linux 및 Unix 환경에서 작동할 수 있습니다.|
## **지원되는 Java 버전**
- JDK 1.6 이상
