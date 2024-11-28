---
title: Note sulla versione di Aspose.PSD for .NET 20.10
type: docs
weight: 30
url: /it/net/aspose-psd-for-net-20-10-release-notes/
---

{{% alert color="primary" %}}

Questa pagina contiene le note sulla versione di [Aspose.PSD for .NET 20.10](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chiave**|**Sommario**|**Categoria**|
| :- | :- | :- |
|PSDNET-565|Eccezione durante il salvataggio di un file PSD specifico con livelli di testo|Bug|
|PSDNET-680|I font vengono persi dopo i passaggi con Aspose.PSD|Bug|
|PSDNET-704|Rendering dello Smart Object Layer|Feature|
|PSDNET-707|Supporto delle trasformazioni non distruttive dello Smart Object|Feature|
|PSDNET-711|Il livello di testo viene spostato dopo il salvataggio senza alcuna modifica|Bug|
|PSDNET-720|Aspose.PSD 20.8: eccezione di conversione da Psd a Tiff|Bug|

## **Cambiamenti nell'API pubblica**
# **API Aggiunte:**
- Nessuna
# **API Rimosse:**
- Nessuna

## **Esempi d'uso:**
**PSDNET-565. Eccezione durante il salvataggio di un file PSD specifico con livelli di testo**
{{< highlight csharp >}}
            string sourceFilePath = "OneReview-InDesign-RefreshPreviewIxD(2).psd";
            string outputFile = "result.psd";

            using (PsdImage image = (PsdImage)Image.Load(sourceFilePath))
            {
                image.Save(outputFile, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-680. I font vengono persi dopo i passaggi con Aspose.PSD**
{{< highlight csharp >}}
            string sourceFilePath = "TwoFonts.psd";

            string outputPsd1 = "output1.psd";
            string outputPsd2 = "output2.psd";
            string outputPng1 = "output1.png";
            string outputPng2 = "output2.png";

            void AreEqual(int expected, int actual)
            {
                if (expected != actual)
                {
                    throw new Exception("I valori non sono uguali.");
                }
            }

            using (var psdImage = (PsdImage)Image.Load(sourceFilePath))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd1, new PsdOptions(psdImage));
                psdImage.Save(outputPng1, new PngOptions());
            }

            using (var psdImage = (PsdImage)Image.Load(outputPsd1))
            {
                var textLayer = (TextLayer)psdImage.Layers[1];

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                textLayer.TextData.UpdateLayerData();

                AreEqual(1, textLayer.TextData.Items[0].Style.FontIndex);
                AreEqual(0, textLayer.TextData.Items[1].Style.FontIndex);

                psdImage.Save(outputPsd2, new PsdOptions(psdImage));
                psdImage.Save(outputPng2, new PngOptions());
            }
{{< /highlight >}}
**PSDNET-704. Rendering dello Smart Object Layer**
{{< highlight csharp >}}
            // Questo esempio mostra come sostituire il contenuto dello Smart Object Layer di Adobe® Photoshop® e il suo corretto rendering.
            string dataDir = "PSDNET704_1\\";
            string filePath = dataDir + "new_panama-papers-4-trans4.psd";
            string pngOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.png";
            string psdOutputPath = dataDir + "new_panama-papers-4-trans4_replaced.psd";
            string newContentPath = dataDir + "new_huset.jpg";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                smartObjectLayer.ReplaceContents(newContentPath);
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }

            // Questo esempio mostra come aggiornare la cache immagine dei livelli Smart Object di Adobe® Photoshop® e il loro corretto rendering.
            filePath = dataDir + "LayeredSmartObjects8bit2.psd";
            pngOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.png";
            psdOutputPath = dataDir + "LayeredSmartObjects8bit2_updated.psd";
            using (PsdImage image = (PsdImage)Image.Load(filePath))
            {
                image.SmartObjectProvider.UpdateAllModifiedContent();
                image.Save(pngOutputPath, new PngOptions() { ColorType = PngColorType.TruecolorWithAlpha });
                image.Save(psdOutputPath, new PsdOptions(image));
            }
{{< /highlight >}}
**PSDNET-707. Supporto delle trasformazioni non distruttive dello Smart Object**
{{< highlight csharp >}}
            string dataDir = "PSDNET707_1\\";
            string outputDir = dataDir;

            // Questi esempi dimostrano le trasformazioni non distruttive del file PSD con SmartObjectLayer.
            // Possiamo ridimensionare, ruotare, piegare, deformare, trasformare la prospettiva o deformare uno strato senza
            // perdere i dati o la qualità dell'immagine originale perché le trasformazioni non influenzano i dati originali.

            // Questo esempio mostra come ridimensionare l'immagine di Adobe® Photoshop® con livelli smart object:
            EsempioDiSupportoAlRidimensionamentoDell'ImmagineSmartObject("new_panama-papers-8-trans4-linked");
            EsempioDiSupportoAlRidimensionamentoDell'ImmagineSmartObject("picture-frame-4-linked3");
            EsempioDiSupportoAlRidimensionamentoDell'ImmagineSmartObject("gorilla");

            // Questo esempio mostra come ridimensionare il file PSD con livelli smart object.
            void EsempioDiSupportoAlRidimensionamentoDell'ImmagineSmartObject(string fileName)
            {
                const int scale = 4;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "Resize_" + fileName + ".psd";
                string outputPngPath = outputDir + "Resize_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    int newWidth = image.Width * scale;
                    int newHeight = image.Height * scale;
                    image.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Questo esempio mostra come ridimensionare lo smart object layer di Adobe® Photoshop®.
            EsempioDiSupportoAlRidimensionamentoDelLivelloSmartObject("new_panama-papers-8-trans4-linked");
            EsempioDiSupportoAlRidimensionamentoDelLivelloSmartObject("gorilla");

            // Questo esempio mostra come ridimensionare uno smart object layer nel file PSD.
            void EsempioDiSupportoAlRidimensionamentoDelLivelloSmartObject(string fileName)
            {
                const double scale = 3.5;
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "ResizeLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "ResizeLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    int newWidth = (int)(smartObjectLayer.Width * scale);
                    int newHeight = (int)(smartObjectLayer.Height * scale);
                    smartObjectLayer.Resize(newWidth, newHeight);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Questo esempio mostra come ritagliare lo smart object layer di Adobe® Photoshop®.
            EsempioDiSupportoAlRitaglioDelLivelloSmartObject("new_panama-papers-8-trans4-linked");
            EsempioDiSupportoAlRitaglioDelLivelloSmartObject("gorilla");

            // Questo esempio mostra come ritagliare uno smart object layer nel file PSD.
            void EsempioDiSupportoAlRitaglioDelLivelloSmartObject(string fileName)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + "CropLast_" + fileName + ".psd";
                string outputPngPath = outputDir + "CropLast_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Crop(25, 15, 30, 10);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Questo esempio mostra come ruotare e capovolgere l'immagine di Adobe® Photoshop® con livelli smart object:
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("gorilla", RotateFlipType.Rotate90FlipNone);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipX);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipY);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.RotateNoneFlipXY);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipNone);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipX);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipY);
            EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject("new_panama-papers-8-trans4-linked", RotateFlipType.Rotate90FlipXY);

            // Questo esempio mostra come ruotare e capovolgere il file PSD con livelli smart object.
            void EsempioDiSupportoARotazioneCapovolgimentoDellImmagineSmartObject(string fileName, RotateFlipType rotateFlipType)
            {
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + rotateFlipType + "_" + fileName + ".psd";
                string outputPngPath = outputDir + rotateFlipType + "_" + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.RotateFlip(rotateFlipType);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Questo esempio mostra come ruotare e capovolgere lo smart object layer di Adobe® Photoshop®.
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("gorilla", RotateFlipType.Rotate90FlipNone);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.RotateNoneFlipX);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.RotateNoneFlipY);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.RotateNoneFlipXY);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipNone);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipX);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipY);
            EsempioDiSupportoARotazioneCapovolgimentoDelLivelloSmartObject("r3-embedded-transform2", RotateFlipType.Rotate90FlipXY);

            // Questo esempio mostra come ruotare lo smart object layer di Adobe® Photoshop® di un determinato angolo:
            const string AngleFormat = "+#;-#;+0";
            EsempioDiSupportoARotazioneDelLivelloSmartObject("gorilla", 45, false);
            EsempioDiSupportoARotazioneDelLivelloSmartObject("gorilla", 45, true);
            EsempioDiSupportoARotazioneDelLivelloSmartObject("r3-embedded-transform2", -30, true);
            EsempioDiSupportoARotazioneDelLivelloSmartObject("r3-embedded-transform2", -30, false);
            EsempioDiSupportoARotazioneDelLivelloSmartObject("new_panama-papers-8-trans4-linked", 190, false);
            EsempioDiSupportoARotazioneDelLivelloSmartObject("new_panama-papers-8-trans4-linked", 190, true);

            // Questo esempio mostra come ruotare uno smart object layer nel file PSD di un determinato angolo.
            void EsempioDiSupportoARotazioneDelLivelloSmartObject(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "RotateLast" +  angle.ToString(AngleFormat) + (resizeProportionally ? "ResizeProportionally" : "") + "_";
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + prefix + fileName + ".psd";
                string outputPngPath = outputDir + prefix + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    var smartObjectLayer = (SmartObjectLayer)image.Layers[image.Layers.Length - 1];
                    smartObjectLayer.Rotate(angle, resizeProportionally, Color.Empty);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }

            // Questo esempio mostra come ruotare l'immagine di Adobe® Photoshop® con uno smart object layer di un determinato angolo
            EsempioDiSupportoARotazioneDellImmagineSmartObject("gorilla", 45, false);
            EsempioDiSupportoARotazioneDellImmagineSmartObject("new_panama-papers-8-trans4-linked", -30, false);

            // Questo esempio mostra come ruotare il file PSD con livelli smart object di un determinato angolo.
            void EsempioDiSupportoARotazioneDellImmagineSmartObject(string fileName, float angle, bool resizeProportionally)
            {
                string prefix = "Rotate" +  angle.ToString(AngleFormat) + (resizeProportionally ? "ResizeProportionally" : "") + "_";
                string filePath = dataDir + fileName + ".psd";
                string outputPath = outputDir + prefix + fileName + ".psd";
                string outputPngPath = outputDir + prefix + fileName + ".png";
                using (PsdImage image = (PsdImage)Image.Load(filePath))
                {
                    image.Rotate(angle, resizeProportionally, Color.Empty);
                    image.Save(outputPath, new PsdOptions(image));
                    image.Save(outputPngPath, new PngOptions { ColorType = PngColorType.TruecolorWithAlpha });
                }
            }
{{< /highlight >}}
**PSDNET-711. Il livello di testo viene spostato dopo il salvataggio senza alcuna modifica**
{{< highlight csharp >}}
            string srcFile = "PsdCompressTest3.psd";
            string output = "PsdCompressTest3.psdoutput.psd";

            void AreNotEqual(object expected, object actual)
            {
                if (object.Equals(expected, actual))
                {
                    throw new Exception("I valori sono uguali.");
                }
            }

            using (PsdImage image = (PsdImage)Image.Load(srcFile))
            {
                image.Save(output, new PsdOptions(image));
            }

            using (PsdImage image = (PsdImage)Image.Load(output))
            {
                TextLayer txtLayer = (TextLayer)image.Layers[2];

                AreNotEqual(txtLayer.Left, txtLayer.TransformMatrix[4]);
                AreNotEqual