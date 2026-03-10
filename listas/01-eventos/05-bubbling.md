# Exercício 05 - Bubbling

Uma página web possui os seguintes elementos HTML:
```html 
<h1>Menu de Pizzas</h1>
<ul id="pizzas">
    <li>Margherita</li>
    <li>Pepperoni</li>
    <li>Quatro Queijos</li>
    <li>Frango com Catupiry</li>
    <li>Portuguesa</li>
    <li>Calabresa</li>
    <li>Brócolis</li>
    <li>Bacon e Milho</li>
    <li>Atum</li>
    <li>Stroganoff</li>
    <li>Burrata e Parma</li>
    <li>Rúcula e Tomate Seco</li>
</ul>
```
Trata-se do menu de sabores de uma pizzaria.
- Um clique duplo sobre um item da lista, o seleciona, mudando sua cor para verde e emitindo um alerta no seguinte formato:
```
Você selecionou o sabor Calabresa!
```
- Um clique duplo sobre um item já selecionado, o remove, mudando sua cor de volta para preto e emitindo um alerta no seguinte formato:
```
Você removeu o sabor Calabresa!
```

**1 -** Prepare os arquivos:
- Crie um arquivo chamado `index.html` com os elementos indicados acima, no corpo da página;
- Crie um arquivo chamado `script.js`;
- No arquivo HTML, adicione uma tag `<script>` dentro do elemento `<head>`, para carregar o arquivo `script.js`. Garanta que o script seja executado apenas após o carregamento do documento;

**2 -** Estilize a lista através do JavaScript:
- adicione os seguintes estilos à lista `<ul>` usando a propriedade `style`:
```css
{
    list-style: none;
    line-height: 30px;
    font-size: 20px;
    cursor: pointer;
    user-select: none;
}
```

**3 -** Implemente o evento de `dblclick` para controlar a seleção de sabores.
- Use apenas um `addEventListener` no elemento `ul`;
- Verifique se o elemento que disparou o evento é um item de lista (`tagName === 'LI'`);
- Como ainda não aprendemos a usar a propriedade `classList`, você pode controlar a seleção diretamente pela propriedade (`style.color === 'green'`); 


