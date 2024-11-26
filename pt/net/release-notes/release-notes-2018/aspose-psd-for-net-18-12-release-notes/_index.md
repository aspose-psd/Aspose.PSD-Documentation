---
title: Aspose.PSD para .NET 18.12 - Notas de Lançamento
type: docs
weight: 10
url: /pt/net/aspose-psd-para-net-18-12-notas-de-lancamento/
---

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-76|Suporte à Camada de Traço|Recurso|
|PSDNET-83|Suporte ao Efeito de Gradiente|Recurso|
|PSDNET-84|Suporte ao Efeito de Padrão|Recurso|
|PSDNET-89|Habilitar a capacidade de adicionar a nova camada regular gerada à PsdImage|Recurso|
|PSDNET-93|Após atualização do conteúdo da camada de texto com o caractere \ (barra invertida), o arquivo resultante não pode ser aberto no Photoshop|Erro|
|PSDNET-39|Imagens quebradas após a exportação com dados de imagem muito grandes no Modo de Cor CMYK|Erro|
|PSDNET-52|Possível: a rotação no PSD não funciona|Erro|
|PSDNET-88|Possível: Os métodos de recorte no Aspose.Psd não estão funcionando|Erro|
|PSDNET-91|Aplicar alterações do Aspose.Imaging ao Aspose.PSD|Melhoria|

## **Alterações na API Pública**
Método Aspose.PSD.FileFormats.Psd.PsdImage.AddRegularLayer

Classe Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException

Método Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String)

Método Aspose.PSD.CoreExceptions.ImageFormats.PsdImageArgumentException.#ctor(System.String,System.Exception)

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.#ctor

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BaseFillSettings.FillType

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.Color

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.ColorFillSettings.FillType

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Color

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Gradient

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.FillType.Pattern

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Color

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.Location

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint.MedianPointLocation

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Color

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AlignWithLayer

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Dither

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Reverse

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.Angle

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GradientType

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.HorizontalOffset

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.VerticalOffset

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.FillType

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.ColorPoints

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.TransparencyPoints

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddColorPoint

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.AddTransparencyPoint

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveTransparencyPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint)

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.RemoveColorPoint(Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientColorPoint)

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Opacity

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.Location

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientTransparencyPoint.MedianPointLocation

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.FillType

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Linked

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Scale

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PointType

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternName

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.PatternId

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.HorizontalOffset

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.VerticalOffset

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.BlendMode

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.IsVisible

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.FillSettings

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.StrokeEffect.Opacity

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Linear

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Radial

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Angle

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Reflected

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.Diamond

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Lfx2Resources.GradientType.ShapeBurst

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource

Método Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor

Método Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.#ctor(System.Byte[])

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternData

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternId

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Name

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Height

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Width

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.ImageMode

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Version

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PatternLength

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Signature

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Key

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Length

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.PsdVersion

Método Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.SetPattern(System.Int32[],Aspose.PSD.Rectangle)

Método Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.Save(Aspose.PSD.StreamContainer,System.Int32)

Campo/Enum Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PattResource.TypeToolKey

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.#ctor

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientFillSettings.GenerateLfx2ResourceNodes

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Settings

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.BlendMode

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.IsVisible

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.GradientOverlayEffect.Opacity

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.Color

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddGradientOverlay

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.BlendingOptions.AddPatternOverlay

Método Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternFillSettings.GenerateLfx2ResourceNodes(System.String,Aspose.PSD.Color,System.String,System.String,System.Double,System.Boolean,Aspose.PSD.PointF)

Classe Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Settings

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.BlendMode

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.IsVisible

Propriedade Aspose.PSD.FileFormats.Psd.Layers.LayerEffects.PatternOverlayEffect.Opacity

## **Exemplos de Uso:**
**PSDNET-76. Suporte à Camada de Traço**

**1) Tipo de Preenchimento - Padrão**

{{< highlight java >}}

     // Efeito de Traço. Tipo de Preenchimento - Padrão. Exemplo

    string nomeArquivoFonte = "Traço.psd";

    string caminhoExportacao = "TraçoPreenchimentoAlterado.psd";

    var opcoesCarregamento = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    // Preparando novos dados

    var novoPadrao = new int[]

    {

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

         Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

    };

   var novosLimitesPadrao = new Rectangle(0, 0, 4, 4);

   var guid = Guid.NewGuid();

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte, opcoesCarregamento))

    {

         var traçoPadrão = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

         Assert.AreEqual(BlendMode.Normal, traçoPadrão.BlendMode);

         Assert.AreEqual(255, traçoPadrão.Opacity);

         Assert.AreEqual(true, traçoPadrão.IsVisible);

         var configPreenchimento = (PatternFillSettings)traçoPadrão.FillSettings;

         Assert.AreEqual(FillType.Pattern, configPreenchimento.FillType);

         traçoPadrão.Opacity = 127;

         traçoPadrão.BlendMode = BlendMode.Color;

         PattResource recurso;

         foreach (var recursoCamadaGlobal in im.GlobalLayerResources)

         {

             if (recursoCamadaGlobal is PattResource)

             {

                  recurso = (PattResource)recursoCamadaGlobal;

                  recurso.PatternId = guid.ToString();

                  recurso.Name = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";        

                  recurso.SetPattern(novoPadrão, novosLimitesPadrao);               

             }

         }

         ((PatternFillSettings)configPreenchimento).PatternName = "$$$/Presets/Patterns/HorizontalLine1=Horizontal Line 9\0";

         ((PatternFillSettings)configPreenchimento).PatternId = guid.ToString() + "\0";

        im.Save(caminhoExportacao);

    }

    // Arquivo de teste após edição

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte, opcoesCarregamento))

    {

        var traçoPadrão = (StrokeEffect)im.Layers[3].BlendingOptions.Effects[0];

        PattResource recurso = null;

        foreach (var recursoCamadaGlobal in im.GlobalLayerResources)

        {

            if (recursoCamadaGlobal is PattResource)

            {

                recurso = (PattResource)recursoCamadaGlobal;

            }

        }

        if (recurso == null)

        {

            throw new Exception("Recurso PattResource não encontrado");

        }

        // Verificar os dados do padrão

        Assert.AreEqual(novoPadrão, recurso.PatternData);

        Assert.AreEqual(novosLimitesPadrao, new Rectangle(0, 0, recurso.Width, recurso.Height));

        Assert.AreEqual(guid.ToString(), recurso.PatternId);

        Assert.AreEqual(BlendMode.Color, traçoPadrão.BlendMode);

        Assert.AreEqual(127, traçoPadrão.Opacity);

         Assert.AreEqual(true, traçoPadrão.IsVisible);

        var configPreenchimento = (PatternFillSettings)traçoPadrão.FillSettings;

        Assert.AreEqual(FillType.Pattern, configPreenchimento.FillType);

    }

{{< /highlight >}}

**2) Tipo de Preenchimento - Gradiente**

{{< highlight java >}}

     // Efeito de Traço. Tipo de Preenchimento - Gradiente. Exemplo

    string nomeArquivoFonte = "Traço.psd";

    string caminhoExportacao = "TraçoGradienteAlterado.psd";

    var opcoesCarregamento = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte, opcoesCarregamento))

    {

        var traçoGradiente = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, traçoGradiente.BlendMode);

        Assert.AreEqual(255, traçoGradiente.Opacity);

        Assert.AreEqual(true, traçoGradiente.IsVisible);

        var configPreenchimento = (GradientFillSettings)traçoGradiente.FillSettings;

        Assert.AreEqual(Color.Black, configPreenchimento.Color);

        Assert.AreEqual(FillType.Gradient, configPreenchimento.FillType);

        Assert.AreEqual(true, configPreenchimento.AlignWithLayer);

        Assert.AreEqual(GradientType.Linear, configPreenchimento.GradientType);

        Assert.IsTrue(Math.Abs(90 - configPreenchimento.Angle) < 0.001, "O ângulo está incorreto");

        Assert.AreEqual(false, configPreenchimento.Dither);

        Assert.IsTrue(Math.Abs(0 - configPreenchimento.HorizontalOffset) < 0.001, "O deslocamento horizontal está incorreto");

        Assert.IsTrue(Math.Abs(0 - configPreenchimento.VerticalOffset) < 0.001, "O deslocamento vertical está incorreto");

        Assert.AreEqual(false, configPreenchimento.Reverse);

        // Pontos de cor

        var pontosCor = configPreenchimento.ColorPoints;

        Assert.AreEqual(2, pontosCor.Length);

        Assert.AreEqual(Color.Black, pontosCor[0].Color);

        Assert.AreEqual(0, pontosCor[0].Location);

        Assert.AreEqual(50, pontosCor[0].MedianPointLocation);

        Assert.AreEqual(Color.White, pontosCor[1].Color);

        Assert.AreEqual(4096, pontosCor[1].Location);

        Assert.AreEqual(50, pontosCor[1].MedianPointLocation);

        // Pontos de transparência

        var pontosTransparência = configPreenchimento.TransparencyPoints;

        Assert.AreEqual(2, pontosTransparência.Length);

        Assert.AreEqual(0, pontosTransparência[0].Location);

        Assert.AreEqual(50, pontosTransparência[0].MedianPointLocation);

        Assert.AreEqual(100, pontosTransparência[0].Opacity);

        Assert.AreEqual(4096, pontosTransparência[1].Location);

        Assert.AreEqual(50, pontosTransparência[1].MedianPointLocation);

        Assert.AreEqual(100, pontosTransparência[1].Opacity);

        // Testar edição

        configPreenchimento.Color = Color.Green;

        traçoGradiente.Opacity = 127;

        traçoGradiente.BlendMode = BlendMode.Color;

        configPreenchimento.AlignWithLayer = false;

        configPreenchimento.GradientType = GradientType.Radial;

        configPreenchimento.Angle = 45;

        configPreenchimento.Dither = true;

        configPreenchimento.HorizontalOffset = 15;

        configPreenchimento.VerticalOffset = 11;

        configPreenchimento.Reverse = true;

        // Adicionar novo ponto de cor

        var pontoCor = configPreenchimento.AddColorPoint();

        pontoCor.Color = Color.Green;

        pontoCor.Location = 4096;

        pontoCor.MedianPointLocation = 75;

        // Alterar a localização doponto anteriormente inserido

        configPreenchimento.ColorPoints[1].Location = 1899;

        // Adicionar novo ponto de transparência

        var pontoTransparência = configPreenchimento.AddTransparencyPoint();

        pontoTransparência.Opacity = 25;

        pontoTransparência.MedianPointLocation = 25;

        pontoTransparência.Location = 4096;

        // Alterar a localização do ponto de transparência anterior

        configPreenchimento.TransparencyPoints[1].Location = 2411;

        im.Save(caminhoExportacao);

    }

    // Arquivo de teste após edição

    using (var im = (PsdImage)Image.Load(caminhoExportacao, opcoesCarregamento))

    {

        var traçoGradiente = (StrokeEffect)im.Layers[2].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Color, traçoGradiente.BlendMode);

        Assert.AreEqual(127, traçoGradiente.Opacity);

        Assert.AreEqual(true, traçoGradiente.IsVisible);

        var configPreenchimento = (GradientFillSettings)traçoGradiente.FillSettings;

        Assert.AreEqual(Color.Green, configPreenchimento.Color);

        Assert.AreEqual(FillType.Gradient, configPreenchimento.FillType);

        // Verificar pontos de cor

        Assert.AreEqual(3, configPreenchimento.ColorPoints.Length);

        var ponto = configPreenchimento.ColorPoints[0];

        Assert.AreEqual(50, ponto.MedianPointLocation);

        Assert.AreEqual(Color.Black, ponto.Color);

        Assert.AreEqual(0, ponto.Location);

        ponto = configPreenchimento.ColorPoints[1];

        Assert.AreEqual(50, ponto.MedianPointLocation);

        Assert.AreEqual(Color.White, ponto.Color);

        Assert.AreEqual(1899, ponto.Location);

        ponto = configPreenchimento.ColorPoints[2];

        Assert.AreEqual(75, ponto.MedianPointLocation);

        Assert.AreEqual(Color.Green, ponto.Color);

        Assert.AreEqual(4096, ponto.Location);

        // Verificar pontos de transparência

        Assert.AreEqual(3, configPreenchimento.TransparencyPoints.Length);

        var pontoTransparência = configPreenchimento.TransparencyPoints[0];

        Assert.AreEqual(50, pontoTransparência.MedianPointLocation);

        Assert.AreEqual(100, pontoTransparência.Opacity);

        Assert.AreEqual(0, pontoTransparência.Location);

        pontoTransparência = configPreenchimento.TransparencyPoints[1];

        Assert.AreEqual(50, pontoTransparência.MedianPointLocation);

        Assert.assertEquals(100, pontoTransparência.Opacity);

        Assert.assertEquals(2411, pontoTransparência.Location);

        pontoTransparência = configPreenchimento.TransparencyPoints[2];

        Assert.assertEquals(25, pontoTransparência.MedianPointLocation);

        Assert.assertEquals(25, pontoTransparência.Opacity);

        Assert.assertEquals(4096, pontoTransparência.Location);

    }

{{< /highlight >}}

**PSDNET-84. Suporte ao Efeito de Padrão.**

{{< highlight java >}}

    // Efeito de sobreposição de padrão. Exemplo

    string nomeArquivoFonte = "SobreposicaoPadrao.psd";

    string caminhoExportacao = "SobreposicaoPadraoAlterada.psd";

    var novoPadrão = new int[]

    {

        Color.Aqua.ToArgb(), Color.Red.ToArgb(), Color.Red.ToArgb(), Color.Aqua.ToArgb(),

        Color.Aqua.ToArgb(), Color.White.ToArgb(), Color.White.ToArgb(), Color.Aqua.ToArgb(),

    };

    var novosLimitesPadrão = new Rectangle(0, 0, 4, 2);

    var guid = Guid.NewGuid();

    var novoNomePadrão = "$$$/Presets/Patterns/Pattern=Novo nome de padrão\0";

    var opcoesCarregamento = new PsdLoadOptions()

    {

        LoadEffectsResource = true

    };

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        var efeitoPadrão = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.AreEqual(BlendMode.Normal, efeitoPadrão.BlendMode);

        Assert.AreEqual(127, efeitoPadrão.Opacity);

        Assert.AreEqual(true, efeitoPadrão.IsVisible);

        var configurações = efeitoPadrão.Settings;

        Assert.AreEqual(Color.Empty, configurações.Color);

        Assert.AreEqual(FillType.Pattern, configurações.FillType);

        Assert.AreEqual("85163837-eb9e-5b43-86fb-e6d5963ea29a\0", configurações.PatternId);

        Assert.AreEqual("$$$/Presets/Patterns/OpticalSquares=Optical Squares\0", configurações.PatternName);

        Assert.AreEqual(null, configurações.PointType);

        Assert.assertEquals(100, configurações.Scale);

        Assert.AreEqual(false, configurações.Linked);

        Assert.IsTrue(Math.Abs(0 - configurações.HorizontalOffset) < 0.001, "O deslocamento horizontal está incorreto");

        Assert.assertTrue(Math.abs(0 - configurações.VerticalOffset) < 0.001, "O deslocamento vertical está incorreto");

        // Testar a edição

        configurações.Color = Color.Green;

        efeitoPadrão.Opacity = 193;

        efeitoPadrão.BlendMode = BlendMode.Difference;

        configurações.HorizontalOffset = 15;

        configurações.VerticalOffset = 11;

        PattResource recurso;

        foreach (var recursoCamadaGlobal in im.GlobalLayerResources)

        {

            if (recursoCamadaGlobal is PattResource)

            {

                recurso = (PattResource)recursoCamadaGlobal;

                recurso.PatternId = guid.ToString();

                recurso.Name = novoNomePadrão;

                recurso.SetPattern(novoPadrão, novosLimitesPadrão);

            }

        }

        configurações.PatternName = novoNomePadrão;

        configurações.PatternId = guid.ToString() + "\0";

        im.Save(caminhoExportacao);

    }

    // Arquivo de teste após edição

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte, opcoesCarregamento))

    {

        var efeitoPadrão = (PatternOverlayEffect)im.Layers[1].BlendingOptions.Effects[0];

        Assert.assertEquals(BlendMode.Difference, efeitoPadrão.BlendMode);

        Assert.assertEquals(193, efeitoPadrão.Opacity);

        Assert.assertEquals(true, efeitoPadrão.IsVisible);

        var configurações = efeitoPadrão.Settings;

        Assert.AreEqual(Color.Empty, configurações.Color);

        Assert.AreEqual(FillType.Pattern, configurações.FillType);

        PattResource recurso = null;

        foreach (var recursoCamadaGlobal in im.GlobalLayerResources)

        {

             if (recursoCamadaGlobal is PattResource)

             {

                 recurso = (PattResource)recursoCamadaGlobal;

             }

        }

        if (recurso == null)

        {

             throw new Exception("Recurso PattResource não encontrado");

        }

        // Verificar os dados do padrão

        Assert.AreEqual(novoPadrão, recurso.PatternData);

        Assert.AreEqual(novosLimitesPadrão, new Rectangle(0, 0, recurso.Width, recurso.Height));

        Assert.assertEquals(guid.ToString(), recurso.PatternId);

        Assert.AreEqual(novoNomePadrão, recurso.Name);

    }

{{< /highlight >}}

**PSDNET-89. Habilitar a capacidade de adicionar a nova camada regular gerada à PsdImage.**

{{< highlight java >}}

  // Habilitar a capacidade de adicionar a nova camada regular gerada à PsdImage

    string nomeArquivoFonte = "UmaCamada.psd";

    string caminhoExportacao = "UmaCamadaEditada.psd";

    string caminhoExportacaoPng = "UmaCamadaEditada.png";

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte))

    {

       // Preparando dois arrays int

       var dados1 = new int[2500];

       var dados2 = new int[2500];

       var limite1 = new Rectangle(0, 0, 50, 50);

       var limite2 = new Rectangle(0, 0, 100, 25);

       for (int i = 0; i < 2500; i++)

       {

           dados1[i] = -10000000;

           dados2[i] = -10000000;

       }

       var camadas = new Layer[4];

       for (int i = 0; i < 4; i++)

       {

           camadas[i] = im.AddRegularLayer();

           camadas[i].SaveArgb32Pixels(limite1, dados1);

       }

       image.Resize(186, 602);

       camadas[0].Crop(new Rectangle(0, 0, 186, 159));

       camadas[1].Crop(new Rectangle(186, 0, 186, 159));

       camadas[2].Crop(new Rectangle(0, 159, 186, 142));

       camadas[3].Crop(new Rectangle(186, 159, 186, 142));

       var camadaAntiga = im.Layers[0];

       camadaAntiga.Dispose();

       im.Layers = camadas;

       var topo = 0;

       for (int i = 0; i < 4; i++)

       {

           var largura = camadas[i].Width;

           var altura = camadas[i].Height;

           camadas[i].Left = 0;

           camadas[i].Top = topo;

           camadas[i].Right = largura;

           camadas[i].Bottom = altura + camadas[i].Top;

           topo += camadas[i].Height;

       }

       // Salvando como psd

       im.Save(caminhoExportacao, new PsdOptions());

       // Salvando como png

       im.Save(caminhoExportacaoPng, new PngOptions());

    }

{{< /highlight >}}

**PSDNET-93. Após atualização do conteúdo da camada de texto com o caractere \ (barra invertida), o arquivo resultante não pode ser aberto no Photoshop.**

{{< highlight java >}}

 using (

var imagem =

Image.Load(

"exemplo.psd"))

{

if (!(imagem is PsdImage)) return;

                var psdImagem = (PsdImage)imagem;

                var camadas = psdImagem.Layers;

                for (var índice = camadas.Length - 1; índice >= 0; índice--)

                {

                    var camada = camadas[índice];

                    if (!(camada is TextLayer)) continue;

                    var camadaTexto = (TextLayer)camada;

                    camadaTexto.UpdateText("展 就");

                }

                var opçõesImagem = new PsdOptions(psdImagem);

                psdImagem.Save("resultado.psd", opçõesImagem);

            }

{{< /highlight >}}

**PSDNET-39. Imagens quebradas após a exportação com dados de imagem muito grandes no Modo de Cor CMYK.**

{{< highlight java >}}

     // Imagens quebradas após a exportação com dados de imagem muito grandes no Modo de Cor CMYK. Exemplo

    string nomeArquivoFonte = "ImagemCMYKOversizedComCamadaDeAjuste.psd";

    string caminhoExportacao = "ImagemCMYKOversizedComCamadaDeAjuste.png";

    using (var im = (PsdImage)Image.Load(nomeArquivoFonte))

    {        

        im.Save(caminhoExportacao, new PngOptions());

    }

{{< /highlight >}}

**PSDNET-52. Possível: a rotação no PSD não funciona.**

{{< highlight java >}}

  // Rotação do PSD. Exemplo

    string nomeArquivoFonte = "OChapéu.psd";

    var opçõesPng = new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha };

    // Rotação da imagem inteira

    using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        for (int i = 0; i < 4; i++)

        {

            int ângulo = i * 45;

            imagem.Rotate(ângulo);

            string nomeArquivoSaida = "OChapéuRotacionado" + ângulo + ".png";

            imagem.Save(nomeArquivoSaida, opçõesPng);

        }

    }

    // Rotação da camada

    using (PsdImage imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        for (int i = 0; i < 4; i++)

        {

            int ângulo = i * 45;

            imagem.Layers[1].Rotate(ângulo);

            string nomeArquivoSaida = "OChapéuCamadaRotacionada" + ângulo + ".png";

            imagem.Save(nomeArquivoSaida, opçõesPng);

        }

    }       

{{< /highlight >}}

**PSDNET-88. Possível: Os métodos de recorte no Aspose.Psd não estão funcionando.**

{{< highlight java >}}

   // Possível: Os métodos de recorte no Aspose.Psd não estão funcionando

    string nomeArquivoFonte = "ArquivoFonte.psd";

    string caminhoExportacao = "ArquivoFonteEditado.psd";

    string caminhoExportacaoPng = "ArquivoFonteEditado.png";

    using (var imagem = (PsdImage)Image.Load(nomeArquivoFonte))

    {

        var camadaAntiga = imagem.Layers[0];

        var limitesAntigos = camadaAntiga.Bounds;

        var dadosCamadaAntiga = imagem.Layers[0].LoadArgb32Pixels(limitesAntigos);

        var camadas = new Layer[4];

        for (int i = 0; i < 4; i++)

        {

            camadas[i] = imagem.AddRegularLayer();

            camadas[i].SaveArgb32Pixels(limitesAntigos, dadosCamadaAntiga);

        }

        imagem.Resize(186, 602);

        camadas[0].Crop(new Rectangle(0, 0, 186, 159));

        camadas[1].Crop(new Rectangle(186, 0, 186, 159));

        camadas[2].Crop(new Rectangle(0, 159, 186, 142));

        camadas[3].Crop(new Rectangle(186, 159, 186, 142));

        camadaAntiga.Dispose();

        imagem.Layers = camadas;

        var topo = 0;

        for (int i = 0; i < 4; i++)

        {

            var largura = camadas[i].Width;

            var altura = camadas[i].Height;

            camadas[i].Left = 0;

            camadas[i].Top = topo;

            camadas[i].Right = largura;

            camadas[i].Bottom = altura + camadas[i].Top;

            topo += camadas[i].Height;

        }

        // Salvar como psd

        imagem.Save(caminhoExportacao, new PsdOptions());

        // Salvar como png

        imagem.Save(caminhoExportacaoPng, new PngOptions());

    }

{{< /highlight >}}
