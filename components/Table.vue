<template>
  <table class="table table-hover table-bordered mt-5 table-striped">
    <thead class="table-light">
    <tr>
      <th scope="col">Rank</th>
      <th scope="col">Chain</th>
    </tr>
    </thead>
    <tbody class="table-group-divider">
    <tr v-for="restaurant in restaurants"
        :key="restaurant.id"
    >
      <th scope="row">{{ restaurant.rank }}</th>
      <td >{{ restaurant.name }}</td>
    </tr>
    </tbody>
  </table>

</template>

<script setup>
defineProps(['restaurants']);
</script>

<style scoped>
.col {
  margin-right: 5rem;
}
</style>
