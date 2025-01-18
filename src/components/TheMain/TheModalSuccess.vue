<script setup></script>

<template>
  <div class="modalBg">
    <div class="modalSuccess">Ваша заявка принята!</div>
  </div>
</template>

<style lang="scss" scoped>
.modalBg {
  display: flex;
  justify-content: center;
  align-items: center;

  position: fixed;
  top: 0;
  left: 0;

  height: 100vh;
  width: 100vw;

  backdrop-filter: blur(5px);
  z-index: 100;
}
.modalSuccess {
  padding: 50px;
  border: 1px solid black;
  background-color: rgb(255, 255, 255);
}
</style>
