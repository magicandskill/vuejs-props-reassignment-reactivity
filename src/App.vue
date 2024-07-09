<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue'
import { ref } from 'vue';


const count = ref(0)
const text = ref('You did it!')
</script>

<template>
  <header>
    <div class="wrapper">
      <HelloWorld :text="text" :count="count" />
    </div>
  </header>

  <main>
    <button @click="count += 1">Add Count</button>
    <button @click="text += 1">Change text</button>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
