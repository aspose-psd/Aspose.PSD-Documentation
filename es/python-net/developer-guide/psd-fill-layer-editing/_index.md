---
title: Actualización de capa de relleno PSD con Python
weight: 100
type: docs
description: Ejemplos de uso de todos los tipos de capas de ajuste, incluyendo Relleno de color, Relleno de degradado y Relleno de patrón
keywords: [capa de relleno, Relleno de color, Relleno de degradado, Relleno de patrón, api de psd, python, ejemplo de código]
url: /es/python-net/actualizacion-de-capa-de-relleno-psd/
---

## **Visión general**

Para crear una capa regular, puede utilizar la función create_regular_layer proporcionada en el código. Esta función toma los parámetros left, top, width y height para definir la posición y el tamaño de la capa. Crea una nueva capa, establece sus límites y la rellena con un color especificado.

Para crear una capa de relleno de color, puede utilizar el método FillLayer.create_instance con el parámetro FillType.COLOR. Después de crear la capa de relleno, puede acceder a su configuración de relleno utilizando la propiedad fill_settings y establecer el color utilizando la propiedad color de la clase ColorFillSettings. En el código proporcionado, el color se establece en Color.coral. La propiedad de recorte de la capa de relleno se establece en 1, lo que hace que la capa actúe como una máscara de recorte.

Para crear una capa de relleno de degradado, puede utilizar el método FillLayer.create_instance con el parámetro FillType.GRADIENT. Al igual que con la capa de relleno de color, puede acceder a la configuración de relleno utilizando la propiedad fill_settings y establecer los puntos de color del degradado y los puntos de transparencia. En el código proporcionado, los puntos de color del degradado se definen utilizando la clase GradientColorPoint y los puntos de transparencia se definen utilizando la clase GradientTransparencyPoint. La propiedad de recorte de la capa de relleno también se establece en 1.

Para crear una capa de relleno de patrón, puede utilizar el método FillLayer.create_instance con el parámetro FillType.PATTERN. Nuevamente, puede acceder a la configuración de relleno utilizando la propiedad fill_settings y establecer los datos del patrón y otras propiedades. En el código proporcionado, los datos del patrón se definen utilizando la clase PatternFillSettings, y la propiedad de recorte se establece en 1.

Después de crear las capas de relleno, puede agregarlas a la imagen PSD utilizando el método add_layer. También puede especificar el nombre de visualización y otras propiedades para cada capa de relleno.

Finalmente, puede guardar la imagen PSD y la imagen PNG correspondiente utilizando el código proporcionado. Las opciones de PNG están configuradas para usar verdadero color con alfa para la transparencia.

Por favor, revise el ejemplo completo.

## **Ejemplo**
{{< gist "aspose-com-gists" "04e945e867d0b7f39bb3eab63074d04c" "Documentacion-Python-Aspose-psd-actualizacion-capa-relleno.py" >}}
