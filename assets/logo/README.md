# Logo

Monograma **NB** dentro de um anel, com a silhueta de uma gestante, um coração
e um ponto.

## Arquivos

| Arquivo | Uso |
|---|---|
| `logo.svg` | Versão principal, vetorial. É a usada no rodapé do site. |
| `logo-original-*.png` | Degradê rosé, a cor da marca. Para fundos claros ou escuros. |
| `logo-branco-*.png` | Branco. Para fundos escuros e fotos. |
| `logo-preto-*.png` | Preto. Para impressão monocromática e fundos claros. |
| `logo-marrom-*.png` | Marrom `#8c6a52`, o `--accent` do site. Para fundos claros. |

Todos os PNGs têm fundo transparente e são quadrados, em 512, 1024 e 2048px.
Use o maior tamanho que o destino aceitar. Para impressão ou ampliação, prefira
o SVG, que não perde nitidez em nenhum tamanho.

A logo só fica legível a partir de ~96px de largura. Abaixo disso, use o
monograma em texto do header.

## Cores

O degradê vai do canto superior esquerdo ao inferior direito:

| Posição | Cor |
|---|---|
| 0% | `#a27b67` |
| 45% | `#d4ae9b` |
| 70% | `#b48a75` |
| 100% | `#9c7663` |

## Origem

- **Letras N e B:** contornos da fonte [Gilda Display](https://fonts.google.com/specimen/Gilda+Display),
  sob a SIL Open Font License, que permite uso comercial e em logotipo.
  Tamanho e posição foram ajustados para reproduzir a composição da logo
  original.
- **Anel, silhueta, coração e ponto:** vetorizados de
  `assets/photos/logo.webp` (512px), a arte original. O arquivo saiu do
  repositório e pode ser recuperado no histórico do git (commit `fd62a52`).

A vetorização reconstruiu cada traço fino pelo seu eixo central, com a
espessura medida pela tinta do original. Isso tira o tremor de pixel sem
perder o afinamento das pontas.

O arquivo original de quem desenhou a logo (`.ai`, `.pdf` ou `.svg`) segue
sendo a melhor fonte para peças grandes, como fachada e papelaria. Se ele
aparecer, deve substituir a parte vetorizada.

## Gerar outra cor

No `logo.svg`, troque `url(#rose)` e `url(#rose-tracos)` pela cor desejada.
São dois degradês com as mesmas cores, um para as letras e outro para os
traços, porque cada grupo tem o próprio sistema de coordenadas.
