<script setup></script>

<template>
  <section className="hello">
    <div className="hello__img">
      <img className="img" src="/img/hello.jpg" alt="" />
    </div>
    <div className="hello__content">
      <div className="hello__title dot">Юрий Гавриков</div>
      <div className="hello__desc">
        Я Frontend developer из Санкт-Петербурга. В настоящее время я изучаю веб
        технологии и разрабатываю свои проекты. Хочу найти работу и повысить
        свои навыки веб-разработчика.
      </div>
    </div>
  </section>
</template>

<style lang="scss" scoped>
.hello {
  display: flex;
  align-items: center;
  justify-content: center;
}
.hello__img {
  width: 450px;
  height: 450px;
}

.img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
}
.hello__content {
  display: flex;
  flex-direction: column;
  gap: 20px;

  width: 50%;
  padding: 40px;
}
.hello__title {
  font-size: 50px;
  font-weight: 900;
  line-height: 100%;
}
.hello__desc {
  font-size: 20px;
}

@media (max-width: 1200px) {
  .hello {
    display: flex;
    flex-direction: column;
  }
  .hello__img {
    width: 500px;
    height: 500px;
  }
  .hello__content {
    width: 100%;
    padding: 40px;
  }
  .hello__title {
    font-size: 40px;
    font-weight: 900;
    line-height: 100%;
  }
}
@media (max-width: 576px) {
  .hello {
    display: flex;
    flex-direction: column;
    gap: 20px;
  }
  .hello__img {
    width: 100%;
    height: 100%;
  }
  .hello__content {
    width: 100%;
    padding: 0;
  }
  .hello__title {
    font-size: 30px;
    font-weight: 900;
    line-height: 100%;
  }
  .hello__desc {
    font-size: 16px;
  }
}
</style>
