---
title: Notas de la versión Aspose.PSD Adapters para .NET 24.4
type: docs
weight: 100
url: /es/net/adapters/aspose-psd-adapters-para-net-24-4-release-notes/
---

{{% alert color="primary" %}}

Esta página contiene notas de la versión de [Aspose.PSD Adapters para .NET 24.4](https://www.nuget.org/packages/Aspose.PSD.Adapters.Imaging/)

{{% /alert %}}

| **Clave**    | **Resumen**                                                          | **Categoría** |
|:------------|:---------------------------------------------------------------------|:------------|
| PSDNET-1985 | Publicación inicial de Aspose.PSD.Adapters.Imaging en Nuget         | Mejora |


## **Cambios en la API pública**
# **APIs añadidas:**
- Ninguna

# **APIs eliminadas:**
- Ninguna

## **Ejemplos de uso:**

Por favor, revise [página de documentación de Aspose.PSD.Adapters](/psd/es/net/adapters)

**PSDNET-1985. Ejemplo más completo de uso de Aspose.PSD.Adapters**

{{< highlight csharp >}}
// Agregar habilitación de adaptadores en su configuración de inicialización
Aspose.PSD.Adapters.Imaging.EnableLoaders(
   FormatoArchivo.Bmp,
   FormatoArchivo.Gif,
   FormatoArchivo.Jpeg2000,
   FormatoArchivo.Jpeg,
   FormatoArchivo.Png,
   FormatoArchivo.Svg,
   FormatoArchivo.Tiff,
   FormatoArchivo.Webp);
            
// Adicionalmente habilitar Exportadores
Aspose.PSD.Adapters.Imaging.EnableExporters();

// Para trabajar con adaptadores, necesita tanto la licencia de Aspose.PSD como la del adaptador
// Aquí tiene cómo aplicar la Licencia de Aspose.PSD
var licencia = new Aspose.PSD.License();
licencia.SetLicense(@"Aspose.PSD.NET.lic");

// Aquí tiene un ejemplo de cómo aplicar la Licencia del Adaptee para Aspose.Imaging
var licImaging = new Aspose.Imaging.License();
licImaging.SetLicense(@"Aspose.Imaging.NET.lic");
// Luego puede ejecutar cualquier código de adaptadores o de las bibliotecas PSD o Imaging

// Después de esto, todos estos archivos pueden ser abiertos por Aspose.PSD sin ningún código adicional, solo use
using (var img = Aspose.PSD.Image.Load("SomeFile.Webp")) 
{
    // Después de ejecutar este código, obtendrá el archivo PSD creado a partir de WEBP y puede aplicar cualquier filtro, capas y ajustes de Aspose.PSD incluyendo la Transformación de deformación
}

// También puede crear imágenes adaptables de exportación al formato PSD
using (WebPImage webp = new WebPImage(300, 300, null))
{
    // Utilice la API de Aspose.Imaging para editar archivos WEBP con funciones específicas de Imaging
    var gr = new Aspose.Imaging.Graphics(webp);             
    gr.Clear(Aspose.Imaging.Color.Wheat);

    gr.DrawArc(
        new Aspose.Imaging.Pen(Aspose.Imaging.Color.Black, 5),
        new Aspose.Imaging.Rectangle(50, 50, 200, 200), 
        0, 
        270);

    // Luego simplemente use el método ToPsdImage() y edite el archivo como un PSD con funciones similares a las de Photoshop incluyendo capas, filtros inteligentes y objetos inteligentes.
    using (var psdImage = webp.ToPsdImage())
    {                   
        psdImage.AddTextLayer("Algún texto", new Rectangle(100, 100, 100, 50));
        var hue = psdImage.AddHueSaturationAdjustmentLayer();
        hue.Hue = 130;

        // Guarde el archivo PSD final usando Aspose.PSD
        psdImage.Save("output.psd");
    }
}

// Si no necesita usar los Loaders o Exportadores proporcionados por los Adaptadores, simplemente deshabilítelos
Adapters.Imaging.DisableLoaders();
Adapters.Imaging.DisableExporters();		
		
{{< /highlight >}}
