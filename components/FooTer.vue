<template>
  <v-card
    tile
    flat
    rounded="lg"
    class="pa-md-10 pa-5 text-center"
    color="pink"
  >
    <h2 class="text-md-h6 font-weight-bold">FreeCommerce</h2>
    <p class="text-md-body-2 mt-5">Temukan Sepatu Impianmu dan Belanja Menjadi Lebih Mudah dengan Kami :)</p>
    <div class="text-center">
      <v-btn
        color="pink"
        class="mr-2"
        v-for="(b, i) in sm"
        :key="`sm${i}`"
        fab
        depressed
      >
        <v-icon>{{ b.icon }}</v-icon>
      </v-btn>
    </div>
    <br />
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      sm: [
        { icon: "mdi-facebook", link: "#" },
        { icon: "mdi-twitter", link: "#" },
        { icon: "mdi-instagram", link: "#" },
        { icon: "mdi-youtube", link: "https://www.instagram.com/sylvi_zistiani/" },
      ],
    };
  },
};
</script>

<style></style>
