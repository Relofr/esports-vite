<script setup>
import Card from './components/Card.vue'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <Navbar />
  <div class="container">
    <p class="title primary-color">Super Smash Brothers</p>
    <div class="tournament-container">
      <Card :src="dk" isOpen regStatus="Registration Open" title="Weekly Smash Party" price="10" location="Murray, UT"
        date="20 August" time="8:00 PM" participants="47" />
      <Card :src="gameover" isOpen regStatus="Registration Open" title="Wavedash 2022" price="FREE" location="Online" date="Aug 10th"
        time="4:00 PM" participants="116" />
      <Card :src="mushroom" isEnding regStatus="Registration Ending" title="Super Smash Con 2022" price="10" location="Online"
        date="Sep 16th" time="4:00 PM" participants="113" />
      <Card :src="nolimits" isEnding regStatus="Registration Ending" title="SHINE" price="20" location="Oceanside, CA"
        date="Aug 18th - 24th" time="10 AM" participants="456" />
      <Card :src="room" isClosed isDisabled regStatus="Registration Closed" title="Super Hitbox Bros" price="5"
        location="Salt Lake City, UT" date="Sep 1st" time="All Day" participants="212" />
      <Card :src="tv" isClosed isDisabled regStatus="Registration Closed" title="Leo VS Kyle 2022" price="FREE"
        location="Provo, UT" date="Aug 24th" time="6:00 PM" participants="2" />
    </div>
  </div>
</template>

<script>
import dk from '../src/assets/images/donkeykong.png';
import gameover from '../src/assets/images/gameover.png';
import mushroom from '../src/assets/images/mushroom.png';
import nolimits from '../src/assets/images/nolimits.png';
import room from '../src/assets/images/room.png';
import tv from '../src/assets/images/tv.png';
</script>

<style scoped>
.container {
  width: 90%;
  /* max-width: 1100px; */
  margin: 50px auto;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  z-index: 999;
}

.tournament-container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  padding: 0px;
  gap: 20px;
  width: 100%;
}

@media (max-width: 915px) {
  .tournament-container {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    padding: 0px;
    gap: 20px;
    width: 100%;
  }
}
</style>
