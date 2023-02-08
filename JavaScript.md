# JavaScript 

__Linkar JS no HTML__

```
<body>
    <script src="./"></script>
</body>
```

__Comentário em JS__

```
SHIFT + ALT + A

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
---
__Number__
> Números

* 33: Inteiros - int
* 12.5:  Reais - float
* NaN: Not a number
* Infinity: Infinito
---
__Boolean__
> Booleano: apenas pode ser verdadeiro ou falso

* true: Verdadeiro
* false: Falso
---
__Undefined x Null__
> Indefinido e Nulo

* Undefined: Valor indefinido
* Null: Valor nulo (Não existe)
---
__Objeto__
> Objeto é uma entidade independente, com propriedades e tipos.

Estrutura base:
```
{propriedade: "valor"}
```
Exemplo de Objeto:
```
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
---
__Array__
> Armazenar uma coleção de elementos em uma única variável

```
propriedade = [
    'valor1',
    'valor2',
]
```
Exemplo de Array
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

Manipulando variável:
```
var clima = "Quente"
clima = "Frio"
// Uma alteração válida.
```
---
__let__
> Let, uma variável que pode ser alterada, mas não possui o método de hoisting.

```
let phrase = "Amanda é pateta"
// Um let foi definido
```

Manipulando let:
```
let phrase = "Amanda é pateta"
phrase = "Eu gosto da Amanda"
// Uma alteração válida.
```
 ---
__const__
> Constante, valor que não pode ser alterado e possui dinamismo de scope

```
const userAdmin = true
// Uma constante recebeu o valor bolleano de "true", portanto, não poderá ser alterado naquele scope.
```

Manipulando const:
```
const userAdmin = true
userAdmin = false
// Error...
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
---
__Parâmetros e Argumentos__

```
const sum = function(number1, number2) {          // Dentro dos () temos parâmetros
    console.log(number1 + number2)
}

sum(2,3)                                          // Dentro dos () temos argumentos
```
---
__Function Arrow__
> Declara funções mais "clean". Não possui o método de Hoisting

```
const sayMyName = () => {
    console.log('Lucas')
}

sayMyName()

```
---
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
---
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
---
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
---
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
---
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

# Condicionais
> Estrutura que vai executar o código, caso verdadeiro ou não executar, caso falso, dependendo do nosso objetivo

__if e else__
> A condicional if é uma estrutura condicional que executa a afirmação, dentro do bloco, se determinada condição for verdadeira. Se for falsa, executa as afirmações dentro de else.

Estrutura Base:
```
if(propriedade1) {
    //codigo
} else if(propriedade2){
    //codigo
} else {
    //codigo
}
```
Exemplo de If e Else:
```
// Ideia basica de medidor de temperatura

let temperature = 36.9
let highTemperature = temperature >= 37.5
let mediumTemperature = temperature >= 37.5 && >= 37

if(highTemperature) {
    console.log('Febre alta')
} else if(mediumTemmperature) {
    console.log('Febre média')
} else {
    console.log('Sem febre')
}
```
---
__Switch Case__
> O switch case é uma estrutura condicional do Javascript como o if e else, serve para analisar os valores e executar um bloco de código condicionalmente. Normalmente é utilizado, quando se deseja analisar diversos valores diferentes para a mesma variável.

Estrutura base
```
switch(expression) {
    case 'a':
        //código a
        break
    case 'b':
        //código b
        break
    default: 
        //código nulo
        break
}
```

Exemplo de Switch Case: 
```
// Validação de um Admin

isAdmin = true;

switch (isAdmin) {
    case true:
        console.log("Usuário logado");
        break;
    case false:
        console.log("Você não é um admin");
        break;
}
```
---
__Throw e Try/Catch__
>

Estrutura Base:
```
throw expression {
    // codigo
}

try {
    expression
} catch(e){
    //codigo 
}
```

Exemplo de Throw e Try/Catch:
```
function sayMyName(name = ' ') {
    if (name === ' ') {
        throw 'Nome é obrigatório'
    }
}

try {
    sayMyName(Lucas)
} catch(e) {
    console.log(e)
}
```

# Estrutura de Dados

> Com a quantidade de caracteres que escrevemos dentro da nossa aplicação, formou-se a necessidade de haver uma organização para entendimento do autor e dos futuros leitores, portanto, entender as estruturas é o principio para a melhor tomada de decisão, visto que a programação é utilizada para criar eficiência e rapidez em atividades que levariam o dobro do tempo para uma pessoa realizar. 

__Stack__

> Stack seria o método linear de organização, como uma pilha onde o último a entrar seria o primeiro a sair.

__.push() - Adicionar um elemento à pilha__
<br>
__.pop() - Remover o elemento do topo da pilha__
<br>
__.peek() - Obter o elemento do topo da pilha__

__Queue__

> Queue seria o método de fila, ou seja, o primeiro a entrar na fila seria o primeiro a sair.

__enqueue() - Adicionar um elemento ao final da fila__
<br>
__dequeue() - Remover o primeiro elemento a entrar na fila__

```
class Queue {
    constructor() {
        this.data = []
    }
    enqueue(item) {
        this.data.push(item)
        console.log(`${item} entrou na fila!`)
    }

    dequeue() {
        const item = this.data.shift()
        console.log(`${item} saiu da fila!`)
    }

}

const fila = new Queue()

fila.enqueue('Lucas')
fila.enqueue('Paiva')
fila.enqueue('Gabriela')
fila.dequeue()
fila.dequeue()
fila.dequeue()
```

# Programação Orientada a Objetos (POO)

> POO seria um paradigma de desenvolvimento, uma maneira de resolver um problema, um modo de pensar. Primeiramente, Criando um recurso com melhor entedimento, sendo adequado para um reuso de código, separando a compexidade de abstraindo de maneira mais simples.
</br>
> Objetos, como dito no nome seriam utensílios recorrentes do seu dia-a-dia, entrentanto, na programação, seriam autenticações, autorizações entre outros, ou seja, ideias abstratas.
</br>
> "Paradigma = Estrutura composta por conceitos, teorias, experiências, métodos... que serve para organizar um determinado afetado"

__Conceitos__

> Todo objeto possui:
>* Propriedades e Funcionalidades
>* Estado e Comportamentos
>* Atributos e Métodos
<br>


__Classes em JS__

```

================ Método Estrutural ================
let altura = 50
let largura = 60

function calcularArea() {
    return altura * largura
}

let area = calcularArea()

console.log(area)

================ Método POO ================

class Poligono{
    constructor(altura, largura){
        this.altura = altura
        this.largura = largura
    }

    get area() {
        return this.#calcularArea()
    }
    
    // O # seria um definição que so seria utilizado dentro da class...
    #calcularArea() {
        return this.altura * this.largura
    }
}

let poligono = new Poligono(50,60)
console.log(poligono.area)
```
 
__Herança em JS__

> Herança seria o conceito de pai e filho, podemos puxar uma definição criada no pai e implementar no filho.

```
class Veiculo {
    rodas = 4;

    mover(direcao){}
    virar(direcao){}
}

// "extends" e "super()" que desiginaram a herança
class Moto extends Veiculo {
    constructor() {
        super()
        this.rodas = 2
    }
}
```

__Polimorfismo em JS__

> Com o método de herança, podemos reutilizar trechos de códigos indenticos de pai para filho, mas também pode-se alterar algum atributo caso necessário.

```
class Atleta {
    peso;
    categoria;

    constructor(peso){
        this.peso = peso
    }

    definirCategoria() {
        if (this.peso <= 50){
            this.categoria = 'Corredor Leve'
        }
        else if (this.peso <= 65) {
            this.categoria = 'Corredor Médio'
        }
        else {
            this.categoria = 'Corredor Pesado'
        }
    }
}

class Lutador extends Atleta {
    constructor(peso){
        super(peso)
    }

    definirCategoria() {
        if (this.peso <= 60){
            this.categoria = 'Peso Leve'
        }
        else if (this.peso <= 75) {
            this.categoria = 'Peso Médio'
        }
        else {
            this.categoria = 'Peso Pesado'
        }
    }
}
```

__Abstração__


# Programação Funcional