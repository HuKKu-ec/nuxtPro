<template>
  <img :src="user.picture" class="profile" />
  <p>{{ user.id }}</p>
  <h1>{{ user.title }}. {{ user.firstName }} {{ user.lastName }}</h1>

  <p>Gender:{{ user.gender }}</p>
  <p>Email:{{ user.email }}</p>
  <p>DOB:{{ user.dateOfBirth }}</p>
  <p>Phone:{{ user.phone }}</p>
  <p>{{ user.gender }}</p>
  <p>{{ user.gender }}</p>
</template>
<script setup>
definePageMeta({
  layout: 'custom',
});
const { id } = useRoute().params;
const user = await $fetch(`https://dummyapi.io/data/v1/user/${id}`, {
  headers: { 'app-id': '647bf5290c47194b44c6ea3b' },
}).catch((error) => {
  throw createError({ statusCode: 404, statusMessage: 'User not found' });
});
// if (user == {}) {
//   throw createError({ statusCode: 404, statusMessage: 'User not found' });
// }
</script>
