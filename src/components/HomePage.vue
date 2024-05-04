<template>
  <div class="container">
    <div class="left-side">
      <img class="centered-image" src="../assets/inventariores.jpg" alt="Inventario">
      <h1 class="welcome-text">Welcome to FoodStockOS</h1>
      <Button @click="goToPage" :label="$t('getStarted')" class="p-button-raised p-button-rounded p-button-success get-started-button"></Button>
    </div>
    <div class="right-side">
      <p>
        FoodStockOS is an innovative application designed to help restaurants manage their inventory efficiently. We understand that managing inventory can be a challenging task, especially in the restaurant industry where ingredients need to be fresh and available at all times.
      </p>
      <p>
        With FoodStockOS, you can track, manage, and optimize your inventory with ease. Our application allows you to have full control over your inventory, reduce waste, save money, and most importantly, ensure that you can always offer your delicious dishes to your customers. Start optimizing your inventory today with FoodStockOS!
      </p>
    </div>
  </div>
</template>

<script>
import Button from 'primevue/button';

export default {
  name: 'HomePage',
  components: {
    Button
  },
  methods: {
    goToPage() {
      window.location.href = 'https://front-end-chefstock.web.app/';
    }
  }
}
</script>

<style scoped>
.container {
  display: flex;
  justify-content: space-between;
  padding: 20px;
}

.left-side {
  width: 40%;
}

.right-side {
  width: 50%;
  padding-left: 20px;
}

.welcome-text {
  margin-top: 20px;
}

.centered-image {
  width: 100%;
  height: auto;
}

.get-started-button {
  margin-top: 20px;
}
</style>
