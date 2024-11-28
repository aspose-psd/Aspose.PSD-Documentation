---
title: Como usar Warp no Aspose.PSD
type: docs
weight: 40
url: /pt/como-usar-warp-no-aspose-psd/
---

## **Parte 1 - Renderizando um Arquivo PSD com o Efeito Warp**

O Photoshop salva a imagem renderizada após aplicar o efeito Warp. Nossa biblioteca pode reproduzir ou re-renderizar a imagem com o efeito Warp. Para habilitar esse recurso, basta definir a flag AllowWarpRepaint nas configurações ao abrir o arquivo PSD.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-Aspose-PSD-Warp-Renderizacao-1.cs" >}}

Resultado:
![Resultado do Warp Aspose.PSD para .NET 1](warp1.png)

Além de renderizar o efeito Warp para SmartLayers, nossa biblioteca também suporta o Warp para TextLayers. O código de implementação permanece idêntico, sendo a única diferença no nome do arquivo.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-Aspose-PSD-Warp-Renderizacao-2.cs" >}}

Resultado:
![Resultado do Warp Aspose.PSD para .NET 2](warp2.png)

**! Nota:** Atualmente, nossa biblioteca suporta a renderização de Warp personalizado (onde os usuários manipulam pontos de malha) e todos os tipos padrão de Warp.


## **Parte 2 - Modificando o Efeito Warp**

Nossa biblioteca permite não apenas renderizar, mas também modificar (adicionar) o efeito Warp.
Essas modificações são facilitadas pelas funcionalidades da classe **WarpParams**.

| **Recurso**  | **Descrição**                                                         | 
|:-------------|:----------------------------------------------------------------------------|
| Limites      | Retorna os limites da imagem distorcida.                                     |
| Pontos da Malha | Uma matriz de pontos, onde cada ponto representa um vértice da malha de distorção. |
| Valor        | O valor do efeito Warp para efeitos de distorção não personalizados.                   |
| Rotacionar e Distorir o Warp | Uma enumeração que define a direção de efeitos de distorção não personalizados.           |
| Estilos de Warp   | Uma enumeração que define o tipo de efeito Warp.                            |

O exemplo de código abaixo demonstra como determinar o tipo de efeito Warp para uma Camada Inteligente e ajustar o tipo e a intensidade da distorção para o efeito.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-Aspose-PSD-Warp-Renderizacao-3.cs" >}}

Resultado:
![Resultado do Warp Aspose.PSD para .NET 3](warp3.png)

## **Parte 3 - Adicionando o Efeito Warp**

O exemplo de código abaixo demonstra como adicionar um efeito Warp padrão a uma Camada Inteligente.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-Aspose-PSD-Warp-Renderizacao-4.cs" >}}

Resultado:
![Resultado do Warp Aspose.PSD para .NET 4](warp4.png)

O exemplo de código abaixo demonstra como adicionar um efeito Warp personalizado a uma Camada Inteligente.
{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-Aspose-PSD-Warp-Renderizacao-5.cs" >}}

Resultado:
![Resultado do Warp Aspose.PSD para .NET 5](warp5.png)

O exemplo de código abaixo demonstra como adicionar um efeito Warp a uma Camada de Texto. 
**! Nota:** De acordo com os padrões do Photoshop, o efeito Warp para Camadas de Texto é tipicamente limitado ao tipo padrão. No entanto, nossa biblioteca suporta o uso de dois tipos de efeitos Warp. Por favor, note que tais arquivos podem não ser totalmente compatíveis com o Photoshop.

{{< gist "aspose-com-gists" "8a4c9d34ce856d1642fc7c0ce974175c" "Documentacao-Aspose-PSD-Warp-Renderizacao-5.cs" >}}

Resultado:
![Resultado do Warp Aspose.PSD para .NET 6](warp6.png)

Continuamos a aprimorar e expandir as capacidades do nosso efeito Warp, focando em melhorar sua velocidade, qualidade e funcionalidades suportadas. Fique atualizado com nossos lançamentos mensais para as últimas novidades.
Sua equipe do Aspose.PSD
