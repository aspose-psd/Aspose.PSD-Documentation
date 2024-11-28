---
title: Notas de lanzamiento de Aspose.PSD para Python vía .NET 24.3
type: docs
weight: 10
url: /es/net/aspose-psd-para-python-via-net-24-3-notas-de-lanzamiento/
---

{{% alert color="primary" %}}

Esta página contiene las notas de lanzamiento para [Aspose.PSD para Python vía .NET 24.3](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**      | **Resumen**                                                          | **Categoría**|
|:-------------|:---------------------------------------------------------------------|:------------|
| PSDPYTHON-42 | [AI Format] Reducir el tiempo de carga de imágenes AI multipágina grandes | Mejora |
| PSDPYTHON-45 | El archivo PSD se volvió ilegible después de la conversión de 8 bits a 16 bits |     Error     |
| PSDPYTHON-46 | El archivo PSD se volvió ilegible después de la conversión de 8 bits a 32 bits |     Error     |
| PSDPYTHON-47 | [AI Format] Corregir la representación de la curva corta en el archivo AI                 |     Error     |



## **Cambios en la API pública**
# **APIs agregadas:**
- Ninguna

# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**PSDPYTHON-42. [AI Format] Reducir el tiempo de carga de imágenes AI multipágina grandes**

{{< highlight python >}}
   # No hay ejemplo
{{< /highlight >}}

**PSDPYTHON-45. El archivo PSD se volvió ilegible después de la conversión de 8 bits a 16 bits**

{{< highlight python >}}
        archivoFuente = "test_smart_layer.psd"
        archivoSalida = "export.psd"

        with PsdImage.load(archivoFuente) as psdImagen8:
            opciones16 = PsdOptions()
            opciones16.channel_bits_count = 16

            psdImagen8.save(archivoSalida, opciones16)

        with PsdImage.load(archivoSalida) as imagen:
            psdImagen16 = cast(PsdImage, imagen)

            recursoPrueba = as_of(psdImagen16.global_layer_resources[5], Lr16Resource)
            if recursoPrueba is not None:
                # está bien
                pass
            else:
                raise Exception("Recurso global incorrecto, el primer recurso debería ser Lr16Resource")
{{< /highlight >}}

**PSDPYTHON-46. El archivo PSD se volvió ilegible después de la conversión de 8 bits a 32 bits**


{{< highlight python >}}
        archivoFuente = "test_smart_layer.psd"
        archivoSalida = "export.psd"

        with PsdImage.load(archivoFuente) as psdImagen8:
            opciones32 = PsdOptions()
            opciones32.channel_bits_count = 32

            psdImagen8.save(archivoSalida, opciones32)

        with PsdImage.load(archivoSalida) as imagen:
            psdImagen32 = cast(PsdImage, imagen)

            recursoPrueba = as_of(psdImagen32.global_layer_resources[5], Lr32Resource)
            if recursoPrueba is not None:
                # está bien
                pass
            else:
                raise Exception("Recurso global incorrecto, el primer recurso debería ser Lr32Resource")
{{< /highlight >}}

**PSDPYTHON-47. [AI Format] Corregir la representación de la curva corta en el archivo AI**

{{< highlight python >}}
        archivoFuente = "shortCurve.ai"
        rutaArchivoSalida = "shortCurve.png"

        with AiImage.load(archivoFuente) as imagen:
            imagen.save(rutaArchivoSalida, PngOptions())
{{< /highlight >}}
