---
title: Licencia con Medición
type: docs
weight: 70
url: /es/java/licencia-con-medicion/
---

{{% alert color="primary" %}} 

Aspose.PSD permite a los desarrolladores aplicar una clave con medición. Es un nuevo mecanismo de licenciamiento. El nuevo mecanismo de licenciamiento se utilizará junto con el método de licenciamiento existente. Los clientes que deseen facturar según el uso de las funciones de la API pueden utilizar el licenciamiento con medición. Para obtener más detalles, consulte la sección de [Preguntas frecuentes sobre Licencias con Medición](https://purchase.aspose.com/faqs/licensing/metered).

{{% /alert %}} 
## **Licencia con Medición**
Aquí están los pasos simples para usar la clase Metered.

1. Crear una instancia de la clase Metered.
1. Pasar las claves públicas y privadas al método setMeteredKey.
1. Realizar el procesamiento (realizar tareas).
1. Llamar al método getConsumptionQuantity de la clase Metered.
1. Devolverá la cantidad/cantidad de solicitudes a la API que ha consumido hasta ahora.

A continuación se muestra un código de ejemplo que demuestra cómo configurar la clave pública y privada con medición.

{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Examples-src-main-java-com-aspose-psd-examples-Licensing-MeteredLicensing-MeteredLicensing.java" >}}
