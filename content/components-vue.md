---
title: 'Introdução aos Vue Components: Criando Componentes Reutilizáveis'
description: 'Aprenda o básico sobre Vue Components, como criar e reutilizar componentes para tornar seu código mais organizado e modular.'
date: '2025-03-08'
tags: ['Vue', 'Frontend', 'JavaScript', 'VueComponents' ,'DesenvolvimentoWeb']
category: 'Vue'
image: 'https://images.unsplash.com/photo-1669023414162-8b0573b9c6b2?q=80&w=1932&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D'
---

::quote{icon="bx bxs-component text-3xl"}

  Aprenda o básico sobre Vue Components, como criar e reutilizar componentes para tornar seu código mais organizado e modular.
::


::imagepost{:image="image" :alt="title"}
::

Os componentes são uma das principais vantagens do Vue.js, permitindo dividir a interface em partes reutilizáveis. Isso facilita a manutenção e melhora a organização do código.

## Criando um Componente Simples

Vamos criar um componente chamado `ButtonComponent.vue`:

```js
<template>
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

```

### Usando o Componente

Para usar esse componente em outro arquivo, basta importá-lo e utilizá-lo dentro do template:

```js
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

```

Com isso, criamos um botão reutilizável que pode ser usado em várias partes da aplicação! 🚀

## A live code example

The block below is a live React component. You can configure multiple live code presets that specify the available npm packages and the default imports. You can also specify a default component that will be rendered in the live code block.

```jsx live
export default function App() {
  return (<div>
  <p>This is a live React component, that's being previewed in codesandbox. </p>
  <p>Editing it will update the fenced codeblock in the markdown.</p>
  </div>)
}
```