---
title: Instalación
type: docs
weight: 40
url: /es/java/instalacion/
---

## **Instalación de Aspose.PSD para Java desde el Repositorio de Maven**
Aspose aloja todas las API de Java en el [repositorio Maven](https://releases.aspose.com/java/repo/com/aspose/). Puede usar fácilmente la API [Aspose.PSD para Java](https://releases.aspose.com/java/repo/com/aspose/aspose-psd/) directamente en sus proyectos de Maven con configuraciones simples.
### **Especificar la Configuración del Repositorio de Maven**
Primero, necesita especificar la configuración/ubicación del Repositorio de Maven de Aspose en su pom.xml de Maven de la siguiente manera:

{{< highlight java >}}

 <repositories>
    <repository>
        <id>AsposeJavaAPI</id>
        <name>Aspose Java API</name>
        <url>https://releases.aspose.com/java/repo/</url>
    </repository>
</repositories>

{{< /highlight >}}
### **Definir la Dependencia de la API de Aspose.PSD para Java**
Luego defina la dependencia de la API de Aspose.PSD para Java en su pom.xml de la siguiente manera:

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

Después de realizar los pasos anteriores, la dependencia de Aspose.PSD para Java finalmente estará definida en su proyecto de Maven.
## **Plataformas Compatibles**
Aspose.PSD para Java es compatible con las plataformas de desarrollo y despliegue más populares.

|**Funcionalidad**|**Descripción**|
| :- | :- |
|Aplicaciones de Escritorio|Aspose.PSD para Java se puede utilizar para desarrollar aplicaciones de escritorio en MS Windows.|
|Aplicaciones Web Empresariales|Aspose.PSD para Java soporta completamente aplicaciones web.|
|Linux/Unix|Aspose.PSD para Java es una API independiente de la plataforma y puede funcionar en un entorno Linux y Unix.|
## **Versiones de Java Compatibles**
- JDK 1.6 o superior
