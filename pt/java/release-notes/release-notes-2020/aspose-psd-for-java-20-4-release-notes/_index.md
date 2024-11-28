---
title: Aspose.PSD para Java 20.4 - Notas da Versão
type: docs
weight: 30
url: /pt/java/aspose-psd-for-java-20-4-release-notes/
---

{{% alert color="primary" %}} Esta página contém notas de lançamento para [Aspose.PSD para Java 20.4](https://downloads.aspose.com/psd/java/new-releases/aspose.psd-for-java-20.4/) {{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDJAVA-156|Suporte do recurso 'Dados de Origem Vetorial'|Recurso|
|PSDJAVA-171|Suporte ao lclrResource (Configuração de cor da planilha)|Recurso|
|PSDJAVA-157|Suporte às propriedades dos dados do LengthRecord. (Operações de caminho (operações booleanas), índice da forma na camada, contagem dos registros de nó do bezier)|Recurso|
|PSDJAVA-158|Suporte à Cor de Fundo do Recurso de Seção de Imagem #1010|Recurso|
|PSDJAVA-161|Adição de Camadas de Preenchimento em tempo de execução|Recurso|
|PSDJAVA-168|Suporte às Informações de Borda do Recurso de Seção de Imagem #1009|Recurso|
|PSDJAVA-169|Suporte a Camadas em Arquivos de Formato AI|Recurso|
|PSDJAVA-163|Suporte à Leitura e Edição do Efeito de Sobreposição Gradiente de Camada|Recurso|
|PSDJAVA-164|Renderização do Efeito de Sobreposição Gradiente de Camada|Recurso|
|PSDJAVA-149|Erro ao obter a propriedade textData.items da camada de texto no Aspose.PSD para Java|Erro|
|PSDJAVA-166|Correção ao salvar imagem PSD com ColorMode em Escala de Cinza e 16 bits por canal para formato PSD em escala de cinza|Erro|
|PSDJAVA-167|Correção ao salvar imagem PSD com ColorMode em Escala de Cinza e 16 bits por canal para formato PNG|Erro|
|PSDJAVA-159|As alterações na propriedade GradientOverlayEffect.BlendMode não são exibidas no Photoshop|Erro|

# **Mudanças na API Pública**
## **APIs Adicionadas:**
- M:com.aspose.psd.fileformats.psd.PsdImage.addBlackWhiteAdjustmentLayer
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float)
- M:com.aspose.psd.fileformats.psd.PsdImage.addExposureAdjustmentLayer(float,float)
- T:com.aspose.psd.fileformats.psd.PsdVersion
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psb
- F:com.aspose.psd.fileformats.psd.PsdVersion.Psd
- F:com.aspose.psd.fileformats.psd.layers.BlendMode.Absent
- M:com.aspose.psd.fileformats.psd.layers.ChannelInformation.#ctor(short,byte[],byte[])
- M:com.aspose.psd.fileformats.psd.layers