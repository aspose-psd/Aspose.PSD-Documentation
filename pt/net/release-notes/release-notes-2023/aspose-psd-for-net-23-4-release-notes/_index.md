---
title: Notas de Lançamento do Aspose.PSD para .NET 23.4
type: docs
weight: 90
url: /pt/net/aspose-psd-para-net-23-4-notas-de-lancamento/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD para .NET 23.4](https://www.nuget.org/packages/Aspose.PSD/).

{{% /alert %}}

| **Chave** | **Resumo** | **Categoria** |
| :- | :- | :- |
| PSDNET-1409 | Projetar classe RawColor para a API pública para usar no PSD API em vez da estrutura Color obsoleta | Melhoria |
| PSDNET-1332 | Integrar a Camada de Ajuste de Mapa de Degradê do Probation para o código principal do Aspose.PSD | Recurso |
| PSDNET-1448 | A edição de texto usando Trechos de Texto não salva o resultado correto | Correção |
| PSDNET-1449 | O início e o fim dos estilos ou parágrafos aparecem no lugar incorreto na edição da Camada de Texto por ITextPortion | Correção |
| PSDNET-1509 | Formatação movendo ao editar no photoshop | Correção |

## Alterações na API Pública

# APIs Adicionadas:
- T: Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind
- F: Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Solid
- F: Aspose.PSD.FileFormats.Psd.Layers.Gradient.GradientKind.Noise
- T: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.#ctor
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Signature
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Key
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Length
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.PsdVersion
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TypeToolKey
- M: Aspose.PSD.FileFormats.Psd.Layers.Layer.Save(System.IO.Stream)
- P: Aspose.PSD.FileFormats.Psd.Layers.FillSettings.GradientColorPoint.ColorMode
- M: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.SetPsdVersion(System.UInt16)
- T: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.#ctor(System.Byte,System.String)
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.PermittedFullNames
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.BitDepth
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Value
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Name
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.Description
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent.FullName
- T: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.FileFormats.Psd.Core.RawColor.ColorComponent[])
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.Components
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetColorModeName
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetBitDepth
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsInt
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsInt(System.Int32)
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.GetAsLong
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.SetAsLong(System.Int64)
- M: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.#ctor(Aspose.PSD.PixelDataFormat,System.Int16)
- P: Aspose.PSD.FileFormats.Psd.Core.RawColor.RawColor.ColorMode
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Reverse
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Dither
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientName
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ExpansionCount
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Interpolation
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.GradientMode
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.RndNumberSeed
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ShowTransparency
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.UseVectorColor
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.Roughness
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorModel
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.ColorPoints
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.TransparencyPoints
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MinimumColor
- P: Aspose.PSD.FileFormats.Psd.Layers.LayerResources.GrdmResource.MaximumColor

# APIs Removidas:
- Nenhuma

## Exemplos de Uso:

**PSDNET-1332. Integrar Camada de Ajuste de Mapa de Degradê do Probation para o código principal do Aspose.PSD**

{{< highlight csharp >}}
string sourceFile = "gradient_map_default.psd";
string outputFile = "gradient_map_res.psd";

using (var image = (PsdImage)Image.Load(sourceFile, new PsdLoadOptions()))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // verificar valores atuais
    AssertAreEqual(false, grdmResource.Reverse);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)65535, grdmResource.ColorPoints[1].RawColor.Components[3].Value);

    grdmResource.Reverse = true;
    // Cor vermelha para o segundo ponto de cor do degradê
    grdmResource.ColorPoints[1].RawColor.Components[1].Value = ushort.MaxValue;
    grdmResource.ColorPoints[1].RawColor.Components[2].Value = 0;
    grdmResource.ColorPoints[1].RawColor.Components[3].Value = 0;

    image.Save(outputFile, new PsdOptions());
}

using (var image = (PsdImage)Image.Load(outputFile))
{
    Layer layer = image.Layers[1];
    GrdmResource grdmResource = (GrdmResource)layer.Resources[0];

    // verificar valores alterados
    AssertAreEqual(true, grdmResource.Reverse);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[2].Value);
    AssertAreEqual((ulong)0, grdmResource.ColorPoints[1].RawColor.Components[3].Value);
}

void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Os objetos não são iguais.");
    }
}
{{< /highlight >}}

**PSDNET-1409. Projetar classe RawColor para a API pública para usá-la na API PSD em vez da estrutura Color obsoleta**

{{< highlight csharp >}}
void AssertAreEqual(object expected, object actual, string message = null)
{
    if (!object.Equals(expected, actual))
    {
        throw new Exception(message ?? "Os objetos não são iguais.");
    }
}

var cor = new RawColor(PixelDataFormat.Rgba32Bpp);
var corAntiga = Color.FromArgb(5, 1, 2, 3);

var valorArgb = corAntiga.ToArgb();
cor.SetAsInt(valorArgb);

AssertAreEqual("ARGB", cor.GetColorModeName());
AssertAreEqual(32, cor.GetBitDepth());
AssertAreEqual("A Alpha", cor.Components[0].FullName);
AssertAreEqual(5, (int)cor.Components[0].Value);
AssertAreEqual("R Vermelho", cor.Components[1].FullName);
AssertAreEqual(1, (int)cor.Components[1].Value);
AssertAreEqual("G Verde", cor.Components[2].FullName);
AssertAreEqual(2, (int)cor.Components[2].Value);
AssertAreEqual("B Azul", cor.Components[3].FullName);
AssertAreEqual(3, (int)cor.Components[3].Value);

AssertAreEqual(valorArgb, cor.GetAsInt());
{{< /highlight >}}

**PSDNET-1448. A edição de texto usando Trechos de Texto não salva o resultado correto**

{{< highlight csharp >}}
string sourceFile = "originalv5.psd";
string psdExportPath = "export.psd";

using (var imageTestEmail = (PsdImage)Image.Load(sourceFile))
{
    var layers = imageTestEmail.Layers;
    foreach (var layerItem in layers)
    {
        var isTextLayer = layerItem.GetType() == typeof(TextLayer) ? true : false;
        if (isTextLayer)
        {
            var layerTLToUpdateText = (TextLayer)layerItem;

            // Buscar texto lsak
            if (layerTLToUpdateText.Text.Contains("lsak"))
            {
                var textoDataTL = layerTLToUpdateText.TextData;

                if (textoDataTL.Text.Contains("lsak") && textoDataTL.Text.Contains("\r"))
                {
                    // Substituir texto
                    replaceLsakText(textoDataTL);
                    // Formatar texto
                    formatStyleText(textoDataTL);
                }
            }
        }
    }

    imageTestEmail.Save(psdExportPath, new PsdOptions());
}

string[] texts = new string[]
{
    "Power play.",
    "// Mundos mais expansivos. Tempos de carregamento rápidos. Altas taxas de frames. E uma gama mais ampla de cores. Um computador com Windows sempre foi a melhor plataforma para jogos—e com o Windows 11, ele só fica melhor.//"
};
...
{{< /highlight >}}

**PSDNET-1449. O início e o fim dos estilos ou parágrafos aparecem no lugar incorreto na edição da Camada de Texto por ITextPortion**

{{< highlight csharp >}}
string sourceFilePSDEmail = "inputv2.psd";
string outputFile = "export.psd";

using (PsdImage imageTestEmail = (PsdImage)Aspose.PSD.Image.Load(sourceFilePSDEmail))
{
    var layers = imageTestEmail.Layers;

    foreach (var layerItem in layers)
    {
        var layerTLToUpdateText = layerItem as TextLayer;

        if (layerTLToUpdateText == null)
        {
            continue;
        }

        // Buscar texto lsak
        if (!layerTLToUpdateText.Text.Contains("lsak") ||
            !layerTLToUpdateText.TextData.Text.Contains("lsak"))
        {
            continue;
        }

        var textDataTL = layerTLToUpdateText.TextData;

        // Etapa: Substituir texto
        ReplaceLsakFourthMethod(textDataTL);

        System.Console.WriteLine("Texto substituído " + textDataTL.Text);

        // Etapa: Formatar texto
        FormatLsakFourthMethod(textDataTL);

        System.Console.WriteLine("Texto formatado " + textDataTL.Text);

        // Etapa: Centralizar camada de texto
        if (layerTLToUpdateText.DisplayName.Equals("cc") ||
            layerTLToUpdateText.DisplayName.Equals("tl") ||
            layerTLToUpdateText.DisplayName.Equals("cl"))
        {
            // Valores antigos
            var boundBoxAntiga = layerTLToUpdateText.TextBoundBox;
            var YAntigo = layerTLToUpdateText.Top;

            textDataTL.UpdateLayerData();

            // Novos valores
            var tamanhoPalavra = layerTLToUpdateText.Size;
            var novoTamanho = new Aspose.PSD.Size((int)Math.Ceiling(boundBoxAntiga.Width), tamanhoPalavra.Height);
            var antesPonto = CenterInRectangle(tamanhoPalavra,
                new Aspose.PSD.RectangleF(layerTLToUpdateText.Left, layerTLToUpdateText.Top,
                    layerTLToUpdateText.Width, boundBoxAntiga.Height));

            layerTLToUpdateText.TextBoundBox =
                new Aspose.PSD.RectangleF(new Aspose.PSD.PointF(0, antesPonto.Y - YAntigo),
                    novoTamanho);

            var novoPonto = CenterInRectangle(tamanhoPalavra,
                new Aspose.PSD.RectangleF(layerTLToUpdateText.Left, layerTLToUpdateText.Top,
                    layerTLToUpdateText.Width, boundBoxAntiga.Height));

            layerTLToUpdateText.Left = (int)novoPonto.X;
            layerTLToUpdateText.Top = (int)novoPonto.Y;

            textDataTL.UpdateLayerData();

            System.Console.WriteLine("Centralizar texto");
        }
    }

    imageTestEmail.Save(outputFile);
}

Aspose.PSD.PointF CenterInRectangle(Aspose.PSD.Size Inner, Aspose.PSD.RectangleF Outer)
{
    return new Aspose.PSD.PointF()
    {
        X = (Outer.X + (Outer.Width - Inner.Width) / 2),
        Y = (Outer.Y + (Outer.Height - Inner.Height) / 2)
    };
}
...
{{< /highlight >}}

**PSDNET-1509. Formato movido ao editar no photoshop**

{{< highlight csharp >}}
string strings1 = "input-lsaks-strings1 - forTicket.txt";
string psdInput = "input_for_ticket.psd";
string outputPsd = "1509_output.psd";
string outputPng = "1509_output.png";
...