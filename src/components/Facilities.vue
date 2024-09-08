<script setup>
import { ref } from "vue";
import FacitiliesItem from "./FacilitiesItem.vue";
const data = [
  {
    id: 1,
    title: "Camping",
  },
  {
    id: 2,
    title: "Mountain Biking",
  },
  {
    id: 3,
    title: "Tracking",
  },
];
let currentCard = ref(1);

const handleClick = (num) => {
  currentCard.value += num;
  if (currentCard.value > 3) {
    currentCard.value = 1;
  } else if (currentCard.value < 1) {
    currentCard.value = 3;
  }
};
</script>

<template>
  <section class="container">
    <div class="cards_header">
      <h2>
        <span>Events</span>
        <br />
        Our Facilities
      </h2>
      <div class="buttons">
        <div class="pagination">
          <div class="line" :style="{ opacity: currentCard === 1 ? 1 : 0.6 }"></div>
          <div class="line" :style="{ opacity: currentCard === 2 ? 1 : 0.6 }"></div>
          <div class="line" :style="{ opacity: currentCard === 3 ? 1 : 0.6 }"></div>
        </div>
        <button class="arrow left" v-on:click="handleClick(-1)"></button>
        <button class="arrow right" v-on:click="handleClick(1)"></button>
      </div>
    </div>
    <div class="cards">
      <FacitiliesItem v-for="item in data" :activeIndex="currentCard" :data="item" />
    </div>
  </section>
</template>

<style scoped>
.cards_header {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.cards {
  display: flex;
  align-items: center;
  gap: 30px;
  margin: 110px 0;
}

.pagination {
  display: flex;
  align-items: center;
}

.line {
  width: 40px;
  height: 3px;
  background: var(--base_white);
  opacity: 0.6;
}

h2 {
  font-size: 72px;
  line-height: 84px;
}

span {
  font-size: 32px;
  opacity: 0.6;
}

.buttons {
  display: flex;
  gap: 48px;
}

.arrow {
  width: 48px;
  height: 48px;
  background: none;
  border: none;
}

.left {
  background-image: url("../assets/icons/arrow.svg");
}

.right {
  background-image: url("../assets/icons/arrow.svg");
  transform: rotate(180deg);
}
</style>
