# Exercício 02 - Input

Uma página web possui os seguintes elementos HTML:
```html 
<h1>Conversor de Temperaturas</h1>
<p>
    <input type="number" id="celsius" value="0">°C =    
    <input type="number" id="fahrenheit" value="32">°F
</p>
```
Trata-se de um conversor de temperaturas:
- A temperatura informada em graus Celsius é convertida para graus Fahrenheit;
- A temperatura informada em graus Fahrenheit é convertida para graus Celsius;
- A conversão é automática, sempre que um dos valores for alterado.

**1 -** Prepare os arquivos:
- Crie um arquivo chamado `index.html` com os elementos indicados acima, no corpo da página;
- Crie um arquivo chamado `script.js`;
- No arquivo HTML, adicione uma tag `<script>` no `<head>`, garantindo que o script seja executado apenas após o carregamento do documento.

**2 -** Implemente o evento de `input` de cada uma das caixas de texto:
- Obtenha o valor da caixa de texto em que ocorreu o input;
- Converta o valor para escala de temperatura de destino;
- Altere o valor da outra caixa de texto com a temperatura convertida.

Utilize as seguinte fórmulas para os cálculos
```
C = (F - 32) * 5 / 9

F = C * 9 / 5 + 32
```
**Dica:** os valores obtidos da caixa de texto são sempre strings. Converta para float utilizando o método `parseFloat()`;

**Observação:** para selecionar os elementos, use apenas o método `querySelector()`.

**3 -** Altere o tipo de evento para `change` e explique o que mudou no comportamento da aplicação.

 
