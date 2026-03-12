# Exercício 06 - Default

Uma página web possui os seguintes elementos HTML:
```html 
<h2>Manipulação de Eventos</h2>
<p>
    Quando um evento ocorre em uma página web, o navegador cria 
    automaticamente um objeto com informações sobre esse evento. 
    Esse objeto é geralmente chamado de event (ou simplesmente e) 
    e passado automaticamente como parâmetro para o manipulador do evento. 
    Para acessá-lo, precisamos explicitar o parâmetro na função que trata o evento. 
</p>
```
E uma página informativa que traz um pequeno texto sobre eventos no JavaScript.
Porém, será necessário desativar o menu contextual quando o usuário clica com o botão direito e impedir que o conteúdo da página seja copiado.

**1 -** Prepare os arquivos:
- Crie um arquivo chamado `index.html` com os elementos indicados acima, no corpo da página;
- Crie um arquivo chamado `script.js`;
- No arquivo HTML, adicione uma tag `<script>` dentro do elemento `<head>`, para carregar o arquivo `script.js`. Garanta que o script seja executado apenas após o carregamento do documento;

**2 -** Implemente o evento de `contextmenu` no objeto `document`.
- Cancele o comportamento padrão através do método `preventDefault()`;
- Emita uma alerta com a seguinte mensagem:
```
O clique com o botão direito do mouse foi desativado.
```

**3 -** Implemente o evento de `copy` no objeto `document`.
- Cancele o comportamento padrão através do método `preventDefault()`;
- Defina o conteúdo que será copiado para a área de transferência como sendo o seguinte texto:
```
Este conteúdo não pode ser copiado.
```
- Para isso, utilize o seguinte comando, onde `message` contém o texto a ser copiado:
```javascript
event.clipboardData.setData("text/plain", message);
```
**Dica:** para testar, abra a página no navegador, selecione um trecho do texto e tente copiar com `ctrl+c`. Então, cole no bloco de notas ou outro programa.
