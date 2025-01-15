<script setup></script>

<template>
  <section className="contacts ">
    <div className="layout__title dot">Контакты</div>
    <div className="contacts__items">
      <div className="contacts__item">
        Телефон:
        <a className="link_hover" href="tel:+79819583833"> +7(981)9583833 </a>
      </div>
      <div className="contacts__item">
        Телеграм:
        <a
          className="link_hover"
          href="https://t.me/yuriu_gavrikov"
          target="_blank"
        >
          @yuriu_gavrikov
        </a>
      </div>
      <div className="contacts__item">Адрес: Санкт-Петербург, Россия</div>
    </div>

    <div className="design_img">
      <img src="/design/design_img/4.png" alt="" />
    </div>
  </section>
</template>

<style lang="scss" scoped>
.contacts {
  position: relative;
  display: flex;
  justify-content: space-between;
  gap: 40px;
}

.contacts__items {
}
.contacts__item {
  font-size: 40px;
}

@media (max-width: 1200px) {
  .contacts__item {
    font-size: 30px;
  }
}
@media (max-width: 576px) {
  .contacts {
    flex-direction: column;
    justify-content: space-between;
    gap: 20px;
  }

  .contacts__items {
  }
  .contacts__item {
    font-size: 20px;
  }
}
</style>
