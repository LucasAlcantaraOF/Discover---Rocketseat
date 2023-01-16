# Node com EJS

> EJS é uma linguagem de modelagem para criação de paginas HTML utilizando JavaScript, EJS permite que crie um "front-end" com JavaScript, tudo com Node. Afinal, tudo está sendo renderizado pelo JS.


__Exemplo de Server.js:__
```
const express = require('express');
const app = express();

app.set("view engine", "ejs");

app.get("/", function (req, res){
    res.render("index");
})

app.get("/sobre", function (req, res){
    res.render("about");
})

app.listen(8080);
console.log("Iniciando Servidor!");
```

__Tag exclusiva do EJS para incluir um layout pre-definido:__
```
<%- include('arquivo.ejs'); %>
```