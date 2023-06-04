<template>
  <header>
    <nav class="nav-container">
      <h1>YoYo</h1>
      <ul class="right-container">
        <li><NuxtLink class="link" to="/">Home</NuxtLink></li>
        <li><NuxtLink class="link" to="/about">About</NuxtLink></li>
        <li><NuxtLink class="link" to="/users">Users</NuxtLink></li>
        <li><NuxtLink class="link" to="/todo">Todo</NuxtLink></li>

        <li>
          <NuxtLink class="link" to="/contact">
            <button class="btn">Contact</button></NuxtLink
          >
        </li>
      </ul>
    </nav>
  </header>
  <div class="body-container">
    <div class="route-container">
      <slot />
    </div>
  </div>
  <footer>
    <Footer />
  </footer>
</template>
<style>
body {
  font-family: 'Georgia', 'Times New Roman', 'Times', 'serif';
  margin: 0px;
  background-color: #faf9ff;
}
.body-container {
  max-width: 1200px;
  margin: 0px auto;
}
.nav-container {
  background-color: #f7f3ff;
  font-weight: bold;
  color: #5c469c;
  display: flex;
  padding: 20px;
}
.right-container {
  list-style: none;
  display: flex;
  margin-left: auto;
  align-items: center;
}
.right-container li {
  padding-left: 10px;
}

.link {
  all: unset;
  cursor: pointer;
}
.btn {
  all: unset;
  background-color: #5c469c;
  color: #faf9ff;
  padding: 10px 13px;
  border-radius: 5px;
}
.route-container {
  padding: 10px;
}
.footer {
  margin: 0px;
}
</style>
