<script setup>
import { ref } from "vue";
import axios from "axios";

const theName = ref("");
const nameTg = ref("");
const messageUser = ref("");
const submitMessage = () => {
  const TOKEN = "6278851300:AAHEwQBj6GQ34KS-vQ6_L5ej_g--UQO6N8A";
  const CHAT_ID = "-1001807655173";
  const URI_API = `https://api.telegram.org/bot${TOKEN}/sendMessage`;

  let message = `<b>Заявка с сайта:</b>\n`;
  message += `<b>Имя: </b>${theName.value}\n`;
  message += `<b>Телега: </b>https://t.me/${nameTg.value}\n`;
  message += `<b>Сообщение: </b>${messageUser.value}\n`;

  axios
    .post(URI_API, {
      chat_id: CHAT_ID,
      parse_mode: "html",
      text: message,
    })
    .catch((err) => {
      console.warn(err);
    })
    .finally(() => {
      console.log("finally");
      theName.value = "";
      nameTg.value = "";
      messageUser.value = "";
    });
};
</script>

<template>
  <div className="form ">
    <div className="layout__title form__title">
      <span>Написать</span>
      <span className="dot">Мне</span>
    </div>
    <div className="form__inputs">
      <div className="form__contacts">
        <input
          className="form__name"
          placeholder="Ваше Имя"
          type="text"
          v-model="theName"
        />
        <input
          className="form__tg"
          placeholder="Ник в Telegram"
          type="text"
          v-model="nameTg"
        />
      </div>
      <div className="form__text">
        <textarea
          className="form__message"
          placeholder="Ваше сообщение"
          v-model="messageUser"
        />
        <button className="form__btn" @click="submitMessage">Отправить</button>
      </div>
    </div>
    <div className="design_img">
      <img src="/design/design_img/2.png" alt="" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.form {
  position: relative;
  display: flex;
  justify-content: space-between;
  gap: 50px;
}
.form__title {
  display: flex;
  flex-direction: column;
  height: 150px;
}
.form__inputs {
  display: flex;
  flex-grow: 1;
  flex-basis: 0;
  gap: 20px;
}

.form__inputs input,
textarea {
  padding: 20px;
}

.form__contacts {
  display: flex;
  flex-direction: column;
  flex-grow: 1;
  flex-basis: 0;
  gap: 20px;
}
.form__contacts input {
  height: 65px;
  border: 1px solid var(--border);
}
.form__text {
  display: flex;
  flex-direction: column;
  flex-grow: 2;
  flex-basis: 0;
  gap: 20px;
}

.form__name {
}

.form__tg {
}
.form__message {
  resize: none;
  height: 150px;
  border: 1px solid var(--border);
}
.form__btn {
  height: 50px;
  background: #ffffff;
  border: 1px solid var(--border);
}
.form__btn:hover {
  box-shadow: 2px 2px 0px var(--designer-color);
}

@media (max-width: 1200px) {
  .form {
    flex-direction: column;
    gap: 0;
  }
  .form__title {
    flex-direction: row;
    height: 80px;
    gap: 10px;
  }
  .form__inputs {
    margin-bottom: 15px;
  }
}
@media (max-width: 576px) {
  .form__inputs {
    display: flex;
    flex-direction: column;
    flex-grow: 1;
    flex-basis: 0;
    gap: 10px;
  }
  .form__title {
    display: flex;
    flex-direction: row;
    height: 80px;
    gap: 10px;
  }
}
</style>
