<script setup>
import { ref, reactive } from "vue";

definePageMeta({
  layout: "auth-layout",
  title: "Login",
  meta: [
    { name: "description", content: "Login to your account" },
    { property: "og:title", content: "Login" },
    { property: "og:description", content: "Login to your account" },
  ],
});


const title = ref("Sign Page");
const description = ref("Please input your details to create an accout");

const data = reactive({
  email: '',
  password: '',
})

const isLoading = ref()

const submit = () => {
  isLoading.value = true

  
}

</script>

<template>
  <div class="border border-green rounded-2xl w-1/2 mx-auto pl-6 pt-6">
    <div class="mb-8">
      <h1 class="text-3xl font-semibold mb-2 text-center">{{ title }}</h1>
      <p>{{ description }}</p>
    </div>

    <form @submit.prevent="submit">
      <div class="flex flex-col w-1/2">
        <input
          type="text"
          placeholder="Email"
          v-model="email"
          class="border border-green rounded-lg mb-7 h-10 pl-4 outline-none" 
        />
        <input
          type="password"
          placeholder="Password"
          v-model="password"
          class="border border-green rounded-lg mb-7 h-10 pl-4 outline-none"
        />
        <button
          type="submit"
          class="border py-3 w-20 my-5 rounded-xl bg-green text-lemon font-semibold"
        >
          Sign in
        </button>
      </div>
    </form>
  </div>
</template>
