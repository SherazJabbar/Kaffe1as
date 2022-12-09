<template>
  <v-container fluid class="mt-10">
    <v-row no-gutters>
      <v-col cols="6">
        <h1 class="font-weight-black">Kaffemaskiner</h1>
      </v-col>
      <v-col cols="6"
        ><p class="caption text-right mt-3">
          Se alle produktene
          <span>
            <v-btn text class="caption">
              <v-icon>mdi-chevron-right</v-icon>
            </v-btn>
          </span>
        </p></v-col
      >
    </v-row>
    <v-row>
  

      <v-carousel>
        <template v-for="(item, index) in products.length">
          <v-carousel-item
            v-if="(index + 1) % columns === 1 || columns === 1"
            :key="index"
          >
            <v-row class="flex-nowrap" style="height: 100%">
              <template v-for="(n, i) in columns">
                <template v-if="+index + i < products.length">
                  <v-col :key="i">
                    <v-sheet v-if="+index + i < products.length" height="100%">
                      <v-row
                        class="fill-height"
                        align="center"
                        justify="center"
                      >
                        <template>
                          <v-card
                            :loading="loading"
                            class="mx-auto my-12"
                            max-width="374"
                          >
                            <template slot="progress">
                              <v-progress-linear
                                color="deep-purple"
                                height="10"
                                indeterminate
                              ></v-progress-linear>
                            </template>

                            <v-img
                              height="250"
                              src="https://cdn.vuetifyjs.com/images/cards/cooking.png"
                            ></v-img>

                            <v-card-title>Cafe Badilico</v-card-title>

                            <v-card-text>
                              <v-row align="center" class="mx-0">
                                <v-rating
                                  :value="4.5"
                                  color="amber"
                                  dense
                                  half-increments
                                  readonly
                                  size="14"
                                ></v-rating>

                                <div class="grey--text ms-4">4.5 (413)</div>
                              </v-row>

                              <div class="my-4 text-subtitle-1">
                                $ • Italian, Cafe
                              </div>

                              <div>
                                Small plates, salads & sandwiches - an intimate
                                setting with 12 indoor seats plus patio seating.
                              </div>
                            </v-card-text>

                            <v-divider class="mx-4"></v-divider>

                            <v-card-title>Tonight's availability</v-card-title>

                            <v-card-text>
                              <v-chip-group
                                v-model="selection"
                                active-class="deep-purple accent-4 white--text"
                                column
                              >
                                <v-chip>5:30PM</v-chip>

                                <v-chip>7:30PM</v-chip>

                                <v-chip>8:00PM</v-chip>

                                <v-chip>9:00PM</v-chip>
                              </v-chip-group>
                            </v-card-text>

                            <v-card-actions>
                              <v-btn
                                color="deep-purple lighten-2"
                                text
                                @click="reserve"
                              >
                                Reserve
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

      slider: [
        "red",
        "green",
        "orange",
        "blue",
        "pink",
        "purple",
        "indigo",
        "cyan",
        "deep-purple",
        "light-green",
        "deep-orange",
        "blue-grey",
      ],
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
    carouselItem() {
      return Number(this.productsData.length / 4);
    },
  },
};
</script>

<style scoped></style>
