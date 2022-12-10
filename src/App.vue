<template>
  <v-app>
    <app-header />
    <v-main>
      <v-container fluid>
        <router-view />
      </v-container>
    </v-main>
    <div class="footer">
      <app-footer/>

    </div>
  </v-app>
</template>

<script>
import AppHeader from "./components/AppHeader.vue";
import AppFooter from "./components/AppFooter.vue";
export default {
  components: {
    "app-header": AppHeader,
    "app-footer": AppFooter
  },
};
</script>

<style>
.footer{
  background-color: #FBF7F5;
}
</style>
