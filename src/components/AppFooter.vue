<template>
  <v-container fluid>
    <v-row no-gutters>
      <v-col cols="12" lg="4" md="4" sm="12" xs="12">
        <div class="ma-8">
          <div
            class="d-flex align-start flex-column mb-6 footer"
            flat
            style="height: 300px"
          >
            <div class="pa-2 mb-auto">
              <v-img
                max-height="60"
                max-width="250"
                src="../assets/images/kaffe-logo.svg"
              >
              </v-img>
            </div>

            <div class="pa-2" flat><p>Abonner på nyhetsbrev</p></div>
            <v-container>
              <div class="pa-2 send-btn-card" flat>
                <v-row class="d-flex flex-row-reverse">
                  <v-text-field rounded filled label="Epost"> </v-text-field>
                  <v-btn class="rounded-pill send-footer-btn" absolute dark x-large>
                    Send
                  </v-btn>
                </v-row>
              </div>
            </v-container>
          </div>
        </div>
      </v-col>
      <v-col cols="12" lg="3" md="3" sm="12" xs="12" class="text-left">
        <div class="text-left ma-8">
          <v-list-item>
            <v-list-item-content class="pr-6">
              <v-list-item-title class="title">Kontakt</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6">
              Kaffe1 AS Postboks 198, 7651 Verdal
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6"> +47 94 472 214 </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6"> +47 94 472 214 </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6"> kaffe1@buisiness.com </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6">
              oddgeirkaffe2@buisiness.com
            </v-list-item-content>
          </v-list-item>
        </div>
      </v-col>
      <v-col cols="12" lg="3" md="3" sm="12" xs="12" class="d-flex">
        <div class="text-left ma-8">
          <v-list-item>
            <v-list-item-content class="pr-6">
              <v-list-item-title class="title">Kontakt</v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6">
              Kaffe1 AS Postboks 198, 7651 Verdal
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6"> +47 94 472 214 </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6"> +47 94 472 214 </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6"> kaffe1@buisiness.com </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-content class="pr-6">
              oddgeirkaffe2@buisiness.com
            </v-list-item-content>
          </v-list-item>
        </div>

        <!-- <v-row class="ma-8">
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
        </v-row> -->
      </v-col>

      <v-col cols="12" lg="2" md="2" sm="12" xs="12">
        <div class="ma-8">
          <v-img
            max-height="100"
            max-width="150"
            contain
            class="my-6"
            src="../assets/images/Fairtrade.svg"
          ></v-img>

          <v-img
            max-height="100"
            max-width="150"
            contain
            src="../assets/images/Rainforest Alliance.svg"
          ></v-img>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {};
</script>

<style>
v-list-item-content {
}

.footer v-card {
  background: #fbf7f5 !important;
}
.send-btn-card {
  width: 100%;
}

.send-footer-btn {
  background-color: #c1272d !important;
  color: white;
}
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
