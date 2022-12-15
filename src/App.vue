<template>
  <v-app class="overflow-x-hidden">
    <v-container>
      <app-header />
    </v-container>
    <v-main>
      <router-view />
    </v-main>
    <div class="footer">
      <app-footer />
    </div>
  </v-app>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  components: {
    "app-header": AppHeader,
    "app-footer": AppFooter,
  },
};
</script>

<style>
body {
  overflow-x: hidden;
}

.container {
  width: 90% !important;
}
.footer {
  background-color: #fbf7f5;
}
</style>
