---
title: Lista dos Recursos de Imagens Globais suportados pela Aspose.PSD
type: docs
weight: 30
url: /pt/list-of-the-supported-psd-global-image-resources/
---

## **Aspose.PSD suporta a edição de baixo nível dos Recursos de Imagens.**
Lista dos Recursos de Imagens totalmente suportados, que você pode encontrar na [Referência da API Aspose.PSD .Net](https://reference.aspose.com/psd/net)

De acordo com a especificação do formato Adobe® Photoshop®: Os recursos de imagem usam vários números de ID padrão, conforme mostrado nos IDs dos Recursos de Imagem. Nem todos os formatos de arquivo usam todos os IDs. Algumas informações podem estar armazenadas em outras seções do arquivo.

Para aqueles IDs de recursos que foram adicionados desde o Photoshop 3.0, a entrada indica a versão em que foram introduzidos, por exemplo, (*Photoshop 6.0).*

ID de Recurso de Imagem.

|**ID**|**Descrição**|
| :- | :- |
|**Decimal**||
|1000|*(Obsoleto - Somente Photoshop 2.0*) Número de canais, linhas, colunas, profundidade e modo|
|1001|Registro de informações de impressão do gerenciador de impressão do Macintosh|
|1002|Informações sobre o formato da página do Macintosh. Não mais lido pelo Photoshop. *(Obsoleto)*|
|1003|*(Obsoleto - Somente Photoshop 2.0*) Tabela de cores indexadas|
|1005|[Estrutura ResolutionInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/resolutioninforesource).|
|1006|Nomes dos canais alfa como uma série de strings de Pascal.|
|1007|*(Obsoleto) Ver estrutura [DisplayInfo](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/displayinforesource) com o ID 1077.*|
|1008|A legenda como uma string Pascal.|
|1009|[Informações sobre a borda.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/borderinformationresource) Contém um número fixo (2 bytes real, 2 bytes fracionários) para a largura da borda e 2 bytes para as unidades de borda (1 = polegadas, 2 = cm, 3 = pontos, 4 = picas, 5 = colunas).|
|1010|[Cor de fundo. ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/backgroundcolorresource/methods/index)|
|1011|Marcas de impressão. Uma série de valores booleanos de um byte: rótulos, marcas de corte, barras de cor, marcas de registro, negativo, espelhar, interpolar, legenda, marcadores de impressão.|
|1012|Informações de semitom para escala de cinza e multicanal|
|1013|[Informações de semitom de cor](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/colorhalftoneinformationresource)|
|1014|Informações de semitom de duotone|
|1015|Função de transferência de escala de cinza e multicanal|
|1016|[Funções de transferência de cor](/pages/createpage.action?spaceKey=psdnet&title=ColorTransferFunctionsResource&linkCreation=true&fromPageId=106204188)|
|1017|Funções de transferência de duotone|
|1018|Informações de imagem duotone|
|1019|Dois bytes para os valores eficazes de preto e branco para o intervalo de ponto|
|1020|*(Obsoleto)*|
|1021|Opções EPS|
|1022|[Informações Quick Mask](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/quickmaskinformationresource). ID do canal da Máscara Rápida; 1 byte booleano indicando se a máscara estava inicialmente vazia.|
|1023|*(Obsoleto)*|
|1024|[Informações do estado da camada](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerstateinformationresource).|
|1025|Caminho de trabalho (não salvo). Formato de recurso de caminho.|
|1026|[Informações de grupo de camadas](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupinformationresource). 2 bytes por camada contendo um ID de grupo para os grupos de arrastar. Camadas em um grupo têm o mesmo ID de grupo.|
|1027|*(Obsoleto)*|
|1028|Registro IPTC-NAA. Contém informações de *File Info...*.|
|1029|Modo de imagem para arquivos de formato bruto|
|1030|Qualidade JPEG. Privado.|
|1032|*(Photoshop 4.0) [Informação de grade e guias.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/gridandguidesresouce)*|
|1033|*(Photoshop 4.0) [](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[Recurso de miniatura](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)[para Photoshop 4.0](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnail4resource)* apenas|
|1034|*(Photoshop 4.0)* Sinal de direitos autorais. Booleano indicando se a imagem está protegida por direitos autorais.|
|1035|*(Photoshop 4.0)* URL. Identificador de uma string de texto com localizador de recurso uniforme*.*|
|1036|*(Photoshop 5.0)[Recurso de miniatura](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/thumbnailresource)* (substitui o recurso 1033).|
|1037|*(Photoshop 5.0) [Ângulo Global](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalangleresource)*. 4 bytes que contêm um inteiro entre 0 e 359, que é o ângulo global de iluminação para a camada de efeitos. Se não estiver presente, presume-se ser 30.|
|1038|*(Obsoleto) Veja o ID 1073 abaixo. (Photoshop 5.0)* Recurso de amostradores de cores.|
|1039|*(Photoshop 5.0) [Perfil ICC](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccprofileresource)*. Os bytes brutos de um perfil de formato ICC (International Color Consortium).*  |
|1040|*(Photoshop 5.0) [Marca d'água](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/watermarkresource)*.|
|1041|*(Photoshop 5.0) [Perfil ICC não marcado](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/iccuntaggedresource)*. 1 byte que desativa qualquer tratamento de perfil assumido ao abrir o arquivo. 1 = intencionalmente sem marcação.|
|1042|*(Photoshop 5.0)* Efeitos visíveis. Bandeira global de 1 byte para mostrar/ocultar todas as camadas de efeito. Presente apenas quando estão ocultas.|
|1043|*(Photoshop 5.0)* Semitom de ponto focal. 4 bytes para a versão, 4 bytes para o comprimento e os dados de comprimento variável.|
|1044|*(Photoshop 5.0)[IDs específicos do documento](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/documentspecificidsresource)*. Número de semente. 4 bytes: Valor base, a partir do qual os IDs de camada serão gerados (ou um valor maior se os IDs existentes já os excederem). Seu objetivo é evitar o caso em que adicionamos camadas, achatamos, salvamos, abrimos e depois adicionamos mais camadas que acabam com os mesmos IDs do primeiro conjunto.|
|1045|*(Photoshop 5.0) [Nomes Alfa Unicode](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unicodealphanamesresource)*.|
|1046|*(Photoshop 6.0)* Contagem da Tabela de Cores Indexadas. 2 bytes para o número de cores na tabela que estão realmente definidas|
|1047|*(Photoshop 6.0)* [Índice de Transparência](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/transparencyindexresource).|
|1049|*(Photoshop 6.0)* [Altitude Global.](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/globalaltituderesource)|
|1050|*(Photoshop 6.0)* Fatias.|
|1051|*(Photoshop 6.0)* URL do Fluxo de Trabalho.|
|1052|*(Photoshop 6.0)* Ir para XPEP. 2 bytes para a versão principal, 2 bytes para a versão secundária, 4 bytes para a contagem. O seguinte é repetido para a contagem: 4 bytes para o tamanho do bloco, 4 bytes para a chave, se a chave for *'jtDd'* , então a próxima é um Booleano para a bandeira suja; caso contrário, é uma entrada de 4 bytes para a data de modificação.|
|1053|*(Photoshop 6.0)* Identificadores Alfa.|
|1054|*(Photoshop 6.0)[Lista de URLs](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/urllistresource)*.|
|1057|*(Photoshop 6.0)* Informações de Versão.|
|1058|*(Photoshop 7.0)* Dados EXIF 1.|
|1059|*(Photoshop 7.0)* Dados EXIF 3*.*|
|1060|*(Photoshop 7.0)* [Metadados XMP](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/xmpresource). Informações do arquivo como descrição XML.|
|1061|*(Photoshop 7.0)[Digerir Legendas](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/captiondigestresource)*. 16 bytes: RSA Data Security, algoritmo de resumo de mensagem MD5|
|1062|*(Photoshop 7.0)[Escala de impressão](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printscaleresource)*. (0 = centrado, 1 = tamanho para ajustar, 2 = definido pelo usuário). 4 bytes para a localização x (ponto flutuante). 4 bytes para a localização y (ponto flutuante). 4 bytes para a escala (ponto flutuante)|
|1064|*(Photoshop CS)* [Razão de Aspecto de Pixels](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/pixelaspectratioresource).|
|1065|*(Photoshop CS)* Composições de Camadas.|
|1066|*(Photoshop CS)* Cores Duotone Alternativas. Este recurso não é lido ou usado pelo Photoshop.|
|1067|*(Photoshop CS)* Cores Spot Alternativas. Este recurso não é lido ou usado pelo Photoshop.|
|1069|*(Photoshop CS2)* [ID(s) de Seleção da Camada](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layerselectionidsresource). 2 bytes para a contagem, a seguir é repetido para cada contagem: 4 bytes para o ID da camada|
|1070|*(Photoshop CS2)* Informações de Tonalização HDR|
|1071|*(Photoshop CS2)* Informações de Impressão|
|1072|*(Photoshop CS2)* [ID de Grupos de Camada Habilitado](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/layergroupsenabledresource). 1 byte para cada camada no documento, repetido pelo comprimento do recurso. NOTA: Os grupos de camadas têm marcadores de início e fim|
|1073|*(Photoshop CS3)* Recurso de amostradores de cores. Veja também o ID 1038 para o formato antigo.|
|1074|*(Photoshop CS3)* Escala de Medição.|
|1075|*(Photoshop CS3)* Informações de Linha do Tempo.|
|1076|*(Photoshop CS3)* Divulgação de Planilha.|
|1077|*(Photoshop CS3) Estrutura de Informações de Exibição* para suportar cores de ponto flutuante. Veja também o ID 1007.|
|1078|*(Photoshop CS3)* Skins de Cebola.|
|1080|*(Photoshop CS4)* Informações de Contagem.|
|1082|*(Photoshop CS5)* Informações de Impressão.|
|1083|*(Photoshop CS5)* Estilo de Impressão. As marcas de impressão, rótulos, ornamentos, etc.|
|1084|*(Photoshop CS5)* Macintosh NSPrintInfo. Informações específicas da OS variáveis para Macintosh.|
|1085|*(Photoshop CS5)* Windows DEVMODE. Informações específicas da OS variáveis para Windows.|
|1086|*(Photoshop CS6)* Caminho do Arquivo de Salvamento Automático.|
|1087|*(Photoshop CS6)* Formato de Salvamento Automático. |
|1088|*(Photoshop CC)* Estado de Seleção de Caminho.|
|2000-2997|Informações de Caminho (caminhos salvos).|
|2999|Nome do caminho de recorte.|
|3000|*(Photoshop CC)* Informações de Origem do Caminho|
|4000-4999|Recurso(s) de Plug-In. Recursos adicionados por um plug-in.|
|7000|Variáveis Image Ready. Representação XML da definição de variáveis|
|7001|Conjuntos de dados Image Ready|
|7002|Estado padrão selecionado por padrão do Image Ready|
|7003|Estado expandido de sobreposição do Image Ready 7|
|7004|Estado expandido de sobreposição do Image Ready|
|7005|Configurações de camada do Image Ready para salvar|
|7006|Versão do Image Ready|
|8000|*(Photoshop CS3)* Fluxo de trabalho do Lightroom, se presente o documento está no meio de um fluxo de trabalho do Lightroom.|
|10000|[Informações de marcas de impressão](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/printflagsresource).|


A Aspose.PSD suporta alguns desses recursos. Se um Recurso não possui sua própria Classe, você pode usar o [UnknownResource ](https://reference.aspose.com/psd/net/aspose.psd.fileformats.psd.resources/unknownresource) da Referência da API Aspose.PSD.

Os Recursos de Imagens Globais PSD podem ser usados em uma grande quantidade de casos. Você pode obter Dados de Baixo Nível específicos que não pode obter no Adobe Photoshop.

Além disso, sinta-se à vontade para relatar sobre os Recursos de Imagens que você precisa. O [Fórum Aspose para PSD](https://forum.aspose.com/c/psd) pode ajudar.
