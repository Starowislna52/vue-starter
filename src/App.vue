<template>
  <div>
    <h1>Witaj w systemie do zapisów na zajęcia</h1>

    <div v-if="authenticated">Witaj {{email}}
    <a @click="logout()">Wyloguj</a>
    </div>
    <div v-else>Zaloguj się na zajęcia <input type="email" v-model="email"><button @click="auth()">Wchodzę</button></div>

  </div>
</template>

<script>
import "milligram";

export default {
  data() {
    return {
      email: '',
      password: '',
      authenticated: false
    };
  },
  methods: {
    auth() {

       this.authenticated =  true
    },
    logout(){

      this.authenticated = false
      this.email = ''

    }
  }



};


</script>

<style>

</style>
