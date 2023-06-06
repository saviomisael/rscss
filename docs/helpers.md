# Helpers

De modo geral, essas classes significam sobrescrita de valores, coloque-as em um arquivo separado e o nome da classe inicia com underscore. Elas tipicamente usam *!important*. Use esse tipo de classe de maneira *bem* cuidadosa.

```css
._unmargin { margin: 0 !important; }
._center { text-align: center !important; }
._pull-left { float: left !important; }
._pull-right { float: right !important; }
```

## Nomeando helpers
Classes devem ter o underscore prefixado. Isso irá facilitar para diferenciá-las dos modificadores definidos nos componentes. Underscores podem parecer feios, mas essa é a intenção e o uso de helpers em excesso deve ser desencorajado.

  ```html
  <div class='order-graphs -slim _unmargin'>
  </div>
  ```

## Organizando helpers
Coloque todos os helpers em um arquivo chamado `helpers`. Enquanto você pode separá-los em vários arquivos, é preferível que você mantenha o número de helpers o menor possível.
