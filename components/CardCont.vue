<template>
  <div class="card-container">
    <NuxtLink :to="`/user/${user.id}`" v-for="user in users">
      <div class="card">
        <img :src="user.picture" class="profile" />
        <p>{{ user.id }}</p>
        <p>
          <b>{{ user.title }}. {{ user.firstName }} {{ user.lastName }}</b>
        </p>
        <p class="red-b">for more details click on card</p>
      </div>
    </NuxtLink>
  </div>
</template>
<script setup>
const { users } = defineProps(['users']);
</script>

<style scoped>
.card-container {
  width: 1000px;

  margin: 0px auto;
  text-align: center;
}
.card {
  display: inline-block;
  width: 240px;
  height: 240px;
  padding: 10px;
  margin: 20px;
  text-align: center;
  color: #fff;
  font-weight: 500;
  border-radius: 10px;
  background-color: #5c469c;
}
.profile {
  border-radius: 50px;
  width: 100px;
}
.red-b {
  color: #8ccc84;
}
</style>
