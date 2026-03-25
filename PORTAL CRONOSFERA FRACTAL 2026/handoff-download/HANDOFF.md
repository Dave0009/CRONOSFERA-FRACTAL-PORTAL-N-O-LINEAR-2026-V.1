# Handoff Seguro

## Estado atual

Esta base foi congelada no estado funcional atual para continuidade por outro agente sem redesenhar o projeto e sem mexer na matematica central.

Arquivos de referencia:

- trabalho: [`cronosfera-fractal-melhorado.html`](C:\Users\david\Documents\New project\cronosfera-fractal-melhorado.html)
- snapshot congelado: [`cronosfera-fractal-melhorado-STABLE.html`](C:\Users\david\Documents\New project\cronosfera-fractal-melhorado-STABLE.html)

## Funcoes criticas que nao devem ser renomeadas

- `updateHex(s)`
- `render(ts)`
- `signalCached(year)`
- `dSignalCached(year)`
- `drawRadar(t)`
- `initFloatingNumericDock()`
- `initFloatingHexbox()`

Essas funcoes estao conectadas ao loop principal, ao painel vivo e ao layout atual. Mudancas nelas devem ser incrementais e cirurgicas.

## IDs e elementos criticos

- `mainPanel`
- `cWarp`
- `cOverlay`
- `cRadar`
- `hexbox`
- `hx-name`
- `hx-num`
- `hx-lines`
- `timeExplorer`
- `floating-numeric-dock`
- `manualLink`
- `mayaHUD`
- `kurHUD`

Nao renomear IDs acima. Nao duplicar. Nao reparentar automaticamente.

## O que esta no painel

- campo principal em tempo real
- relogio UTC central
- controles temporais
- hexagrama no lado esquerdo
- radar no lado direito
- overlays e canvas de painel

## O que esta abaixo do painel

- dock horizontal com blocos numericos/HUDs que ja foram destacados do painel
- faixas graficas auxiliares
- grafico principal do campo fractal
- seções analiticas e operacionais abaixo da dobra

## Regras de continuidade

- Nao mover radar nem hexagrama sem pedido explicito.
- Nao mover de volta para o painel os blocos que ja estao no dock inferior.
- Nao abrir novo hardening estrutural.
- Nao alterar a matematica atual sem instrucao explicita.
- Nao renomear funcoes ou IDs criticos.
- Futuras mudancas devem ser pequenas, reversiveis e localizadas.

## Observacao pratica

`updateHex(s)` e `render(ts)` estao ativos e preservados. Radar e hexagrama estao funcionando na base atual. O snapshot `STABLE` deve ser tratado como referencia de seguranca para rollback ou comparacao.
