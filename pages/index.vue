<template>
  <div>
    <div class="container mt-5 text-center">
      <h1>Welcome to {{ appName }}!</h1>
      <NuxtLink to="/restaurants">Go to restaurants?</NuxtLink>
    </div>
  </div>
</template>

<script setup>

import {useHead} from "nuxt/app";

const appName = 'Restaurantly';

useHead({
  title: appName
})

</script>
