<template>
  <div>
    <button class="button" v-on:click="count++">You clicked me {{ count }} times.</button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data: function () {
    return {
      count: 0
    }
  },
}
</script>

<style scoped>
.button {
  color: red;
}
</style>