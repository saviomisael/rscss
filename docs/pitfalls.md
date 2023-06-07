# Erros

## Elementos com o mesmo nome em componentes aninhados
Tome cuidado com elementos de componentes aninhados terem o mesmo nome que elementos do componente pai.

```html
<article class='article-link'>
 <div class='vote-box'>
    <button class='up'></button>
    <button class='down'></button>
    <span class='count'>4</span>
  </div>

  <h3 class='title'>Article title</h3>
  <p class='count'>3 votes</p>
</article>
```

```scss
.article-link {
  > .title { /* ... */ }
  > .count { /* ... (!!!) */ }
}

.vote-box {
  > .up { /* ... */ }
  > .down { /* ... */ }
  > .count { /* ... */ }
}
```

Nesse caso, se `.article-link > .count` não usasse o seletor de filho `>`, ele também teria aplicado os estilos para o elemento `.vote-box .count`. Isso é uma das razões pela qual é preferível usar o seletor de filho.
