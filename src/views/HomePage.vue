<template>
  <v-row>
    <v-container>
      <v-row class="text-center" :column="$vuetify.breakpoint.mdAndDown">
        <v-col cols="12" lg="6" md="6" sm="6" xs="4" class="d-flex">
          <div class="py-16 align-self-center">
            <p class="text-left display-2 font-weight-medium">
              Ny kaffemaskin til din bedrift?
            </p>
            <br />
            <p class="text-left font-weight-regular subtitle-1">
              Vi tilbyr kaffemaskiner for bedrifter av alle størrelser. Fri levering,
              montering og justering av maskinen etter din smak, og en meget god
              vedlikeholdsavtale. Kontakt oss i dag for et uforpliktende tilbud!
            </p>
            <div class="text-left py-6">
              <v-btn rounded x-large class="customButton"> Se våre kaffeautomater </v-btn>
            </div>
          </div>
        </v-col>

        <v-col cols="12" lg="6" md="6" sm="6" xs="12">
          <div>
            <v-img src="../assets/images/img bg.svg"> </v-img>
          </div>
        </v-col>
      </v-row>
    </v-container>

    <v-row>
      <v-app-bar flat class="px-8 end-toolbar">
        <v-btn class="buttonGroup" text
          >Kaffemaskiner
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
        <v-spacer></v-spacer>

        <v-btn text class="buttonGroup"
          >Kaffe
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text class="buttonGroup"
          >Kaffemaskiner
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text class="buttonGroup"
          >Kaffe
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text class="buttonGroup"
          >Kaffemaskiner
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text class="buttonGroup"
          >Kaffe
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
        <v-spacer></v-spacer>
        <v-btn text class="buttonGroup"
          >Kaffemaskiner
          <span>
            <v-icon>mdi-circle-medium</v-icon>
          </span>
        </v-btn>
      </v-app-bar>
    </v-row>
    <v-row :column="$vuetify.breakpoint.mdAndDown">
      <item-slider :productsData="data" />
    </v-row>
    <v-row>
      <jumbo-tron />
    </v-row>

    <v-row :column="$vuetify.breakpoint.mdAndDown">
      <item-slider :productsData="data" />
    </v-row>

    <v-container :column="$vuetify.breakpoint.mdAndDown">
      <v-row class="my-10">
        <v-col cols="12" sm="6">
          <v-col class="mt-10">
            <h1>Litt om oss</h1>
            <p></p>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipiscing elit. Etiam eu turpis
              molestie, dictum est a, mattis tellus. Sed dignissim, metus nec fringilla
              accumsan, risus sem sollicitudin lacus, ut interdum tellus elit sed risus.
              Maecenas eget condimentum velit, sit amet feugiat lectus. Class aptent
              taciti sociosqu ad litora torquent per conubia nostra, per inceptos
              himenaeos.
            </p>
            <p>
              Praesent auctor purus luctus enim egestas, ac scelerisque ante pulvinar.
              Donec ut rhoncus ex. Suspendisse ac rhoncus nisl, eu tempor urna. Curabitur
              vel bibendum lorem. Morbi convallis convallis diam sit amet lacinia. Aliquam
              in elementum tellus.
            </p>
            <v-btn outlined x-large rounded color="red"> Bli firmakunde </v-btn>
          </v-col>
        </v-col>
        <v-col cols="12" sm="6" class="text-left">
          <v-img
            class="fill-height"
            contain
            src="../assets/images/placeholder for arbeidere.svg"
          >
          </v-img>
        </v-col>
      </v-row>
    </v-container>
  </v-row>
</template>

<script>
import ItemSlider from "@/components/ItemSlider.vue";
import Jumbotron from "@/components/Jumbotron.vue";
import AppFooter from "@/components/AppFooter.vue";
import { productsData } from "@/utils/productData";
export default {
  name: "Homepage",

  data() {
    return {
      data: productsData,
    };
  },
  mounted() {
    console.log("productsData:", productsData);
  },

  components: {
    "item-slider": ItemSlider,
    "app-footer": AppFooter,
    "jumbo-tron": Jumbotron,
  },
};
</script>

<style scoped>
.end-toolbar {
  background-color: #ce666a !important;
}
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
  box-shadow: 0px 8px 15px rgb(193, 39, 45, 0.2);
  color: white;
  font-weight: light;
  text-transform: lowercase;
  padding: 16px 32px !important;
}

.appBar {
  margin-left: 5rem;
}
@media screen and (min-width: 480px) {
  .appBar {
    margin: 0%;
  }
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
