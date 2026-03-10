# Exercício 04 - Mousemove

Uma página web possui um quadrado:
```html 
<div id="square">
    <p>X: <span id="pos-x">0</span></p>
    <p>Y: <span id="pos-y">0</span></p>
</div>
```
Dentro do quadrado são apresentadas as coordenadas X e Y da posição do canto superior esquerdo do quadrado em relação à página:
- Ao clicar sobre o quadrado e manter o botão do mouse pressionado, o usuário pode arrastar o quadrado pela página;
- Ao soltar o botão do mouse, o quadrado para de ser arrastado;
- Enquanto é arrastado, o canto superior esquerdo do quadrado deve seguir o cursor do mouse e as coordenadas X e Y de sua posição devem ser atualizadas.

**1 -** Prepare os arquivos:
- Crie um arquivo chamado `index.html` com os elementos indicados acima, no corpo da página;
- Crie um arquivo chamado `script.js`;
- No arquivo HTML, adicione uma tag `<script>` dentro do elemento `<head>`, para carregar o arquivo `script.js`. Garanta que o script seja executado apenas após o carregamento do documento;
- Crie um arquivo chamado `styles.css` 
- No arquivo HTML, adicione uma tag `<link>` dentro do elemento `<head>` para carregar o arquivo de estilos `styles.css`.

**2 -** Prepare o CSS:
- No arquivo `styles.css`, adicione o seguinte código:
```css
#square {
    /* define o tamanho e a cor do quadrado */
    width: 100px;
    height: 100px;
    background-color: red;
    /* define a posição */
    position: absolute; 
    top: 0px;
    left: 0px;    
    /* define cor, estilo e alinhamento do texto interno */
    color: white;
    font-weight: bold;
    display: flex;
    flex-direction: column;
    align-items: center;  
    /* define o cursor do mouse */
    cursor: grab;
}

p span {
    /* ignora os eventos do mouse para o texto interno 
       isso permite que o quadrado seja arrastado mesmo 
       quando o mouse estiver sobre o texto */
    pointer-events: none; 
}
```

**3 -** Primeiros passos:
- Crie uma variável `isDragging` para controlar se o quadrado está ou não sendo arrastado:
	- quando o usuário pressiona o botão do mouse **sobre o quadrado**, a variável recebe `true`;
	- quando o usuário solta o botão do mouse, **mesmo que fora do quadrado**, a variável recebe `false`, pois nada mais está sendo arrastado;
- Assim, implemente os eventos de `mousedown` e `mouseup` para atualizar a variável de controle.
- Escolha adequadamente os elementos em que os eventos serão observados!

**4 -** Implemente o evento de `mousemove`:
- Quando o mouse se move e **apenas se o quadrado estiver sendo arrastado**:
	- atualize o texto das coordenadas X e Y com a posição atual do mouse;
	- altere a posição do quadrado para a posição atual do mouse.
- Caso o quadrado não esteja sendo arrastado, nada deve acontecer!

**Dicas:** 
- Use a propriedade `event.clientX` e `event.clientY` para obter a posição do mouse;
- Utilize as propriedades `style.left` e `style.top` para definir a nova posição do quadrado;
