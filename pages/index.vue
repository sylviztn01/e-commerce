<template>
  <div>
    <NavBar />
    <HomeCarousel :sale_items="sale_items" />
    <br /><br />
    <v-container>
      <h1 class="text-md-h4 text-h6">Lihat selengkapnya...</h1>
      <br />
      <ProductSlider :products="products" />
      <br /><br /><br />
      <NewsLetter />
    </v-container>
    <br /><br />
    <FooTer />
    <ScrollTop />
  </div>
</template>

<script>
export default {
  async created() {
    this.sale_items = await this.$content("products")
      .where({ onSale: true })
      .fetch();
    this.products = await this.$content("products").fetch();
  },
  data() {
    return {
      products: null,
      sale_items: null,
    };
  },
};
</script>

<style></style>
