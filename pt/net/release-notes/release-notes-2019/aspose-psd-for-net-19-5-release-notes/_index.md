---
title: Notas da Versão do Aspose.PSD para .NET 19.5
type: docs
weight: 80
url: /pt/net/aspose-psd-para-net-19-5-notas-de-versao/
---

{{% alert color="primary" %}}

Esta página contém notas de versão para o Aspose.PSD para .NET 19.5

{{% /alert %}}

| **Chave** | **Resumo** | **Categoria** |
| :- | :- | :- |
|PSDNET-133|Adicionar suporte a camadas de preenchimento: Padrão|Recurso|
|PSDNET-138|Suporte de PtFlResource|Recurso|
|PSDNET-129|Implementar método de recorte correto para arquivos PSD|Recurso|
|PSDNET-140|Suporte de VsmsResource|Recurso|
|PSDNET-121|As camadas visíveis em uma subpasta visível em uma pasta invisível são renderizadas, mas não deveriam|Erro|
|PSDNET-119|PSD (modo RGB 16 bits por canal) não convertido adequadamente para JPG|Erro|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Linked
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PointType
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternId
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.HorizontalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.VerticalOffset
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.IPatternFillSettings.PatternHeight
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternData
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternWidth
- P:Aspose.PSD.FileFormats.Psd.Layers.FillSettings.PatternFillSettings.PatternHeight
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.#ctor(System.String,System.String)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PsdVersion
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternName
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Offset
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Scale
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.IsLinkedWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.AlignWithLayer
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.PatternId
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.PtFlResource.TypeToolKey
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VectorPathDataResource.Save(Aspose.PSD.StreamContainer,System.Int32)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.#ctor(System.Byte[])
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.Key
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VsmsResource.TypeToolKey
- M:Aspose.PSD.Image.DoAfterCreate(System.Int64@,System.Int64)
- P:Aspose.PSD.ImageOptionsBase.BufferSizeHint
- M:Aspose.PSD.Metered.GetConsumptionCredit
# **APIs Removidas:**
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Paths
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Version
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsDisabled
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsNotLinked
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.IsInverted
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Signature
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.PsdVersion
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.VmskResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Exemplos de Uso:**
**PSDNET-133. Adicionar suporte a camadas de preenchimento: Padrão**

{{< highlight java >}}

 // Adicionar suporte a camadas de preenchimento: Padrão

    string sourceFileName = "CamadaDePreenchimentoPadrao.psd";

    string exportPath = "CamadaDePreenchimentoPadrao_Edited.psd";

    double tolerância = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var camada in im.Layers)

         {

             if (camada is FillLayer)

             {

                  FillLayer fillLayer = (FillLayer)camada;

                  PatternFillSettings fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                  if (fillSettings.HorizontalOffset != -46 || 

                      fillSettings.VerticalOffset != -45 || 

                      fillSettings.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5"||

                      fillSettings.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares" ||

                      fillSettings.AlignWithLayer != true ||

                      fillSettings.Linked != true ||

                      fillSettings.PatternHeight != 64 ||

                      fillSettings.PatternWidth != 64 ||

                      fillSettings.PatternData.Length != 4096 ||

                      Math.Abs(fillSettings.Scale - 50) > tolerância) 

                      {

                          throw new Exception("A imagem PSD foi lida incorretamente");

                      }

                  // Edição

                  fillSettings.Scale = 300;

                  fillSettings.HorizontalOffset = 2;

                  fillSettings.VerticalOffset = -20;

                  fillSettings.PatternData = new int[]

                  {

                       Color.Red.ToArgb(), Color.Blue.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Red.ToArgb(),  Color.Blue.ToArgb(),

                       Color.Blue.ToArgb(), Color.Blue.ToArgb(),  Color.Red.ToArgb()

                  };

                  fillSettings.PatternHeight = 3;

                  fillSettings.PatternWidth = 3;

                  fillSettings.AlignWithLayer = false;

                  fillSettings.Linked = false;

                  fillSettings.PatternId = Guid.NewGuid().ToString();

                  fillLayer.Update();

                  break;

             }

         }

         im.Save(exportPath);

    }

{{< /highlight >}}

**PSDNET-138. Suporte de PtFlResource**

{{< highlight java >}}

  // Suporte de PtFlResource

    string sourceFileName = "CamadaDePreenchimentoPadrao.psd";

    string exportPath = "PtFlResource_Edited.psd";

    double tolerância = 0.0001;

    var im = (PsdImage)Image.Load(sourceFileName);

    using (im)

    {

         foreach (var camada in im.Layers)

         {

             if (camada is FillLayer)

             {

                var fillLayer = (FillLayer)camada;

                var recursos = fillLayer.Resources;

                foreach (var res in recursos)

                {

                    if (res is PtFlResource)

                    {

                        // Leitura

                        PtFlResource recurso = (PtFlResource)res;

                        if (

                            recurso.Offset.X != -46 || 

                            recurso.Offset.Y != -45 || 

                            recurso.PatternId != "a6818df2-7532-494e-9615-8fdd6b7f38e5\0" ||

                            recurso.PatternName != "$$$/Presets/Patterns/OpticalSquares=Optical Squares\0" ||

                            recurso.AlignWithLayer != true ||

                            recurso.IsLinkedWithLayer != true ||

                            !(Math.Abs(recurso.Scale - 50) < tolerância)) {

                                throw new Exception("O recurso PtFl foi lido incorretamente");

                            }

                        // Edição

                        recurso.Offset = new Point(-11, 13);

                        recurso.Scale = 200;

                        recurso.AlignWithLayer = false;

                        recurso.IsLinkedWithLayer = false;

                        fillLayer.Resources = fillLayer.Resources;

                        // Não temos dados de padrão em PattResource, então podemos adicioná-los.

                        var fillSettings = (PatternFillSettings)fillLayer.FillSettings;

                        fillSettings.PatternData = new int[]

                        {

                            Color.Black.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                            Color.White.ToArgb(),

                        };

                        fillSettings.PatternHeight = 1;

                        fillSettings.PatternWidth = 4;

                        fillSettings.PatternName = "$$$/Presets/Patterns/VerticalLine=Vertical Line New\0";

                        fillSettings.PatternId = Guid.NewGuid().ToString() + "\0";

                        fillLayer.Update();

                    }

                    break;

                }

                break;

            }

         }

         im.Save(exportPath);

    } 

{{< /highlight >}}

**PSDNET-129. Implementar método de recorte correto para arquivos PSD**

{{< highlight java >}}

             // Implementar método de recorte correto para arquivos PSD.

            string sourceFileName = "1.psd";

            string exportPathPsd = "CropTest.psd";

            string exportPathPng = "CropTest.png";

            using (RasterImage imagem = Image.Load(sourceFileName) as RasterImage)

            {

                imagem.Crop(new Rectangle(10, 30, 100, 100));

                imagem.Save(exportPathPsd, new PsdOptions());

                imagem.Save(exportPathPng, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });

            }

{{< /highlight >}}

**PSDNET-140. Suporte de VsmsResource**

{{< highlight java >}}

 // Suporte de VsmsResource

        static void ExemploDoSuporteDeVsmsResource()

        {

            string sourceFileName = "RetânguloVazio.psd";

            string exportPath = "RetânguloVazio_modificado.psd";

            var im = (PsdImage)Image.Load(sourceFileName);

            using (im)

            {

                var recurso = GetVsmsResource(im);

                // Leitura

                if (recurso.IsDisabled != false ||

                    recurso.IsInverted != false ||

                    recurso.IsNotLinked != false ||

                    recurso.Paths.Length != 7 ||

                    recurso.Paths[0].Type != VectorPathType.PathFillRuleRecord ||

                    recurso.Paths[1].Type != VectorPathType.InitialFillRuleRecord ||

                    recurso.Paths[2].Type != VectorPathType.ClosedSubpathLengthRecord ||

                    recurso.Paths[3].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    recurso.Paths[4].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked ||

                    recurso.Paths[5].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked||

                    recurso.Paths[6].Type != VectorPathType.ClosedSubpathBezierKnotUnlinked)

                {

                        throw new Exception("VsmsResource foi lido incorretamente");

                }

                var pathFillRule = (PathFillRuleRecord)recurso.Paths[0];

                var initialFillRule = (InitialFillRuleRecord)recurso.Paths[1];

                var subpathLength = (LengthRecord)recurso.Paths[2];

                // A regra de preenchimento do caminho não contém nenhuma informação adicional

                if (pathFillRule.Type != VectorPathType.PathFillRuleRecord || 

                initialFillRule.Type != VectorPathType.InitialFillRuleRecord ||

                initialFillRule.IsFillStartsWithAllPixels != false ||

                subpathLength.Type != VectorPathType.ClosedSubpathLengthRecord ||

                subpathLength.IsClosed != true ||

                subpathLength.IsOpen != false) 

                {

                    throw new Exception("Os caminhos do VsmsResource foram lidos incorretamente");

                }

                // Edição

                recurso.IsDisabled = true;

                recurso.IsInverted = true;

                recurso.IsNotLinked = true;

                var bezierKnot = (BezierKnotRecord)recurso.Paths[3];

                bezierKnot.Points[0] = new Point(0, 0);

                bezierKnot = (BezierKnotRecord)recurso.Paths[4];

                bezierKnot.Points[0] = new Point(8039798, 10905191);

                initialFillRule.IsFillStartsWithAllPixels = true;

                subpathLength.IsClosed = false;

                im.Save(exportPath);

            }         

        }

        static VsmsResource GetVsmsResource(PsdImage imagem)

        {

            var camada = imagem.Layers[1];

            VsmsResource recurso = null;

            var recursos = camada.Resources;

            for (int i = 0; i < recursos.Length; i++)

            {

                if (recursos[i] is VsmsResource)

                {

                    recurso = (VsmsResource)recursos[i];

                    break;

                }

            }

            if (recurso == null)

            {

                throw new Exception("VsmsResource não encontrado");

            }

            return recurso;

        }  

{{< /highlight >}}



**PSDNET-121: As camadas visíveis em uma subpasta visível em uma pasta invisível são renderizadas, mas não deveriam**

{{< highlight java >}}

 // As camadas visíveis em uma subpasta visível em uma pasta invisível são renderizadas, mas não deveriam

            string sourceFileName = "MuitasPastas.psd.psd";

            string caminhoSaidaJpg = "outMuitasPastas.jpg";

            string caminhoSaidaPsd = "outMuitasPastas.psd";

            var opções = new PsdLoadOptions();

            using (PsdImage imagem = (PsdImage)Image.Load(sourceFileName, opções))

            {

                imagem.Save(caminhoSaidaPsd, new PsdOptions(imagem));

                imagem.Save(caminhoSaidaJpg, new JpegOptions() { Qualidade = 100 });

            }

{{< /highlight >}}



**PSDNET-119. PSD (modo RGB 16 bits por canal) não convertido adequadamente para JPG**

{{< highlight java >}}

  // Psd não convertido adequadamente para jpg

            string sourceFileName = "in.psd";

            string caminhoExportação = "outRgb.jpg";

            var opções = new PsdLoadOptions();

            using (PsdImage imagem = (PsdImage)Image.Load(sourceFileName, opções))

            {

                imagem.Save(caminhoExportação, new JpegOptions() { Qualidade = 100 });

            }

{{< /highlight >}}