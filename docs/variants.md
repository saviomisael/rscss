# Variantes

Componentes podem ter variantes. Elementos também podem ter variantes.

![](images/component-modifiers.png)

<br>

## Nomeando variantes
Classes para variantes devem ser prefixadas com um traço (`-`).

  ```scss
  .like-button {
    &.-wide { /* ... */ }
    &.-short { /* ... */ }
    &.-disabled { /* ... */ }
  }
  ```

## Variantes de elementos
Elementos também podem ter variantes.

  ```scss
  .shopping-card {
    > .title { /* ... */ }
    > .title.-small { /* ... */ }
  }
  ```

## Prefixos com traços
Porque usar o traço como prefixo:

  * Ele previne ambiguidade com elementos.
  * Uma classe CSS pode somente começar com uma letra, `_` ou `-`.
  * Um traço é mais fácil de escrever do que o underscore.
  * Ele se parece com flags de comandos UNIX (`gcc -O2 -Wall -emit-last`).

Como você lida com elementos complexos? Aninha-os.
[Continuar →](nested-components.md)
<!-- {p:.pull-box} -->
