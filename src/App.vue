<template>
  <v-app>
    <app-header />
    <v-main>
      <v-container fluid>
        <router-view />
      </v-container>
    </v-main>
  </v-app>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
export default {
  components: {
    "app-header": AppHeader,
  },
};
</script>

<style lang="scss"></style>
