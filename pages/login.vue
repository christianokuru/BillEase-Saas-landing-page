<script setup>
definePageMeta({
    layout: 'auth-layout', // ✅ Use string, not an import
    keepalive: true,
    title: 'Login',
    meta: [
      { name: 'description', content: 'Login to your account' },
      { property: 'og:title', content: 'Login' },
      { property: 'og:description', content: 'Login to your account' },
    ],
});
</script>

<template>
  <div>
    <h1>Login Page</h1>
  </div>
</template>
