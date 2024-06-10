<!-- Qui va la logica del componente (Vue3 + Javascript) -->
<script>
export default {
  data() {
    return {
      count: 0
    }
  }
}
</script>



<!-- Qui va il contenuto di questo elemento (HTML) -->
<template>
  <button @click="count++">Count is: {{ count }}</button>
</template>



<!-- Qui va lo stile CSS di questo elemento (CSS) -->
<style scoped lang="scss">
button {
  font-weight: bold;
}
</style>