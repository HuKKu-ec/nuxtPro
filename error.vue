<template>
  <div class="error-container">
    <h1 class="error-head">Error...!</h1>
    <h2>{{ error.statusCode }}</h2>
    <p class="error-head">{{ error.message }}</p>
    <NuxtLink class="link" to="/"
      ><button class="btn">Go Home</button></NuxtLink
    >
  </div>
</template>
<script setup>
defineProps(['error']);
</script>
<style scope>
.error-container {
  text-align: center;
  background-color: #e4e4e4;
  border-radius: 20px;
  width: 400px;
  padding: 100px;
  margin: 50px auto;
}
.error-head {
  color: #c75151;
}
h2 {
  color: #5c469c;
}
</style>
