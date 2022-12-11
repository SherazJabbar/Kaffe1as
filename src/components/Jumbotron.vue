<template>
  <v-container fluid>
    <v-row class="layout" :column="$vuetify.breakpoint.mdAndDown" >
      <v-col class="text-left">
        <v-img
          contain
          class="fill-height"
          lazy-src="https://picsum.photos/id/11/10/6"
          src="../assets/images/image-from-rawpixel-id-6738730-png 1.svg"
        >
        </v-img>
      </v-col>
      <v-col class="text-left mt-lg-10 mt-md-10 mt-sm-3 mt-xs-3">
        <div class="mt-lg-10 mt-md-10 mt-sm-3 mt-xs-3">
          <h1 >Service og vedlikehold</h1>
          <p></p>
          <p>
            Vi tilbyr våre kunder kanskje <span></span> den beste vedlikeholdsavtalen og den
            raskeste servicen i markedet.
            <p></p>
            Vår målsetning er å være hos din bedrift innen to timer ved akutt
            service.
          </p>
          <v-btn  outlined x-large rounded color="red"> Bli firmakunde </v-btn>
        </div>
      </v-col>
    </v-row>
  </v-container>
  
</template>

<script>
export default {
  computed: {
  
    }
};
</script>

<style scoped>
.layout {
  background-color: #f2e5df;
  border-radius: 25px;
}
</style>
