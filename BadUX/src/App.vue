<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>


  <div class="homepage">
    <h1>Welcome to the Homepage</h1>
    <div class="button-container">
      <router-link to="/register" class="button">Register</router-link>
      <router-link to="/login" class="button">Login</router-link>
      <router-link to="/settings" class="button">Settings</router-link>
      <router-link to="/profile" class="button">Profile</router-link>
    </div>
  </div>


</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

nav {
  width: 100%;
  font-size: 12px;
  text-align: center;
  margin-top: 2rem;
}

nav a.router-link-exact-active {
  color: var(--color-text);
}

nav a.router-link-exact-active:hover {
  background-color: transparent;
}

nav a {
  display: inline-block;
  padding: 0 1rem;
  border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
  border: 0;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }

  nav {
    text-align: left;
    margin-left: -1rem;
    font-size: 1rem;

    padding: 1rem 0;
    margin-top: 1rem;
  }
}

.homepage {
  background-color: black;
  color: green;
  height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-family: 'Arial', sans-serif;
  text-align: center;
  padding: 20px;
}

.homepage h1 {
  font-size: 3rem;
  margin-bottom: 2rem;
  text-shadow: 2px 2px 5px green;
}

.button-container {
  display: flex;
  gap: 30px;
  flex-wrap: wrap;
  justify-content: center;
}

.button {
  color: green;
  text-decoration: none;
  border: 2px solid green;
  padding: 15px 25px;
  border-radius: 10px;
  font-size: 1.2rem;
  font-weight: bold;
  transition: background-color 0.3s, color 0.3s, transform 0.2s;
}

.button:hover {
  background-color: green;
  color: black;
  transform: scale(1.1);
  box-shadow: 0 0 10px green;
}

.button:active {
  transform: scale(1.05);
}
</style>
