# Node.JS

> NodeJS é uma ferramenta que pode ser desenvolvida em "backend" e "frontend", criando micro serviços, ou seja, micro aplicações para o desenvolvimento, ou por exemplo "APIs"... existe derivados problemas que podem ser mitigados com Node.JS


Principais qualidades do Node:
* Rapido
* Alta escalabilidade
* Aplicações de ponta
* JS everywhere (Tudo é JS)
* Comunidade ativa

> Node.JS é um JS Runtime Enviroment, ou seja, se comunica diretamente com o Sistema Operacional, que logo após se direciona para o "Hardware", portanto, pode-se concluir que Node não é uma linguagem de programação, sendo uma tecnologia utilizada para o JavaScript server-side.

# Funcionamento 

> NodeJS não segue uma linha de progessão como o JavaScript, indo da linha 1 para baixo, temos um sistema unico de transações, o "Node.JS System" cria o "event queue" que funciona de acordo com a forma que você configurou a sua aplicação, parelalemente, o "worker threads" é uma lista de eventos que não poderam ser executados de imediato e são colocados na fila de espera, para assim que liberado serem executados.
> Limpar terminal = ctrl + L

# Módulos

> Um módulo é uma coleção de funções e objetos do JavaScript que podem ser utilizados por aplicativos externos

__Módulo nativo__

```
// Linkando um modulo nativo do Node.JS, "path", logo após, chamando um "console.log" para ver o resultado no terminal
const module = require('Path')
console.log(module)
```

__Criar módulo__

> Arquivo: exports
> 
```
/ Criamos um arquivo denominado "exports", e utilizamos o "module.exports" para criar um modulo próprio.
module.exports = 'Meu módulo'
```
> Arquivo: principal

```
// Chamamos nosso modulo com um "require", mas diferente de antes linkamos o nosso arquivo
// por fim chamamos um "console.log" para vermos no terminal.
const myModule = require('./exports')
console.log(myModule)
```

# NPM - Node Package Manager

> o NPM é um gerenciador de pacotes. Esse, por sua vez, é um ambiente para a execução de JavaScript no lado do servidor de hospedagem. Em outras palavras, ele permite utilizar a linguagem JavaScript no back-end da aplicação.
```
npm init
// Começando um arquivo NPM manualmente

npm init -y
// Começando um arquivo NPM com todas as configurações em "yes"
```
```
npm install "pacote"
// Instalando um pacote

npm install "pacote" -D
// Instalando um pacote de desenvolvimento

npm install "pacote" -G
// Instalando um pacote global

npm install "pacote@version"
// Instalando um pacote e definindo a versão

npm install "pacote@latest"
// Instalando um pacote com a ultima versão

npm uninstall "pacote"
// Desistalando o pacote

npm upgrade
//
```

# Timers

> Trabalhando com tempo dentro do Node.JS, ou seja, agendar que alguma parte do nosso codigo seja executado depois de x milisegundos.

* setTimeout: Esperar um tempo para executar
* clearTimeout: Cancelar tempo
* setInterval: Intervalo
* clearInterval: Cancelar intervalo

__setTimeout__

```
// seTimeout serve para rodar uma função depois de x milissegundos

const timeOut = 3000
const finished = () => console.log('Resposta enviada depois de 3 segundos')

setTimeout(finished, timeOut)
// setTimeout pede dois argumentos: (função, tempo)

console.log('Resposta enviada imediatamente')
```

__clearTimeout__

```
// clearTimeout cancelar uma timeOut
const timeOut = 3000
const finished = () => console.log('Done')
// Realizamos um registro e colocamos no setTimeout

let timer = setTimeout(finished, timeOut)
clearTimeout(timer)
// Cancelamos o timer e encerramos a operação
````

__setInterval__

```
// setInterval roda uma função x vezes, depois de y milissegundos

const timeOut = 1000
const checking = () => console.log('Checking!')
// Um "agente" vai ficar checando esse time sem fim!

setInterval(checking, timeOut)
// Dois argumento(função, tempo)
```

__clearInterval__

```
// clearInterval cancela o setInterval

const timeOut = 1000
const checking = () => console.log('Checking!')
// Um "agente" vai ficar checando esse time sem fim!

let interval = setInterval(checking, timeOut)
clearInterval(interval)

setTimeout( () => clearInterval(interval), 3000)
// Definindo um timer para executar o clearInterval
```