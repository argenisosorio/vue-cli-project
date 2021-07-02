<template>
  <li>{{ prop.title }}</li>
</template>
<script>
export default {
  props: ['prop'],
  data() {
    return {
      bookList: [
        { title: 'Il cimpendium malefican' },
        { title: 'Free demololatrie' },
        { title: 'The nine gate' }
      ]  
    }
  }
}
</script>