# Outros recursos

 * [ITCSS](https://speakerdeck.com/dafed/managing-css-projects-with-itcss#49) ("Inverted Triangle CSS") é um ótimo complemento para a estrutura do rscss.
 * [rsjs](http://ricostacruz.com/rsjs/) ("Reasonable Standard of JavaScript Structure") é um documento em progresso para estruturar JavaScript em sites básicos.

Outras soluções
---------------

### BEM
[BEM] é ótimo, mas algumas pessoas podem achá-lo irritante pela sua sintaxe não convencional. RSCSS é bem parecido com BEM, porém com uma sintaxe diferente.

```html
<!-- BEM -->
<form class='site-search site-search--full'>
  <input  class='site-search__field' type='text'>
  <button class='site-search__button'></button>
</form>
```

```html
<!-- rscss -->
<form class='site-search -full'>
  <input  class='field' type='text'>
  <button class='button'></button>
</form>
```

## Terminologias

Os mesmos conceitos existem em formas parecidas de estruturar o CSS.

| RSCSS     | BEM      | SMACSS        |
| ---       | ---      | ---           |
| Componente | Bloco    | Módulo        |
| Elemento   | Elemento  | Sub-Componente |
| Layout    | ?        | Layout        |
| Variante   | Modificador | Sub-Módulo & Estado |

[BEM]: http://bem.info/
[Smacss]: https://smacss.com/
