<template>
  <v-container class="mt-10">
    <v-row no-gutters>
      <v-col cols="6" lg="6" md="6" sm="6" xs="6">
        <p class="text-left display-1 font-weight-medium">Kaffemaskiner</p>
      </v-col>
      <v-col cols="6" lg="6" md="6" sm="6" xs="6">
        <v-btn depressed color="white" class="float-right red--text">
          Se alle produktene

          <v-icon right>mdi-chevron-right</v-icon>
        </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <!-- 
 <v-carousel  hide-delimiters> 
        <template v-for="(item, index) in products.length"> 
          <v-carousel-item v-if="(index + 1) % columns === 1 || columns === 1"
            :key="index"
          > 
            <v-row class="flex-nowrap" style="height:100%"> 
              <template v-for="(product, i) in products"> 
                <template v-if="+index + i < products.length"> 
                  <v-col :key="i"> 
                    
                    <v-sheet v-if="(+index + i) < products.length"
                             height="100%"
                    >
                      
                             <template>
                          <v-card
                            :loading="loading"
                            class="mx-auto my-12"
                            max-width="320"
                          >
                            <v-img
                              height="250"
                              contain
                              class="my-5"
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
                                > </v-rating>
                                <div class="font-weight-black ml-1">{{ product?.rating }}</div> 
<v-spacer></v-spacer>
                                <div class="grey--text float-right">
                                 ({{ product?.sold }})
                                </div>
                              </v-row>
                            </v-card-text>

                            <v-card-title class="mr-10 subtitle-1 font-weight-medium product-name-carousel">{{ product?.name }}</v-card-title>

                            <v-divider class="mx-4"></v-divider>

                            <v-card-title
                              >{{ product?.originalPrice }},- <span  class="subtitle-1 text--disabled font-weight-medium px-4 mt-2 text-decoration-line-through">
     3200
    </span></v-card-title
                            >

                            <v-card-actions class="justify-center">
                              <v-btn
                                
                                class="cart-btn rounded-lg"
                              >
                                <span class="mr-3">
                                  <v-icon> mdi-cart-outline </v-icon>
                                </span>
                                Kjøp
                              </v-btn>
                            </v-card-actions>
                          </v-card>
                        </template>
                       
                    </v-sheet>
                  </v-col> 
                </template> 
              </template> 
            </v-row> 
          </v-carousel-item> 
        </template> 
      </v-carousel>   -->

      <v-carousel height="auto" hide-delimiters>
        <template v-for="(item, index) in products.length">
          <v-carousel-item
            v-if="(index + 1) % columns === 1 || columns === 1"
            :key="index"
          >
            <v-row class="flex-nowrap" style="height: 100%">
              <template v-for="(product, i) in products">
                <template v-if="+index + i < products.length">
                  <v-col class="mx-3" lg="3" md="4" sm="4" xs="12">
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
                            max-width="260"
                          >
                            <v-img
                              height="250"
                              contain
                              class="my-5"
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
                                >
                                </v-rating>
                                <div class="font-weight-black ml-1">
                                  {{ product?.rating }}
                                </div>
                                <v-spacer></v-spacer>
                                <div class="grey--text float-right">
                                  ({{ product?.sold }})
                                </div>
                              </v-row>
                            </v-card-text>

                            <v-card-title
                              class="mr-10 subtitle-1 font-weight-medium product-name-carousel"
                              >{{ product?.name }}</v-card-title
                            >

                            <v-divider class="mx-4"></v-divider>

                            <v-card-title
                              >{{ product?.originalPrice }},-
                              <span
                                class="subtitle-1 text--disabled font-weight-medium px-4 mt-2 text-decoration-line-through"
                              >
                                3200
                              </span></v-card-title
                            >

                            <v-card-actions class="justify-center">
                              <v-btn class="cart-btn rounded-lg white--text subtitle-2">
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
      rating: 4.3,
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
        return 3;
      }

      return 1;
    },
  },
};
</script>

<style>
.product-name-carousel {
  line-height: 1.1 !important
  ;
}
.v-window__prev,
.v-window__next {
  /* position: fixed !important; */
}

.cart-btn {
  width: 225px !important;
  height: 52px !important;
  background: #c1272d !important;
}
.customButton {
  background-color: #c1272d !important;
  color: white;
  font-weight: light;
  text-transform: lowercase;
  width: 18rem;
  height: 10rem;
}
</style>
