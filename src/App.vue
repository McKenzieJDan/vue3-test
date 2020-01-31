<template>
  <img src="./logo.png">
  <h1>Hello Vue 3!</h1>
  <button @click="inc">Clicked {{ count }} times.</button>
  <table>
      <tr>
        <fragment-component />
      </tr>
    </table>
</template>

<script>
import { ref } from 'vue'
import FragmentComponent from './FragmentComponent.vue'

export default {
  components: {
    FragmentComponent,
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
