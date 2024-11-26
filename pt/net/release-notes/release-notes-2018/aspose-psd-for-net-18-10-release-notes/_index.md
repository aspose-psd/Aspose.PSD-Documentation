---
title: Aspose.PSD para .NET 18.10 - Notas da Versão
type: docs
weight: 30
url: /pt/net/aspose-psd-para-net-18-10-notas-da-versao/
---

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-14|Adicionar suporte a modos de mesclagem além de Normal|Recurso|
|PSDNET-69|Adicionar suporte ao efeito de sobreposição de cores|Recurso|
|PSDNET-70|Adicionar suporte ao efeito de sombra|Recurso|
|PSDNET-71|Renderização para exportação do efeito de sobreposição de cores|Recurso|
|PSDNET-72|Renderização para exportação do efeito de sombra|Recurso|
|PSDNET-74|Suporte para adição de Efeitos de Camada em tempo de execução|Recurso|
|PSDNET-73|Otimização de desempenho de carregamento de recursos que contêm tipo de estruturas osType|Erro|
|PSDNET-79|Refatoração e correções de vazamentos de memória em LayerAndMaskInfo|Aprimoramento|

## **Exemplos de Uso:**
**PSDNET-14 Adicionar suporte a modos de mesclagem além de Normal**

{{< highlight java >}}

 var arquivos = new string[]

{

    "Normal",

    "Dissolver",

    "Escurecer",

    "Multiplicar",

    "QueimarCor",

    "QueimaLinear",

    "CorMaisEscura",

    "Clarear",

    "Tela",

    "SuperexposicaoCor",

    "AdicaoLinear",

    "CorClara",

    "Sobrepor",

    "LuzSuave",

    "LuzDura",

    "LuzViva",

    "LuzLinear",

    "Luminosidade",

    "LuzReflexo",

    "Diferenca",

    "Exclusao",

    "Subtracao",

    "Divisao",

    "Matiz",

    "Saturacao",

    "Cor",

    "Luminosidade",

};

foreach (var nomeArquivo in arquivos)

{

    using (var im = LoadFile(nomeArquivo + ".psd"))

    {

        // Exportar para PNG

        var opcoesDeSalvamento = new PngOptions();

        opcoesDeSalvamento.TipoDeCor = PngColorType.TruecolorWithAlpha;

        var caminhoExportacaoPng100 = "ModoMesclagem" + nomeArquivo + "_Teste100.png";

        im.Save(caminhoExportacaoPng100, opcoesDeSalvamento);

        // Definir opacidade 50%

        im.Layers[1].Opacidade = 127;

        var caminhoExportacaoPng50 = "ModoMesclagem" + nomeArquivo + "_Teste50.png";

        im.Save(caminhoExportacaoPng50, opcoesDeSalvamento);

    }

}

{{< /highlight >}}

**PSDNET-69 Adicionar suporte ao efeito de sobreposição de cores**

{{< highlight java >}}

     // Edição do efeito de Sobreposição de Cores

    string nomeArquivoFonte = "SobreposicaoDeCores.psd";

    string caminhoPsdAposAlteracao = "SobreposicaoDeCoresAlterada.psd";

    using (var im = LoadFile(nomeArquivoFonte))

    {

       var sobreposicaoCor = (ColorOverlay)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Vermelho, sobreposicaoCor.Cor);

       Assert.AreEqual(153, sobreposicaoCor.Opacidade);

       sobreposicaoCor.Cor = Cor.Verde;

       sobreposicaoCor.Opacidade = 128;

       im.Save(caminhoPsdAposAlteracao);

    }

{{< /highlight >}}

**PSDNET-70 Adicionar suporte ao efeito de sombra**

{{< highlight java >}}

     // Edição do efeito de Sombra

    string nomeArquivoFonte = "Sombra.psd";

    string caminhoPsdAposAlteracao = "SombraAlterada.psd";

    using (var im = LoadFile(nomeArquivoFonte))

    {

       var efeitoSombra = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Preto, efeitoSombra.Cor);

       Assert.AreEqual(255, efeitoSombra.Opacidade);

       Assert.AreEqual(3, efeitoSombra.Distancia);

       Assert.AreEqual(7, efeitoSombra.Tamanho);

       Assert.AreEqual(true, efeitoSombra.UsarLuzGlobal);

       Assert.AreEqual(90, efeitoSombra.Angulo);

       Assert.AreEqual(0, efeitoSombra.Espalhamento);

       Assert.AreEqual(0, efeitoSombra.Ruido);

       efeitoSombra.Cor = Color.Verde;

       efeitoSombra.Opacidade = 128;

       efeitoSombra.Distancia = 11;

       efeitoSombra.UsarLuzGlobal = false;

       efeitoSombra.Tamanho = 9;

       efeitoSombra.Angulo = 45;

       efeitoSombra.Espalhamento = 3;

       efeitoSombra.Ruido = 50;

       im.Save(caminhoPsdAposAlteracao);

    }

{{< /highlight >}}

**PSDNET-71 Renderização para exportação do efeito de sobreposição de cores**

{{< highlight java >}}

    // Edição do efeito de Sobreposição de Cores

    string nomeArquivoFonte = "SobreposicaoDeCores.psd";

    string caminhoExportacaoPng = "SobreposicaoDeCores.png";

    using (var im = LoadFile(nomeArquivoFonte))

    {

       var sobreposicaoCor = (ColorOverlayEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Vermelho, sobreposicaoCor.Cor);

       Assert.AreEqual(153, sobreposicaoCor.Opacidade);

       // Salvar PNG

       var opcoesDeSalvamento = new PngOptions();

       opcoesDeSalvamento.TipoDeCor = PngColorType.TruecolorWithAlpha;

       im.Save(caminhoExportacaoPng, opcoesDeSalvamento);

    }

{{< /highlight >}}

**PSDNET-72 Renderização para exportação do efeito de sombra**

{{< highlight java >}}

     // Exportação da Sombra

    string nomeArquivoFonte = "Sombra.psd";

    string caminhoExportacaoPng = "Sombra.png";

    using (var im = LoadFile(nomeArquivoFonte))

    {

       var efeitoSombra = (DropShadowEffect)(im.Layers[1].BlendingOptions.Effects[0]);



       Assert.AreEqual(Color.Preto, efeitoSombra.Cor);

       Assert.AreEqual(255, efeitoSombra.Opacidade);

       Assert.AreEqual(3, efeitoSombra.Distancia);

       Assert.AreEqual(7, efeitoSombra.Tamanho);

       Assert.AreEqual(true, efeitoSombra.UsarLuzGlobal);

       Assert.AreEqual(90, efeitoSombra.Angulo);

       Assert.AreEqual(0, efeitoSombra.Espalhamento);

       Assert.AreEqual(0, efeitoSombra.Ruido);

       // Salvar PNG

       var opcoesDeSalvamento = new PngOptions();

       opcoesDeSalvamento.TipoDeCor = PngColorType.TruecolorWithAlpha;

       im.Save(caminhoExportacaoPng, opcoesDeSalvamento);

    }

{{< /highlight >}}

**PSDNET-74 Suporte para adição de Efeitos de Camada em tempo de execução**

{{< highlight java >}}

     // Adicionar efeito de sobreposição de cor da camada em tempo de execução

    string nomeArquivoFonte = "TresCamadasRegularesComEfeitoDeCamada.psd";

    string caminhoPsdExportacao = "TresCamadasRegularesComEfeitoDeCamadaAlterado.psd";

    string caminhoExportacaoPng = "TresCamadasRegularesComEfeitoDeCamadaAlterado.psd";

    var opcoesDeCarregamento = new PsdLoadOptions()

    {

        CarregarRecursosDeEfeitos = true

    };



    var pastaTeste = string.Empty;

    var im = (PsdImage)Image.Load(caminhoTeste, opcoesDeCarregamento) 

    using (im)

    {

        var efeito = im.Layers[1].BlendingOptions.AdicionarSobreposicaoDeCor();

        efeito.Opacidade = 128;

        efeito.Cor = Color.Verde;

        efeito.ModoMesclagem = ModoMesclagem.Normal;

        var efeito = im.Layers[1].BlendingOptions.AdicionarSombra();

        efeito.Cor = Color.Vermelho;

        efeito.Opacidade = 128;

        efeito.ModoMesclagem = ModoMesclagem.Normal;



        // Salvar PSD

        im.Save(caminhoPsdExportacao);



        // Salvar PNG

        var opcoesDeSalvamento = new PngOptions();

        im.Save(caminhoExportacaoPng, opcoesDeSalvamento);

    }

{{< /highlight >}}
