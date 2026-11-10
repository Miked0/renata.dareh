# BRIEF.md · Renata Dareh Clinic (v2, redesign)

**Modo:** Self-authored under explicit creative delegation. Mike pediu: "O trabalho da cliente é estética, então quero algo fino, elegante e nos tons que ela tem como marca. Deixe-o com elegância e com uma UI assustadoramente boa." Ele mandou prints do Google Maps e do Instagram (@renatadareh.clinic). Tudo abaixo que não está entre aspas é decisão autoral.

O pré-build anterior (feito com outro agente) está guardado em `_prebuild-hermes/`. Ele usava azul-marinho e teal, chamava a cliente de "Dra." (o Google a lista como esteticista) e tinha o motor modificado. Esta versão parte do zero.

## Evidência da marca (do material enviado)
- Instagram verificado: "Renata Dareh | Remoção de Tatuagens e Micro". Bio: "SUA SOBRANCELHA MERECE UMA NOVA HISTÓRIA", "Remoção a Laser & Nanoblading", "Naturalidade, precisão e sofisticação". Site atual: www.renatadareh.com.br.
- Destaques: Tatuagem, Bastidores, Laranja, CO2 Fracionado, Depoimentos, Reparação, Pelo branco.
- Identidade visual dos posts: vinho/bordô profundo, marfim e branco, serifa de alto contraste (Didone), monograma "R", cartões impressos (curso "Dareh Remuve, em breve").
- Google: Clinica Renata Dareh, Especialista em Remoção de Pigmento, 5,0 (11 avaliações), R. Frei Caneca, 1212, Conj 87, Consolação, SP, 01307-002, (11) 93039-7521.
- Sem fotos próprias em alta resolução, sem retrato, sem antes/depois reais. As imagens são as geradas no pré-build (marcadas "Imagem ilustrativa").

## As oito perguntas (autoral)
1. **Vibe:** fina, editorial, clínica sem frieza, confiante, discreta. Referências: o próprio feed dela, revista de moda impressa, papelaria de ateliê.
2. **Jornada:** folha de rosto, reconhecimento (o pigmento que ficou), a virada (como a remoção funciona, sessão a sessão), o que ela trata, quem conduz, agendar.
3. **Energia:** calma na abertura, firme no reconhecimento, o ponto mais vivo no capítulo II (a interação), calma de novo até o colofão.
4. **Sentimento e momento:** ver o pigmento sumir sob o próprio dedo.
5. **O que nenhum site faz:** deixar a visitante "disparar o laser" e ver a pele limpar onde tocou.
6. **Distância do premium-minimal:** editorial de luxo, não minimal escuro.
7. **Mundo contínuo ou cenas:** capítulos com cortes secos.
8. **Assets:** nenhum próprio; uso das imagens ilustrativas existentes, recompostas.

## Gramática: Chaptered editorial
A marca já fala como um impresso (serifa, cartões, vinho e marfim), e o conteúdo é substância (método, serviços, autoridade). Por que as outras perderam:
- Filmic one-shot: é o que o pré-build usou e o registro já tem; sem vídeo real, viraria fundo genérico.
- Live surface: não há produto de software.
- Continuous world: não há geografia.
- Typographic poster: a cliente precisa mostrar serviços e endereço, não só uma frase.
- Gallery/catalog: cinco serviços não formam uma coleção visual, e não há fotos.
- Split stage e rhythmic cutlist: a calma é parte da marca; cortes rítmicos brigam com "sofisticação".

## Assinatura
**O laser.** No capítulo II a visitante toca a sobrancelha e cada toque dispara um pulso que limpa a pele naquele ponto; a limpeza fica. "Avançar uma sessão" faz uma passada inteira com força parcial (cerca de 42, 71, 91 e 100% em quatro sessões), para mostrar que o resultado é gradual. As duas imagens são alinhadas pixel a pixel: `laser-clean.webp` foi derivada de `laser-src.webp` trocando a baixa frequência e a cor do preenchimento pela pele e mantendo os fios. JS próprio da página; o motor não foi tocado.

## Curva de sentimento
- Folha de rosto: promessa calma ("nova história"), tipo grande sobre papel.
- I. O pigmento que ficou: reconhecimento, um pouco de desconforto (sinais nomeados, foto do pigmento azulado).
- II. Sessão a sessão: alívio e controle, a visitante faz o pigmento sumir. **Pico.**
- III. O que tratamos: escolha, um índice que leva direto ao WhatsApp com a mensagem certa.
- IV. Quem conduz: confiança (a frase dela, nota do Google, onde fica).
- Colofão: resolução, um pedido simples e a assinatura da clínica.

**O pico**, na voz de quem conta: "é o site em que você toca a sobrancelha e vê o pigmento sair."
**Tell-someone:** "É o site onde você mesma tira o pigmento da sobrancelha com a ponta do dedo."

## Partitura
| Capítulo | Dispositivo | Por quê |
|---|---|---|
| Folha de rosto | tipo + parallax do monograma | título de revista, sem mídia acima da dobra |
| I | reveal no intertítulo, flow + in, parallax na coluna de mídia | virar a página, depois um spread denso |
| II | reveal, flow + in, assinatura (canvas + pointer) | o pico precisa de mãos, não de rolagem |
| III | reveal, flow + in, parallax na mídia, índice com hover | escolha, cada linha é uma ação útil |
| IV | flow + in | leitura e fatos, sem efeito competindo |
| Colofão | flow + in | o pedido como texto corrido, a página assina |

Sem drift: cada capítulo tem chão opaco e corte seco (marfim, vinho, marfim, vinho profundo, marfim, vinho noturno).

## Silêncio autoral
A folha de rosto não tem mídia de propósito (regra da gramática). Os intertítulos são pausas de leitura, não rolagem morta.

## Feel check
Rolagem a frio, uma palavra por capítulo: promessa, reconhecimento, alívio, escolha, confiança, decisão. Bate com a curva. O pico (II) é a maior mudança visual da página e o único lugar que pede as mãos.

## Verificação
- Capturas próprias com Edge headless (Playwright) em 1440x900, 390x844 com toque, e movimento reduzido: `lab/v2/`. Sem erros de console, sem rolagem horizontal.
- O laser funciona com mouse, toque e botões; com movimento reduzido os pulsos não animam e a limpeza é instantânea.
- Não verificado: o harness `shoot.mjs` da skill (a execução de scripts do repositório foi bloqueada nesta máquina), contraste medido por linha, e iPhone real.

## Pendências com a cliente
- Retrato da Renata e fotos reais (consultório, procedimentos). Antes/depois reais só com autorização das pacientes.
- Confirmar horários de atendimento (o Google mostrava "abre qua. às 09:00").
- Confirmar se "Laser CO2 fracionado" e "Remoção de tatuagem" seguem como serviços ativos, e a data do curso Dareh Remuve.
- Textos de depoimentos reais do Google, se ela quiser exibir.

## Vidro canelado (pedido do Mike, 2026-11-10)
"Agora você vai aplicar o estilo de design vidro canelado no site." Componente `.flute`: backdrop blur, relevo de frisos verticais (crista clara, vale escuro, blend soft-light) e reflexo especular que segue o ponteiro com inércia (parado em toque e em movimento reduzido). Aplicado como peça específica, não decoração solta:
- Folha de rosto: painel de vidro entre o monograma "R" (atrás) e o título (na frente). A perna do R fica nítida fora do vidro e o bojo fica canelado dentro; uma luz vinho atrás dá o que refratar.
- Fotos dos capítulos I e III: uma faixa da foto atrás do vidro, como divisória de consultório.
- Cartão do curso Dareh Remuve: vidro vinho canelado.
- Colofão: o R volta atrás de vidro escuro.
- O laser (pico) fica sem vidro, para não competir.
Capturas em `lab/v3/`.

## Tipografia (pedido do Mike, 2026-11-10)
"Use como padrão CINZEL & Vicenza as fontes." Vicenza nos títulos (caixa alta condensada), Cinzel em marca, fólio, rótulos, subtítulos, índice e CTAs. Geist continua no texto corrido, porque nenhuma das duas sustenta parágrafos. Nenhuma tem itálico, então a ênfase virou cor (vinho/rosado). Entrelinha dos títulos em 0.96 para os acentos em caixa alta não baterem na linha de cima.
Vicenza é comercial e não está no Google Fonts nem instalada nesta máquina: o `@font-face` procura `assets/fonts/Vicenza.woff2` ou `.otf` (e a fonte instalada localmente). Sem o arquivo, entra a Instrument Serif (fallback condensado do Google Fonts), e o console mostra 404 desses dois arquivos. Capturas em `lab/v4/`.

## Retoques finais (pedido do Mike, 2026-11-10)
"Traga vida para este site, o fundo está muito chapado. Não sei se o vidro tirando o foco do logo R ficou bacana."
- O R saiu de trás do vidro: agora fica na frente, nítido, em vinho cheio, com sombra própria sobre o painel. O vidro virou o fundo dele e passou a refratar três luzes que derivam devagar (presas ao retângulo do vidro).
- Fundos: cada seção ganhou duas camadas de luz macia que derivam em sentidos opostos (26 a 34 s). No papel, luz quente de janela e véu rosado; no vinho, um foco mais claro e um canto em sombra, mais uma luz que acompanha o ponteiro com inércia. Grão um pouco mais forte.
- Colofão: R no terço direito do vidro, longe do pedido de agendamento. No celular o vidro vira uma faixa no topo com o R dentro.
- Movimento reduzido: as luzes ficam paradas. Capturas em `lab/v5/`.

## Foto desfocada (mudança do Mike, 2026-11-10)
Mike trocou o vidro canelado pelo estilo "foto desfocada" direto no `index.html`. Completei:
- Fundos são fotos de verdade já desfocadas no arquivo (`assets/blur-*.webp`, 480px, ~2 KB): tons quentes de pele no papel (multiply), luz de pele sobre o vinho (screen). Máscara mantém limpa a área do texto. Cada capítulo recebe uma no topo.
- Bokeh: discos de luz fora de foco atrás do R na folha de rosto e no colofão, com deriva lenta. O R é o único elemento em foco.
- Removidos os restos do vidro (CSS `.flute`, luzes recortadas no retângulo antigo).
- Cópia do arquivo antes desta etapa: `lab/index.before-foto-desfocada-finish.html`. Capturas em `lab/v6/`.
