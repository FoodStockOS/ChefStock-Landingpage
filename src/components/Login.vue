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
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  background-color: #f8f9fa;
}

.container h2 {
  text-align: center;
  color: #007bff;
}

.container form {
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.container form input {
  padding: 10px;
  border-radius: 5px;
  border: 1px solid #ccc;
}

.container form button {
  padding: 10px;
  border-radius: 5px;
  border: none;
  color: #fff;
  background-color: #007bff;
  cursor: pointer;
  transition: background-color 0.3s ease;
}

.container form button:hover {
  background-color: #0056b3;
}
</style>
