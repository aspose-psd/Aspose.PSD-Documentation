---
title: Notas de Lançamento do Aspose.PSD para .NET 22.7
type: docs
weight: 60
url: /pt/net/aspose-psd-for-net-22-7-release-notes/
---

{{% alert color="primary" %}}

Esta página contém notas de lançamento para [Aspose.PSD for .NET 22.7](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}}

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-482|Suporte ao recurso da Seção de Imagem #4000-4999 do recurso Plug-In(s)|Recurso|
|PSDNET-875|Ocorre uma exceção não tratada do tipo "System.OutOfMemoryException" no Aspose.PSD.dll|Erro|
|PSDNET-1050|Após exportar o arquivo PSD, o resultado é muito maior do que o arquivo de origem|Erro|
|PSDNET-1083|Análise incorreta dos dados para XmpResource|Erro|
|PSDNET-1205|Após a exportação, o tamanho dos arquivos PSD com subpastas aumentou|Erro|


## **Alterações na API Pública**
# **APIs Adicionadas:**
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Key
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Length
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.Items
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.SaveData(Aspose.PSD.StreamContainer)
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.AnimatedDataSectionStructure.StructureKey
- T:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.DataSize
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.MinimalVersion
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.KeyName
- P:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.AnimatedDataSection
- M:Aspose.PSD.FileFormats.Psd.Resources.AnimatedDataSectionResource.SaveData(Aspose.PSD.StreamContainer)


# **APIs Removidas:**
- Nenhuma


## **Exemplos de Uso:**

**PSDNET-482. Suporte ao recurso da Seção de Imagem #4000-4999 Plug-In(s)**

{{< highlight csharp >}}
// O código a seguir demonstra como definir/atualizar o tempo de atraso no quadro de linha do tempo da animação de dados.
string arquivoOrigem = "3_animated.psd";
string psdSaida = "output_3_animated.psd";

T FindStructure<T>(IEnumerable<OSTypeStructure> estruturas, string nomeChave) where T : OSTypeStructure
{
    foreach (var estrutura in estruturas)
    {
        if (estrutura.KeyName.ClassName == nomeChave)
        {
            return estrutura as T;
        }
    }

    return null;
}

OSTypeStructure[] AddOrReplaceStructure(IEnumerable<OSTypeStructure> estruturas, OSTypeStructure novaEstrutura)
{
    List<OSTypeStructure> listaDeEstruturas = new List<OSTypeStructure>(estruturas);

    for (int i = 0; i < listaDeEstruturas.Count; i++)
    {
        OSTypeStructure estrutura = listaDeEstruturas[i];
        if (estrutura.KeyName.ClassName == novaEstrutura.KeyName.ClassName)
        {
            listaDeEstruturas.RemoveAt(i);
            break;
        }
    }

    listaDeEstruturas.Add(novaEstrutura);

    return listaDeEstruturas.ToArray();
}

using (PsdImage imagem = (PsdImage)Image.Load(arquivoOrigem))
{
    foreach (var recursoDeImagem in imagem.ImageResources)
    {
        if (recursoDeImagem is AnimatedDataSectionResource)
        {
            var dadosAnimados =
            (AnimatedDataSectionStructure) (recursoDeImagem as AnimatedDataSectionResource).AnimatedDataSection;
            var listaDeQuadros = FindStructure<ListStructure>(dadosAnimados.Items, "FrIn");

            var quadro1 = (DescriptorStructure)listaDeQuadros.Types[1];

            // Cria o registro de atraso de quadro com valor de 100 centésimos que equivale a 1 segundo.
            var atrasoQuadro = new IntegerStructure(new ClassID("FrDl"));
            atrasoQuadro.Value = 100; // define o tempo em centésimos.

            quadro1.Structures = AddOrReplaceStructure(quadro1.Structures, atrasoQuadro);

            break;
        }
    }

    imagem.Save(psdSaida);
}
{{< /highlight >}}

**PSDNET-875. Ocorre uma exceção não tratada do tipo "System.OutOfMemoryException" no Aspose.PSD.dll**

{{< highlight csharp >}}
string arquivoSrc = "001-.psd";
string caminhoParaJpg = "T_0003.jpg";
string caminhoParaSaida = "output_newPsd.psd";

using (var img = (PsdImage)Image.Load(arquivoSrc))
{
    using (FileStream fs = new FileStream(caminhoParaJpg, FileMode.Open))
    {
        var novaCamada = new Aspose.PSD.FileFormats.Psd.Layers.Layer(fs);
        novaCamada.DisplayName = "NovaCamada";

        img.AddLayer(novaCamada);

        img.Save(caminhoParaSaida, true);   
    }
}
{{< /highlight >}}

**PSDNET-1050. Após exportar o arquivo PSD, o resultado é muito maior do que o arquivo de origem**

{{< highlight csharp >}}
string src = "ShimadzuLetterhead100.psd";
string output = "output.psd";
using (var img = (PsdImage)Image.Load(src))
{
    img.Save(output);
}

double tamSaidaMb = new FileInfo(output).Length / 1024d / 1024d;
if (tamSaidaMb > 6)
{
    throw new Exception("O arquivo de saída é maior do que deveria ser.");
}
{{< /highlight >}}

**PSDNET-1083. Análise incorreta dos dados para XmpResource**

{{< highlight csharp >}}
string caminhoImagemPsdInput = @"input.psd";
string caminhoImagemPsdSalva = @"saved.psd";

bool originalContem = false;
bool salvaContem = false;

// Encontrar subchave XMP no arquivo de entrada
using (PsdImage img = (PsdImage)Image.Load(caminhoImagemPsdInput))
{
    foreach (var pacote in img.XmpData.Packages)
    {
        foreach (var pac in pacote)
        {
            if (pac.Value is XmpArray)
            {
                XmpArray arrayXmp = (XmpArray)pac.Value;

                string valorXml = arrayXmp.GetXmlValue();

                if (valorXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    originalContem = true;
                    break;
                }
            }
        }

        if (originalContem)
        {
            break;
        }
    }
    img.Save(caminhoImagemPsdSalva);
}

// Encontrar subchave XMP no arquivo salvo
using (PsdImage img = (PsdImage)Image.Load(caminhoImagemPsdSalva))
{
    foreach (var pacote in img.XmpData.Packages)
    {
        foreach (var pac in pacote)
        {
            if (pac.Value is XmpArray)
            {
                XmpArray arrayXmp = (XmpArray)pac.Value;

                string valorXml = arrayXmp.GetXmlValue();

                if (valorXml.Contains("<photoshop:LayerName>test1</photoshop:LayerName>"))
                {
                    salvaContem = true;
                    break;
                }
            }
        }

        if (salvaContem)
        {
            break;
        }
    }
    img.Save(caminhoImagemPsdSalva);
}

if (originalContem && salvaContem)
{
    // Tudo certo!
}
else
{
    throw new Exception("Isso não funciona");
}
{{< /highlight >}}

**PSDNET-1205. Após exportar, o tamanho dos arquivos PSD com subpastas aumentou**

{{< highlight csharp >}}
string[] arquivosFonte = new string[] { "1lvlFoldersTest.psd", "5lvlFoldersTest.psd"};

foreach (var nomeArquivo in arquivosFonte)
{
    string caminhoArquivoFonte = nomeArquivo;
    string caminhoArquivoSaida = "output_" + nomeArquivo;

    using (PsdImage imagem = (PsdImage)Image.Load(caminhoArquivoFonte))
    {
        imagem.Save(caminhoArquivoSaida);
    }

    double tamSaidaMb = new FileInfo(caminhoArquivoSaida).Length / 1024d / 1024d;
    if (tamSaidaMb > 1.9)
    {
        throw new Exception("O arquivo de saída é maior do que deveria ser.");
    }
}
{{< /highlight >}}
