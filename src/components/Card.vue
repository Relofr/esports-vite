<template>
  <div>
    <div>
      <div class="tournament-card">
        <div class="image-container">
          <img :src="src" alt="" style="width:100%;">
          <div class="registration-status" :class="{ 'isOpen': isOpen, 'isEnding': isEnding, 'isClosed': isClosed }">{{
              regStatus
          }}</div>
        </div>
        <div class="title-price-container">
          <p class="card-title">{{ title }}</p>
          <p class="card-price">
            <fa icon="dollar-sign"></fa>{{ price }}
          </p>
        </div>
        <div class="card-info">
          <p>
            <fa icon="location-dot"></fa>{{ location }}
          </p>
          <p>
            <fa icon="calendar-days"></fa>{{ date }} - {{ time }}
          </p>
          <p>
            <fa icon="user"></fa>{{ participants + ' participants' }}
          </p>
          <button class="btn secondary-btn" :class="{ 'isDisabled': isDisabled }">Register</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
    }
  },
  props: {
    src: {
      type: String
    },
    regStatus: {
      type: String
    },
    isOpen: {
      type: Boolean
    },
    isEnding: {
      type: Boolean
    },
    isClosed: {
      type: Boolean
    },
    isDisabled: {
      type: Boolean
    },
    title: {
      type: String
    },
    price: {
      type: String
    },
    location: {
      type: String
    },
    date: {
      type: String
    },
    time: {
      type: String
    },
    participants: {
      type: String
    }
  }
}
</script>

<style scoped>
.tournament-card {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  padding: 0px;
  gap: 15px;
  width: auto;
  max-width: 400px;
  color: var(--primary-color);
  margin-bottom: 50px;
}

img {
  border-radius: 5px;
  box-shadow: inset 0px -65px 50px rgba(0, 0, 0, 0.75);
}

.image-container {
  position: relative;
  text-align: center;
  color: var(--primary-color);
}

.registration-status {
  position: absolute;
  bottom: 15px;
  left: 9px;
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 3px 12px;
  gap: 10px;
  width: auto;
  border-radius: 5px;
  font-weight: var(--fw-bold);
}

.isOpen {
  background: #0096FF;
}

.isEnding {
  background-color: #9222C9;
}

.isClosed {
  background-color: #DE1200;
}

.title-price-container {
  display: flex;
  flex-direction: row;
  padding: 0px;
  width: 100%;
  justify-content: space-between;
  align-items: center;
}

.card-title {
  font-family: Poppins;
  font-size: 24px;
  font-weight: 700;
  line-height: 37px;
  letter-spacing: 0.06em;
  text-align: left;
}

.card-price {
  display: flex;
  flex-direction: row;
  align-items: flex-start;
  padding: 5px 15px;
  gap: 10px;

  width: auto;
  height: 40px;

  background: #1F232E;
  border-radius: 50px;
  font-weight: 600;
  font-size: 20px;
  display: flex;
  align-items: center;
  letter-spacing: 0.06em;

  color: var(--primary-color);
}

.card-info {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
  padding: 0px;
  gap: 10px;
}

.card-info svg {
  padding-right: 10px;
}

.date-time {
  display: flex;
  flex-direction: row;
  align-items: center;
  padding: 0px;
  gap: 5px;
}

.date-time .dot {
  font-size: 8px;
  align-content: center;
}

.btn {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 5px 25px;
  gap: 10px;
  color: var(--secondary-color);
  text-transform: uppercase;
  font-weight: var(--fw-bold);
  width: 400px;
  height: 34px;
  border: none;
  background: #FFB039;
  mix-blend-mode: normal;
  border-radius: 3px;
  cursor: pointer;
}

.btn:hover {
  background: #ffb84e;
}

.isDisabled, .isDisabled:hover {
  background-color: grey;
  cursor: not-allowed;
}

p {
  padding: 0;
}
</style>