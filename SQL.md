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

* 1 - Campo deve começar por uma letra do alfabeto
* 2 - Caracteres não permitidos: ( ) + - * ; = & > < ^ ' {} %
* 3 - Não pode conter espaços