---
title: Notas de Lançamento do Aspose.PSD para .NET 20.9
type: docs
weight: 40
url: /pt/net/aspose-psd-for-net-20-9-release-notes/
---

{{% alert color="primary" %}} 

Esta página contém notas de lançamento para o [Aspose.PSD para .NET 20.9](https://www.nuget.org/packages/Aspose.PSD/)

{{% /alert %}} 

|**Chave**|**Resumo**|**Categoria**|
| :- | :- | :- |
|PSDNET-408|Suporte do recurso SoLEResource (recurso de camada de objeto inteligente externo)|Recurso|
|PSDNET-614|Suporte de Objetos Inteligentes Vinculados|Recurso|
|PSDNET-615|Suporte de Objetos Inteligentes Incorporados|Recurso|
|PSDNET-690|Atualização de texto em arquivo PSD específico e salvamento que altera algumas camadas e muitos parâmetros de texto|Correção de Bug|
|PSDNET-696|As camadas FillLayer não são atualizadas após a criação e não podem ser renderizadas corretamente|Correção de Bug|
|PSDNET-712|Regreção: Aspose.PSD 20.8.0 não consegue abrir arquivo|Correção de Bug|
|PSDNET-714|Em um arquivo PSD específico, redimensionar TextLayer quebra o valor de localização|Correção de Bug|

## **Mudanças na API Pública**
# **APIs Adicionadas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AdicionarRegistroDeTexto(System.String,Aspose.PSD.RectangleF)
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.CernagemAutomática
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LigadurasPadrão
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.LigadurasDiscretas
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.AlternânciasContextuais
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.ÍndiceIdioma
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.EscalaVertical
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.EscalaHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.Text.ITextStyle.Frações
- T:Aspose.PSD.FileFormats.Psd.AutoKerning
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Manual
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Métrico
- F:Aspose.PSD.FileFormats.Psd.AutoKerning.Óptico
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.LinkResource.Item(System.Guid)
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.ISmartObjectLayerResource.IdColocado
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Versão
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.IdÚnico
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.ÉPersonalizado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.NúmeroPágina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.TotalPáginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.PolíticaSuavização
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.TipoCamadaColocada
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Esquerda
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Topo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Direita
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Base
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Limites
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.MatrizTransformação
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.PontosMalhaHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.PontosMalhaVertical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.UnidadePontosMalhaHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.UnidadePontosMalhaVertical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Assinatura
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Valor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Perspectiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.OutraPerspectiva
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.UPedido
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.VPedido
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado.Itens
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.IdComp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.OriginalIdComp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.IdÚnico
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.IdColocado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.NúmeroPágina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.TotalPáginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.PolíticaSuavização
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.TipoCamadaColocada
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.MatrizTransformação
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.NãoMatrizTransformação
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Assinatura
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Comprimento
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.VersãoPSD
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Itens
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Recorte
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.ContagemQuadro
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Resolução
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.UnidadeResolução
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Comp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Largura
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Altura
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.PassosQuadroNumerador
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.PassosQuadroDenominador
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.DuraçãoNumerador
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.DuraçãoDenominador
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoObjetoInteligente.Salvar(Aspose.PSD.StreamContainer,System.Int32)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.#ctor
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor(System.Guid,System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.#ctor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.Chave
- F:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.SoLeResource.ChaveFerramentaTipo
- T:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente.#ctor
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente.#ctordo(Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoColocado)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente.#ctor(System.Boolean,System.Boolean)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente.GerarRecursoColocado
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente.GerarRecursoIncorporadoInteligente
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.CriadorRecursoInteligente.GerarRecursoExternoInteligente
- T:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente
- P:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.LimitesConteúdos
- P:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.FonteConteúdos
- P:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.Conteúdos
- P:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.TipoConteúdo
- P:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.ProvedorObjetoInteligente
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.ExportarConteúdos(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.CarregarConteúdos(Aspose.PSD.OpçõesCarregamento)
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.SubstituirConteúdos(Aspose.PSD.Imagem)
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.SubstituirConteúdos(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.AnexarLink
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.ConverterParaVinculado(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.RevincularParaArquivo(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.CamadaObjetoInteligente.AtualizarConteúdoModificado
- T:Aspose.PSD.FileFormats.Psd.ProvedorObjetoInteligente
- M:Aspose.PSD.FileFormats.Psd.ProvedorObjetoInteligente.AnexarTodosVinculados
- M:Aspose.PSD.FileFormats.Psd.ProvedorObjetoInteligente.AtualizarTodosConteúdosModificados
- T:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.TipoObjetoInteligente
- F:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.TipoObjetoInteligente.Incorporado
- F:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.TipoObjetoInteligente.VinculadoDisponível
- F:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.TipoObjetoInteligente.VinculadoIndisponível
- F:Aspose.PSD.FileFormats.Psd.Layers.Objs.Inteligentes.TipoObjetoInteligente.LinkBiblioteca
- P:Aspose.PSD.FileFormats.Psd.PsdImagem.ProvedorObjetoInteligente

# **APIs Removidas:**
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.Txt2Resource.AdicionarRegistroDeTexto(System.String)
- M:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.#ctor(System.Guid,System.Boolean)
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Versão
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.IdÚnico
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.ÉPersonalizado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.NúmeroPágina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.TotalPáginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.PolíticaAntiSerrilhado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.TipoCamadaColocada
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Esquerda
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Topo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Direita
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Base
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Limites
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.MatrizTransformação
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.PontosMalhaHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.PontosMalhaVertical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.UnidadePontosMalhaHorizontal
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.UnidadePontosMalhaVertical
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoPlLd.Valor
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.IdComp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.OriginalIdComp
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.Versão
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.IdÚnico
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.IdColocado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.ÉPersonalizado
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.NúmeroPágina
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.TotalPáginas
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.PolíticaSuavização
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.TipoCamadaColocada
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.Esquerda
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.Topo
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.Direita
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.Base
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.Limites
- P:Aspose.PSD.FileFormats.Psd.Layers.LayerResources.RecursoSoLd.MatrizTransformaçãoPonto fora da curva