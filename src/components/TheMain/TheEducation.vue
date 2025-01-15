<script setup></script>

<template>
  <section className="education">
    <div className="education__hello">
      <div className="layout__title dot">Образование</div>
      <div className="education__hello__desc">
        Всю свою жизнь я руководствовался твердой верой в то, что образование
        важно. Я стараюсь узнавать что-то новое каждый день.
      </div>
    </div>

    <div className="education__items">
      <div className="education__item">
        <div className="education__item__title">Frontend разработчик</div>
        <div className="education__item__desc">
          <p>2020-2021</p>
          <p>LoftSchool - Школа онлайн обучения IT профессиям</p>
        </div>
      </div>
      <div className="education__item">
        <div className="education__item__title">JS: React</div>
        <div className="education__item__desc">
          <p>2021-2022</p>
          <p>Хекслет — онлайн-школа программирования</p>
        </div>
      </div>
      <div className="education__item">
        <div className="education__item__title">
          Современный JavaScript + Vue
        </div>
        <div className="education__item__desc">
          <p>2022-2023</p>
          <p>www.udemy.com</p>
        </div>
      </div>
    </div>
    <div className="design_img">
      <img src="/design/design_img/3.png" alt="" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.education {
  position: relative;
  display: flex;
  gap: 30px;
}
.education__hello {
  flex-grow: 1;
  flex-basis: 0;
}
.title {
  font-size: 60px;
  font-weight: 900;
  line-height: 100%;
}

.education__hello__desc {
  font-size: 20px;
}
.education__items {
  display: flex;
  flex-direction: column;
  gap: 20px;

  flex-grow: 1;
  flex-basis: 0;
}
.education__item {
}
.education__item__title {
  font-size: 30px;
}
.education__item__desc {
  font-size: 20px;
}

@media (max-width: 1200px) {
}
@media (max-width: 576px) {
  .education {
    flex-direction: column;
  }
}
</style>
