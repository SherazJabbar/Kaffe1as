<template>
  <v-container>
    <v-container class="jumbotron-card" :column="$vuetify.breakpoint.smAndDown">
      <!-- Stack the columns on mobile by making one full-width and the other half-width -->
      <v-row>
        <v-col cols="12" sm="6">
          <v-img
            contain
            class="fill-height"
            src="../assets/images/image-from-rawpixel-id-6738730-png 1.svg"
          >
          </v-img>
        </v-col>
        <v-col cols="12" sm="5" offset-sm="1" class="text-left ml-0 lg-ml-16">
          <div class=" ">
            <h1>Service og vedlikehold</h1>
            <p></p>

            Vi tilbyr våre kunder kanskje <span></span> den beste vedlikeholdsavtalen og
            den raskeste servicen i markedet.
            <p>
              Vår målsetning er å være hos din bedrift innen to timer ved akutt service.
            </p>

            <v-btn outlined x-large rounded color="red"> Bli firmakunde </v-btn>
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-container>
</template>

<script>
export default {
  computed: {},
};
</script>

<style scoped>
.jumbotron-card {
  background-color: #f2e5df;
  border-radius: 52px !important;
}
</style>
