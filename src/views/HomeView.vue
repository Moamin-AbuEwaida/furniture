<template>
  <v-app>
    <NavBar />
    <v-container fluid>
      <v-card
        color="#f7f7f7"
        height="180px"
        tile
        flat
        class="d-flex align-center justify-center mt-12"
        dark
      >
        <v-row>
          <v-col cols="12" sm="12">
            <v-item-group mandatory class="mt-n1">
              <v-container>
                <v-row justify="center" class="space">
                  <v-col
                    cols="12"
                    xs="12"
                    sm="4"
                    v-for="(category, i) in categories"
                    :key="i"
                  >
                    <v-item v-slot="{ active, toggle }">
                      <v-card
                        :color="active ? '#d5f0c0' : 'white'"
                        :class="active ? 'borderme' : 'borderout'"
                        class="d-flex align-center rounded-lg mx-2"
                        dark
                        height="170"
                        @click="toggle"
                        flat
                      >
                        <v-row>
                          <v-col cols="12" sm="12">
                            <v-list-item three-line class="text-center">
                              <v-list-item-content>
                                <div align="center" justify="text-center">
                                  <v-img
                                    :src="category.img"
                                    max-height="80"
                                    max-width="80"
                                    contain
                                  ></v-img>
                                </div>
                                <v-list-item-subtitle
                                  :class="active ? 'green--text' : 'back-text'"
                                  class="caption mt-4"
                                >
                                  {{ category.title }}
                                </v-list-item-subtitle>
                              </v-list-item-content>
                            </v-list-item>
                          </v-col>
                        </v-row>
                      </v-card>
                    </v-item>
                  </v-col>
                </v-row>
              </v-container>
            </v-item-group>
          </v-col>
        </v-row>
      </v-card>
      <v-toolbar color="transparent" class="mt-3">
        <v-checkbox
          v-model="chair"
          label="Chairs"
          class="check mt-4 black--text"
          color="black"
        ></v-checkbox>
        <v-checkbox
          v-model="other"
          label="Othermass"
          class="check mx-4 mt-4 black--text"
          color="black "
        ></v-checkbox>
        <v-divider vertical class="mx-2"></v-divider>
        <v-btn variant="text" class="ml-10"
          >LEATHER COLORS
          <v-icon right class="ml-2 mt-n1">fas fa-caret-right</v-icon>
        </v-btn>
        <v-divider vertical class="mx-2"></v-divider>
        <v-btn variant="text" class="mx-10"
          >Choose Design
          <v-icon right class="ml-2 mt-n1">fas fa-caret-right</v-icon>
        </v-btn>
        <v-divider vertical class="mx-2"></v-divider>
        <span class="text-caption mx-2">Price tile</span>
        <v-slider v-model="sliders" class="mt-5"></v-slider>
        <span class="text-caption mx-2">€9,432</span>
      </v-toolbar>
      <v-divider class="mt-2"></v-divider>
      <v-toolbar color="transparent">
        <v-toolbar-title>LOUNGE CHAIRS</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn variant="text" color="transparent" class="grey--text"
          >sort by</v-btn
        >
        <v-btn variant="text" color="transparent" class="black--text"
          >name</v-btn
        >
        <v-btn variant="text" color="transparent" class="grey--text"
          >popularity</v-btn
        >
        <v-btn variant="text" color="transparent" class="grey--text"
          >price</v-btn
        >
      </v-toolbar>
      <v-row>
        <v-col cols="12" sm="3" v-for="(chair, i) in chairs" :key="i">
          <v-card height="300" align="center" flat tile>
            <v-img :src="chair.image" width="200" height="200" contain></v-img>
            <v-card-text class="mt-n1">
              <strong>{{ chair.title }}</strong>
            </v-card-text>
            <v-card-text class="mt-n4">
              <strong>{{ chair.price }}</strong>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
      <v-divider></v-divider>
      <v-toolbar color="transparent">
        <v-toolbar-title class="text-caption">show more chairs</v-toolbar-title>
        <v-spacer></v-spacer>
        <v-icon color="grey" left class="mr-4 mt-n1"
          >fas fa-long-arrow-alt-left</v-icon
        >
        <span class="text-caption">1</span>
        <v-icon color="grey" left class="ml-4 mt-n1 mr-2"
          >fas fa-long-arrow-alt-right</v-icon
        >
      </v-toolbar>
    </v-container>
    <Footer />
  </v-app>
</template>

<script>
import NavBar from "../components/NavBar";
import Footer from "@/components/Footer.vue";

export default {
  name: "HomePage",
  setup() {
    return {
      chair: true,
      other: false,
      slider2: 50,
      categories: [
        { img: "0.png", title: "SLEEPING BEDS" },
        { img: "2.png", title: "LOUNGE CHAIRS" },
        { img: "4.png", title: "CHAIRS" },
        { img: "1.png", title: "OFFICE CHAIRS" },
        { img: "8.png", title: "TABLES NIGHTSTANDS" },
        { img: "6.png", title: "KITCHEN FURNITURE" },
      ],
      chairs: [
        {
          class: "pa-0",
          image: "C1.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C2.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C3.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C4.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C5.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C6.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C7.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C8.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C9.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C10.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C11.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C12.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C13.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C14.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C15.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
        {
          class: "pa-0",
          image: "C16.png",
          title: "Modern Lounge",
          price: "€ 120.00",
        },
      ],
    };
  },

  components: {
    NavBar,
    Footer,
  },
};
</script>

<style scoped>
.v-container {
  width: 100%;
  padding: 16px 0px !important;
  margin-right: auto;
  margin-left: auto;
}
.v-card.borderme {
  border: 2px solid black !important;
}
.v-card.borderout {
  border: 1px solid #d5f0db !important;
}
/* .black--text /deep/ label {
  color: black;
} */
</style>
