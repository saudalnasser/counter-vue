<script setup lang="ts">
import { ref } from 'vue';

const counter = ref(0);

const increment = () => counter.value++;
const decrement = () => counter.value--;
</script>

<template>
  <main>
    <header>
      <h1 id="app-header">Counter App</h1>
    </header>
    <section>
      <article>
        <h2 id="counter-header">The current count is...</h2>
        <h2 id="counter">{{ counter }}</h2>
        <button id="decrement-btn" @click="decrement">-</button>
        <button id="increment-btn" @click="increment">+</button>
      </article>
    </section>
  </main>
</template>

<style scoped>
main {
  height: 100vh;
  width: 100vw;
  background: aliceblue;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}

#app-header {
  font-size: 3rem;
}

#counter-header {
  font-size: 2rem;
}

#counter {
  font-weight: bold;
  font-size: 4rem;
}

button {
  width: 7rem;
  height: 2.25rem;
  border-radius: 50px;
  font-size: 1.25rem;
  text-align: center;
  margin: 15px;
  border: none;
  box-shadow: 1px 2px 7px rgba(0, 0, 0, 0.8);
  transition: box-shadow 0.15s ease-in-out;
}

button:active {
  box-shadow: 0 0 0 rgba(0, 0, 0, 0.5);
}

#increment-btn {
  background-color: #00abb3;
}

#decrement-btn {
  background-color: #f96666;
}
</style>
