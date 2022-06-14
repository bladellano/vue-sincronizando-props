<template>
<div class="container">
  <img alt="Vue logo" src="./assets/logo.png">

  <EmailPass
  :email="email"
  v-model="password"
  @emailUpdate="emailUpdate"
  @passwordUpdate="passwordUpdate"
  />
  =======================<br>
  Email: {{email}}<br/>
  Password: {{password}}
  <br>=======================
  </div>
</template>

<script>

import 'bootstrap/dist/css/bootstrap.css'

import EmailPass from '@/components/EmailPass'

export default {
  name: 'App',
  components: {
    EmailPass,
  },
  data(){
    return{
      email:'bladellano@gmail.com',
      password:''
    }
  },
   methods: {
        emailUpdate(email){
            this.email = email
        },
        passwordUpdate(password){
            this.password = password
        },
        
    },
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
