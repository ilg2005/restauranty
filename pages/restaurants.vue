<template>
  <div>
    <Navbar/>
    <div class="container mt-5 text-center">
      <h1 class="text-uppercase">Top 50: The Ranking</h1>
        <div class="row">
          <Table class="col" :restaurants="data1"/>
          <Table class="col" :restaurants="data2"/>
        </div>
    </div>
  </div>
</template>

<script setup>
import data from '@/data.json';

const data1 = [...data].splice(0, data.length / 2);
const data2 = [...data].splice(data.length / 2, data.length);
</script>
