# Exercício 03 - Keydown

Uma página web possui uma imagem de uma espaçonave:
```html 
<img src="hope1.png" alt="Spaceship" id="spaceship">
```
A nave **Hope 1** está viajando pelo espaço e o usuário pode controlá-la:
- as teclas `a` e `d` deslocam a nave na horizontal;
- as teclas `w` e `s` deslocam a nave na vertical; 
- a tecla `Esc` leva a nave de volta à posição inicial no centro da tela.

**1 -** Prepare os arquivos:
- Crie um arquivo chamado `index.html` com o elemento indicado acima, no corpo da página;
- Crie um arquivo chamado `script.js`;
- No arquivo HTML, adicione uma tag `<script>` dentro do elemento `<head>`, para carregar o arquivo `script.js`. Garanta que o script seja executado apenas após o carregamento do documento;
- Crie um arquivo chamado `styles.css` 
- No arquivo HTML, adicione uma tag `<link>` dentro do elemento `<head>` para carregar o arquivo de estilos `styles.css`.
- Copie o arquivo `hope1.png` para a pasta onde estão os demais arquivos do projeto;

**2 -** Prepare o CSS:
- No arquivo `styles.css`, adicione o seguinte código:
```css
body {
	/* ocupa toda a altura da janela do navegador */
    min-height: 100vh; 
	/* remove a margem padrão do body */
    margin: 0; 
	/* cor de fundo preta para simular o espaço sideral */
	background-color: black; 
}

img {
	/* posicionamento absoluto para permitir o movimento da nave */
	position: absolute; 
	/* ajusta a posição para que o centro da imagem seja o ponto de referência */
	transform: translate(-50%, -50%); 
	/* adiciona uma transição suave para o movimento da nave */
	transition: 0.5s ease;
	/* define o tamanho da nave */
	width: 84px;	
	height: 112px;
}
```
**3 -** Prepare o script JS:
- No arquivo `script.js`, adicione o seguinte trecho de código:
```javascript
// as variáveis posX e posY armazenam a posição atual da nave
// - posX representa a posição horizontal (esquerda-direita) 
// - posY representa a posição vertical (cima-baixo)
// a nave começa no centro da janela do navegador
let posX = window.innerWidth / 2;
let posY = window.innerHeight / 2;

// seleciona a imagem da nave e define sua posição inicial
const spaceship = document.querySelector('#spaceship');
spaceship.style.left = posX + 'px';
spaceship.style.top = posY + 'px';

// define a velocidade de movimento da nave
// quantos pixels a nave deve se mover a cada deslocamento
const speed = 20;
```

**4 -** Implemente o evento de `keydown` no elemento `body`:
- se o usuário pressionar a tecla `a`, desloque a nave para a esquerda;
- se o usuário pressionar a tecla `d`, desloque a nave para a direita;
- se o usuário pressionar a tecla `w`, desloque a nave para cima;
- se o usuário pressionar a tecla `s`, desloque a nave para baixo;
- se o usuário pressionar a tecla `Esc`, reposicione a nave no centro da tela;
- a cada movimento, a nave deve se deslocar a quantidade de pixels indicada na variável `speed`.

**Dicas:** 
- Como no CSS definimos a propriedade `position: absolute`, para alterar a posição da nave, definimos as distâncias, em pixels, da borda esquerda (`left`) e da borda superior (`top`) da página. Para isso:
	- atualize as variáveis `posX` e `posY` com a nova posição da nave;
		- se a nave vai para a esquerda: `posX -= speed;`
		- se a nave vai para a direita: `posX += speed;`
		- se a nave vai para cima: `posY -= speed;`
		- se a nave vai para baixo: `posY += speed;`
	- altere as propriedades `left` e `top` do elemento que representa a nave:
	```js
 	spaceship.style.left = posX + 'px';
 	spaceship.style.top = posY + 'px';
 	```
	- lembre que você está definindo um estilo CSS, por isso o `'px'` concatenado!
- use a propriedade `event.key` para identificar qual tecla foi pressionada;
- utilize as propriedades `style.left` e `style.top` para definir a nova posição da nave após cada movimento;
- para verificar se usuário pressionou a tecla `Esc`, veja se `event.key === 'Escape'`.


**5 -** Altere o código para garantir que o movimento seja realizado tanto com letras maiúsculas ou minúsculas.

**6 -** Altere o código de modo que as setas do teclado também controlem a nave.
***Dica:** use `'ArrowRight'`, `'ArrowLeft'`, `'ArrowUp'`, `'ArrowDown'`. 
 
