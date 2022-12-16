# JavaScript 


__Linkar JS no HTML__

```
<body>
    <script src="./"></script>
</body>
```

__Comentário em JS__

```
// Comentário

/*
   Comentário 1
   Comentário 2
*/
```

#  Tipos de Dados 


__String__
> Cadeia de caracteres que constituem algum termo ("ABC").

* "" Aspas Duplas
* '' Aspas Simples
* `` Crase

__Number__
> Números

* 33: Inteiros - int
* 12.5:  Reais - float
* NaN: Not a number
* Infinity: Infinito

__Boolean__
> Booleano: apenas pode ser verdadeiro ou falso

* true: Verdadeiro
* false: Falso

__Undefined x Null__
> Indefinido e Nulo

* Undefined: Valor indefinido
* Null: Valor nulo (Não existe)

__Objeto__
> Objeto é uma entidade independente, com propriedades e tipos.

```
{propriedade: "valor"}

console.log({
    name: "Lucas",
    idade: 17,
    isAdmin: true
})

const person = {
    name: 'Lucas',
    age: 17,
    weight: 60.5,
    isAdmin: true
}
```

__Array__
> Armazenar uma coleção de elementos em uma única variável
```
const persons = [
    'Lucas',
    'Caio',
    'Yelena',
]
```

# Tipos de Variáveis

__var__
> Variável, pode ser variada ao decorrer da aplicação, paralelamente, possui o método de hoisting

```
var clima = "Quente"
// Uma variável foi definida.
```

> Manipulando variável
```
var clima = "Quente"
clima = "Frio"
// Uma variável foi definida e logo após um novo valor foi fornecido para ela.
```

__let__
> Let, uma variável que pode ser alterada, mas não possui o método de hoisting.

```
let phrase = "Amanda é pateta"
// Um let foi definido
```

```
let phrase = "Amanda é pateta"
phrase = "Eu gosto da Amanda"
// Uma alteração válida.
```
 

__const__
> Constante, valor que não pode ser alterado e possui dinamismo de scope

```
const userAdmin = true
// Uma constante recebeu o valor bolleano de "true", portanto, não poderá ser alterado naquele scope.
```
```
const userAdmin = true
userAdmin = false
// 
```

# Concatenando e Interpolando 

```
let name = "Lucas"
let age = 17

(' o' + name + ' tem ' + age = ' anos.')
// Concatenando
(`o ($name) tem ($age) anos`) 
// Interpolando
```

#  Funções

__Functions Statement__
> Função é um conjunto de instruções que executa uma tarefa. Dinamismo no método de Hoisting

```
function phrases() {
    console.log('Uma vida de merda te transfoma em alguém de merda')
    console.log('Atitudes de um babaca, mas sentimentos de um anjo')
    console.log('Você me mostrou que as vezes a vida merece ser vivida')
}

phrases()
```

__Parâmetros e Argumentos__

```
const sum = function(number1, number2) {          // Dentro dos () temos parâmetros
    console.log(number1 + number2)
}

sum(2,3)                                          // Dentro dos () temos argumentos
```

__Function Arrow__
> Declara funções mais "clean". Não possui o método de Hoisting

```
const sayMyName = () => {
    console.log('Lucas')
}

sayMyName()

```
__Callback function__
> Função que passa como parâmetro para outra função.

```
function sayMyName(name) {
    console.log('Antes da function callback')
    name()
    console.log('Depois da function callback')
}

sayMyName(
    () =>{
        console.log('Estou em uma callback')
    }
)
```

__Function Constructor__

```
function Person() {}
const lucas = new Person()
```

# Manipulação de dados

* Type Conversion: Coesão causada pelo autor 
* Type Coersion: Coesão causada pelo JavaScript

__Number( ) - String( )__
> Alterando o dado string para um number e vice-versa

```
let string = "123"
console.log(Number(string))
// Transformando String para Number

let number = 123
console.log(String(number))
// Transformando Number para String
```
---
__.length__
> Contando caracteres e dígitos

```
let word = "Paralelepidedo"
console.log(word.length)
// Denominando uma string e utilizando a propriedade ".length" para contabilizar seus caracteres

let number = 1234
console.log(number.length)
// Denominando um number e utilizando a propriedade ".length" para contabilizar seus dígitos
```
---
__.toFixed( ) .replace( )__

> Determinando a quantidade de decimais e formatando pontos por virgulas

```
let number = 324.321531
console.log(number.toFixed(2).replace(".", ","))
// A propriedade ".toFixed()" arruma os decimais do numero, no exemplo serão 2
// A propriedade ".replace()" altera os pontos por virgulas
```
---
__.toUpperCase( ) .toLowerCase__

> Transformando todos os algoritimos em maiúsculas ou minúsculas

```
let word = "Eu acho a Gabi pateta"
console.log(word.toLowerCase())
// Todos os caracteres estaram em minúsculo

console.log(word.toUpperCase())
// Todos os caracteres estaram em maiúsculo
```
---
__.includes__

```
let phrase = "A Rayssa é minha irmã"
console.log(phrase.includes("irmã"))
// A propriedade ".includes" vai procurar se encontrar o seu objetivo PS: Maiúsculas e Minúsculas tem diferença
```
---
__Array.from( )__

> Transformando sting em array

```
let word = "Gabriele"
console.log(Array.from(word))
```

# Expressões e Operadores

__Operadores Aritméticos__
> A programação utiliza operadores da matemática na sua composição, portanto, vale entender os sinais correspondentes a matemática no JavaScript

* Multiplicação: *
* Divisão: /
* Adição: +
* Subtração: -

* Resto da divisão: %
* Incremento: ++
* Decremento: --
* Exponencial: ^ 

__Operadores de comparação__
> Existem diversas necessidades de comparar um número ao outro em uma aplicação. Assim, faz-se necessário revisar os fundamentos de comparação da matemática

```
let one = 1
let two = 2

// Igual a:
one == 1

// Diferente de:
two != 1

// Estritamente igual a:
one === 1

// Estritamente diferente de:
two !== "2"

// Maior que:
two > one

// Maior ou igual que:
two >= 2

// Menor que
one < 2

// Menor ou igual que:
one <= 1
```

__Operadores lógicos__

```
let isAdmin = true
let user = false

// AND &&
console.log(isAdmin && user) - true

// OR || - true
console.log(isAdmin || user)

// NOT ! - false
console.log(!isAdmin)
```

__Falsy e Truthy__

> FALSY: Valores booleanos que são considerados falsos

* false
* 0
* -0
* ""
* null
* Undefined
* NaN

> TRUTHY: Valores booleanos que são considerados verdadeiros

* true
* {}
* []
* 1
* 1.11
* "0"
* "false"
* -1
* Infinity
* -Infinity
