<template>
  <div>
    <a href="#" v-on:click="makeActive('home')">Home</a>&nbsp;
    <a href="#" v-on:click="makeActive('projects')">Projects</a>&nbsp;
    <a href="#" v-on:click="makeActive('services')">Services</a>&nbsp;
    <a href="#" v-on:click="makeActive('contact')">Contact</a>&nbsp;
    <p>You chose <b>{{ active }}</b></p>
  </div>
</template>

<script>
export default {
  name: 'App',
  data () {
    return {
      active: 'home'
    }
  },
  methods: {
    makeActive: function(item){
      this.active = item;
    }
  }
}
</script>

<style>
</style>