# Cronosfera Fractal

Projeto visual e analitico em HTML unico, executado localmente no navegador, com painel principal em tempo real e modulos analiticos abaixo dele.

## Como executar

Abra [`cronosfera-fractal-melhorado.html`](C:\Users\david\Documents\New project\cronosfera-fractal-melhorado.html) diretamente no navegador.

Para congelar a base atual para handoff, use tambem [`cronosfera-fractal-melhorado-STABLE.html`](C:\Users\david\Documents\New project\cronosfera-fractal-melhorado-STABLE.html), que e um snapshot identico do estado funcional atual.

## Estrutura principal

No painel principal:

- campo visual central em tempo real
- marcador temporal/presente e relogio UTC
- radar no lado direito
- hexagrama I Ching no lado esquerdo
- controles temporais `PASSADO`, `PRESENTE`, `FUTURO`
- HUDs e metricas visuais conectadas ao estado atual do sistema

Abaixo do painel:

- dock horizontal com blocos numericos e HUDs destacados
- faixa Maya e faixas auxiliares
- grafico principal do campo fractal
- blocos analiticos e seções operacionais abaixo da dobra

## Observacoes importantes

- O projeto roda localmente no navegador e depende do JavaScript inline do proprio HTML.
- A matematica atual deve ser preservada. Nao altere sem instrucao explicita:
  - `updateHex(s)`
  - `render(ts)`
  - `signalCached(...)`
  - `dSignalCached(...)`
  - `KW_SEQ`
  - `HN`
  - `MAYA`
  - `NOW_YEAR`
  - `timeOffset`
- O layout atual ja foi ajustado manualmente. Nao mova elementos entre painel e area inferior sem pedido explicito.
