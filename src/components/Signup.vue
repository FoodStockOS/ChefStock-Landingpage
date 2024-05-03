<template>
  <div class="container">
    <h2>Registrarse</h2>
    <form @submit.prevent="handleSubmit">
      <input type="text" v-model="username" placeholder="Nombre de usuario" required />
      <input type="password" v-model="password" placeholder="Contraseña" required />
      <button type="submit">Registrarse</button>
    </form>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      password: '',
    };
  },
  methods: {
    async handleSubmit() {
      const response = await axios.post('http://localhost:3000/users', {
        username: this.username,
        email: this.email,
        password: this.password,
      });
      console.log(response.data);
      this.$router.push('/login');
    },
  },
}
</script>

<style scoped>
.container {
  width: 300px;
  margin: auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
</style>
