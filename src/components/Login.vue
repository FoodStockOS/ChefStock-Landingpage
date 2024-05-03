<template>
  <div class="container">
    <h2>Log In</h2>
    <form @submit.prevent="handleSubmit">
      <input type="text" v-model="username" placeholder="Username" required />
      <input type="password" v-model="password" placeholder="Password" required />
      <button type="submit">Log In</button>
    </form>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  data() {
    return {
      username: '',
      password: ''
    }
  },
  methods: {
    async handleSubmit() {
      const response = await axios.get(`http://localhost:3000/users?username=${this.username}&password=${this.password}`, {
        username: this.username,
        password: this.password,
      });
      console.log(response.data.length);
      if (response.data.length > 0) {
        this.$router.push('/homepage');
      } else {
      }
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
