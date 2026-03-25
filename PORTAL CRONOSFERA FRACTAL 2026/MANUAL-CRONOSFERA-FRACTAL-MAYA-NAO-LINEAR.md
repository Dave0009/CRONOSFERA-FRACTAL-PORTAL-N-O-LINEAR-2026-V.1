# Manual da Cronosfera Fractal Maya Nao Linear

## 1. Titulo e apresentacao

**Cronosfera Fractal Maya Nao Linear** e o nome dado a este instrumento computacional de leitura temporal, visualizacao analitica e interpretacao experimental. Na sua forma atual, trata-se de uma pagina unica executada localmente no navegador, onde um painel vivo em tempo real convive com modulos de analise historica, projecao, validacao, simulacao e experimentacao.

A proposta geral da Cronosfera e articular, numa mesma interface, varias camadas de observacao:

- dinamica nao linear
- sinal historico sintetico e suas derivadas
- curvatura temporal
- acoplamentos entre modulos
- leitura fractal e ritmica
- visualizacao matematica em multiplas escalas
- camadas simbolicas de apoio interpretativo

Em linguagem rigorosa, a Cronosfera nao e um oraculo, nem uma maquina de adivinhacao. E uma arquitetura de software que combina um motor visual em tempo real, um conjunto de sinais sinteticos e campos derivados, modulos analiticos que organizam leituras por convergencia, clusterizacao, oscilacao, caos, validacao e simulacao, e uma camada simbolica que deve ser lida como operador de interpretacao e nao como verdade empirica absoluta.

## 2. Prefacio conceitual

O tempo cronologico mede sucessao. O tempo dinamico mede transformacao. O tempo de fase mede posicao dentro de um ciclo. A curvatura historica mede o quanto uma trajetoria muda de regime. A leitura de ressonancia procura correspondencias, acoplamentos e ritmos recorrentes entre eventos, modulacoes e campos.

Na Cronosfera, essas dimensoes nao aparecem separadas por conveniencia estetica, mas por necessidade epistemologica. Uma cronologia simples diz "quando". Um campo dinamico procura sugerir "como" um sistema muda. Uma leitura de fase pergunta "em que momento de um ciclo maior estamos". Uma curvatura pergunta "quanto o sistema esta infletindo". Uma leitura de ressonancia pergunta "quais estruturas parecem se alinhar, ecoar ou se comprimir".

O espirito do sistema e o de um observatorio interpretativo. Ele oferece uma engenharia de software coerente, visualizacoes sinteticas e analiticas, hipoteses computacionais sobre regime, fase e instabilidade, e uma camada simbolica auxiliar. O que ele nao oferece, por si, e uma certificacao metafisica do futuro. Sua dignidade reside menos em prometer certeza e mais em organizar inteligibilidade.

## 3. Arquitetura geral da pagina

### 3.1 Topo temporal

No topo da interface encontram-se o relogio UTC, a data corrente, a legenda central do sistema e a primeira camada de orientacao temporal. Essa regiao funciona como frontispicio do instrumento: ela fixa o agora, enuncia o regime geral do painel e ancora a observacao.

### 3.2 Painel principal

O painel principal ocupa a altura inicial da pagina e e o coracao do sistema. Nele operam, em renderizacao continua:

- o campo central de intensidade
- as camadas de ressonancia
- a topologia de conexoes
- o fluxo de particulas
- os atratores e orbitas
- o campo de singularidades
- o warp reativo ao cursor
- a sobreposicao do cursor e do marcador do presente
- o radar de fase
- a mini-visualizacao de Kuramoto
- a faixa inferior interna com singularidades, Maya, sinal resumido, DFT e autocorrelacao

### 3.3 Dock numerico abaixo do painel

Entre o painel principal e o grande grafico analitico foi instalada uma faixa horizontal chamada `floating-numeric-dock`. Ela recebeu blocos que antes disputavam espaco lateral no painel:

- painel superior de invariantes
- bloco de fase e pulso
- HUD de Kuramoto
- HUD Maya Long Count
- bloco de ressonancias
- bloco de atratores
- bloco de acoplamento Maya-campo
- bloco de Lyapunov
- bloco de ondas
- bloco de singularidades

Essa faixa deve ser entendida como extensao funcional do painel principal. Ela nao e uma secao secundaria: e o anel metrologico do sistema.

### 3.4 Blocos analiticos inferiores

Abaixo do dock horizontal surgem os modulos de leitura analitica, agrupados em secoes autonomas: `analytic`, `cluster`, `harmonic`, `predictive`, `forecast`, `osc`, `lorenz`, `validation`, `level4`, `dna`, `production`, `confidence`, `lab`, `universe` e `multiverse`.

### 3.5 O que atualiza continuamente e o que depende de acao

**Atualizacao continua:** painel principal, relogio UTC, marcador do presente, hexagrama, radar, atratores visiveis, camadas do campo, strips inferiores do painel e HUDs ligados ao loop principal.

**Atualizacao por visibilidade da secao:** `analytic`, `cluster`, `harmonic`, `predictive`, `forecast`, alem de varios modulos avancados que inicializam resize, desenho ou primeira execucao quando entram no viewport.

**Atualizacao sob demanda por botoes:** `validation`, `level4`, `DNA`, `production`, `confidence`, `lab`, `universe` e `multiverse`. Embora algumas dessas secoes montem visualizacoes quando visiveis, sua leitura plena depende dos controles `data-click-action`.

## 4. Explicacao detalhada de cada item do painel

### 4.1 Relogio superior UTC

**O que e visualmente:** um mostrador numerico central, de grande destaque, exibindo a hora em formato UTC.

**O que representa conceitualmente:** a ancora cronologica do sistema. Ele fixa o referencial temporal objetivo a partir do qual o resto do painel deriva seu estado presente.

**Como se relaciona com o restante:** a Cronosfera trabalha com camadas simbolicas e dinamicas, mas se prende a um eixo temporal concreto. O relogio impede que a interpretacao perca o contato com a medicao.

**Como deve ser lido:** como ponto de fixacao do agora, nao como mera decoracao.

**Valor operacional:** serve de referencia para o seed temporal do estado atual e para a orientacao do observador diante do painel vivo.

### 4.2 Data mostrada

**O que e visualmente:** uma linha textual abaixo do relogio UTC, indicando a data corrente.

**O que representa conceitualmente:** a passagem do instante numerico para o calendario humano legivel.

**Como se relaciona com o restante:** amarra o fluxo continuo do relogio a um quadro civil e historico.

**Como deve ser lida:** como traducao do agora para o calendario usual.

**Valor operacional:** ajuda a cruzar a leitura do painel com marcos conhecidos e com a navegacao temporal manual.

### 4.3 Faixa ou legenda central do painel

**O que e visualmente:** a linha textual sob o relogio, hoje identificando o campo fractal Maya, a dinamica historica, Kuramoto e a orientacao de rolagem.

**O que representa conceitualmente:** o manifesto sintatico da interface. Ela diz ao observador que o instrumento opera por composicao de lentes, nao por um unico indice.

**Como se relaciona com o restante:** faz a ponte entre o painel vivo e os modulos abaixo, anunciando que o topo e apenas o primeiro estrato de leitura.

**Como deve ser lida:** como legenda epistemologica.

**Valor operacional:** reduz a opacidade da interface para primeira entrada do usuario.

### 4.4 Campo visual principal

**O que e visualmente:** o grande campo colorido de fundo, composto por multiplos canvases sobrepostos (`cField`, `cResonance`, `cTopo`, `cFlow`, `cOrbits`, `cSing`, `cWarp`, `cOverlay`, `cKuramoto` e `cRadar`).

**O que representa conceitualmente:** uma paisagem dinamica de intensidades, gradientes, tensoes e organizacoes temporais.

**Como se relaciona com o restante:** e a base onde os demais elementos se inscrevem. Atratores, radar, cursor, hexagrama e strips inferiores sao leituras ou cortes dessa mesma dinamica.

**Como deve ser lido:** primeiro por contraste global; depois, por cruzamento com marcadores, orbitas e graficos.

**Valor operacional:** oferece uma intuicao imediata de regime, densidade e estabilidade antes que o usuario desca aos modulos mais discretos.

### 4.5 Atratores, objetos e marcadores

**O que e visualmente:** pontos coloridos, orbitas pequenas, halos e marcadores anuais distribuidos no painel, desenhados a partir da lista de `ATTRACTORS`.

**O que representam conceitualmente:** eventos, polos historicos ou nodos privilegiados aos quais o sistema atribui peso estrutural.

**Como se relacionam com o restante:** eles alimentam clusterizacao, harmonia temporal, faixas de ressonancia e leituras de proximidade no radar.

**Como devem ser lidos:** nao como eventos "previsos" isoladamente, mas como pontos de referencia em torno dos quais o campo organiza tensao, recorrencia e memoria.

**Valor operacional:** fornecem alvos semanticos para a observacao, evitando que o painel permaneça apenas abstrato.

### 4.6 Faixa do presente

**O que e visualmente:** a linha vertical central e os chips que assinalam `PRESENTE` e o ano/era correspondente.

**O que representa conceitualmente:** o corte de simultaneidade do sistema; o lugar em que a leitura corrente intercepta o campo historico.

**Como se relaciona com o restante:** todas as comparacoes do painel partem desse eixo, inclusive o explorador temporal, o radar e a faixa Maya.

**Como deve ser lida:** como linha de referencia. O que esta a esquerda pertence ao passado relativo do recorte; o que esta a direita, ao horizonte futuro daquele enquadramento.

**Valor operacional:** disciplina a leitura, evitando que o usuario se perca em puro panorama.

### 4.7 Cursor temporal e ponto pulsante

**O que e visualmente:** o ponto luminoso pulsante no centro do presente e a figura luminosa de cursor que se move com rastro no painel.

**O que representa conceitualmente:** duas camadas distintas. O ponto central marca o presente estrutural do sistema. O cursor luminoso e um operador de navegacao perceptiva, acoplado ao gesto e ao warp local.

**Como se relaciona com o restante:** o marcador do presente fixa; o cursor explora. Um estabiliza a leitura, o outro a tensiona.

**Como deve ser lido:** o ponto central deve ser tratado como ancora. O cursor luminoso deve ser entendido como lente local de inspecao do campo, especialmente quando interage com o warp.

**Valor operacional:** permite simultaneamente uma leitura objetiva do eixo presente e uma leitura exploratoria das zonas de interesse.

### 4.8 Explorador temporal

**O que e visualmente:** a barra central inferior do painel, com botoes e `range` de exploracao.

**O que representa conceitualmente:** a capacidade de deslocar o observador ao longo da linha do tempo analitica, sem abandonar a mesma arquitetura de leitura.

**Como se relaciona com o restante:** altera `timeOffset`, portanto reancora o campo, o presente, o radar, os atratores visiveis, os HUDs e os strips inferiores.

**Como deve ser lido:** como instrumento de translacao temporal.

**Valor operacional:** e a principal ferramenta de comparacao entre passado, presente e futuro relativos.

### 4.9 Botoes de Passado, Presente e Futuro

**O que sao visualmente:** os tres botoes centrais do explorador temporal.

**O que representam conceitualmente:** macros de posicionamento de epoca.

**Como se relacionam com o restante:** ajustam diretamente o `timeOffset` para regimes predefinidos e recalibram a leitura do painel.

**Como devem ser lidos:** `PASSADO` e uma janela de grande recuo; `PRESENTE` reestabelece o referencial atual; `FUTURO` desloca a observacao para um horizonte adiante.

**Valor operacional:** aceleram a consulta e oferecem enquadramentos narrativos rapidos antes do ajuste fino pelo slider.

### 4.10 Indicadores numericos vinculados ao painel

**O que sao visualmente:** os blocos numericos hoje deslocados para o dock horizontal abaixo do painel, mas ainda semanticamente acoplados ao estado em tempo real.

**O que representam conceitualmente:** o plano metrologico do instrumento.

**Como se relacionam com o restante:** todos dependem do estado calculado no loop principal ou de agregados diretos dele.

**Como devem ser lidos:** como traducao numerica do que o olho capta no painel.

**Valor operacional:** permitem comparar impressoes qualitativas com magnitudes observaveis.

### 4.11 Painel superior de invariantes (`topStatsPanel`)

**O que e visualmente:** o bloco que exibe `F(x,y,t)`, `dF/dt`, `LYAP`, `ENT`, `SING`, `MAYA d2F` e a zona do sistema.

**O que representa conceitualmente:** o sumario de estado global do campo.

**Como se relaciona com o restante:** condensa em poucos valores aquilo que aparece distribuido no campo, no strip Maya e nas leituras de estabilidade.

**Como deve ser lido:** primeiro a zona (`STABLE`, `TRANSITION`, `CHAOTIC`), depois Lyapunov, depois gradientes e singularidades.

**Valor operacional:** oferece uma triagem imediata do regime em curso.

### 4.12 Bloco de fase e pulso (`metp`)

**O que e visualmente:** um bloco numerico com `FASE`, `PULSO`, `ATT VIS`, `TOPO E`, `RESS` e `FPS`.

**O que representa conceitualmente:** o estado operacional sintetico da maquina.

**Como se relaciona com o restante:** cruza metrica temporal (`FASE`, `PULSO`) com metrica de composicao visual (`ATT VIS`, `RESS`) e de custo de execucao (`FPS`).

**Como deve ser lido:** como painel de diagnostico e ritmo. `FASE` e `PULSO` contam mais para interpretacao; `FPS` conta mais para engenharia de uso.

**Valor operacional:** separa leitura conceitual de saude de execucao.

### 4.13 HUD de Kuramoto (`kurHUD`)

**O que e visualmente:** bloco com `ORDER R`, `COUPLING K`, `N OSC`, `FIELD` e `STATE`.

**O que representa conceitualmente:** o grau de sincronizacao da rede de osciladores.

**Como se relaciona com o restante:** o modelo de Kuramoto recebe modulacao do campo hibrido, da instabilidade e da energia de Lorenz.

**Como deve ser lido:** `R` baixo sugere caos, `R` medio sugere borda de fase, `R` alto sugere sincronizacao parcial ou global.

**Valor operacional:** oferece uma leitura de coesao sistemica complementar ao painel central.

### 4.14 HUD Maya Long Count (`mayaHUD`)

**O que e visualmente:** bloco com `Long Count`, `BAKTUN`, `KATUN`, `TUN`, `UINAL-KIN`, `CICLO %`, `d2F->CAMPO`, `SPAWN` e `DIAS TOTAIS`.

**O que representa conceitualmente:** a camada calendrica e moduladora Maya do instrumento.

**Como se relaciona com o restante:** alimenta o strip Maya, a curvatura `d2F`, o `boost` do campo, a multiplicacao de `spawn` de ressonancias e o tingimento cromatico do sistema.

**Como deve ser lido:** como quadro de fase calendrica, nao como almanaque literal.

**Valor operacional:** ancora a leitura fractal numa fase estrutural mais lenta e de maior periodo.

### 4.15 Bloco de ressonancias (`res-p`)

**O que e visualmente:** lista de ressonancias em texto.

**O que representa conceitualmente:** intervalos ou acoplamentos detectados como recorrentes no estado atual.

**Como se relaciona com o restante:** dialoga com a teia harmonica, os atratores e as ondas em atividade.

**Como deve ser lido:** como um quadro de intervalos de interesse, nao como calendario determinista.

**Valor operacional:** fornece um resumo textual de alinhamentos que o olho poderia perder no campo.

### 4.16 Bloco de atratores (`att-p`)

**O que e visualmente:** lista textual dos atratores visiveis.

**O que representa conceitualmente:** a populacao ativa de nodos historicos no recorte presente.

**Como se relaciona com o restante:** seu numero aparece em `ATT VIS`, seus pontos aparecem no painel e sua posicao se projeta no radar.

**Como deve ser lido:** como inventario de focos ativos na janela atual.

**Valor operacional:** ajuda a saber se o recorte temporal esta mais rarefeito ou mais povoado de referencias.

### 4.17 Bloco de acoplamento Maya-campo (`math-p`)

**O que e visualmente:** quadro curto que explicita `boost`, `spawn` e `tint`.

**O que representa conceitualmente:** a interface entre curvatura Maya e render do campo.

**Como se relaciona com o restante:** informa como a EMA da curvatura altera intensidade, surgimento de ondas e tingimento visual.

**Como deve ser lido:** como chave de leitura estrutural; ele explica por que o painel esta mais vivo, mais denso ou mais cromaticamente tenso em certos momentos.

**Valor operacional:** torna a interface menos opaca ao revelar parte da logica de acoplamento.

### 4.18 Bloco de Lyapunov (`lyap-p`)

**O que e visualmente:** barra de intensidade e texto resumindo o regime de `lambda(t)`.

**O que representa conceitualmente:** uma medida sintetica do grau de estabilidade ou divergencia local do sinal.

**Como se relaciona com o restante:** conversa diretamente com `vLy`, com a zona do sistema e com leituras de caos ou transicao.

**Como deve ser lido:** `lambda < 0` indica estabilidade relativa; perto de zero, limiar; positivo, sensibilidade crescente.

**Valor operacional:** e um dos indicadores mais importantes para saber se o sistema esta em regime tranquilo, critico ou caotico.

### 4.19 Bloco de ondas (`res-info`)

**O que e visualmente:** lista textual de ondas ou ativacoes recentes.

**O que representa conceitualmente:** memoria curta das ressonancias em curso.

**Como se relaciona com o restante:** reflete o estoque de `resonanceWaves` que tambem colore o campo.

**Como deve ser lido:** como diario resumido de atividade ondulatoria.

**Valor operacional:** auxilia na correlacao entre o que pulsa no campo e os nomes ou cores associados.

### 4.20 Bloco de singularidades (`sing-log`)

**O que e visualmente:** lista textual de singularidades recentes com ano e intensidade.

**O que representa conceitualmente:** pontos de curvatura mais forte, rupturas locais ou eventos de alta tensao estrutural.

**Como se relaciona com o restante:** alimenta a faixa de singularidades e ajuda a interpretar picos da curvatura.

**Como deve ser lido:** como registro de concentracoes fortes, mas nao como proclamacao automatica de "evento historico inevitavel".

**Valor operacional:** permite acompanhar emergencias de ruptura sem depender apenas do olhar.

### 4.21 Radar de fase

**O que e visualmente:** um cartao escuro, no lado direito do painel, com aneis concentricos, grades radiais, varredura e pontos.

**O que representa conceitualmente:** uma cartografia polar da distribuicao dos atratores em regime de fase e distancia relativa.

**Como se relaciona com o restante:** condensa no plano polar o que, no painel central, aparece espalhado ao longo do eixo temporal.

**Como deve ser lido:** ver secao especifica do radar mais abaixo.

**Valor operacional:** mede coesao, dispersao e varrimento do conjunto de atratores.

### 4.22 Hexagrama do I Ching em atualizacao

**O que e visualmente:** um cartao no lado esquerdo do painel com nome do hexagrama, linha de metricas e seis linhas yin/yang reconstituidas continuamente.

**O que representa conceitualmente:** uma camada simbolico-operacional derivada do estado dinamico do sistema.

**Como se relaciona com o restante:** seu estado depende de fase, sinal, pulso e seed temporal.

**Como deve ser lido:** ver secao especifica do hexagrama mais abaixo.

**Valor operacional:** oferece uma leitura condensada, simbolicamente estruturada, para complementar a analise matematica.

### 4.23 HUD de warp

**O que e visualmente:** pequeno painel `WARP` acima do centro, com barra e valor.

**O que representa conceitualmente:** a intensidade da perturbacao local produzida pela exploracao do cursor sobre o campo.

**Como se relaciona com o restante:** reage ao mouse, mede curvatura local e evidencia hotspots do painel.

**Como deve ser lido:** como indicador de sensibilidade de inspecao, nao como fenomeno autonomo.

**Valor operacional:** facilita a leitura localizada e a exploracao visual fina.

### 4.24 Faixas internas inferiores do painel

**O que sao visualmente:** `sing-strip`, `maya-strip`, `twz-strip`, `fft-w` e `ac-w`.

**O que representam conceitualmente:** cortes reduzidos, derivados do estado do painel, que mostram singularidades, ritmos Maya, o sinal resumido, sua transformada e sua autocorrelacao.

**Como se relacionam com o restante:** sao o elo entre o painel vivo e os blocos analiticos extensos logo abaixo.

**Como devem ser lidas:** como instrumentos de pretriagem.

**Valor operacional:** transformam o painel em observatorio de varias escalas simultaneas.

### 4.25 Botao de Manual Interpretativo

**O que e visualmente:** um botao central inferior chamado `Manual Interpretativo`.

**O que representa conceitualmente:** a consciencia reflexiva da propria interface; um convite explicito a leitura assistida.

**Como se relaciona com o restante:** abre a camada textual interna do projeto sem interromper a natureza visual do instrumento.

**Como deve ser lido:** como porta de contextualizacao, especialmente para usuarios em primeiro contato.

**Valor operacional:** reduz a opacidade da interface e ajuda a transitar da contemplacao para a interpretacao informada.

### 4.26 Aviso de rolagem

**O que e visualmente:** a pequena indicacao para rolar em direcao a analise completa.

**O que representa conceitualmente:** a afirmacao de que o painel inicial e apenas o limiar do sistema.

**Como se relaciona com o restante:** convida o usuario a sair da experiencia meramente cenografica e entrar no laboratorio completo.

**Como deve ser lido:** como chamado metodico a profundidade.

**Valor operacional:** orienta a navegacao para as secoes em que a maquina analitica se explicita por inteiro.

## 5. Explicacao detalhada do grafico do campo fractal

O primeiro grande bloco abaixo do painel, identificado como `CAMPO FRACTAL MAYA - MODELO COMPLETO`, e o principal espaco de leitura historico-analitica da Cronosfera.

### 5.1 A curva principal

A curva principal do grafico cumpre o papel de sinal historico sintetico. Na interface atual, sua base e descrita como campo Maya-fractal continuo. Em termos interpretativos, ela pode ser lida como um `S(t)` operacional: uma amplitude temporal sintetica cuja variacao importa mais que o valor absoluto nu.

### 5.2 `S(t)` e `F(t)`

Embora o projeto use, em varios pontos, a letra `F`, a funcao do grafico e a de um sinal de estado historico. Em linguagem prudente, convem dizer que `F(t)` e a nomenclatura funcional predominante, enquanto `S(t)` e uma forma conceitual aceitavel de nomear o sinal enquanto grandeza sintetica.

### 5.3 `dS/dt` ou `dF`

A primeira derivada aparece como velocidade de mudanca. Quando sua magnitude sobe, o sistema nao esta apenas "alto" ou "baixo": ele esta mudando rapidamente. Isso e crucial para distinguir estabilidade de transicao.

### 5.4 Curvatura e `C(t)`

O mapa de convergencia explicita `C(t) = |dF| x |d2F_Maya|`. Esta e uma das chaves interpretativas mais nobres do projeto: nao basta mudar, importa tambem o quanto a mudanca esta sendo curvada, comprimida ou desviada pela estrutura Maya.

### 5.5 Histograma e barras

O histograma torna visivel a distribuicao de aceleracoes ao longo do tempo, com threshold explicito. Seu papel e menos narrativo e mais estatistico: mostrar se o sistema entra em regimes de variacao acentuada com frequencia rara ou recorrente.

### 5.6 Heatmap e mapa preditivo

O mapa preditivo organiza a probabilidade normalizada futura a partir da mesma logica de convergencia. O heatmap historico, por sua vez, oferece uma textura de instabilidade ao longo do grande intervalo temporal.

### 5.7 Datas, anos, marcadores de pico e agora

Os anos e chips sobre a curva servem para evitar que a visualizacao se dissolva em puro grafismo. `AGORA` fixa o presente da janela; `PICO` sinaliza regioes de valor maximo ou inflexao forte.

### 5.8 Linhas verticais e sua leitura

As linhas verticais funcionam como costelas da leitura temporal. Elas particionam o eixo historico, ajudam a localizar epocas e intervalos, e permitem perceber compressao e rarefacao.

### 5.9 Relacao entre eixo temporal e intensidade do sinal

O eixo horizontal organiza a cronologia; o eixo vertical nao e "valor historico" literal, mas intensidade sintetica do campo. Por isso, a leitura mais correta nao e moral nem literalista. O que importa e tendencia, inflexao, persistencia, aceleracao, compressao e proximidade entre picos.

### 5.10 Como interpretar inflexoes, picos, compressoes e regimes estaveis

**Zonas de inflexao:** sugerem mudanca de regime.  
**Picos:** indicam maxima tensao ou maxima expressividade do sinal.  
**Compressoes:** quando varios indicadores se adensam num recorte estreito, o sistema sugere epoca de condensacao dinamica.  
**Regimes estaveis:** longas faixas suaves, com menor variacao derivativa e curvatura mais baixa, apontam para periodos de menor turbulencia interna do modelo.

## 6. Explicacao dos blocos analiticos abaixo do painel

### 6.1 `analytic`

**Funcao:** reunir o grafico principal, convergencia, histograma, mapa preditivo e heatmap.

**Automatico ou sob demanda:** desenha quando a secao entra em vista e responde aos botoes de faixa temporal.

**Tipo de leitura:** leitura-base do campo historico sintetico.

**Como consultar:** comecar pelo grafico principal, depois convergencia e por fim mapas auxiliares.

**O que nao inferir precipitadamente:** pico alto nao e prova de fato historico inevitavel.

### 6.2 `cluster detector`

**Funcao:** detectar agrupamentos de convergencia acima de threshold adaptativo.

**Automatico ou sob demanda:** automatico por desenho quando a secao entra em vista.

**Tipo de leitura:** identifica janelas de tensao agregada.

**Como consultar:** observar numero de clusters, centro, largura, intensidade e atrator proximo.

**O que nao inferir precipitadamente:** cluster nao e "profecia"; e aglomerado matematico.

### 6.3 `teia harmonica`

**Funcao:** procurar razoes entre intervalos de atratores, com filtros como phi, inteiro, Fibonacci, raiz de 2 e pi.

**Automatico ou sob demanda:** automatico ao entrar em vista.

**Tipo de leitura:** leitura de proporcao, intervalo e recorrencia.

**Como consultar:** olhar pares harmonicos, melhor razao e coerencia aurea.

**O que nao inferir precipitadamente:** harmonia detectada nao implica causalidade.

### 6.4 `predictive`

**Funcao:** construir janelas preditivas futuras moduladas por fase Maya.

**Automatico ou sob demanda:** automatico ao entrar em vista.

**Tipo de leitura:** janelas futuras com banda de incerteza.

**Como consultar:** ler a curva, a banda e os cards de anos destacados.

**O que nao inferir precipitadamente:** horizonte calculado nao e calendario de ocorrencias garantidas.

### 6.5 `forecast`

**Funcao:** produzir um campo probabilistico futuro a partir de recorrencias e KDE gaussiano.

**Automatico ou sob demanda:** automatico ao entrar em vista; o horizonte pode ser trocado por botoes.

**Tipo de leitura:** distribuicao de probabilidade futura em diferentes alcances.

**Como consultar:** alternar `+200a`, `+400a`, `+600a`, `+1000a` e observar picos.

**O que nao inferir precipitadamente:** probabilidade alta e densidade interna do modelo, nao garantia externa.

### 6.6 `osc`

**Funcao:** mostrar a rede de osciladores de Kuramoto com parametro de ordem.

**Automatico ou sob demanda:** automatico, pois deriva do estado do painel.

**Tipo de leitura:** coesao, borda de fase, sincronizacao parcial ou caos.

**Como consultar:** olhar `R`, `K` e o regime textual.

**O que nao inferir precipitadamente:** sincronizacao nao significa consenso historico literal; e uma analogia dinamica.

### 6.7 `lorenz`

**Funcao:** exibir o atrator de Lorenz e sua energia.

**Automatico ou sob demanda:** automatico, integrado ao loop principal e refletido tambem nos acoplamentos.

**Tipo de leitura:** sensibilidade, turbulencia e energia caotica.

**Como consultar:** observar a trilha, `x`, `y`, `z`, energia e contribuicao extra ao acoplamento.

**O que nao inferir precipitadamente:** caos nao quer dizer aleatoriedade absoluta.

### 6.8 `validation`

**Funcao:** avaliar desempenho de modelos por treino/teste, causalidade, cross-validation, permutation, calibration e reducao de overfitting.

**Automatico ou sob demanda:** ha disparos iniciais por visibilidade, mas a consulta plena e claramente sob demanda via botoes.

**Tipo de leitura:** leitura metodologica e de consistencia do software analitico.

**Como consultar:** comecar por `RODAR VALIDACAO COMPLETA`, depois ler metricas, causalidade, cross-validation e veredito.

**O que nao inferir precipitadamente:** boa metrica interna nao equivale a validacao cientifica universal.

### 6.9 `level 4`

**Funcao:** auto-tuning, evolucao de features, discovery e previsao.

**Automatico ou sob demanda:** a secao prepara futura visualizacao ao entrar em vista, mas sua riqueza depende dos botoes.

**Tipo de leitura:** exploracao de hiperparametros e crescimento do repertorio analitico.

**Como consultar:** seguir a ordem `AUTO-TUNING`, `EVOLUIR FEATURES`, `FEATURE DISCOVERY`, `PREVER FUTURO`.

**O que nao inferir precipitadamente:** descoberta automatica de features nao substitui criterio teorico.

### 6.10 `DNA`

**Funcao:** extrair padroes, construir modelo minimo, validar e congelar um DNA de modelo.

**Automatico ou sob demanda:** essencialmente sob demanda.

**Tipo de leitura:** consolidacao estrutural de features mais recorrentes.

**Como consultar:** rodar a cadeia completa ou cada etapa em separado.

**O que nao inferir precipitadamente:** "DNA" aqui e metafora de assinatura estrutural do modelo, nao substancia natural.

### 6.11 `production`

**Funcao:** testar estabilidade, construir consenso de DNA, comparar modelos e congelar um modelo de producao.

**Automatico ou sob demanda:** sob demanda.

**Tipo de leitura:** maturidade operacional do pipeline analitico.

**Como consultar:** `STABILITY TEST`, `CONSENSUS DNA`, `FINAL BATTLE`, `FREEZE PRODUCAO`.

**O que nao inferir precipitadamente:** producao congelada ainda e producao de um experimento computacional.

### 6.12 `confidence`

**Funcao:** quantificar incerteza, ensemble de DNAs, aprendizado continuo e score global.

**Automatico ou sob demanda:** sob demanda, com apoio de render por visibilidade.

**Tipo de leitura:** graduacao de confianca e spread.

**Como consultar:** comecar por incerteza, depois ensemble, depois score global.

**O que nao inferir precipitadamente:** score de confianca e confianca interna do modelo, nao atestado universal.

### 6.13 `lab`

**Funcao:** simular cenarios, medir impacto causal, usar fallback de dados e executar experimentos.

**Automatico ou sob demanda:** sob demanda.

**Tipo de leitura:** laboratorio de hipoteses e comparacao de cenarios.

**Como consultar:** ajustar sliders dos cenarios A e B, rodar comparacao e depois o experimento.

**O que nao inferir precipitadamente:** um cenario extremo no lab e ensaio de sensibilidade, nao predicao literal do mundo.

### 6.14 `universe`

**Funcao:** simular um universo multiagente com emergencia, DNA injection e Monte Carlo.

**Automatico ou sob demanda:** sob demanda.

**Tipo de leitura:** dinamica emergente entre agentes economy, climate, population stress e conflict.

**Como consultar:** primeiro `SIMULAR`, depois `MONTE CARLO`, depois `PREDICT 2030` e `COMPARAR MODELOS`.

**O que nao inferir precipitadamente:** agentes sinteticos nao representam sociedades reais de modo exaustivo.

### 6.15 `multiverse`

**Funcao:** evoluir multiplos universos, selecionar os melhores, prever 2040 e operar um loop vivo.

**Automatico ou sob demanda:** fortemente sob demanda, com suporte de sliders e controles humanos.

**Tipo de leitura:** selecao de regras, convergencia ou divergencia entre universos simulados.

**Como consultar:** evoluir universos, observar score por geracao, depois executar previsao e live mode.

**O que nao inferir precipitadamente:** "multiverso" aqui e arquitetura de simulacoes concorrentes, nao ontologia cosmologica.

## 7. Explicacao especifica do hexagrama

O hexagrama ocupa um lugar singular na Cronosfera porque condensa, em forma simbolica, um estado matematico em curso. Ele nao substitui o campo, o radar ou as metricas. Ele opera como transdutor simbolico.

### 7.1 Papel simbolico-operacional

Seu papel nao e meramente decorativo nem meramente esoterico. Ele organiza um nome de estado, um numero de hexagrama, uma composicao de seis linhas e uma pequena frase metrica de fase, amplitude, forca e derivada. Assim, ele oferece uma forma compacta de leitura sintetica do sistema.

### 7.2 Relacao com a atualizacao em tempo real

No arquivo atual, `updateHex(s)` esta ativo dentro de `render(ts)`. Isso significa que o modulo do hexagrama participa da respiracao do painel. Ele nao e uma imagem estatica; ele responde ao tempo, ao seed, ao sinal e ao pulso.

### 7.3 Leitura simbolica versus leitura matematica

**Leitura matematica:** as linhas resultam de uma transformacao do estado computado.  
**Leitura simbolica:** o observador pode consultar o hexagrama como indicacao de regime, composicao ou tonalidade do instante.

### 7.4 Como consultar o modulo

O melhor uso do hexagrama e comparativo: olhar o estado geral do painel, verificar a fase e o pulso, observar o hexagrama e ver se a mudanca do sistema produz mudanca na forma.

### 7.5 Como evitar supersticao

E preciso resistir a tres abusos: tomar o hexagrama como previsao infalivel, ignora-lo como puro ornamento, ou ler sua mudanca sem confronto com radar, curva e metricas. Seu lugar correto e o de um operador hermeneutico disciplinado.

## 8. Explicacao especifica do radar

O radar e uma das melhores pecas de sintese visual do sistema.

### 8.1 O que o radar mostra

Ele mostra, em coordenadas polares:

- um centro pulsante
- aneis concentricos
- eixos radiais
- um feixe de varredura
- pontos correspondentes aos atratores

### 8.2 Como ler posicao, fase, dispersao, proximidade e agrupamento

**Posicao angular:** distribui os atratores segundo uma transformacao angular do seu ano.  
**Distancia radial:** indica distancia relativa ao presente em escala comprimida.  
**Varredura:** o feixe rotativo funciona como instrumento de revelacao e acentuacao de proximidades.  
**Agrupamento:** muitos pontos em regioes vizinhas sugerem coesao de fase ou condensacao de referencias.  
**Dispersao:** pontos afastados e mal concentrados sugerem regime mais espalhado e menos coeso.

### 8.3 Como ele complementa o painel central

O painel central distribui os atratores ao longo do tempo e do campo. O radar reordena essa informacao em forma polar. Em outras palavras: o painel mostra a paisagem; o radar mostra a geometria relacional.

### 8.4 Regime coeso e regime disperso

**Regime mais coeso:** pontos mais organizados, leitura mais nitida de clusters e feixe com recorrencias perceptiveis.  
**Regime mais disperso:** pontos espalhados, menor continuidade aparente, mais dificuldade de encontrar alinhamentos.

## 9. Guia de uso da Cronosfera

### 9.1 Como abrir e usar a pagina

Abra o arquivo HTML principal localmente no navegador. Aguarde o painel estabilizar. Observe primeiro o topo, depois o campo, depois o dock numerico e so entao os modulos inferiores.

### 9.2 Por onde olhar primeiro

Uma boa ordem inicial e:

1. relogio UTC e data
2. zona do sistema e Lyapunov
3. ponto do presente e campo central
4. radar de fase
5. hexagrama
6. strips inferiores do painel
7. dock numerico horizontal
8. grande grafico do campo fractal

### 9.3 Como cruzar painel, radar, hexagrama e grafico

O painel mostra atmosfera e distribuicao. O radar mostra geometria relacional. O hexagrama mostra sintese simbolico-operacional. O grafico do campo mostra a historia do sinal em larga escala. A consulta so amadurece quando esses quatro planos conversam.

### 9.4 Como navegar entre passado, presente e futuro

Use os botoes rapidos para saltos largos e o slider para ajuste fino. Cada deslocamento altera o recorte, mas preserva a mesma logica do instrumento.

### 9.5 Como usar o explorador temporal

Observe o valor textual do explorador enquanto move o slider. Em seguida:

- veja quais atratores entram ou saem da janela
- note se o radar se adensa ou dispersa
- veja se o hexagrama se reconfigura
- desca ao grande grafico para comparar o recorte com o comportamento historico amplo

### 9.6 Como consultar os modulos inferiores

Os modulos inferiores pedem metodo. Nao clique tudo de uma vez. Escolha uma pergunta:

- o sistema esta coeso?
- a curvatura esta alta?
- ha clusters historicos?
- ha recorrencia harmonica?
- a previsao interna sobe ou cai?
- o modelo se sustenta quando validado?

Entao consulte o modulo correspondente.

### 9.7 Como usar a interface para observacao, comparacao e interpretacao

Use a Cronosfera em tres modos:

- **observacao:** leitura do presente e da atmosfera do campo
- **comparacao:** alternancia entre janelas temporais e modulos
- **interpretacao:** sintese disciplinada entre curvas, radar, hexagrama e secoes avancadas

## 10. Metodo de consulta

Segue um procedimento recomendado.

### Etapa 1 - Leitura do estado presente

Ler UTC, data, zona do sistema, Lyapunov e ponto central do presente.

### Etapa 2 - Leitura da curvatura

Observar `dF`, `d2F`, strips inferiores e mapa de convergencia.

### Etapa 3 - Leitura de fase

Consultar HUD Maya, fase e pulso, e o radar de fase.

### Etapa 4 - Leitura de ressonancia

Examinar o campo de ressonancia, o bloco de ondas e a teia harmonica.

### Etapa 5 - Leitura do radar

Verificar coesao, agrupamento e proximidade relativa dos atratores.

### Etapa 6 - Leitura do hexagrama

Consultar a sintese simbolico-operacional como complemento e nao como autoridade isolada.

### Etapa 7 - Leitura do grafico do campo

Descer ao grafico principal, localizar `AGORA`, `PICOS`, compressoes e regimes.

### Etapa 8 - Leitura cruzada com modulos inferiores

Usar `cluster`, `predictive`, `forecast`, `validation`, `confidence`, `lab`, `universe` ou `multiverse` conforme a pergunta.

### Etapa 9 - Sintese interpretativa final

Somente entao formular uma leitura. Ela deve ser comparativa, provisoria, justificada por mais de um modulo e consciente dos limites do sistema.

## 11. Limites, cuidados e epistemologia

Esta secao e essencial.

### 11.1 O que e software funcional

O projeto atual e um software funcional: desenha, atualiza, calcula, responde a controle temporal, aciona modulos e organiza varias visualizacoes e simulacoes.

### 11.2 O que e modelo interpretativo

Quando o sistema associa essas visualizacoes a leituras de regime, ressonancia ou convergencia historica, entra em campo um modelo interpretativo. Isso e mais do que interface, mas menos do que prova universal.

### 11.3 O que e hipotese experimental

Modulos como `validation`, `DNA`, `production`, `confidence`, `lab`, `universe` e `multiverse` combinam engenharia computacional real, simulacao coerente e hipoteses sobre como extrair sentido dessas estruturas. Por isso, devem ser tratados como laboratorios experimentais.

### 11.4 O que nao deve ser tratado como certeza empirica absoluta

Nao se deve transformar picos internos em decretos sobre o mundo, scores de validacao em verdade final, ensemble em garantia objetiva do futuro, ou simbolo em prova.

### 11.5 Postura epistemologica recomendada

Use a Cronosfera como instrumento de observacao, gerador de hipoteses, painel comparativo e apoio a leitura de regime. Nao a use como fonte unica de certeza, substituto de metodo historico ou mecanismo de promessas absolutas.

## 12. Glossario

**Atrator:** nodo ou evento de referencia capaz de organizar parte do campo.

**Autocorrelacao:** medida de semelhanca do sinal consigo mesmo em diferentes defasagens.

**Campo fractal:** representacao sintetica de um sinal historico em varias escalas.

**Cluster:** agrupamento local de alta convergencia ou alta tensao.

**Confidence:** camada de confianca interna, spread, ensemble e score.

**Convergencia:** encontro de derivada e curvatura em pontos de tensao.

**Curvatura:** segunda derivada ou medida equivalente de inflexao do campo.

**DNA:** metafora para a assinatura minimamente recorrente do modelo.

**Explorer temporal:** conjunto de controles para deslocar o recorte temporal do sistema.

**Fase:** posicao relativa dentro de um ciclo.

**Forecast:** distribuicao probabilistica futura baseada em recorrencias.

**Hexagrama:** sintese simbolico-operacional do estado dinamico do sistema.

**Historico sintetico:** sinal construido pelo modelo e nao serie cronica empirica pura.

**Kuramoto:** modelo de osciladores acoplados usado para medir sincronizacao.

**Lab:** laboratorio de cenarios, causalidade e experimento.

**Lorenz:** sistema classico de caos determinista usado como fonte de turbulencia e energia.

**Lyapunov / Lyap:** medida associada a estabilidade ou divergencia de trajetorias.

**Multiverse:** conjunto de universos simulados com regras mutantes e selecao natural interna.

**Pulso:** medida dinamica de intensidade de variacao ou excitacao do sistema.

**Predictive:** modulo de janelas futuras e bandas projetivas.

**Production:** consolidacao operacional do modelo em versao congelada.

**Radar de fase:** visualizacao polar de atratores, fase e dispersao.

**Ressonancia:** alinhamento ou eco estrutural entre componentes, eventos ou periodos.

**Sinal:** grandeza sintetica temporal cujo comportamento interessa mais que o valor absoluto isolado.

**Singularidade:** ponto de alta curvatura ou ruptura local.

**Time offset:** deslocamento da janela observada em relacao ao agora.

**Universe:** simulacao multiagente de estado emergente.

**Validation:** secao de testes, metricas e controles de consistencia.

## 13. Conclusao

A Cronosfera Fractal Maya Nao Linear deve ser compreendida como um instrumento hibrido. Ela nao e somente um painel bonito, nem somente uma maquina de metrica, nem somente uma fantasia simbolica. E uma interface de observacao que combina analise, visualizacao, simulacao, sintese e interpretacao disciplinada.

Seu valor maior reside em abrir uma arena onde o tempo pode ser visto como paisagem, como ritmo, como curvatura, como probabilidade, como memoria de atratores e, por fim, como campo de leitura.

Tomada com seriedade, a Cronosfera nao promete onisciencia: oferece um mapa dinamico. E esse mapa, precisamente por unir software funcional, visualizacao matematica, hipotese interpretativa e imaginacao conceitual sob prudencia metodologica, constitui uma plataforma aberta para aprofundamentos futuros.
