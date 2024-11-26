---
title: Cabeçalho do Arquivo PSD e PSB
type: docs
weight: 40
url: /pt/net/psd-and-psb-file-header/
---

## **Descrição**
O cabeçalho do arquivo do Adobe Photoshop contém informações sobre a versão do arquivo (1 para PSD e 2 para PSB), contagem de canais, modo de cor e profundidade de bits.

Você pode aprender sobre as combinações suportadas por Aspose.PSD de Modo de Cor e Profundidade de Bits no artigo relacionado.


O cabeçalho do arquivo contém as propriedades básicas da imagem.

|**Comprimento**|**Descrição**|
| :- | :- |
|4|Assinatura: sempre igual a *"8BPS"*|
|2|[Versão PSD](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd/fileformatversion): sempre igual a 1 para arquivos PSD e 2 para arquivos PSB. Aspose.PSD pode detectar a versão do Formato do Arquivo e lê-la corretamente.|
|6|Reservado: deve ser zero.|
|2|O número de canais na imagem, incluindo quaisquer canais alfa. A faixa suportada é de 1 a 56.|
|4|A altura da imagem em pixels. A faixa suportada é de 1 a 30.000. O arquivo PSB suporta uma altura de até 300.000 pixels. Arquivos PSB também são suportados por Aspose.PSD|
|4|A largura da imagem em pixels. A faixa suportada é de 1 a 30.000. O arquivo PSB suporta uma largura de até 300.000 pixels. O processamento em lote de arquivos grandes PSD/PSB também é suportado por Aspose.PSD|
|2|Profundidade: o número de bits por canal. Os valores suportados são 1, 8, 16 e 32. Mas nem todo Modo de Cor funciona com toda profundidade.|
|2|O [modo de cor PSD](https://reference.aspose.com/psd/java/com.aspose.psd.fileformats.psd/ColorModes) do arquivo. Os valores suportados são: Bitmap = 0; Tons de Cinza = 1; Indexado = 2; RGB = 3; CMYK = 4; Multicanal = 7; Duotone = 8; Lab = 9.|
Você pode verificar a nossa [Referência de API PSD](https://reference.aspose.com/psd) para isso.
