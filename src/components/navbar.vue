<template>
  <nav class="navbar">
    <div class="nav-left">
      <router-link to="/">Portfolio</router-link>
    </div>
    <div class="nav-right">
      <router-link to="/projects">My Projects</router-link>
      <router-link to="/contact">Contact Me</router-link>
    </div>
  </nav>
</template>

<script>
export default {
  name: 'Navbar'
};
</script>

<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background-color: #333;
  color: #fff;
  padding: 10px 20px;
}

.nav-left {
  font-size: 24px;
}

.nav-right {
  display: flex;
  gap: 20px;
}

.nav-right a {
  color: #fff;
  text-decoration: none;
  font-size: 16px;
}
</style>
