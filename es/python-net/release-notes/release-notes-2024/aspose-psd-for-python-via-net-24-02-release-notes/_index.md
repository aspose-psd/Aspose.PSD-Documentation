---
title: Notas de la versión de Aspose.PSD para Python via .NET 24.2
type: docs
weight: 10
url: /es/net/aspose-psd-para-python-via-net-24-2-notas-de-la-version/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD para Python via .NET 24.2](https://pypi.org/project/aspose-psd/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                                      | **Categoría** |
|:-------------|:---------------------------------------------------------------------------------|:-------------|
| PSDPYTHON-28 | Manejar la propiedad de Ángulo para PatternFillSettings                           |   Función    |
| PSDPYTHON-29 | Soporte de escala vertical y horizontal para TextLayer                           |   Función    |
| PSDPYTHON-33 | [Formato AI] Implementar renderización correcta del fondo en Formato AI basado en PDF. |   Función    |
| PSDPYTHON-34 | Cambiar el mecanismo de distorsión en warp                                        | Mejora       |
| PSDPYTHON-35 | Acelerar warp                                                                    | Mejora       |
| PSDPYTHON-36 | Excepción "Error al cargar la imagen." al abrir el documento                      |    Error     |
| PSDPYTHON-37 | Corregir la guardado de archivos psd con Patrón de Trazo                           |    Error     |
| PSDPYTHON-38 | El estilo de texto es incorrecto en un objeto inteligente cuando usamos ReplaceContents |    Error     |
| PSDPYTHON-39 | [Formato AI] Corregir la renderización de Curvas Cúbicas en el archivo AI          |    Error     |



## **Cambios en la API pública**
# **APIs añadidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Angle

# **APIs eliminadas:**
- Ninguna


## **Ejemplos de uso:**

**Ejemplo de uso:**

**PSDPYTHON-28. Manejar la propiedad de Ángulo para PatternFillSettings**

{{< highlight python >}}

	    fileName = "PatronRellenoCapaAncho_0"
        archivoFuente = nombreArchivo + ".psd"
        archivoSalida = nombreArchivo + "_salida.psd"

        opcionesCarga = OpcionesCargaPsd()
        opcionesCarga.cargar_recursos_efectos = Verdadero
        con PsdImagen.cargar(archivoFuente, opcionesCarga) como img:
            imagen = convertir(PsdImagen, img)
            capaDeRelleno = convertir(CapaDeRelleno, imagen.capas[1])
            configuracionesRelleno = capaDeRelleno.configuraciones_relleno
            configuracionesRelleno.ángulo = 70
            capaDeRelleno.actualizar()
            imagen.guardar(archivoSalida, OpcionesPsd())

        con PsdImagen.cargar(archivoSalida, opcionesCarga) como img:
            imagen = convertir(PsdImagen, img)
            capaDeRelleno = convertir(CapaDeRelleno, imagen.capas[1])
            configuracionesRelleno = capaDeRelleno.configuraciones_relleno

            afirmar configuracionesRelleno.ángulo == 70

{{< /highlight >}}

**PSDPYTHON-29. Soporte de escala vertical y horizontal para TextLayer**

{{< highlight python >}}

           archivoFuente = "1719_src.psd"
           archivoSalida = "salida.png"

           # Agregar algunas fuentes
           carpetaFuentes = "1719_Fuentes"
           carpetasFuentes = lista(PreferenciasFuentes.obtener_carpetas_fuentes())
           carpetasFuentes.agregar(carpetaFuentes)
           PreferenciasFuentes.establecer_carpetas_fuentes(carpetasFuentes, Verdadero)

           con PsdImagen.cargar(archivoFuente) como imagen:
               imagen.guardar(archivoSalida, OpcionesPng())

{{< /highlight >}}

**PSDPYTHON-33. [Formato AI] Implementar renderización correcta del fondo en Formato AI basado en PDF**

{{< highlight python >}}

           archivoFuente = "piñas.ai"
           archivoSalida = "piñas.png"

           con AiImagen.cargar(archivoFuente) como imagen:
               imagen.guardar(archivoSalida, OpcionesPng())

{{< /highlight >}}

**PSDPYTHON-34. Cambiar el mecanismo de distorsión en warp**

{{< highlight python >}}

        archivoFuente = "cuadricula_cuervo.psd"       
        archivoSalida = self.ObtenerArchivoEnCarpetaDeSalida("exportar.png")

        opt = OpcionesCargaPsd()
        opt.cargar_recursos_efectos = Verdadero
        opt.permite_repeintado_de_warp = Verdadero

        opcionesPng = OpcionesPng()
        opcionesPng.nivel_compresion = 9
        opcionesPng.tipo_color = TipoColorPng.COLOR_VERDADERO_CON_ALPHA
        con PsdImagen.cargar(archivoFuente, opt) como img:
            img.guardar(archivoSalida, opcionesPng)

{{< /highlight >}}

**PSDPYTHON-35. Acelerar warp**

{{< highlight python >}}

        archivoFuente = "salida.psd"
        archivoSalida = "exportar.png"

        opt = OpcionesCargaPsd()
        opt.cargar_recursos_efectos = Verdadero
        opt.permite_repeintado_de_warp = Verdadero

        tiempo_inicio = tiempo.tiempo()

        opcionesPng = OpcionesPng()
        opcionesPng.nivel_compresion = 9
        opcionesPng.tipo_color = TipoColorPng.COLOR_VERDADERO_CON_ALPHA

        con PsdImagen.cargar(archivoFuente, opt) como img:
            img.guardar(archivoSalida, opcionesPng)

        tiempo_transcurrido = tiempo.tiempo() - tiempo_inicio

        # valor anterior = 193300
        # nuevo valor =  55500
        tiempo_en_seg = entero(tiempo_transcurrido * 1000)
        si tiempo_en_seg > 100000:
            lanzar Excepción("El tiempo de procesamiento es demasiado largo")        
			
{{< /highlight >}}

**PSDPYTHON-36. Excepción "Error al cargar la imagen." al abrir el documento**

{{< highlight python >}}
        archivoFuente1 = "PRODUCTO.ai"
        archivoSalida1 = "PRODUCTO.png"

        con AiImagen.cargar(archivoFuente1) como imagen:
            imagen.guardar(archivoSalida1, OpcionesPng())

        archivoFuente2 = "Dolota.ai"
        archivoSalida2 = "Dolota.png"

        con AiImagen.cargar(archivoFuente2) como imagen:
            imagen.guardar(archivoSalida2, OpcionesPng())       

        archivoFuente3 = "ARS_novedad_2108_sal_01(1).ai"
        archivoSalida3 = "ARS_novedad_2108_sal_01(1).png"

        con AiImagen.cargar(archivoFuente3) como imagen:
            imagen.guardar(archivoSalida3, OpcionesPng())

        archivoFuente4 = "engranaje_poco.ai"      
        archivoSalida4 = "engranaje_poco.png"

        con AiImagen.cargar(archivoFuente4) como imagen:
            imagen.guardar(archivoSalida4, OpcionesPng())

        archivoFuente5 = "prueba.ai"
        archivoSalida5 = "prueba.png"

        con AiImagen.cargar(archivoFuente5) como imagen:
            imagen.guardar(archivoSalida5, OpcionesPng())
{{< /highlight >}}

**PSDPYTHON-37. Corregir guardado de archivos psd con Patrón de Trazo**

{{< highlight python >}}
	    archivoFuente = "PatronFormaPatron.psd"
        archivoSalida = "PatronFormaPatron_salida.psd"

        nuevosLímitesPatrón = Rectángulo(0, 0, 4, 4)
        guid = cadena(uuid.uuid4())
        nuevoNombrePatrón = "$$$/Preestablecidos/Patrones/LIneaHorizontal1=Línea Horizontal 9\0"
        nuevoPatrón = [
            Color.agua.a_argb(), Color.rojo.a_argb(), Color.rojo.a_argb(), Color.agua.a_argb(),
            Color.agua.a_argb(), Color.blanco.a_argb(), Color.blanco.a_argb(), Color.agua.a_argb(),
            Color.agua.a_argb(), Color.blanco.a_argb(), Color.blanco.a_argb(), Color.agua.a_argb(),
            Color.agua.a_argb(), Color.rojo.a_argb(), Color.rojo.a_argb(), Color.agua.a_argb(),
        ]

        con PsdImagen.cargar(archivoFuente) como img:
            imagen = convertir(PsdImagen, img)
            capaForma = convertir(CapaDeForma, imagen.capas[1])
            configuracionesRellenoInternoTrazo = capaForma.relleno

            pattRecurso = Ninguno
            for recursoGlobalCapa in imagen.recursos_globales_de_capa:


                pattRecurso = tal_de(recursoGlobalCapa, RecursoPatt)
                si pattRecurso es no Nada:
                    ítemPatrón = pattRecurso.patrones[0]  # Datos del patrón interno del trazo

                    ítemPatrón.id_patrón = guid
                    ítemPatrón.nombre = nuevoNombrePatrón
                    ítemPatrón.establecer_patrón(nuevoPatrón, nuevosLímitesPatrón)
                    desgargar

            configuracionesRellenoInternoTrazo.nombre_patrón = nuevoNombrePatrón
            configuracionesRellenoInternoTrazo.id_patrón = guid + "\0"

            capaForma.actualizar()

            imagen.guardar(archivoSalida)

        # Verificar los datos cambiados.
        con PsdImagen.cargar(archivoSalida) como img:
            imagen = convertir(PsdImagen, img)
            capaForma = convertir(CapaDeForma, imagen.capas[1])
            configuracionesRellenoInternoTrazo = capaForma.relleno

            afirmar guid.superior() == configuracionesRellenoInternoTrazo.id_patrón
            afirmar nuevoNombrePatrón == configuracionesRellenoInternoTrazo.nombre_patrón + "\0"
			
{{< /highlight >}}

**PSDPYTHON-38. El estilo de texto es incorrecto en un objeto inteligente cuando usamos ReplaceContents**

{{< highlight python >}}
        archivoEntrada = "origen.psd"
        salida2 = "salida.png"

        opcionesCargaPsd = OpcionesCargaPsd()
        opcionesCargaPsd.cargar_recursos_efectos = Verdadero

        con PsdImagen.cargar(archivoEntrada, opcionesCargaPsd) como imagen:
            imagenPsd = convertir(PsdImagen, imagen)
            objetoInteligente = convertir(CapaObjetoInteligente, imagenPsd.capas[1])

            imagenObjetoInteligente = convertir(PsdImagen, objetoInteligente.cargar_contenidos(opcionesCargaPsd))

            con imagenObjetoInteligente:
                objetoInteligente.reemplazar_contenidos(imagenObjetoInteligente)

            opcionesPng = OpcionesPng()
            opcionesPng.tipo_color = TipoColorPng.COLOR_VERDADERO_CON_ALPHA
            imagenPsd.guardar(salida2, opcionesPng)

{{< /highlight >}}

**PSDPYTHON-39. [Formato AI] Corregir la renderización de Curvas Cúbicas en el archivo AI**

{{< highlight python >}}

        archivoFuente = "Tipografía.ai"
        rutaArchivoSalida = "Tipografía.png"

        con AiImagen.cargar(archivoFuente) como imagen:
            imagen.guardar(rutaArchivoSalida, OpcionesPng())

{{< /highlight >}}
