<template>
  <div>
    <NuxtLayout name="custom">
      <div class="restaurant-container mt-10">
        <div class="image-container">
          <img :src="restaurant.imageUrl" alt="Restaurant picture" />
        </div>
        <div class="info-container">
          <h1>{{ restaurantName }}</h1>
          <div class="stats-container">
            <h5>Revenue (in billions)</h5>
            <p>${{ restaurant.revenue }}</p>
          </div>
          <div class="stats-container">
            <h5>Number of Stores</h5>
            <p>{{ restaurant.numberOfStores }}</p>
          </div>
          <p class="content">{{ restaurant.content }}</p>
        </div>
      </div>
    </NuxtLayout>
  </div>
</template>

<script setup>
import restaurants from "@/data.json";
import {useHead} from "nuxt/app";

const route = useRoute();
const router = useRouter();
const restaurantName = route.params.restaurant;

const restaurant = restaurants.filter(r => r.name === restaurantName)[0];
useHead({
  title: restaurant ? restaurantName : '404 - Not Found',
})

if (!restaurant) {
  router.push('/404');
}
</script>

<style scoped>
.restaurant-container {
  display: flex;
  align-items: center;
}
.image-container {
  width: 75%;
  height: 95vh;
}

.image-container img {
  width: 100%;
  height: 100%;
}
.restaurant-not-found {
  height: 75vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
.info-container {
  padding: 3rem;
  width: 50%;
}
.info-container h1 {
  text-transform: uppercase;
  font-size: 6rem;
  margin-bottom: 3rem;
}
.stats-container {
  display: flex;
  align-items: flex-end;
  margin-bottom: 1rem;
}
.stats-container h5 {
  width: 20rem;
  font-size: 2rem;
  margin: 0;
  margin-right: 5rem;
}
.stats-container p {
  font-size: 2rem;
  margin: 0;
}
.content {
  font-size: 1.5rem;
  margin-top: 4rem;
}
</style>
