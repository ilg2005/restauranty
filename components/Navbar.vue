<template>
  <div>
    <nav class="navbar navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="/">Restaurantly</a>
        <ul class="navbar-nav">
          <li class="nav-item">
            <NuxtLink class="nav-link"
                      aria-current="page"
                      to="/"
                      active-class="active"
                      exact-active-class="active"
            >Home</NuxtLink>
          </li>
          <li class="nav-item">
            <NuxtLink class="nav-link"
                      to="/restaurants"
                      active-class="active"
                      exact-active-class="active"
            >Restaurants</NuxtLink>
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<script setup>

</script>

<style scoped>
.navbar-nav {
  margin-left: auto;
  flex-direction: row;
}
.nav-item {
  margin-left: 2rem;
}
</style>
