<template>
  <div id="main" class="container">
    <div class="row">
      <div class="col-12">
        <table border="1px">
          <thead>
            <tr>
              <th scope="col">First Name</th>
              <th scope="col">Age</th>
              <th scope="col">Picture</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(usuario, index) in listaUsuarios" v-bind:key="index">
              <td v-text="usuario.location.street.name"></td>
              <td v-text="usuario.dob.age"></td>
              <td>
                <img v-bind:src="usuario.picture.thumbnail" v-bind:alt="usuario.picture.thumbnail" class="rounded-circle" />
              </td>
            </tr>
          </tbody>
        </table>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';
export default {
  name: 'App',
  data() {
    return {
      listaUsuarios: []
    }
  },
  created: function(){
    this.consultarUsuarios();
  },
  methods: {
    consultarUsuarios: function() {
      axios.get('https://randomuser.me/api/?results=3').then(response => {
        this.listaUsuarios = response.data.results
      });
    }
  }
}
</script>

<style>
</style>