# Componentes aninhados

![](images/component-nesting.png)

```html
<div class='article-link'>
  <div class='vote-box'>
    ...
  </div>
  <h3 class='title'>...</h3>
  <p class='meta'>...</p>
</div>
```

Algumas vezes é necessário aninhar componentes. Aqui estão algumas recomendações para fazer isso.

## Variantes
Um componente precisa ter um estilo específico quando aninhado a outro componente. Evite modificar o componente aninhado através do componente pai.

```scss
.article-header {
  > .vote-box > .up { /* ✗ evite isso */ }
}
```

  Ao invés de utilizar da forma acima, prefira adicionar uma variante para o componente aninhado e aplique a variante dentro do componente pai.

```html
<div class='article-header'>
  <div class='vote-box -highlight'>
    ...
  </div>
  ...
</div>
```

```scss
.vote-box {
  &.-highlight > .up { /* ... */ }
}
```

## Simplificando componentes aninhados
Ao utilizar componentes aninhados, você pode causar uma marcação suja:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='search-button -red -large'></button>
</div>
```

Você pode simplificar isso usando um pré processador CSS e o mecanismo de `@extend`:

```html
<div class='search-form'>
  <input class='input' type='text'>
  <button class='submit'></button>
</div>
```

```scss
.search-form {
  > .submit {
    @extend .search-button;
    @extend .search-button.-red;
    @extend .search-button.-large;
  }
}
```

E sobre repetir elementos como listas? Aprenda sobre Layouts.
[Continuar →](layouts.md)
<!-- {p:.pull-box} -->
