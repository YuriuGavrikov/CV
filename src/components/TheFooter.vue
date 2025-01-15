<script setup></script>

<template>
  <div className="container">
    <footer className="footer">
      <div className="footer__github">
        <a
          className="link_hover"
          href="https://github.com/YuriuGavrikov"
          target="_blank"
        >
          GitHub
        </a>
      </div>
      <div className="footer__year">2024</div>
    </footer>
  </div>
</template>

<style lang="scss" scoped>
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 0;
}
.footer__github {
  font-size: 30px;
}
.footer__year {
  font-size: 20px;
}
</style>
