---
title: 'Entendendo o Hoisting no JavaScript: Como Funciona?'
description: 'Descubra como o Hoisting funciona no JavaScript e evite armadilhas comuns ao declarar variáveis e funções.'
date: '2025-03-07'
tags: ['JavaScript', 'Hoisting', 'DesenvolvimentoWeb', 'Frontend']
category: 'Javascript'
---

Entendendo o Hoisting no JavaScript: Como Funciona?

O Hoisting é um comportamento do JavaScript onde declarações de variáveis e funções são "movidas" para o topo do escopo antes da execução do código. Isso pode gerar comportamentos inesperados se não for bem compreendido.
Hoisting com `var`

Quando usamos `var`, a variável é içada, mas seu valor não:

`
console.log(nome); // undefined
var nome = "João";
console.log(nome); // "João"

`

Aqui, o JavaScript "move" a declaração para o topo, mas não a inicialização:

`
var nome;
console.log(nome); // undefined
nome = "João";

`

### Hoisting com let e const

Diferente de var, let e const também são içados, mas não podem ser acessados antes da inicialização:

`
console.log(sobrenome); // ReferenceError: Cannot access 'sobrenome' before initialization
let sobrenome = "Silva";

`

### Hoisting com Funções

As funções declaradas com function são completamente içadas, podendo ser chamadas antes da declaração:

``
saudacao(); // "Olá, mundo!"

function saudacao() {
  console.log("Olá, mundo!");
}

``

No entanto, funções armazenadas em variáveis `(function expressions)` não funcionam da mesma forma:

`
saudacao(); // TypeError: saudacao is not a function

var saudacao = function () {
  console.log("Olá, mundo!");
};

`

### Conclusão

O Hoisting pode causar confusão, então prefira let e const em vez de var e evite chamar funções antes de declará-las para evitar erros no código! 🚀