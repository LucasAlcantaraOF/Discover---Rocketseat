# SQL - Banco de Dados

> Banco de Dados é um repositório sistêmico de informações, ou seja, um local que guardaria informações de forma organizada/sistêmatica.


| Last_Name | Fist_Name | Gender | 
| -- | --------------- | ------- | 
| Alcântara | Lucas | M | 
| Paiva | Felipe | M | 
| Holanda | Gabriela | F 

> Os arquivos "ID" "Nome" "Tipo" foram organizados em uma tabela, visto que, esses dados serão utilizados nas aplicações.

__Exemplos de banco de dados:__
* SQLite
* MariaDB
* MySQL
* PostgreSQL
* Oracle
* Firebase
* MongoDB
* Redis
* Outros...

# Conceitos

__Organização__

Todo repositório é organizado em formato de tabela:

| Last_Name | Fist_Name | Gender | Title |
| -- | --------------- | ------- | -- |
| Alcântara | Lucas | M | Programmer |
| Paiva | Felipe | M | Programmer |
| Holanda | Gabriela | F | User |

 Campos = Cabeçalho da tabela
 </br>
 Informações = Dados da tabela
 </br>
 ⬇ Colunas
 </br>
 ➡ Linhas

 # Tipos de Campos

| id_User | Last_Name | Fist_Name | Gender | Age | Title | Last_Login |
| -- | --------------- | ------- | -- | -- | -- | -- |
| 01 | Alcântara | Lucas | M | 17 | Programmer | 15-01-2023-09-30-22 |
| 02 | Paiva | Felipe | M | 30 | Programmer | 01-01-2023-10-45-42 |
| 03 | Holanda | Gabriela | F| 16 | User | 29-12-2022-02-50-34  |

> O dado fornecido dentro do campo possui um tipo, dentre eles:

__Text__

> Campos que possuem algum tipo de texto

__Number__

> Campos que somente possuem números como dado.

__Datatime__

> Campos que possuem o valor de data e hora (Dia-Mes-Ano-Hora-Minuto-Segundo)

__Primary Key__

> Campo de identificador unico (ID) 
</br>
> PS: Primary Key/Number

__Regras__

* 1 - Campo/Tabela deve começar por uma letra do alfabeto
* 2 - Caracteres não permitidos: ( ) + - * ; = & > < ^ ' {} %
* 3 - Não pode conter espaços
* 4 - Não pode contar acentuação

# Comando Select

__SELECT__

> Buscar informações e mostra-las

```
SELECT * FROM nomedatabela

// Relizando uma pesquisa completa de todos os dados dentro daquela tabela
```

__Definindo campo especifico__

```
SELECT <campo1, campo2> FROM <nomedatabela>

// Realizando uma pesquisa apenas nos campos desejados daquela tabelada
```

__SELECT com WHERE__

```
SELECT * FROM <nomedatabela> WHERE <campo> = <dado>

// Pesquisando todos os dados da tabela onde o campo é igual a um dado desejado
```

__SELECT buscando um dado que começa com uma letra__

```
SELECT * FROM <nomedatabela> WHERE <campo> like '<dado>%'

// Pesquisando uma tabela onde o campo comece com um dado especifico
// 'L%' Dado começa especificamente com L
```
__SELECT buscando um dado que possue uma determinada letra__

```
SELECT * FROM <nomedatabela> WHERE <campo> like '%<dado>%'

// Pesquisando uma tabela onde o campo tenha em algum caractere um dado especifico
// '%L%' Dado possui em algum caractere a letra L 
```

# Operadores Relacionais

> Operadores que criam o sentido de relação entre dados.

__igual =__

> O operador de igual retrata a igualdade do dado buscado com o da tabela

```
SELECT * FROM <nomedatabela> WHERE <dado> = <dado>
```
> PS: Somente funciona com dados do tipo NUMBER
---
__Like__

> Método para procurar dados do tipo texto, trocamos o igual por like, vale rememorar a importância das "" aspas no dado pesquisado.
```
SELECT * FROM <nomedatabela> WHERE <dado> like <"dado">
```
---

__Outros operadores Relacionais__

> Todos seguem ideias matemáticas, portanto, é basico como no JS

* Maior que >
* Menor que <
* Maior ou igual >=
* Menor ou igual <=
* Não igual a <>
* Diferente de !=

```
SELECT * FROM <nomedatabela> WHERE <campo> >= 2

// Realizando pesquisa onde o campo é maior ou igual a 2
``` 

# Operadores Matemáticos

> Conteúdos semelhantes aos desenvolvido na escola.

* Adição +
* Subtração -
* Multiplicação *
* Divisão /
* Módulo %

# Operadores Lógicos

__AND__

> Operador lógico que trabalha um campo e outro campo.

```
// EXEMPLO: Procurando um aluno que começa com a letra L e sua matricula é inferior aos 100 primeiros estudantes

SELECT * FROM alunos WHERE nome like "L%" AND matricula < 100
```

__OR__

> Operador lógico que trabalha com um campo ou outro campo.
</br>
> PS: Duas condições são expostas, ele somente precisa satisfazer uma para entregar um resultado.

```
// EXEMPLO: Procurando um aluno que possui uma matricula menor que 50 ou que termine o nome com a letra A

SELECT * FROM alunos WHERE matricula < 50 OR nome like "%A"
```

__BETWEEN / NOT BETWEEN__

> Método para realizar a pesquisa entre um x valor para outro y valor.

```
// EXEMPLO 1: Preciso procurar matriculas de alunos entre o valor 10 ao 1000. 

SELECT * FROM alunos WHERE matriculas BETWEEN 10 and 1000


// EXEMPLO 2: Preciso procurar matriculas de alunos, mas quero desprezar os estudantes entre o valor 10 ao 1000.

SELECT * FROM alunos WHERE matriculas NOT BETWEEN 10 and 1000
```

__IN / NOT IN__

> Relizando busca de valores especificos determinado por IN, paralelamente, fazendo buscas em todos os valores menos os definidos no NOT IN

```
// EXEMPLO 1: Procurando os alunos que estão cursando os anos letivos do 3º EM, 9º EF e 5º EF. 

SELECT * FROM alunos WHERE ano_letivo IN (3,9,5)


// EXEMPLO 2: Procurando os alunos que estão cursando os anos letivos, desprezando os do 3º EM, 9º EF e 5º EF. 

SELECT * FROM alunos WHERE ano_letivo NOT IN (3,9,5)
```

__NULL / NOT NULL__

```
// EXEMPLO 1: Dentro do meu banco de dados existem diversos alunos que não possuem um número para contato.
// portanto, preciso avaliar os campos nulos.

SELECT * FROM alunos WHERE number_contact IS NULL


// EXEMPLO 2: Dentro do meu banco de dados existem diversos alunos que não possuem um número para contato.
// Entretanto, gostaria de apenas avaliar os que possuem dado no campo

SELECT * FROM alunos WHERE number_contact IS NOT NULL
```

#  Modificando tabelas

__INSERT__

> Trabalhando em inserir valores para uma tabela

```
INSERT INTO <nomedatabela> (campo1, campo2, campo2) VALUES (dado1, dado2, 'dado3')


// EXEMPLO: Inserindo um novo aluno
INSERT INTO alunos (nome, cpf, responsavel) VALUES ('Lucas Alcântara', 85547486394, 'Mara Edwirges')
```

__UPDATE__

> Alterando algum dado que foi inserido anteriormente

```
UPDATE <nomedatabela> SET campo1='dado_novo1', campo2='dado_novo2' WHERE id = <dado>


// EXEMPLO: Alterando o responsavel do cadastro anterior da escola[
UPDATE alunos SET responsavel='Cleylton Luiz' WHERE matricula = 4
```
> PS: WHERE defini especificamente qual campo alterar, vale rememorar que a falta de especificação dele, causara a alteração de todos os campos.

__DELETE__

> Excluir um registro.

```
DELETE FROM <nomedatabela> WHERE <campo> = <valor>


// EXEMPLO: O aluno foi expulso da escola e precisa ser retirado o registro dele.
DELETE FROM alunos WHERE matricula = 4
```
> PS: WHERE defini especificamente qual campo deletar, vale rememorar que a falta de especificação dele, causara o apagamento de todos os campos.


# Tradução de termos
__* = "Todos" afetar todos os arquivos de determinada tabela__
</br>
__A% = Começa com A__
</br>
__%A = Terminar com A__
</br>
__%A% = Possui A__
</br>
__SELECT = "Selecionar" utilizado na busca por algum dado__
</br>
__FROM = "Onde" método para definir onde vai ser feita a busca__
</br>
__WHERE = "Onde" definir uma condição para pesquisa__
</br>
__like = "Contendo" definir um pesquisa que contem um X dado desejado__
</br>

