<template>
  <v-container fluid >
    <v-row class="text-center" :column="$vuetify.breakpoint.mdAndDown">
      <v-col cols="12" lg="6" md="6" sm="6" xs="4" class="d-flex" >
        <div  class="pa-2 align-self-center">
          <h1 class="text-left">Ny kaffemaskin til din bedrift?</h1>
          <br>
          <p class="caption text-left display-1">
            Vi tilbyr kaffemaskiner for bedrifter av alle størrelser. Fri
            levering, montering og justering av maskinen etter din smak, og en
            meget god vedlikeholdsavtale. Kontakt oss i dag for et uforpliktende
            tilbud!
          </p>
          <div class="text-left">
            <v-btn rounded large class="customButton">
              Se våre kaffeautomater
            </v-btn>
          </div>
        </div>
      </v-col>

      <v-col cols="12" lg="6" md="6" sm="6" xs="4">
        <div>
          <v-img src="../assets/images/img bg.svg"> </v-img>
        </div>
      </v-col>

      
    </v-row>
    <v-row>
      <v-col cols="12" lg="12" md="12" sm="6" xs="4">
          <v-app-bar flat class="d-flex justify-space-around mainAppbar">
              <v-btn class="buttonGroup" text
              >Kaffemaskiner
              <span>
                <v-icon>mdi-circle-small</v-icon>
              </span>
            </v-btn>

            <v-btn text class="buttonGroup"
              >Kaffe
              <span>
                <v-icon >mdi-circle-small</v-icon>
              </span>
            </v-btn>

            <v-btn text class="buttonGroup"
              >Kaffemaskiner
              <span>
                <v-icon >mdi-circle-small</v-icon>
              </span>
            </v-btn>

            <v-btn text class="buttonGroup"
              >Kaffe
              <span>
                <v-icon >mdi-circle-small</v-icon>
              </span>
            </v-btn>

            <v-btn text class="buttonGroup"
              >Kaffemaskiner
              <span>
                <v-icon >mdi-circle-small</v-icon>
              </span>
            </v-btn>

            <v-btn text class="buttonGroup"
              >Kaffe
              <span>
                <v-icon >mdi-circle-small</v-icon>
              </span>
            </v-btn>

            <v-btn text class="buttonGroup"
              >Kaffemaskiner
              <span>
                <v-icon >mdi-circle-small</v-icon>
              </span>
            </v-btn>
           
          </v-app-bar>
      </v-col>
    </v-row>
  <item-slider :productsData="data"/>

  </v-container>
</template>

<script>
import ItemSlider from '@/components/ItemSlider.vue';
import { productsData } from '@/utils/productData';
export default {
  name: "Homepage",

  data(){
    return{
      data : productsData
    }
  },
  mounted(){
    console.log("productsData:", productsData)
  },

  components:{
    'item-slider': ItemSlider
  }
};
</script>

<style scoped>
.img-1 {
  position: absolute;
  width: 703.54px;
  height: 621.99px;
  left: 606px;
  top: 68px;
}
.img-2 {
  position: absolute;
  width: 596.57px;
  height: 373.78px;
  left: 792.89px;
  top: 100px;
  border-radius: 50%;
  background: #f2e5df;
  transform: rotate(30deg);
}
.image {
  position: absolute;
  width: 320px;
  height: 488px;
  left: 900px;
  top: 50px;
}
.customButton {
  background-color: #c1272d !important;
  color: white;
  font-weight: light;
  text-transform: lowercase;
}

.appBar {
  margin-top: 10rem;
}

.mainAppbar {
  background-color: #c1272d !important;
}
.buttonGroup {
  color: white;
  text-transform: lowercase;
}

.main {
  margin-top: 10rem;
}

h1 {
  font-size: 3rem;
}
</style>
