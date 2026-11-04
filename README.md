# Pelada Royale

Um roguelike de baralho com tema de futebol brasileiro, inspirado no Balatro.
Monte escalações em vez de mãos de pôquer, bata a meta de pontos e ganhe o
campeonato.

**Jogar agora:** https://SEU-USUARIO.github.io/pelada-royale/
*(troque `SEU-USUARIO` depois de ativar o GitHub Pages)*

## Como jogar

Você recebe 8 jogadores na mão e escala até 5 por vez. Cada escalação vale:

```
pontos = (jogo + overalls que pontuam) × moral
```

Bateu a meta do adversário, venceu o jogo. Acabaram as escalações antes disso,
você é rebaixado. São 3 jogos por campeonato, e as metas sobem a cada um.

Cada carta é um jogador com uma **posição** (que faz o papel do naipe) e um
**overall de 1 a 13** (que faz o papel do valor da carta):

| Símbolo | Posição |
|---|---|
| ✛ | Goleiro |
| ◆ | Defesa |
| ● | Meio |
| ▲ | Ataque |

As combinações funcionam como mãos de pôquer, com nome de futebol: *Dupla de
área* (par), *Triangulação* (trinca), *Jogada ensaiada* (quadra). E uma que só
existe aqui: escalar as **4 posições ao mesmo tempo** forma o *Time armado* —
no pôquer ter os 4 naipes não vale nada, aqui vale.

O terceiro jogo de cada campeonato é o clássico, e vem com uma regra chata
sorteada: chuva, gramado ruim, juiz ladrão ou torcida adversária.

Ao fim de cada campeonato abre o **mercado da bola**, onde você contrata
técnicos (os coringas) e melhorias permanentes.

## Rodar na sua máquina

Baixe o `index.html` e dê dois cliques. Não tem build, não tem dependência,
não precisa instalar nada.

O jogo funciona **offline**. A única exceção são as fotos de alguns jogadores,
que vêm do Wikimedia Commons; sem internet, essas cartas caem sozinhas num
retrato desenhado em SVG e o jogo segue igual.

## Mexer no jogo

Tudo fica no começo do `<script>`, dentro do `index.html`:

| Constante | O que controla |
|---|---|
| `BARALHO` | os 52 jogadores (nome, posição, overall, clube, foto) |
| `COMBINACOES` | nomes, `jogo` (base) e `moral` (multiplicador) |
| `RODADAS_DO_ANTE` | as metas dos 3 jogos |
| `CRESCIMENTO_ANTE` | quanto as metas sobem por campeonato |
| `TECNICOS` | os coringas e seus efeitos |
| `MELHORIAS` | os itens permanentes da loja |

Para dar foto a um jogador, procure a imagem no
[Wikimedia Commons](https://commons.wikimedia.org), copie o título do arquivo
depois de `File:` e acrescente na linha dele:

```js
{ nome: "Pedro", pos: "ATA", ovr: 13, clube: "Flamengo",
  foto: fotoCommons("Nome Do Arquivo.jpg") },
```

## Aviso sobre direito de imagem

As cartas usam **nomes e fotos de jogadores reais**. Para projeto pessoal e de
estudo, sem problema. Para uso comercial, nome e imagem de atleta exigem
licença — nesse caso, troque por jogadores fictícios. As fotos vêm do Wikimedia
Commons e cada uma tem a sua própria licença, que precisa ser creditada se o
projeto for além do uso pessoal. Os técnicos já são arquétipos inventados.

Este é um projeto de estudo, sem vínculo com os clubes citados nem com o
Balatro ou a LocalThunk.
