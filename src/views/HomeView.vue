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
    </v-container>
  </v-app>
</template>

<script>
import NavBar from "../components/NavBar";

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
        { img: "1.png", title: "CHAIRS" },
        { img: "4.png", title: "OFFICE CHAIRS" },
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
</style>
