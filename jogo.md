# contexto

Jogo inspirado no Balatro, com tema de futebol brasileiro. Roguelike de baralho:
em vez de mãos de pôquer, você monta escalações.

## O que é

Cada rodada é um jogo contra um adversário com uma pontuação mínima a bater.
Mão de 8 jogadores, escale até 5, 4 escalações e 3 descartes. Três jogos por
campeonato — o terceiro é o clássico, e vem com uma regra chata.

## A tradução do Balatro

- Carta -> jogador. Naipe -> posição (GOL/DEF/MEI/ATA). Valor -> overall (1 a 13).
- Mão de pôquer -> escalação. Chips x Mult -> jogo x moral.
- Blind -> adversário. Boss blind -> clássico. Ante -> campeonato.
- Joker -> técnico. Loja -> mercado da bola.

## A identidade do jogo

No pôquer, ter os 4 naipes na mão não vale nada. Aqui, escalar as 4 posições
vale ("Time armado"). **A posição tem que importar de um jeito que naipe não
importa** — é isso que separa o jogo de ser Balatro com skin de futebol.

## Regras do projeto

- Gratuito e fácil: sem API paga, sem cadastro, sem npm, sem CDN.
- Roda em `file://` com duplo clique, então sem `fetch` e sem `import`.
- Tudo em português: interface, variáveis e comentários.
- Jogadores reais no baralho (risco de direito de imagem se publicar).
  Técnicos são arquétipos inventados.

## Adendo — fotos dos jogadores

As cartas aceitam foto por URL no campo `foto` de cada jogador. Quando o campo
está vazio, ou a imagem não carrega, a carta cai no retrato desenhado em SVG,
que é gerado a partir do nome. Consequências assumidas:

- O jogo **deixa de ser 100% offline** nas cartas com foto (o resto continua).
- URL de terceiro quebra com o tempo; o retrato SVG é a rede de segurança.
- Foto de atleta real é o caso mais claro de direito de imagem. Para uso
  pessoal, sem problema. Para publicar, trocar por jogadores fictícios.

## O que falta

Balancear a curva (`CRESCIMENTO_ANTE`), mais regras de clássico, consumíveis,
e escolher clube no início (cada um com um viés de baralho).
