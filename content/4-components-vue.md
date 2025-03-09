---
title: 'Introdução aos Vue Components: Criando Componentes Reutilizáveis'
description: 'Aprenda o básico sobre Vue Components, como criar e reutilizar componentes para tornar seu código mais organizado e modular.'
date: '2025-03-08'
tags: ['Vue', 'Frontend', 'JavaScript', 'VueComponents' ,'DesenvolvimentoWeb']
category: 'Vue'
---

Introdução aos Vue Components: Criando Componentes Reutilizáveis

Os componentes são uma das principais vantagens do Vue.js, permitindo dividir a interface em partes reutilizáveis. Isso facilita a manutenção e melhora a organização do código.
Criando um Componente Simples

Vamos criar um componente chamado `ButtonComponent.vue`:

`<template>
  <button @click="handleClick" class="btn">
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: String
  },
  methods: {
    handleClick() {
      alert("Botão clicado!");
    }
  }
};
</script>

<style scoped>
.btn {
  padding: 10px 20px;
  background-color: #42b983;
  color: white;
  border: none;
  cursor: pointer;
  border-radius: 5px;
}
</style>
`

Usando o Componente

Para usar esse componente em outro arquivo, basta importá-lo e utilizá-lo dentro do template:

`
<template>
  <div>
    <ButtonComponent label="Clique Aqui" />
  </div>
</template>

<script>
import ButtonComponent from "./ButtonComponent.vue";

export default {
  components: {
    ButtonComponent
  }
};
</script>
`

Com isso, criamos um botão reutilizável que pode ser usado em várias partes da aplicação! 🚀