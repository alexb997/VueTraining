<!-- Composition API
  <script setup>
import { ref } from "vue";

let count = ref(0);

const addToCount = () => {
  count.value += 1;
};

const substractFromCount = () => {
  count.value -= 1;
};
</script>
-->
<!-- Options API -->
<script>
export default {
  data() {
    return {
      count: 0,
    };
  },
  methods: {
    addToCount() {
      this.count += 1;
    },
    substractFromCount() {
      this.count -= 1;
    },
  },
};
</script>

<template>
  <main>
    <container class="container">
      <h4>The current count is...</h4>
      <h1>{{ count }}</h1>
      <button @click="substractFromCount">-</button>
      <button @click="addToCount">+</button>
    </container>
  </main>
</template>

<style scoped>
main {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
}

.container {
  text-align: center;
}
</style>
