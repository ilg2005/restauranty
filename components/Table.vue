<template>
  <table class="table table-hover table-bordered mt-5 table-striped">
    <thead class="table-light">
    <tr>
      <th scope="col" class="header">Rank</th>
      <th scope="col" class="header">Chain</th>
    </tr>
    </thead>
    <tbody class="table-group-divider">
    <tr v-for="restaurant in restaurants"
        :key="restaurant.id"
    >
      <th scope="row" class="rank">{{ restaurant.rank }}</th>
      <td class="header link"><a :href="`/restaurants/${restaurant.name}`">{{ restaurant.name }}</a></td>
    </tr>
    </tbody>
  </table>

</template>

<script setup>
defineProps(['restaurants']);
</script>

<style scoped>
thead {
  border-top: 2px solid black;
}
.col {
  margin-right: 5rem;
}

.header {
  font-size: 1.25rem;
  color: rgb(10, 31, 148);
  margin: 0;
  margin-right: 2rem;
  padding: 0.5rem 1rem;
  font-weight: 700;
  width: 4rem;
}

.rank {
  color: black;
}
.link a {
  text-decoration: none;
  color: rgb(228, 157, 27) !important;
  width: auto;
  font-weight: 500;
}
</style>
