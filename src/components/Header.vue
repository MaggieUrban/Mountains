<template>
  <header>
    <div class="container">
      <a class="logo">
        <img src="../assets/logo_header.svg" alt="" />
      </a>
      <nav>
        <a href=""> Home </a>
        <a href=""> Package </a>
        <a href="">Ticket</a>
        <a href=""> About Us </a>
        <a href=""> Contact Us </a>
        <a href=""> Blog </a>
      </nav>
    </div>
  </header>
</template>

<style scoped>
header {
  border-bottom: 1px solid rgba(255, 255, 255, 0.5);
}

.container {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 32px 0;
}

.container nav a {
  margin: 0 24px;
  font-size: 18px;
}
</style>
