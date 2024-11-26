---
title: Notas de Lançamento do Aspose.PSD for Java 20.6
type: docs
weight: 50
url: /pt/java/aspose-psd-for-java-20-6-release-notes/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para o [Aspose.PSD for Java 20.6](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.6/) {{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-216|Suporte ao LnkEResource (Recurso da Camada de Objeto Inteligente)|Recurso|
|PSDJAVA-219|Suporte ao britResource (Recurso do Ajuste de Brilho/Contraste)|Recurso|
|PSDJAVA-222|Mover a configuração DefaultReplacementFont para a classe ImageOptionsBase|Melhoria|
|PSDJAVA-217|Redimensionamento errado de arquivos PSD se houver uma máscara na camada de ajuste com limites vazios|Erro|
|PSDJAVA-218|Imagem Psd com modo RGB de 16 bits/canal atualiza camadas apenas na visualização|Erro|
|PSDJAVA-220|Alterações em Máscaras de Camada PSD são descartadas ao salvar|Erro|
|PSDJAVA-221|Ordem Incorreta da Camada após adicionar um Grupo de Camadas vazio|Erro|
|PSDJAVA-223|Exceção ao carregar um arquivo PSD específico com o recurso LnkE composto e propriedade adobeStockLicenseState|Erro|
|PSDJAVA-224|Salvar Arquivo AI no Formato Jpeg2000 não funciona|Erro|
|PSDJAVA-225|Grupo de Camadas com Modo de Mesclagem não PassThrough não é Renderizado|Erro|
|PSDJAVA-226|Exceção NullReference ao tentar converter um arquivo Psd específico em imagem|Erro|
|PSDJAVA-227|OverflowException ao tentar abrir um arquivo Psd específico|Erro|

# **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFileSize
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getFullPath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.getRelativePath
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setAdobeStockId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setDate(java.util.Date)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setElementRef(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFileSize(long)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setFullPath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource.setRelativePath(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetLockedState
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getAssetModTime
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getChildDocId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileCreator
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getFileType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalCompId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getOriginalFileName
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getType
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getUniqueId
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.getVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.hasFileOpenDescriptor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.isLibraryLink
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetLockedState(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setAssetModTime(double)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setChildDocId(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileCreator(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileOpenDescriptor(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setFileType(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setLibraryLink(boolean)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalCompId(int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setOriginalFileName(java.lang.String)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource.setUniqueId(java.util.UUID)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getDataSourceCount
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getLength
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getPsdVersion
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.getSignature
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.isEmpty
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource.save(com.aspose.psd.StreamContainer,int)
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.#ctor(com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource[])
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.getKey
- M:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource.get_Item(int)
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFdDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LiFeDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkDataSourceType
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LinkResource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.Lnk2Resource
- T:com.aspose.psd.fileformats.psd.layers.layerresources.linkresources.LnkeResource
## **APIs Removidas:**
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.getDefaultReplacementFont
- M:com.aspose.psd.imageloadoptions.PsdLoadOptions.setDefaultReplacementFont(java.lang.String)
# **Exemplos de Uso:**

**PSDJAVA-216: Suporte ao LnkEResource (Recurso da Camada de Objeto Inteligente)**

{{< highlight java >}}

 // Um exemplo de vinculação de diferentes tipos de ativos (imagens rasterizadas, bibliotecas CC) ao PSD.

// Além disso, a API de LnkeResource é considerada.

// Uma classe que mantém métodos no escopo local

class LocalScopeExtension

{

    void assertIsTrue(boolean condition)

    {

        if (!condition)

        {

            throw new FormatException("O Exemplo de Suporte ao LnkeResource funciona incorretamente.");

        }

    }

    void assertAreEqual(Object actual, Object expected)

    {

        assertIsTrue(actual != null && actual.equals(expected));

    }

    // Este exemplo demonstra como obter e definir propriedades do Recurso LnkE do Photoshop Psd

    // que contém informações sobre um arquivo vinculado externamente.

    void exampleOfLnkEResourceSupport(

            String fileName,

            int length,

            int length2,

            int length3,

            int length4,

            String fullPath,

            String date,

            double assetModTime,

            String childDocId,

            boolean locked,

            String uid,

            String name,

            String originalFileName,

            String fileType,

            long size)

    {

        String outputPath = "out_" + fileName;

        // Carregar um PSD predefinido

        PsdImage image = (PsdImage)Image.load(fileName);

        try

        {

            // Procurar LnkeResource entre os recursos globais

            LnkeResource lnkeResource = null;

            for (LayerResource resource : image.getGlobalLayerResources())

            {

                if (resource instanceof LnkeResource)

                {

                    lnkeResource = (LnkeResource)resource;

                    // Verificar as propriedades do LnkeResource

                    assertAreEqual(lnkeResource.getLength(), length);

                    assertAreEqual(lnkeResource.get_Item(0).getUniqueId(), UUID.fromString(uid));

                    assertAreEqual(lnkeResource.get_Item(0).getFullPath(), fullPath);

                    assertAreEqual(new SimpleDateFormat("MM/dd/yyyy HH:mm:ss").format(lnkeResource.get_Item(0).getDate()), date);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetModTime(), assetModTime);

                    assertAreEqual(lnkeResource.get_Item(0).getAssetLockedState(), locked);

                    assertAreEqual(lnkeResource.get_Item(0).getFileName(), name);

                    assertAreEqual(lnkeResource.get_Item(0).getFileSize(), size);

                    assertAreEqual(lnkeResource.get_Item(0).getChildDocId(), childDocId);

                    assertAreEqual(lnkeResource.get_Item(0).getVersion(), 7);

                    assertAreEqual(lnkeResource.get_Item(0).getFileType().trim(), fileType);

                    assertAreEqual(lnkeResource.get_Item(0).getFileCreator().trim(), "");

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalFileName(), originalFileName);

                    assertAreEqual(lnkeResource.get_Item(0).getCompId(), -1);

                    assertAreEqual(lnkeResource.get_Item(0).getOriginalCompId(), -1);

                    assertIsTrue(lnkeResource.get_Item(0).hasFileOpenDescriptor());

                    assertIsTrue(!lnkeResource.isEmpty());

                    assertIsTrue(lnkeResource.get_Item(0).getType() == LinkDataSourceType.liFE);

                    // Atualizar as propriedades do LnkeResource

                    lnkeResource.get_Item(0).setFullPath("file:///C:/Aspose/net/Aspose.Psd/test/testdata/Images/Psd/SmartObjects/rgb8_2x2.png");

                    assertAreEqual(lnkeResource.getLength(), length2);

                    lnkeResource.get_Item(0).setFileName("rgb8_2x23.png");

                    assertAreEqual(lnkeResource.getLength(), length3);

                    lnkeResource.get_Item(0).setChildDocId(UUID.randomUUID().toString());

                    assertAreEqual(lnkeResource.getLength(), length4);

                    lnkeResource.get_Item(0).setDate(new Date());

                    lnkeResource.get_Item(0).setAssetModTime(Double.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileSize(Long.MAX_VALUE);

                    lnkeResource.get_Item(0).setFileType("test");

                    lnkeResource.get_Item(0).setFileCreator("file");

                    lnkeResource.get_Item(0).setCompId(Integer.MAX_VALUE);

                    break;

                }

            }

            // Certificar-se de que LnkeResource é suportado

            assertIsTrue(lnkeResource != null);

            // Salvar uma cópia do PSD carregado

            image.save(outputPath, new PsdOptions(image));

        }

        finally

        {

            image.dispose();

        }

        // Carregar a cópia salva

        PsdImage image1 = (PsdImage)Image.load(outputPath);

        try

        {

            // Converter PSD para formato de arquivo PNG (com canal alfa para transparência)

            PngOptions pngOptions = new PngOptions();

            pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

            image1.save(Path.changeExtension(outputPath, "png"), pngOptions);

        }

        finally

        {

            image1.dispose();

        }

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE da Psd Photoshop

// que contém informações sobre um arquivo JPEG externamente vinculado.

$.exampleOfLnkEResourceSupport(

        "photooverlay_5_new.psd",

        0x21c,

        0x26c,

        0x274,

        0x27c,

        "file:///C:/Users/cvallejo/Desktop/photo.jpg",

        "05/09/2017 22:24:51",

        0,

        "F062B9DB73E8D124167A4186E54664B0",

        false,

        "02df245c-36a2-11e7-a9d8-fdb2b61f07a7",

        "photo.jpg",

        "photo.jpg",

        "JPEG",

        0x1520d);

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE Psd que

// contém informações sobre um arquivo PNG externamente vinculado.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_linked.psd",

        0x284,

        0x290,

        0x294,

        0x2dc,

        "file:///C:/Aspose/net/Aspose.Psd/test/testdata/Issues/PSDNET-491/rgb8_2x2.png",

        "04/14/2020 14:23:44",

        0,

        "",

        false,

        "5867318f-3174-9f41-abca-22f56a75247e",

        "rgb8_2x2.png",

        "rgb8_2x2.png",

        "png",

        0x53);

// Este exemplo demonstra como obter e definir propriedades do Recurso LnkE da Psd Photoshop

// que contém informações sobre um ativo de bibliotecas CC externas vinculado.

$.exampleOfLnkEResourceSupport(

        "rgb8_2x2_asset_linked.psd",

        0x398,

        0x38c,

        0x388,

        0x3d0,

        "CC Libraries Asset “rgb8_2x2_linked/rgb8_2x2” (O recurso está disponível no Photoshop CC 2015)",

        "01/01/0001 00:00:00",

        1588890915488.0d,

        "",

        false,

        "ec15f0a8-7f13-a640-b928-7d29c6e9859c",

        "rgb8_2x2_linked",

        "rgb8_2x2.png",

        "png",

        0);


{{< /highlight >}}

**PSDJAVA-219: Suporte ao britResource (Recurso do Ajuste de Brilho/Contraste)**

{{< highlight java >}}

 // Este exemplo demonstra como você pode alterar programaticamente a Camada de Ajuste de Brilho/Contraste de Imagens PSD.

// Esta API de Camada de Brilho/Contraste permitirá um controle maior sobre o conteúdo do arquivo PSD,

// mas a edição direta do recurso de camada do Photoshop lhe dará mais controle sobre o conteúdo do arquivo PSD.

String srcPath = "BrightnessContrastPS6.psd";

String dstPath = "BrightnessContrastPS6_output.psd";

// Carregar um documento do Photoshop contendo uma camada de ajuste de brilho/contraste

PsdImage psdImage = (PsdImage)Image.load(srcPath);

try

{

    // Procurar por BritResource

    for (Layer layer : psdImage.getLayers())

    {

        if (layer instanceof BrightnessContrastLayer)

        {

            for (LayerResource layerResource : layer.getResources())

            {

                if (layerResource instanceof BritResource)

                {

                    BritResource resource = (BritResource)layerResource;

                    // Verificar propriedades do recurso

                    if (resource.getBrightness() != -40 ||

                            resource.getContrast() != 10 ||

                            resource.getLabColor() ||

                            resource.getMeanValueForBrightnessAndContrast() != 127)

                    {

                        throw new RuntimeException("BritResource foi lido incorretamente");

                    }

                    // Atualizar propriedades do recurso

                    resource.setBrightness((short)25);

                    resource.setContrast((short)-14);

                    resource.setLabColor(true);

                    resource.setMeanValueForBrightnessAndContrast((short)200);

                    // Salvar umacópia do PSD atualizada

                    psdImage.save(dstPath, new PsdOptions());

                    break;

                }

            }

        }

    }

}

finally

{

    psdImage.dispose();

}

{{< /highlight >}}


**PSDJAVA-217: Redimensionamento de arquivos PSD funciona incorretamente se houver uma máscara na camada de ajuste com limites vazios**

{{< highlight java >}}

 // Um exemplo de redimensionamento de uma imagem que contém uma máscara de camada de ajuste com limites vazios.

// O programa carrega um PSD predefinido apenas para verificar se não há exceções.

final int escala = 2; // coeficiente arbitrário

String[] nomes = {

        "UmaRegularEUmaDeAjusteComVetorELayerMask",

        "CamadaDeNíveisComMáscaraDeCamadaRgb",

        "CamadaDeNíveisComMáscaraDeCamadaCmyk",

};

for (String nome : nomes)

{

    String srcFilePath = nome + ".psd";

    String dstFilePath = "output_" + srcFilePath;

    String dstPngFilePath = "output_" + nome + ".png";

    // Carregar um PSD predefinido contendo uma máscara de camada de ajuste com limites vazios

    PsdLoadOptions opçõesPsd = new PsdLoadOptions();

    opçõesPsd.setLoadEffectsResource(true);

    PsdImage image = (PsdImage)Image.load(srcFilePath, opçõesPsd);

    try

    {

        // Redimensionar a imagem

        image.resize(image.getWidth() * escala, image.getHeight() * escala);

        // Salvar uma cópia do PSD carregado

        image.save(dstFilePath, new PsdOptions());

        // Exportar PSD para o formato de arquivo PNG (com canal alfa para transparência)

        PngOptions opçõesPng = new PngOptions();

        opçõesPng.setColorType(PngColorType.TruecolorWithAlpha);

        image.save(dstPngFilePath, opçõesPng);

    }

    finally

    {

        image.dispose();

    }

}

{{< /highlight >}}


**PSDJAVA-218: A imagem Psd com modo RGB de 16 bits/canal atualiza as camadas apenas na visualização**

{{< highlight java >}}

 // Um exemplo de atualização de camadas regulares para uma imagem RGB de 16 bits. O programa desenha algo

// em cada camada apenas para garantir que toda a camada seja atualizada corretamente.

String sourceFilePath = "in.psd";

String outputFilePath = "output.psd";

 // Carregar um PSD predefinido em modo RGB de 16 bits

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    for (Layer layer : image.getLayers())

    {

        // Desenhar o nome da camada e uma borda interna para a camada regular

        if (!(layer instanceof LayerGroup) && !(layer instanceof AdjustmentLayer) &&

                (layer.getWidth() > 100) && (layer.getHeight() > 100))

        {

            Graphics graphics = new Graphics(layer);

            graphics.drawString(layer.getName(), new Font("Arial", 10),

                    new SolidBrush(Color.getRed()), 15, 45);

            graphics.drawRectangle(new Pen(Color.getRed()), new Rectangle(30, 10, 40, 80));

        }

    }

    // Salvar uma cópia do PSD carregado

    image.save(outputFilePath, new PsdOptions(image));

}

finally

{

    image.dispose();

}

{{< /highlight >}}


**PSDJAVA-220: Alterações em Máscaras de Camada PSD são descartadas ao salvar**

{{< highlight java >}}

 // Uma classe que mantém métodos no escopo local

class LocalScopeExtension

{

    void assertAreEqual(Object actual, Object expected)

    {

        if (!(actual != null && actual.equals(expected)))

        {

            throw new FormatException("O exemplo funciona incorretamente.");

        }

    }

    // Obtém o valor int convertido para bytes de ordem big-endian.

    byte[] getBigEndianBytesInt32(int value)

    {

        byte[] bytes = new byte[4];

        bytes[0] = (byte)((value >> 24) & 0x000000FF);

        bytes[1] = (byte)((value >> 16) & 0x000000FF);

        bytes[2] = (byte)((value >> 8) & 0x000000FF);

        bytes[3] = (byte)value;

        return bytes;

    }

    // Obtém o valor convertido do big endian para Int32.

    int fromBigEndianToInt32(byte[] bytes, int index)

    {

        if (bytes == null)

        {

            throw new ArgumentNullException("bytes");

        }

        if (index < 0 || index + 4 > bytes.length)

        {

            throw new ArgumentOutOfRangeException("index", "O índice está fora do array de bytes.");

        }

        return ((bytes[index] & 0xff) << 24) | ((bytes[index + 1] & 0xff) << 16) |

                ((bytes[index + 2] & 0xff) << 8) | (bytes[index + 3] & 0xff);

    }

    // Obtém uma máscara de raster da camada de uma imagem PSD e a salva em um arquivo

    void saveRasterMask(String maskFilePath, Layer layer)

    {

        LayerMaskDataShort maskData = (LayerMaskDataShort)layer.getLayerMaskData();

        FileStreamContainer container = FileStreamContainer.createFileStream(maskFilePath, false);

        try

        {

            container.write(getBigEndianBytesInt32(maskData.getTop()));

            container.write(getBigEndianBytesInt32(maskData.getLeft()));

            container.write(getBigEndianBytesInt32(maskData.getBottom()));

            container.write(getBigEndianBytesInt32(maskData.getRight()));

            container.writeByte(maskData.getDefaultColor());

            container.writeByte((byte)maskData.getFlags());

            container.write(getBigEndianBytesInt32(maskData.getImageData().length));

            container.write(maskData.getImageData(), 0, maskData.getImageData().length);

        }

        finally

        {

            container.dispose();

        }

    }

    // Adiciona uma máscara de raster do arquivo à camada e salva a imagem no formato PSD

    void addRasterMask(Layer layer, String maskSourcePath)

    {

        LayerMaskDataShort maskData = new LayerMaskDataShort();

        FileStreamContainer container = FileStreamContainer.openFileStream(maskSourcePath);

        try

        {

            byte[] bytes = new byte[22];

            assertAreEqual(container.read(bytes), 22);

            maskData.setTop(fromBigEndianToInt32(bytes, 0));

            maskData.setLeft(fromBigEndianToInt32(bytes, 4));

            maskData.setBottom(fromBigEndianToInt32(bytes, 8));

            maskData.setRight(fromBigEndianToInt32(bytes, 12));

            maskData.setDefaultColor(bytes[16]);

            maskData.setFlags(bytes[17]);

            int imageDataLength = fromBigEndianToInt32(bytes, 18);

            byte[] data = new byte[imageDataLength];

            assertAreEqual(maskData.getMaskRectangle().getWidth() *

                    maskData.getMaskRectangle().getHeight(), imageDataLength);

            assertAreEqual(container.read(data), imageDataLength);

            maskData.setImageData(data);

        }

        finally

        {

            container.dispose();

        }

        // Apenas adicionar LayerMaskData não é suficiente para a correta salvaguarda por causa de canais não atualizados;

        // layer.setLayerMaskData(mask); // Isso não adiciona o canal de máscara

        // Adicionar (ou atualizar) a máscara

        layer.addLayerMask(maskData); // Mas isso adiciona/atualiza a máscara e os canais!

    }

}

LocalScopeExtension $ = new LocalScopeExtension();

// Este exemplo mostra como obter, atualizar, remover e adicionar máscaras de camada de raster no arquivo Adobe® Photoshop® programaticamente.

PngOptions pngOptions = new PngOptions();

pngOptions.setColorType(PngColorType.TruecolorWithAlpha);

String sourceFilePath = "QuatroComMáscaras.psd";

PsdImage image = (PsdImage)Image.load(sourceFilePath);

try

{

    Layer layer = image.getLayers()[2];

    // Obter uma máscara de raster da camada e salvar em um arquivo

    $.saveRasterMask("QuatroComMáscaras2.msk", layer);

    // Alterar a máscara da camada (inverter) e salvar a imagem

    LayerMaskData mask = layer.getLayerMaskData();

    byte[] maskData = mask.getImageData();

    for (int i = 0; i < maskData.length; i++)

    {

        maskData[i] = (byte)~maskData[i];

    }

    // Apenas alterar LayerMaskData é suficiente para afetar a renderização

    image.save("QuatroComMáscarasAtualizado2.png", pngOptions);

    // Mas apenas alterar LayerMaskData não é suficiente para a salvaguarda correta porque os canais não são atualizados;

    layer.setLayerMaskData(mask); // Isso também não funciona

    layer.addLayerMask(mask); // Mas isso atualiza tanto a máscara quanto os canais!

    image.save("QuatroComMáscarasAtualizado2.psd");

    // Remover uma máscara de raster da camada e salvar a imagem

    layer.setLayerMaskData(null); // Apenas remover LayerMaskData é suficiente para afetar a renderização mas não para salvar no formato PSD

    image.save("QuatroComMáscarasRemovido2.png", pngOptions);

    layer.addLayerMask(null); // Mas isso remove tanto a máscara quanto o canal da máscara!

    image.save("QuatroComMáscarasRemovido2.psd");

    // Adicionar uma máscara de raster do arquivo à camada e salvar a imagem

    $.addRasterMask(layer, "raster.msk");

    image.save("QuatroComMáscarasAdicionado2.png", pngOptions);

    image.save("QuatroComMáscarasAdicionado2.psd");

}

finally

{

    image.dispose();

}

{{< /highlight >}}