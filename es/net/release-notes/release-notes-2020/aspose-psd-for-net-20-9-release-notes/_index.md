---
title: Notas de la versión de Aspose.PSD para .NET 20.9
type: docs
weight: 40
url: /es/net/notas-de-version-aspose-psd-para-net-20-9/
---

{{% alert color="primary" %}}

Esta página contiene las notas de la versión de [Aspose.PSD para .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Clave**|**Resumen**|**Categoría**|
| :- | :- | :- |
|PSDNET-408|Soporte de SoLEResource (recurso externo de capa de objeto inteligente)|Función|
|PSDNET-614|Soporte de Objetos inteligentes vinculados|Función|
|PSDNET-615|Soporte de Objetos inteligentes incrustados|Función|
|PSDNET-690|Actualizar texto en el archivo PSD dado y guardar los cambios afecta algunas capas y muchos parámetros de texto|Error|
|PSDNET-696|FillLayer no se actualiza después de la creación y no se puede renderizar correctamente|Error|
|PSDNET-712|Regresión: Aspose.PSD 20.8.0 no puede abrir archivo|Error|
|PSDNET-714|En un archivo PSD específico, cambiar el tamaño de TextLayer rompe el valor de la ubicación|Error|

## **Cambios en la API pública**
# **APIs añadidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AddTextRecord(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AutoKerning
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.StandardLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.DiscretionaryLigatures
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ContextualAlternates
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LanguageIndex
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.VerticalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.HorizontalScale
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Fractions
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Metric
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Optical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
...

{{< /highlight >}}

```csharp
...
...
``````csharp
...
...
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.ResolutionUnit
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Width
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Height
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.FrameStepNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.FrameStepDenominator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DurationNumerator
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.DurationDenominator
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SmartObjectResource.Save(Aspose.PSD.StreamContainer,System.Int32)

## **Ejemplos de uso:**
**PSDNET-408. Soporte de SoLEResource (Recurso externo de capa de objeto inteligente)**
{{< highlight csharp >}}
            void AssertIsTrue(bool condition)
            {
                if (!condition)
                {
                    throw new FormatException(string.Format("Se esperaba verdadero"));
                }
            }

            void AssertAreEqual(object actual, object expected)
            {
                var areEqual = object.Equals(actual, expected);
                if (!areEqual && actual is Array && expected is Array)
                {
                    var actualArray = (Array)actual;
                    var expectedArray = (Array)actual;
                    if (actualArray.Length == expectedArray.Length)
                    {
                        for (int i = 0; i < actualArray.Length; i++)
                        {
                            if (!object.Equals(actualArray.GetValue(i), expectedArray.GetValue(i)))
                            {
                                break;
                            }
                        }

                        areEqual = true;
                    }
                }

                if (!areEqual)
                {
                    throw new FormatException(
                        string.Format("El valor actual {0} no es igual al esperado {1}.", actual, expected));
                }
            }

            void CheckSmartObjectResourceValues(object[] expectedValue, SmartObjectResource resource)
            {
                AssertAreEqual(expectedValue[0], resource.IsCustom);
                AssertAreEqual(expectedValue[2], resource.PageNumber);
                AssertAreEqual(expectedValue[3], resource.TotalPages);
                AssertAreEqual(expectedValue[4], resource.AntiAliasPolicy);
                AssertAreEqual(expectedValue[5], resource.PlacedLayerType);
                AssertAreEqual(8, resource.TransformMatrix.Length);
                AssertAreEqual((double[])expectedValue[6], resource.TransformMatrix);
                AssertAreEqual(expectedValue[7], resource.Value);
                AssertAreEqual(expectedValue[8], resource.Perspective);
                AssertAreEqual(expectedValue[9], resource.PerspectiveOther);
                AssertAreEqual(expectedValue[10], resource.Top);
                AssertAreEqual(expectedValue[11], resource.Left);
                AssertAreEqual(expectedValue[12], resource.Bottom);
                AssertAreEqual(expectedValue[13], resource.Right);
                AssertAreEqual(expectedValue[14], resource.UOrder);
                AssertAreEqual(expectedValue[15], resource.VOrder);

                AssertAreEqual(expectedValue[16], resource.Crop);
                AssertAreEqual(expectedValue[17], resource.FrameStepNumerator);
                AssertAreEqual(expectedValue[18], resource.FrameStepDenominator);
                AssertAreEqual(expectedValue[19], resource.DurationNumerator);
                AssertAreEqual(expectedValue[20], resource.DurationDenominator);
                AssertAreEqual(expectedValue[21], resource.FrameCount);
                AssertAreEqual(expectedValue[22], resource.Width);
                AssertAreEqual(expectedValue[23], resource.Height);
                AssertAreEqual(expectedValue[24], resource.Resolution);
                AssertAreEqual(expectedValue[25], resource.ResolutionUnit);
                AssertAreEqual(expectedValue[26], resource.Comp);
                AssertAreEqual(expectedValue[27], resource.CompId);
                AssertAreEqual(expectedValue[28], resource.OriginalCompId);
                AssertAreEqual(expectedValue[29], resource.PlacedId.ToString());
                AssertAreEqual(expectedValue[30], resource.NonAffineTransformMatrix);
                if (resource.IsCustom)
                {
                    AssertAreEqual(expectedValue[31], resource.HorizontalMeshPointUnit);
                    AssertAreEqual((double[])expectedValue[32], resource.HorizontalMeshPoints);
                    AssertAreEqual(expectedValue[33], resource.VerticalMeshPointUnit);
                    AssertAreEqual((double[])expectedValue[34], resource.VerticalMeshPoints);
                }
            }

            void SetNewSmartValues(SmartObjectResource resource, object[] newValues)
            {
                // This values we do not change in resource
                newValues[0] = resource.IsCustom;
                newValues[1] = resource.UniqueId.ToString();
                newValues[5] = resource.PlacedLayerType;
                newValues[14] = resource.UOrder;
                newValues[15] = resource.VOrder;
                newValues[28] = resource.OriginalCompId;

                // This values should be changed in the PlLdResource (with the specified UniqueId) as well
                // and some of them must be in accord with the underlining smart object in the LinkDataSource
                resource.PageNumber = (int)newValues[2]; // 2;
                resource.TotalPages = (int)newValues[3]; // 3;
                resource.AntiAliasPolicy = (int)newValues[4]; // 0;
                resource.TransformMatrix = (double[])newValues[6];
                resource.Value = (double)newValues[7]; // 1.23456789;
                resource.Perspective = (double)newValues[8]; // 0.123456789;
                resource.PerspectiveOther = (double)newValues[9]; // 0.987654321;
                resource.Top = (double)newValues[10]; // -126;
                resource.Left = (double)newValues[11]; // -215;
                resource.Bottom = (double)newValues[12]; // 248;
                resource.Right = (double)newValues[13]; // 145;
                resource.Crop = (int)newValues[16]; // 5;
                resource.FrameStepNumerator = (int)newValues[17]; // 1;
                resource.FrameStepDenominator = (int)newValues[18]; // 601;
                resource.DurationNumerator = (int)newValues[19]; // 2;
                resource.DurationDenominator = (int)newValues[20]; // 602;
                resource.FrameCount = (int)newValues[21]; // 11;
                resource.Width = (double)newValues[22]; // 541;
                resource.Height = (double)newValues[23]; // 249;
                resource.Resolution = (double)newValues[24]; // 144;
                resource.ResolutionUnit = (UnitTypes)newValues[25];
                resource.Comp = (int)newValues[26]; // 21;
                resource.CompId = (int)newValues[27]; // 22;
                resource.NonAffineTransformMatrix = (double[])newValues[30];

                // This unique Id should be changed in references if any
                resource.PlacedId = new Guid((string)newValues[29]);  // "12345678-9abc-def0-9876-54321fecba98");
                if (resource.IsCustom)
                {
                    resource.HorizontalMeshPointUnit = (UnitTypes)newValues[31];
...
...
```