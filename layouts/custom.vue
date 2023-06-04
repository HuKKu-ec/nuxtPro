<template>
  <div>
    <nav class="nav-container">
      <h1>YoYo</h1>
      <ul class="right-container">
        <li><NuxtLink class="link" to="/">Home</NuxtLink></li>
        <li><NuxtLink class="link" to="/users">Users</NuxtLink></li>
      </ul>
    </nav>
    <slot />
  </div>
</template>
