<template>
  <v-footer>
    <v-card
      elevation="0"
      rounded="0"
      width="100%"
      class="text-center"
      color="#fafafa"
    >
      <v-card-text>
        <v-btn class="mx-4" variant="text" color="transparent">Catalog</v-btn>
        <v-btn class="mx-4" variant="text" color="transparent"
          >Categories</v-btn
        >
        <v-btn class="mx-4" variant="text" color="transparent">Blog</v-btn>
        <v-btn class="mx-4" variant="text" color="transparent"
          >Inspiration</v-btn
        >
        <v-btn class="mx-4" variant="text" color="transparent">About</v-btn>
        <v-btn class="mx-4" variant="text" color="transparent">Contact</v-btn>
      </v-card-text>
      <v-card-text>
        @ {{ new Date().getFullYear() }}
        <strong>Furniture && IdeaPro. All rights Reserved</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
  name: "FooterView",
};
</script>

<style>
.v-footer {
  padding: 8px 0 !important;
}
</style>
