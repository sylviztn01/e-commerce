<template>
  <v-card rounded="lg" class="pa-md-10 pa-5 text-center" color="blue" dark>
    <h2 class="text-md-h3">Newsletter</h2>
    <p class="text-md-h6 mt-5">Ikuti kami untuk informasi discount & lainnya !</p>
    <br />
    <v-sheet color="transparent" class="mx-auto" max-width="400">
      <v-text-field
        v-model="email"
        color="white"
        label="Email"
        outlined
      ></v-text-field>
      <v-btn @click="submit" outlined min-height="50" block>Subscribe</v-btn>
    </v-sheet>
  </v-card>
</template>

<script>
export default {
  data() {
    return {
      email: null,
    };
  },
  methods: {
    async submit() {
      await this.$swal({
        title: "Terimakasih telah mengikuti :)",
        icon: "success",
        allowEscapeKey: false,
        allowOutsideClick: false,
        timer: 2000,
        timerProgressBar: true,
        text: "Anda akan menerima notifikasi untuk informasi discount & lainnya. Check your email !",
        showConfirmButton: false,
      });
    },
  },
};
</script>

<style></style>
