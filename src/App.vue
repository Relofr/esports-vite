<script setup>
import Card from './components/Card.vue'
import Navbar from './components/Navbar.vue'
</script>

<template>
  <Navbar />
  <div class="container">
    <p class="title primary-color">Super Smash Brothers</p>
    <div class="tournament-container">
      <Card isOpen regStatus="Registration Open" title="Weekly Smash Party" price="10" location="Murray, UT" date="20 August" time="8:00 PM"
        participants="47" />
      <Card isOpen regStatus="Registration Open" title="Wavedash 2022" price="FREE" location="Online" date="Aug 10th" time="4:00 PM" participants="116" />
      <Card isEnding regStatus="Registration Ending" title="Super Smash Con 2022" price="10" location="Online" date="Sep 16th" time="4:00 PM"
        participants="113" />
      <Card isEnding regStatus="Registration Ending" title="SHINE" price="20" location="Oceanside, CA" date="Aug 18th - 24th" time="10 AM" participants="456" />
      <Card isClosed isDisabled regStatus="Registration Closed" title="Super Hitbox Bros" price="5" location="Salt Lake City, UT" date="Sep 1st" time="All Day"
        participants="212" />
      <Card isClosed isDisabled regStatus="Registration Closed" title="Leo VS Kyle 2022" price="FREE" location="Provo, UT" date="Aug 24th" time="6:00 PM"
        participants="2" />
    </div>
  </div>
</template>

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
</style>
