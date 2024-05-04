<template>
  <div class="team">
    <div class="member">
      <img class="centered-image" src="../assets/tomas.jpg" alt="Tomas">
      <h2>Tomas Ortiz Fajardo</h2>
    </div>
    <div class="member">
      <img class="centered-image" src="../assets/joan.jpeg" alt="Joan">
      <h2>Joan Jefferson Talizo Balbin</h2>
    </div>
    <div class="member">
      <img class="centered-image" src="../assets/jose.jpg" alt="Jose">
      <h2>José Daniel Mario Calderón Huamán</h2>
    </div>
    <div class="member">
      <img class="centered-image" src="https://i.ibb.co/BGJhHVC/vittorio.png" alt="Vittorio">
      <h2>Vittorio Marcelo Eduardo Espinoza</h2>
    </div>
  </div>
</template>

<script>
import tomas from '@/assets/tomas.jpg';

export default {
  name: 'AboutUsPage',
  data(){
    return{
      tomas: tomas
    }
  }
}
</script>

<style scoped>
.team {
  display: flex;
  justify-content: space-around;
  padding: 20px;
  background-color: #f8f9fa;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.2);
}
.member {
  text-align: center;
  width: 200px;
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
  box-shadow: 0 0 10px rgba(0,0,0,0.1);
}
.member img {
  width: 100px;
  height: 100px;
  border-radius: 50%;
  object-fit: cover;
  margin-bottom: 15px;
}
.member h2 {
  font-size: 18px;
  margin-bottom: 10px;
}
</style>
