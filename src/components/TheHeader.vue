<script setup></script>

<template>
  <div className="container sticky">
    <header className="header">
      <h1 className="header__logo dot">Юрий</h1>
      <nav className="nav">
        <h2 className="dot">Frontend dev</h2>
        <!-- <div className="nav__item">
          <a href="">Навыки</a>
        </div>
        <div className="nav__item">
          <a href="">Портфолио</a>
        </div> -->
      </nav>
    </header>
  </div>
</template>

<style lang="scss" scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;

  background-color: #ffffff;

  padding: 20px 0;
}

.header__logo {
  font-size: 30px;
}
.nav {
  display: flex;
  gap: 20px;
}
.nav__item {
}
.sticky {
  position: sticky;
  top: 0;
  z-index: 100;
}

@media (max-width: 1200px) {
}
@media (max-width: 576px) {
  .nav {
    gap: 10px;
  }
}
</style>
