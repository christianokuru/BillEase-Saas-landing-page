<script setup>
import { ref } from 'vue';


definePageMeta({
    layout: 'auth-layout', // Use the layout name as a string
    title: 'Login', // This sets the page title
    meta: [
      { name: 'description', content: 'Login to your account' },
      { property: 'og:title', content: 'Login' },
      { property: 'og:description', content: 'Login to your account' },
    ],
});

const title = ref('Sign Page')
const description = ref('Please input your details to create an accout');
</script>

<template>
  <div>
    <h1>{{ title }}</h1> <!-- Display the title prop -->
    <p>{{ description }}</p> <!-- Display the description prop -->
    <form @submit.prevent="submit">
      <!-- Your form elements here -->
      <!-- <input type="text" placeholder="Email" v-model="email" />
      <input type="password" placeholder="Password" v-model="password" />
      <button type="submit">Login</button> -->
    </form>
  </div>
</template>
