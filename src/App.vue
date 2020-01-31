<template>
  <img src="./logo.png">
  <h1>Hello Vue 3!</h1>
  <button @click="inc">Clicked {{ count }} times.</button>
  <table>
    <tr>
      <fragment-component />
    </tr>
  </table>
  <Suspense>
    <template #default>
      <async-component />
    </template>
    <template #fallback>
      <div>Loading...</div>
    </template>
  </Suspense>
</template>

<script>
import { ref } from 'vue'
import FragmentComponent from './FragmentComponent.vue'
import AsyncComponent from './AsyncComponent.vue';

export default {
  components: {
    FragmentComponent,
    AsyncComponent,
  },
  setup() {
    const count = ref(0)
    const inc = () => {
      count.value++
    }

    return {
      count,
      inc
    }
  }
}
</script>

<style scoped>
img {
  width: 200px;
}
h1 {
  font-family: Arial, Helvetica, sans-serif;
}
</style>
