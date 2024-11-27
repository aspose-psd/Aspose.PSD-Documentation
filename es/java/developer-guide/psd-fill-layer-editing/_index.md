---
title: Actualización de capa de relleno PSD usando Java
weight: 100
type: docs
description: Ejemplos de uso de todos los tipos de capas de ajuste, incluyendo Color Fill, Gradient Fill y Pattern Fill
keywords: [capa de relleno, Color Fill, Gradient Fill, Pattern Fill, api psd, java, código de ejemplo]
url: es/java/psd-fill-layer-editing/
---

## **Descripción general**

La creación de una capa regular implica el uso de la función createRegularLayer, la cual requiere parámetros para definir la posición y el tamaño de la capa. Esta función crea una nueva capa, establece sus límites y la rellena con un color especificado.

Para una capa de relleno de color, se utiliza el método FillLayer.createInstance con el parámetro FillType.Color. Una vez creada la capa de relleno, se accede a su configuración de relleno a través de la propiedad fill_settings y se establece el color deseado utilizando la propiedad color de la clase ColorFillSettings. En este contexto, el color se establece en Color.getCoral(). Además, la propiedad de recorte de la capa de relleno se establece en 1, lo que hace que funcione como una máscara de recorte.

Las capas de relleno de degradado se crean de manera similar utilizando el método FillLayer.create_instance, pero con el parámetro FillType.Gradient. Al igual que las capas de relleno de color, se accede a la configuración de relleno a través de fill_settings y se establecen los puntos de color del degradado y los puntos de transparencia. En este ejemplo, los puntos de color del degradado se definen con la clase GradientColorPoint y los puntos de transparencia con la clase GradientTransparencyPoint. La propiedad de recorte de la capa de relleno también se establece en 1.

Las capas de relleno de patrón se crean utilizando FillLayer.createInstance con el parámetro FillType.Pattern. Una vez más, se accede a la configuración de relleno a través de fill_settings y se establecen los datos del patrón y otras propiedades. En este código, los datos del patrón se definen utilizando la clase PatternFillSettings, y la propiedad de recorte se establece en 1.

Una vez creadas las capas de relleno, agréguelas a la imagen PSD utilizando el método addLayer, especificando el nombre de visualización y otras propiedades para cada capa de relleno.

Por último, guarde la imagen PSD y su correspondiente imagen PNG con el código proporcionado. Las opciones PNG están configuradas para utilizar color verdadero con alfa para transparencia.

Consulte el ejemplo completo para obtener más detalles.

## **Ejemplo**
{{< gist "aspose-com-gists" "31800d807a72f1f50fe4b29374119227" "Documentation-Java-Aspose-psd-fill-layer-editing.java" >}}
