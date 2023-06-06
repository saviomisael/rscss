# Layouts

![](images/layouts.png)

## Evite propriedades de posicionamento
Componentes devem ser criados de forma que eles possam ser reutilizados em diferentes contextos. Evite colocar essas propriedades em componentes:

  * Posicionamento (`position`, `top`, `left`, `right`, `bottom`)
  * Floats (`float`, `clear`)
  * Margens (`margin`)
  * Dimensões (`width`, `height`) *

## Dimensões fixas

Podem acontecer exceções em elementos que tem a largura ou altura fixas, como avatares e logos.

## Defina posicionamento no pai

Se você precisa definir essas propriedades, tente defini-las no contexto em que elas estão. No exemplo a seguir, perceba que a largura e o float são aplicados no componente *list*, não no componente em si.

  ```css
  .article-list {
    & {
      @include clearfix;
    }

    > .article-card {
      width: 33.3%;
      float: left;
    }
  }

  .article-card {
    & { /* ... */ }
    > .image { /* ... */ }
    > .title { /* ... */ }
    > .category { /* ... */ }
  }
  ```

Como aplicar margens fora do layout? Tente isso com Helpers.
[Continuar →](helpers.md)
<!-- {p:.pull-box} -->
