# Box Model

Box Model é um conceito fundamental do `CSS` que define como os elementos são orgnizados e ocupam espaços na página.
Cada elemento é representado como uma caixa retangular, comporta por quatro camadas:

- **Content** (Conteúdo): A área onde o texto ou outros elementos são exibidos.
- **Padding** (Preenchimento): Espaço entre o conteúdo e a borda do elemento.
- **Border** (Borda): A borda ao redor do padding e do conteúdo
- **Margin** (Margem): Espaço externo entre o elemento e outros elementos ao redor.

O tamanho total do elemento é calculado somando `content` + `padding` + `border` + `margin`. Para facilitar o controle
pode-se usar `box-sizing: boder-box`, que faz o `width` e o `height` incluírem `padding` e `border`.

# Colapso de margens (margin collapse)

O colapso de margens acontece quando duas margens verticais de elementos se encontram. Em vez de somar os valores,
apenas a maior delas é aplicada.

## Quando isso acontece?

Entre elementos empilhados: Se um elemento tem `margin-bottom: 30px` e o próximo tem `margin-top: 40px`, a distância
entre eles será `40px`, não `70px`.

Em elementos vazios sem borda ou padding: Se uma `<div>` não tem conteúdo, borda ou `padding`, sua `margin-top` e
`margin-bottom` podem colapsar.

Em elementos pai e filho: Se um elemento filho tem `margin-top`, essa margem pode se fundir com a do elemento pai,
empurrando-o também.

## Quando as margens NÃO colapsam?

Se houver `padding`, borda ou conteúdo entre as margens. - Se forem margens laterais (essas sempre se somam).

O colapso evita espaços exagerados e ajuda no fluxo natural dos elementos!
