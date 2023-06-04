<template>
  <h1 class="todo-head">Users list is here....!</h1>
  <CardCont :users="users" />
</template>
<script setup>
const { data: users } = await $fetch('https://dummyapi.io/data/v1/user', {
  headers: { 'app-id': '647bf5290c47194b44c6ea3b' },
}).catch((error) => error.data);
</script>
