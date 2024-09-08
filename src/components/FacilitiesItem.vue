<script setup>
const { data, activeIndex } = defineProps(["activeIndex", "data"]);
</script>

<template>
  <div :class="`card ${data.id === activeIndex ? 'active' : 'no_active'}`">
    <span>0{{ data.id }}</span>

    <img v-if="data.id === activeIndex" src="../assets/card.png" />

    <h4>{{ data.title }}</h4>
    <a href="">see details</a>
  </div>
</template>

<style scoped>
.card {
  width: 530px;
  height: 520px;
  border-radius: 12px;
  background: var(--base_dark-green);
  position: relative;
  overflow: hidden;
  padding: 48px 148px 48px 48px;
  display: flex;
  flex-direction: column;
  justify-content: space-around;
}

.active {
  height: 640px;
}
img {
  position: absolute;
  top: 0;
  right: 0;
}

span {
  font-size: 120px;
  opacity: 0.2;
}

h4 {
  font-size: 72px;
}
</style>
