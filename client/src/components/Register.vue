<template>
  <div>
    <h1>Register</h1>
    <input type="email" name="email" placeholder="email" v-model="email" >
    <br>
    <input type="password" name="password" placeholder="password" v-model="password" >
    <br>
    <button @click="register" >Register</button>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'
export default {
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    async register () {
      // const response = await AuthenticationService.register({
      await AuthenticationService.register({
        email: this.email,
        password: this.password
      })
      // console.log(response.data)
      // console.log('register button was clicked', this.email, this.password)
    }
  } /* ,
  watch: {
    email (value) {
      console.log('email has changed', value)
    }
  },
  mounted () {
    setTimeout(() => {
      this.email = 'hello world'
    }, 2000)
  } */
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
