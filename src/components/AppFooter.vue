<template>
  <v-container fluid>
    <v-row no-gutters>
      <v-col lg="4">
        <div class="mt-10 ml-10">
          <h1>
            Kaffe<svg
              width="27"
              height="27"
              viewBox="0 0 37 37"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
            >
              <path
                fill-rule="evenodd"
                clip-rule="evenodd"
                d="M18.2133 0.000132725C14.6094 0.0139762 11.0906 1.11145 8.10215 3.15367C5.11368 5.1959 2.78985 8.09108 1.42473 11.4729C0.0596176 14.8546 -0.285429 18.571 0.433255 22.1517C1.15194 25.7323 2.90205 29.0164 5.46213 31.5882C8.02221 34.1601 11.2772 35.9041 14.8152 36.5996C18.3531 37.2952 22.0151 36.9109 25.3376 35.4956C28.6602 34.0802 31.4939 31.6973 33.4804 28.6484C35.4668 25.5996 36.5166 22.0217 36.4969 18.3677C36.4705 13.475 34.5304 8.79277 31.1024 5.34906C27.6744 1.90535 23.0388 -0.0184038 18.2133 0.000132725ZM23.4612 33.4841C20.0859 33.9359 16.6677 33.9523 13.2884 33.5329C12.6972 31.2714 14.2026 31.118 15.0996 30.3479C15.0698 24.2684 15.0411 18.1842 15.0136 12.0953C14.4569 11.3008 12.6079 12.8167 11.8827 11.8479C10.807 9.62125 13.9448 8.87553 15.5154 7.60015C17.5775 5.92055 18.3095 2.69725 22.0178 3.07011L22.1415 29.7869C22.2515 31.3585 24.0351 31.2191 23.4612 33.4841Z"
                fill="#C1272D"
              /></svg
            >as
          </h1>
          <p></p>
          <p></p>
          <p></p>
          <p></p>
          <p></p>
          <p></p>
          <p>Abonner på nyhetsbrev</p>
          <v-text-field rounded filled label="Epost"> </v-text-field>
          <!-- <template v-slot:append>
              <v-btn  class="customButton" rounded>
                show
              </v-btn>
            </template> -->
        </div>
      </v-col>
      <v-col lg="4" class="text-left">
        <div class="sectionB text-left">
          <h3>Kontakt</h3>
          <p></p>
          <p></p>
          <p>Kaffe1 AS</p>
          <p>Postboks 198, 7651 Verdal</p>
          <p></p>
          <p></p>
          <p>+47 94 472 214</p>
          <p>+47 94 472 214</p>
          <p></p>
          <p></p>
          <p>kaffe1@buisiness.com</p>
          <p>oddgeirkaffe2@buisiness.com</p>
        </div>
      </v-col>
      <v-col lg="4">
        <v-row>
          <v-col>
            <div>
              <h3>Menu</h3>
              <p></p>
              <p>Kaffemaskiner</p>
              <p></p>
              <p></p>
              <p>Kaffebønner</p>
              <p></p>
              <p></p>
              <p>Om oss</p>
              <p></p>
              <p></p>
              <p>Kontakt oss</p>
            </div>
          </v-col>
          <v-col>
            <div>
              <v-img
              max-height="100"
                max-width="150"
                contain
                src="../assets/images/Fairtrade.svg"
              ></v-img>
            </div>
            <div class="mt-5">
              <v-img
                max-height="100"
                max-width="150"
                contain
                src="../assets/images/Rainforest Alliance.svg"
              ></v-img>
            </div>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style scoped>
.customButton {
  background-color: #c1272d !important;
  color: white;
  font-weight: light;
  text-transform: lowercase;
}

.sectionB {
  margin-left: 10rem;
}
</style>
