<template>
  <div>
    <nav class="navbar navbar-dark bg-dark">
      <div class="container-fluid">
        <a class="navbar-brand" href="/">Restaurantly</a>
        <ul class="navbar-nav">
          <li class="nav-item">
            <a class="nav-link active" aria-current="page" href="/">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="/restaurants">Restaurants</a>
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
