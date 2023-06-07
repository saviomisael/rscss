# Estrutura do CSS

## Um componente por arquivo
Para cada componente coloque-o em seu próprio arquivo.

  ```scss
  /* css/components/search-form.scss */
  .search-form {
    > .button { /* ... */ }
    > .field { /* ... */ }
    > .label { /* ... */ }

    // variants
    &.-small { /* ... */ }
    &.-wide { /* ... */ }
  }
  ```

## Use expressões regulares
No sass-rails e stylus é fácil importar todos os arquivos de uma vez:

  ```scss
  @import 'components/*';
  ```

## Evite aninhar componentes em componentes aninhados
Aninhe componentes em 1 nível de profundidade no máximo. É fácil se perder com componentes aninhados dentro de outros componentes aninhados.

  ```scss
  /* ✗ Evite: 3 níveis de profundidade */
  .image-frame {
    > .description {
      /* ... */

      > .icon {
        /* ... */
      }
    }
  }

  /* ✓ Melhor: 2 níveis de profundidade */
  .image-frame {
    > .description { /* ... */ }
    > .description > .icon { /* ... */ }
  }
  ```
