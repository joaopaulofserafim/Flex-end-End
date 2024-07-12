# Diferenca entre os valores "flex-end" e "end" da propriedade justify-content do Flexbox


Sim, existe uma diferença entre os valores "flex-end" e "end" na propriedade `justify-content` do Flexbox. O valor "flex-end" é específico do Flexbox e alinha os itens ao final do contêiner ao longo do eixo principal. Já o valor "end" é utilizado tanto no Flexbox quanto no Grid Layout e alinha os itens ao final do contêiner considerando o eixo de escrita, o que pode variar dependendo da direção de escrita (esquerda para direita, direita para esquerda, etc.). O "flex-end" é mais amplamente suportado e utilizado, enquanto "end" faz parte das especificações mais recentes e pode não ser suportado em todos os navegadores.


##  Exemplo com 'flex-end'

~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .container-flex-end {
            display: flex;
            justify-content: flex-end;
            background-color: lightgray;
            height: 100px;
        }
        .item {
            width: 50px;
            height: 50px;
            background-color: blue;
            margin: 10px;
        }
    </style>
    <title>Flex-end Example</title>
</head>
<body>
    <div class="container-flex-end">
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
    </div>
</body>
</html>

~~~

Neste exemplo, todos os itens dentro do contêiner .container-flex-end são alinhados ao final do contêiner ao longo do eixo principal (por padrão, o eixo horizontal).

## Exemplo com 'end'
~~~html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        .container-end {
            display: flex;
            justify-content: end;
            background-color: lightgray;
            height: 100px;
        }
        .item {
            width: 50px;
            height: 50px;
            background-color: green;
            margin: 10px;
        }
    </style>
    <title>End Example</title>
</head>
<body>
    <div class="container-end">
        <div class="item"></div>
        <div class="item"></div>
        <div class="item"></div>
    </div>
</body>
</html>


~~~

Neste exemplo, os itens dentro do contêiner .container-end são alinhados ao final do contêiner considerando o eixo de escrita. Se a direção de escrita for da esquerda para a direita, o comportamento será similar ao flex-end.




# Basicamnete falando o "flex-end" é específico do Flexbox, já o "end" é utilizado tanto no Flexbox quanto no Grid Layout. Os dois alinham ao final do container 