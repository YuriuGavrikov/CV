<script setup>
import TheContacts from "./TheMain/TheContacts.vue";
import TheHello from "./TheMain/TheHello.vue";
import TheForm from "./TheMain/TheForm.vue";
import TheEducation from "./TheMain/TheEducation.vue";
import TheSkills from "./TheMain/TheSkills.vue";

</script>

<template>
  <div className="container">
    <main className="main">
      
      <TheHello />
      <hr />
      <TheSkills />
      <hr />
      <TheEducation />
      <hr />
      <TheForm />
      <hr />
      <TheContacts />
      <hr />
    </main>
  </div>
</template>

<style lang="scss" scoped>
.main {
  display: flex;
  flex-direction: column;
  gap: 50px;
}
@media (max-width: 1200px) {
  .main {
    gap: 40px;
  }
}
@media (max-width: 576px) {
  .main {
    gap: 30px;
  }
}
</style>
