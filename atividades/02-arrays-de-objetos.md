# Arrays de Objetos

### Atividade envolvendo a manipulação de um array de objetos

------------------------------------------------------------------------

## 1. Criação do array

Em um arquivo chamado `script.js`, crie um array de objetos chamado
`clientes` para representar o seguinte conjunto de dados:

| Nome       | E-mail              | Limite |
|------------|---------------------|--------|
| Elesbão    | elesbao@email.com   | 4500   |
| Genoveva   | genoveva@email.com  | 5750   |
| Marvelino  | marvelino@email.com | 9980   |
| Marieta    | marieta@email.com   | 2600   |

------------------------------------------------------------------------

## 2. Percorrendo com `for`

Utilizando o comando `for`, percorra o array e imprima no console a
seguinte saída:
```
Elesbão tem um limite de R\$ 4.500,00\
Genoveva tem um limite de R\$ 5.750,00\
Marvelino tem um limite de R\$ 9.980,00\
Marieta tem um limite de R\$ 2.600,00
```
------------------------------------------------------------------------

## 3. Gerando HTML com `forEach()`

Crie uma variável chamada `linhas`, inicialmente com uma string vazia
(`""`).

Use o método `forEach()` para percorrer o array e gerar dinamicamente o
conteúdo HTML das linhas da tabela.

Em seguida, imprima o conteúdo da variável `linhas` no console.
```
<tr>
    <td>Elesbão</td>
    <td>elesbao@email.com</td>
    <td>R$ 4.500,00</td>
</tr>
<tr>
    <td>Genoveva</td>
    <td>genoveva@email.com</td>
    <td>R$ 5.750,00</td>
</tr>
<tr>
    <td>Marvelino</td>
    <td>marvelino@email.com</td>
    <td>R$ 9.980,00</td>
</tr>
<tr>
    <td>Marieta</td>
    <td>marieta@email.com</td>
    <td>R$ 2.600,00</td>
</tr>
```

------------------------------------------------------------------------

## 4. Integração com HTML

Crie um arquivo chamado `index.html` com o seguinte conteúdo:
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Lista de Clientes</title>
</head>
<body>
    <table border="1" cellpadding="10" cellspacing="0">
    <thead>
        <tr>
            <th>Nome</th>
            <th>E-mail</th>
            <th>Limite</th>
        </tr>
    </thead>
    <tbody id="dados-clientes">
    </tbody>
    <tfoot>
        <tr>
            <td colspan="2">Limite Médio</td>
            <td id="limite-medio"></td>
        </tr>
    </tfoot>
</table>
</body>
</html>
```
- Inclua o script no HTML.
- Use a propriedade `innerHTML` para inserir as linhas da tabela
- Aproveite um dos laços criados para calcular a média dos limites
- Use a propriedade `textContent` para mostrar a média formatada no rodapé

------------------------------------------------------------------------

## 💡 Dica para formatar valores monetários

``` javascript
let valor = 9980;

console.log(valor.toLocaleString("pt-BR", {
    style: "currency",
    currency: "BRL"
}));
```
