<template>
  <q-layout view="lHh Lpr lFf">
    <q-header>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />
      </q-toolbar>
      <div class="q-px-lg q-pt-md q-mb-md">
        <h3 class="text-h3">IT ARMY OF UKRAINE</h3>
        <h2>{Доброго вечора, ми з України!}</h2>
        <p class="text-subtitle">{{ todaysDate }}</p>
      </div>
    </q-header>

    <q-drawer v-model="leftDrawerOpen" show-if-above bordered>
      <q-list>
        <q-item-label header> Menu </q-item-label>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.title"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";
import EssentialLink from "components/EssentialLink.vue";
import { date } from "quasar";

const linksList = [
  {
    title: "Головна",
    caption: "",
    icon: "school",
    link: "https://quasar.dev",
  },
  {
    title: "Інструкції старту DDOS",
    caption: "",
    icon: "code",
    link: "https://github.com/quasarframework",
  },
  {
    title: "Інструкції з розгортання VPS",
    caption: "",
    icon: "chat",
    link: "https://chat.quasar.dev",
  },
  {
    title: "Потужні інструменти",
    caption: "",
    icon: "record_voice_over",
    link: "https://forum.quasar.dev",
  },
  {
    title: "Статуси цілей",
    caption: "",
    icon: "rss_feed",
    link: "https://twitter.quasar.dev",
  },
  {
    title: "Вакансії",
    caption: "",
    icon: "public",
    link: "https://facebook.quasar.dev",
  },
  {
    title: "Партнери",
    caption: "",
    icon: "favorite",
    link: "https://awesome.quasar.dev",
  },
];

export default defineComponent({
  name: "MainLayout",

  components: {
    EssentialLink,
  },

  computed: {
    todaysDate() {
      const timeStamp = Date.now();
      return date.formatDate(timeStamp, "dddd, DD MMM YYYY");
    },
  },

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      essentialLinks: linksList,
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
