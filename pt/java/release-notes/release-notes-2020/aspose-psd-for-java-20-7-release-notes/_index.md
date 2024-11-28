---
title: Notas da Versão Aspose.PSD para Java 20.7
type: docs
weight: 50
url: /pt/java/aspose-psd-for-java-20-7-release-notes/
---

{{% alert color="primary" %}} Esta página contém as notas de lançamento para o [Aspose.PSD para Java 20.7](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.7/) {{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-231|Suporte para adição de Efeito de Traçado em tempo de execução|Recurso|
|PSDJAVA-249|Suporte para Recursos lnk2 / lnk3 (Recursos de Camada de Objeto Inteligente)|Recurso|
|PSDJAVA-247|Alteração da Mensagem de Exceção ao tentar abrir formatos não suportados como imagem|Melhoria|
|PSDJAVA-235|Se salvarmos um arquivo PSD após a criação de novo Grupo de Camada, obtemos um aviso do Photoshop na abertura do arquivo.|Erro|
|PSDJAVA-236|Falha ao salvar a Máscara de Camada|Erro|
|PSDJAVA-237|Máscara de Recorte não se aplica à pasta|Erro|
|PSDJAVA-238|Não é possível abrir arquivo com Aspose.PSD para Java|Erro|
|PSDJAVA-239|Exceção ao salvar imagem ao converter PSD para PDF|Erro|
|PSDJAVA-240|Operação de Recorte torna o Caminho de Recorte inválido na imagem PSD|Erro|
|PSDJAVA-241|Exceção NullReference ao tentar salvar um arquivo PSD específico com o Efeito de Sombra|Erro|
|PSDJAVA-243|Aspose.PSD retorna true em Image.CanLoad(pdfStream)|Erro|
|PSDJAVA-244|Camadas falharam ao renderizar em PNG gerado|Erro|
|PSDJAVA-245|Exceção ao acessar TextData|Erro|
|PSDJAVA-246|ImageSaveException ao salvar o PSD|Erro|

# **Alterações na API pública**
# **APIs Adicionadas:**
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Center
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Inside
- F:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition.Outside
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.TypeToolKey
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.layers.layereffects.BlendingOptions.addStroke(int)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getOverprint
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getPosition
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.getSize
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setOverprint(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setPosition(short)
- M:com.aspose.psd.fileformats.psd.layers.layereffects.StrokeEffect.setSize(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.getData
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource.setData(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.get_Item(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getPaths
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isDisabled
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isInverted
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.isNotLinked
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData.setVersion(int)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.#ctor(byte[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getDataSize
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getMinimalVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getPaths
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.getVersion
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isDisabled
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isInverted
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.isNotLinked
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.saveData(com.aspose.psd.StreamContainer)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setDisabled(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setInverted(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setNotLinked(boolean)
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setPaths(com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathRecord[])
- M:com.aspose.psd.fileformats.psd.resources.WorkingPathResource.setVersion(int)
- T:com.aspose.psd.fileformats.psd.layers.layereffects.StrokePosition
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk3Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.IVectorPathData
- T:com.aspose.psd.fileformats.psd.layers.layerresources.vectorpaths.VectorPathData
- T:com.aspose.psd.fileformats.psd.resources.WorkingPathResource
## **APIs Removidas:**
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.DescriptorVersion
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.UnexpectedLinkResourceTypeValue
- F:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.ZeroChar
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureLayer(float,float,float)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
# **Exemplos de Uso:**

**PSDJAVA-231. Suporte à adição de Efeito de Traçado em tempo de execução**
{{< highlight java >}}
// Este exemplo mostra como adicionar um efeito de traçado (borda) a camadas existentes de um arquivo PSD em Java.
// Existem três tipos de traçado: cor, gradiente e padrão. Cada tipo tem
// três formas (posições) nas quais o traçado é renderizado: dentro, no centro e fora.
// Este exemplo demonstra o uso de todos esses casos.

String srcPsdPath = "StrokeEffectsSource.psd";
String dstPngPath = "output.png";

PsdLoadOptions psdLoadOptions = new PsdLoadOptions();
psdLoadOptions.setLoadEffectsResource(true);
PsdImage psdImage = (PsdImage)Image.load(srcPsdPath, psdLoadOptions);
try
{
    StrokeEffect strokeEffect;
    IColorFillSettings colorFillSettings;
    IGradientFillSettings gradientFillSettings;
    IPatternFillSettings patternFillSettings;

    // 1. Adiciona preenchimento de cor, na posição Interna
    strokeEffect = psdImage.getLayers()[1].getBlendingOptions().addStroke(FillType.Color);
    strokeEffect.setSize(7);
    strokeEffect.setPosition(StrokePosition.Inside);
    colorFillSettings = (IColorFillSettings)strokeEffect.getFillSettings();
    colorFillSettings.setColor(Color.getGreen());

    // ...
{{< /highlight >}}**PSDJAVA-249. Suporte a Recursos lnk2 / lnk3 (Recursos de Camada de Objeto Inteligente)**
{{< highlight java >}}
// Este exemplo demonstra como trabalhar com recursos de objetos inteligentes (basicamente Lnk2Resource).
// O programa carrega vários documentos do Photoshop e exporta seus objetos inteligentes para
// formatos de arquivo de rasterização. Além disso, o código demonstra o uso de métodos públicos de Lnk2Resource.

class LocalScopeExtension
{
    void assertAreEqual(Object expected, Object actual)
    {
        if (!actual.equals(expected))
        {
            throw new FormatException(String.format("O valor atual %s não é igual ao esperado %s.", actual, expected));
        }
    }

    // Salva os dados de um objeto inteligente em um arquivo PSD
    void saveSmartObjectData(String filePath, byte[] data)
    {
        FileStreamContainer container = FileStreamContainer.createFileStream(filePath, false);
        try
        {
            container.write(data);
        }
        finally
        {
            container.dispose();
        }
    }

    // Carrega os novos dados para um objeto inteligente de um arquivo
    byte[] loadNewData(String filePath)
    {
        FileStreamContainer container = FileStreamContainer.openFileStream(filePath);
        try
        {
            return container.toBytes();
        }
        finally
        {
            container.dispose();
        }
    }

    // Obtém e define propriedades do Recurso Lnk2 / Lnk3 do PSD e suas fontes de dados LiFD na imagem PSD
    void exampleOfLnk2ResourceSupport(
            String fileName,
            int dataSourceCount,
            int length,
            int newLength,
            Object[] dataSourceExpectedValues)
    {
        String srcPsdPath = fileName;
        String dstPsdPath = "out_" + fileName;

        PsdImage image = (PsdImage)Image.load(srcPsdPath);
        try
        {
            // Procura por Lnk2Resource
            Lnk2Resource lnk2Resource = null;
            for (LayerResource resource : image.getGlobalLayerResources())
            {
                if (resource instanceof Lnk2Resource)
                {
                    lnk2Resource = (Lnk2Resource)resource;

                    // Verifique as propriedades do Lnk2Resource
                    assertAreEqual(lnk2Resource.getDataSourceCount(), dataSourceCount);
                    assertAreEqual(lnk2Resource.getLength(), length);
                    assertAreEqual(lnk2Resource.isEmpty(), false);

                    for (int i = 0; i < lnk2Resource.getDataSourceCount(); i++)
                    {
                        // Verifique e altere as propriedades de LiFdDataSource
                        LiFdDataSource lifdSource = lnk2Resource.get_Item(i);
                        Object[] expected = (Object[])dataSourceExpectedValues[i];
                        assertAreEqual(LinkDataSourceType.liFD, lifdSource.getType());
                        assertAreEqual(expected[0], lifdSource.getUniqueId().toString());
                        assertAreEqual(expected[1], lifdSource.getOriginalFileName());
                        assertAreEqual(expected[2], lifdSource.getFileType().trim());
                        assertAreEqual(expected[3], lifdSource.getFileCreator().trim());
                        assertAreEqual(expected[4], lifdSource.getData().length);
                        assertAreEqual(expected[5], lifdSource.getAssetModTime());
                        assertAreEqual(expected[6], lifdSource.getChildDocId());
                        assertAreEqual(expected[7], lifdSource.getVersion());
                        assertAreEqual(expected[8], lifdSource.hasFileOpenDescriptor());
                        assertAreEqual(expected[9], lifdSource.getLength());

                        if (lifdSource.hasFileOpenDescriptor())
                        {
                            assertAreEqual(-1, lifdSource.getCompId());
                            assertAreEqual(-1, lifdSource.getOriginalCompId());
                            lifdSource.setCompId(Integer.MAX_VALUE);
                        }

                        saveSmartObjectData(
                                fileName + "_" + lifdSource.getOriginalFileName(),
                                lifdSource.getData());
                        lifdSource.setData(loadNewData("new_" + lifdSource.getOriginalFileName()));
                        assertAreEqual(expected[10], lifdSource.getLength());

                        lifdSource.setChildDocId(UUID.randomUUID().toString());
                        lifdSource.setAssetModTime(Double.MAX_VALUE);
                        lifdSource.setFileType("test");
                        lifdSource.setFileCreator("me");
                    }

                    assertAreEqual(newLength, lnk2Resource.getLength());
                    break;
                }
            }

            // Verifique se o Lnk2Resource foi encontrado
            assertAreEqual(true, lnk2Resource != null);

            // Faça uma cópia do PSD carregado
            if (image.getBitsPerChannel() < 32) // 32 bits por canal não são suportados ainda
            {
                image.save(dstPsdPath, new PsdOptions(image));
            }
        }
        finally
        {
            image.dispose();
        }
    }
}
LocalScopeExtension $ = new LocalScopeExtension();


Object[] Lnk2ResourceSupportCases = new Object[]
        {
                new Object[]
                        {
                                "00af34a0-a90b-674d-a821-73ee508c5479",
                                "rgb8_2x2.png",
                                "png",
                                "",
                                0x53,
                                0d,
                                "",
                                7,
                                true,
                                0x124L,
                                0x74cL
                        }
        };

// Este exemplo demonstra como obter e definir propriedades do Recurso Lnk2 do PSD e suas fontes de dados LiFD para 8 bits por canal.
$.exampleOfLnk2ResourceSupport("rgb8_2x2_embedded_png.psd", 1, 0x12C, 0x0000079c, Lnk2ResourceSupportCases);
{{< /highlight >}}