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

#increment-btn,
#decrement-btn {
  width: 7rem;
  height: 2.25rem;
  border-radius: 50px;
  font-size: 1.25rem;
  text-align: center;
  margin: 15px;
}

#increment-btn {
  background-color: #a8e890;
}

#decrement-btn {
  background-color: #dd5353;
}
</style>
