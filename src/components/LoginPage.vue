<template>
  <div class="login">
    <h2>Login</h2>
    <form @submit.prevent="handleLogin">
      <div>
        <label for="username">Username:</label>
        <input type="text" v-model="username" id="username" />
      </div>
      <div>
        <label for="password">Password:</label>
        <input type="password" v-model="password" id="password" />
      </div>
      <button type="submit">Login</button>
    </form>
  </div>
</template>

<script>
export default {
  name: 'LoginPage',
  data() {
    return {
      username: '',
      password: ''
    };
  },
  methods: {
    handleLogin() {
      alert(`Username: ${this.username}, Password: ${this.password}`);
    }
  }
};
</script>

<style scoped>
.login {
  max-width: 300px;
  margin: 0 auto;
  padding: 1em;
  border: 1px solid #ccc;
  border-radius: 5px;
}
.login div {
  margin-bottom: 1em;
}
label {
  margin-bottom: .5em;
  color: #333333;
  display: block;
}
input {
  border: 1px solid #CCCCCC;
  padding: .5em;
  font-size: 1em;
  width: 100%;
  box-sizing: border-box;
}
button {
  padding: 0.7em;
  color: #fff;
  background-color: #007BFF;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
button:hover {
  background-color: #0056b3;
}
</style>
