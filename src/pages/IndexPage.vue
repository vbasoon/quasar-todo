<template>
  <q-page class="q-px-lg q-pt-lg flex-direction flex-center">
    <h1>IT ARMY OF UKRAINE</h1>
    <p>
      Дуже важливо! Для ефективної атаки ми повинні всі завдавати ударів по
      одним цілям та тримати їх в такому положенні стільки часу, скільки для
      цього потрібно. Тому дуже просимо Вас в чатах не приєднуватись і не
      починати самостійні атаки по іншим цілям.
    </p>
    <h4>ЩОБ ПРИЄДНАТИСЯ ВИКОНАЙТЕ 2 ПРОСТИХ КРОКИ</h4>
    <div class="container-cards flex">
      <q-card class="my-card">
        <q-card-section>
          <div class="text-h4">Встановіть відповідне ПЗ</div>
          <div class="text-subtitle2">Краще встановлювати на VPS</div>
          <p>
            Ми автоматизували ПЗ для атак таким чином, що відтепер не потрібно
            слідкувати за цілями, вони автоматично будуть оновлюватись під час
            Вашої атаки, якщо відбулася зміна.
          </p>
          <br />
          <p>
            Тому просимо усіх, навіть якщо Ви вже використовуєте якесь ПЗ,
            перейти до рекомендованих нами, щоб синхронно завдавати ураження.
          </p>
        </q-card-section>

        <q-card-actions align="around">
          <q-btn flat>Action 1</q-btn>
          <q-btn flat>Action 2</q-btn>
        </q-card-actions>
      </q-card>
      <q-card class="my-card">
        <q-card-section>
          <div class="text-h4 fa-bold">Створіть готову команду</div>
          <div class="text-subtitle2">Перейдіть до блока команд, а далі:</div>
          <p>Перейдіть до блока команд, а далі:</p>
          <ul>
            <li>Оберіть Ваше ПЗ</li>
            <li>Якщо потрібно змініть параметри кількості потоків</li>
            <li>Натисніть "Створити команду"</li>
          </ul>
          <q-btn flat>Action 1</q-btn>
        </q-card-section>

        <q-card-actions align="around">
          <q-btn flat>Action 1</q-btn>
          <q-btn flat>Action 2</q-btn>
        </q-card-actions>
      </q-card>
    </div>
    <p font-bold>Поділіться будь ласка в соц. мережах:</p>
    <button class="share">Share</button>
    <h4>ДОДАТКОВА ІНФОРМАЦІЯ:</h4>
    <div class="container-cards">
      <div class="card">Card1</div>
      <div class="card">Card2</div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "IndexPage",
});
</script>

<style lang="scss">
.my-card {
  max-width: 400px;
  margin: 0 auto;
}

.container-cards {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  margin-top: 40px;
  margin-bottom: 40px;
}

.card {
  width: 100%;
  margin: 0 auto;
}
</style>
