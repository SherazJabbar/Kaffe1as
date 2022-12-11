<template>
  <div>
    <div class="desktopMenu">
      <v-toolbar flat>
        <!-- <v-btn icon @click="switchTheme()">
        <v-icon v-if="theme === themes[0]">mdi-weather-sunny</v-icon>
        <v-icon v-if="theme === themes[1]">mdi-weather-night</v-icon>
      </v-btn> -->
        <v-toolbar-title
          ><v-btn text x-large
            ><router-link to="/" tag="li"
              >Kaffe<svg
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
              >as</router-link
            ></v-btn
          ></v-toolbar-title
        >
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn text
            ><router-link to="/" tag="li">Maskiner </router-link>
          </v-btn>
          <v-btn text
            ><router-link to="/" tag="li">Kaffebønner </router-link>
          </v-btn>
          <v-btn text><router-link to="/" tag="li">Te </router-link> </v-btn>
          <v-btn text
            ><router-link to="/" tag="li">Tilbehør </router-link>
          </v-btn>
          <v-btn text>
            <router-link to="/" tag="li">Sjokolade </router-link>
          </v-btn>
          <!-- <v-avatar color="grey lighten-1" class="mt-2">
          <span class="white--text text-h5">
            
          </span>
        </v-avatar> -->
        </v-toolbar-items>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-sm-and-down">
          <v-btn text
            ><router-link to="/" tag="li"
              ><v-icon>mdi-magnify</v-icon>
            </router-link>
          </v-btn>
          <v-btn text
            ><router-link to="/" tag="li"
              ><v-icon>mdi-heart-outline</v-icon>
            </router-link>
          </v-btn>
          <v-btn text
            ><router-link to="/" tag="li"
              ><v-icon>mdi-account-circle-outline</v-icon>
            </router-link>
          </v-btn>
          <v-btn text
            ><router-link to="/" tag="li"
              ><v-icon>mdi-cart-outline</v-icon>
            </router-link>
          </v-btn>
          <v-btn text class="caption">
            No
            <v-icon>mdi-chevron-down</v-icon>
          </v-btn>
          <!-- <v-avatar color="grey lighten-1" class="mt-2">
          <span class="white--text text-h5">
            
          </span>
        </v-avatar> -->
        </v-toolbar-items>
      </v-toolbar>
    </div>
    <div class="mobileMenu">
      <v-app-bar flat>
        <v-app-bar-nav-icon @click.stop="drawer = !drawer"></v-app-bar-nav-icon>

        <v-spacer></v-spacer>
        <v-btn icon
          ><router-link to="/" tag="li"
            ><v-icon>mdi-magnify</v-icon>
          </router-link>
        </v-btn>
        <v-btn icon
          ><router-link to="/" tag="li"
            ><v-icon>mdi-heart-outline</v-icon>
          </router-link>
        </v-btn>

        <v-btn icon
          ><router-link to="/" tag="li"
            ><v-icon>mdi-account-circle-outline</v-icon>
          </router-link>
        </v-btn>
        <v-btn icon
          ><router-link to="/" tag="li"
            ><v-icon>mdi-cart-outline</v-icon>
          </router-link>
        </v-btn>
        <v-btn icon class="caption">
          No
          <v-icon>mdi-chevron-down</v-icon>
        </v-btn>
      </v-app-bar>

      <v-navigation-drawer v-model="drawer" absolute left temporary>
        <v-list nav dense>
          <v-list-item-group v-model="group" class="text-center">
            <v-list-item-title class="mt-5">
              <v-btn plain
                ><router-link to="/" tag="li"
                  >Kaffe<svg
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
                  >as</router-link
                ></v-btn
              >
            </v-list-item-title>
            <div class="mt-10">
              <v-list-item>
                <v-list-item-title>
                  <v-btn text
                    ><router-link to="/" tag="li">Maskiner </router-link>
                  </v-btn></v-list-item-title
                >
              </v-list-item>

              <v-list-item>
                <v-list-item-title>
                  <v-btn text
                    ><router-link to="/" tag="li">Kaffebønner </router-link>
                  </v-btn></v-list-item-title
                >
              </v-list-item>

              <v-list-item>
                <v-list-item-title
                  ><v-btn text
                    ><router-link to="/" tag="li">Te </router-link>
                  </v-btn></v-list-item-title
                >
              </v-list-item>

              <v-list-item>
                <v-list-item-title>
                  <v-btn text
                    ><router-link to="/" tag="li">Tilbehør </router-link>
                  </v-btn></v-list-item-title
                >
              </v-list-item>

              <v-list-item>
                <v-list-item-title>
                  <v-btn text>
                    <router-link to="/" tag="li">Sjokolade </router-link>
                  </v-btn></v-list-item-title
                >
              </v-list-item>
            </div>
          </v-list-item-group>
        </v-list>
      </v-navigation-drawer>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    drawer: false,
    group: null,
  }),

  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>

<style scoped>
@media screen and (max-width: 600px) {
  .desktopMenu {
    display: none;
  }
}
@media screen and (min-width: 480px) {
  .mobileMenu {
    display: none;
  }
}
li {
  list-style: none;
  text-transform: lowercase;
}
</style>
