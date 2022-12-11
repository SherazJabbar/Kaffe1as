<template>
  <v-container fluid class="mt-10">
    <v-row no-gutters>
      <v-col cols="6" lg="6" md="6" sm="6" xs="6">
        <p class="font-weight-black text-lg-h3 text-lg-h3 text-sm-h6 ">Kaffemaskiner</p>
      </v-col>
      <v-col cols="6" lg="6" md="6" sm="6" xs="6"
        ><p class="caption text-right">
          Se alle produktene
          <span>
            <v-btn icon class="caption">
              <v-icon>mdi-chevron-right</v-icon>
            </v-btn>
          </span>
        </p></v-col
      >
    </v-row>
    <v-row>
      <v-carousel height="auto">
        <template v-for="(item, index) in products.length">
          <v-carousel-item
            v-if="(index + 1) % columns === 1 || columns === 1"
            :key="index"
          >
            <v-row class="flex-nowrap" style="height: 100%">
              <template v-for="(product, i) in products">
                <template v-if="+index + i < products.length">
                  <v-col lg="3" md="6" sm="12" xs="12">
                    <v-sheet v-if="+index + i < products.length" height="100%">
                      <v-row
                        class="fill-height d-flex align-center"
                        align="center"
                        justify="center"
                      >
                        <template>
                          <v-card
                            :loading="loading"
                            class="mx-auto my-12"
                            max-width="300"
                          >
                            <v-img
                              height="250"
                              contain
                              src="../assets/images/productImages/img3.svg"
                            ></v-img>
                            <v-card-text>
                              <v-row align="center" class="mx-0">
                                <v-rating
                                  :value="product?.rating"
                                  color="amber"
                                  dense
                                  half-increments
                                  readonly
                                  size="14"
                                ></v-rating>

                                <div class="grey--text ms-4">
                                  {{ product?.rating }} ({{ product?.sold }})
                                </div>
                              </v-row>
                            </v-card-text>

                            <v-card-title>{{ product?.name }}</v-card-title>

                            <v-divider class="mx-4"></v-divider>

                            <v-card-title
                              >{{ product?.originalPrice }},- <span></span></v-card-title
                            >

                            <v-card-actions class="justify-center">
                              <v-btn
                                rounded
                                class="customButton"
                              >
                                <span class="mr-3">
                                  <v-icon> mdi-cart-outline </v-icon>
                                </span>
                                Kjøp
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </template>
                      </v-row>
                    </v-sheet>
                  </v-col>
                </template>
              </template>
            </v-row>
          </v-carousel-item>
        </template>
      </v-carousel>
    </v-row>

    <v-row>
      <v-col> </v-col>
      <v-col> </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: "Item Slider",
  props: {
    productsData: Array,
  },
  data() {
    return {
      products: [],
    };
  },
  mounted() {
    this.products = this.productsData;
    console.log("this.products", this.product);
  },
  computed: {
    columns() {
      if (this.$vuetify.breakpoint.xl) {
        return 4;
      }

      if (this.$vuetify.breakpoint.lg) {
        return 4;
      }

      if (this.$vuetify.breakpoint.md) {
        return 2;
      }

      return 1;
    },
  
  },
};
</script>

<style scoped>
.customButton {
  background-color: #c1272d !important;
  color: white;
  font-weight: light;
  text-transform: lowercase;
  width: 18rem;
  height: 10rem;
}


</style>
