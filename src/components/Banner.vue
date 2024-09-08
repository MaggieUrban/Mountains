<template>
  <div class="banner">
    <img src="../assets/bg1.png" class="background" />
    <div class="title">
      <h1>
        <span>THE BEAUTY OF</span> <br />
        Beau Mountain
      </h1>
    </div>
    <img src="../assets/bg2.png" class="foreground" />
  </div>
</template>

<style scoped>
.banner {
  position: relative;
  top: -100px;
  color: white;
  width: 100vw;
  height: 1000px;
}
.background,
.foreground {
  position: absolute;
  width: 100%;
}

.background {
  z-index: -3;
}

.foreground {
  z-index: -1;
  top: 0px;
}

.title {
  text-align: center;
  position: relative;
  top: 100px;
  mix-blend-mode: overlay; /*эффекта наложения,  */
  color: #ffffff;
  z-index: -2;
}

.title span {
  font-size: 56px;
}

h1 {
  font-size: 156px;
  line-height: 120px;
  font-weight: 900;
}
</style>
