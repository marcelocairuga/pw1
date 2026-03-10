# Exercício 01 - Clique

Uma página web possui os seguintes elementos HTML:
```html 
<p>Qual o seu nome? <input type="text" id="name" autofocus></p>
<p>Qual a sua idade? <input type="number" id="age"></p>
<button id="send">Enviar</button>
<p id="result"></p>
```
- O usuário informa o seu nome e a sua idade;
- Ao clicar no botão `Enviar`, um parágrafo no corpo da página exibe uma mensagem no seguinte formato:
``` 
Olá, Elesbão! Você tem 27 anos.
```
- Caso o nome ou a idade não sejam informados, um alerta é emitido com a seguinte mensagem:
```
Por favor, preencha os campos corretamente!
```
**1 -** Prepare os arquivos:
- Crie um arquivo chamado `index.html` com os elementos indicados acima, no corpo da página;
- Crie um arquivo chamado `script.js`;
- No arquivo HTML, adicione uma tag `<script>` no `<head>`, garantindo que o script seja executado apenas após o carregamento do documento.

**2 -** Implemente o evento `click` do botão:
- Obtenha os valores informados para o nome e a idade;
- Verifique se os dois campos foram preenchidos e, se necessário, emita o alerta solicitando o preenchimento correto;
- Se tudo estiver correto, altere o conteúdo de texto do parágrafo com a mensagem indicada no exemplo acima;
- Então, limpe (esvazie) os campos para que novos dados possam ser informados;
- Por fim, o cursor deve voltar automaticamente para o campo nome.

**Observação:** para selecionar os elementos, use apenas o método `querySelector()`.

**Dicas**
- para limpar um campo, você pode usar `.value = ''`;
- para fazer um elemento receber o foco, use `.focus()`;
 
