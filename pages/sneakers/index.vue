<template>
<NavBar />
  <v-card
    max-width="400"
    class="mx-auto"
  >
    <v-container>
      <v-row dense>
        <v-col cols="12">
          <v-card
            color="#385F73"
            dark
          >
          </v-card>
        </v-col>
        <v-col
         <v-list-item
                link
                v-for="(s, i) in sneakers"
                :key="`sneakers${i}`"
              >
          cols="12"
        >
          <v-card
            :color="item.color"
            dark
          >
            <div class="d-flex flex-no-wrap justify-space-between">
              <div>
                <v-card-title
                  class="text-h5"
                  v-text="{{ s.name }}"
                ></v-card-title>

                <v-card-subtitle v-text="{{s.price}}"></v-card-subtitle>
              </div>

              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="s.image"></v-img>
              </v-avatar>
            </div>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
   <FooTer />
    <ScrollTop />
</template>

<script>
export default {
  async created() {
    this.sneakers = await this.$content("sneakers").fetch();
  },
  data() {
    return {
      sneakers: null,
    };
  }
};
</script>

<style></style>