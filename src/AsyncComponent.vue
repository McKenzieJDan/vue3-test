<template>
  <div>
    This is our asynchronous component!!
  </div>
</template>

<script lang="ts">

async function wait(ms) {
  return new Promise(resolve => {
    setTimeout(resolve, ms);
  });
}
export default {
  async setup () {
    await wait(3000)
    return
  }
}
</script>