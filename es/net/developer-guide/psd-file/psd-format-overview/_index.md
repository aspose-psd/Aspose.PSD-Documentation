---
title: Descripción del formato PSD
type: docs
weight: 60
url: /es/net/psd-format-overview/
---

## **Descripción**
PSD, Documento de Photoshop, representa el formato de archivo nativo de Adobe Photoshop utilizado para el diseño y desarrollo gráfico.
## **Especificaciones del formato de archivo**
Los datos en un archivo PSD se almacenan en orden de bytes big-endian. Esto implica intercambiar los enteros cortos y largos al leer o escribir en la plataforma Windows. El formato de archivo de Photoshop se divide en cinco partes principales. Tiene muchos marcadores de longitud que se pueden usar para pasar de una sección a la siguiente. Los marcadores de longitud suelen estar rellenados con bytes para redondear al intervalo de 2 o 4 bytes más cercano. Las cinco partes principales son:

- Cabecera del archivo
- Datos del modo de color
- Recursos de imagen
- Información de capas y máscaras
- Datos de imagen

Para cumplir con ello, los datos deben escribirse en todos estos campos en la sección, ya que Photoshop puede intentar leer toda la sección. También implica que se escriban ceros en los campos omitidos al escribir en un archivo. El campo de longitud en las secciones delimitadas por longitud debe usarse para decidir cuándo detener la lectura. En la mayoría de los casos, el campo de longitud indica la cantidad de bytes, no registros, siguientes. Se deben recordar los siguientes puntos al leer un archivo.

- Los valores en la columna "Longitud" en todas las tablas están en bytes.
- Todos los valores definidos como cadena Unicode consisten en:
- Un campo de longitud de 4 bytes, que representa el número de caracteres en la cadena (no bytes).
- La cadena de valores Unicode, dos bytes por carácter.
## **Características del formato**
Los archivos PSD pueden incluir capas de imagen, capas de ajuste, máscaras de capa, anotaciones, información de archivo, palabras clave y otros elementos específicos de Photoshop. Los archivos de Photoshop tienen la extensión predeterminada .PSD y tienen una altura y ancho máximo de 30,000 píxeles, y un límite de longitud de dos gigabytes.
## **Cómo se puede utilizar**
1. Un instrumento para el corte de PSD.
1. [Convertir PSD](/psd/es/net/converting-psd-image-to-raster-format/) a HTML.
1. Usar [PSD como plantilla](/psd/es/net/using-psd-files-as-templates-for-automation-business-cards-case/) para correos electrónicos.
1. PSD a HTML de CMS específico.
1. Identikit en Archivo PSD (Boceto de la policía).
1. Crear imágenes de vista previa pseudo-3D utilizando Objetos Inteligentes para productos como botellas, tazas, camisetas, etc.
1. Edición rápida de PSD: Auto-tono, Preajustes, Objeto Inteligente, Recorte de Imagen de Capa de Texto.

Y mucho más. Si ha creado algo genial con Aspose.PSD, comparta con nosotros su caso de estudio utilizando los [Foros de Aspose](https://forum.aspose.com/).


Puede aprender más ejemplos adicionales de:

- [Estudios de caso](https://downloads.aspose.com/corporate/case-studies/aspose.psd/)
- [Demostraciones](/psd/es/net/showcases-html/)
