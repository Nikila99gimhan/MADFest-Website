<template>
  <v-app dark>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer padless color="#ffffff">
      <v-container>
        <v-row no-gutters justify="center">
          <span class="text-center mb-6 mt-8 font-weight-bold footerTitle">
            ORGANIZED BY
          </span>
        </v-row>
        <v-row class="mb-6">
          <v-col cols="2"></v-col>
          <v-col cols="8">
            <v-row>
              <v-col cols="3"
                ><v-img
                  quality="100"
                  format="webp"
                  :aspect-ratio="16 / 9"
                  contain
                  alt="Brand Logo"
                  src="Assets/Footer/DEpartment.png"
              /></v-col>
              <v-col cols="3"
                ><v-img
                  quality="100"
                  format="webp"
                  :aspect-ratio="16 / 9"
                  contain
                  alt="Brand Logo"
                  src="Assets/Footer/IEEE.png"
              /></v-col>
              <v-col cols="3"
                ><v-img
                  quality="100"
                  format="webp"
                  :aspect-ratio="16 / 9"
                  contain
                  alt="Brand Logo"
                  src="Assets/Footer/WIE.png"
              /></v-col>
              <v-col cols="3"
                ><v-img
                  quality="100"
                  format="webp"
                  :aspect-ratio="16 / 9"
                  contain
                  alt="Brand Logo"
                  src="Assets/Footer/IEEECS.png"
              /></v-col>
            </v-row>
          </v-col>
          <v-col cols="2"></v-col>
        </v-row>
        <hr />
        <v-row align="center" width="100%">
          <v-col cols="4" class="copyrightText" align="left">
            <i>&copy</i> Copyright MAD-FEST 2022. All Rights Reserved - IEEE
            NSBM
          </v-col>
          <v-col cols="4">
            <v-layout justify-center align-center>
              <v-flex shrink>
                <v-img
                  mx-auto
                  quality="100"
                  format="webp"
                  width="150"
                  aspect-ratio="1"
                  contain
                  alt="Brand Logo"
                  src="Assets/MADFEST.png"
                />
              </v-flex> </v-layout
          ></v-col>
          <v-col cols="4" class="copyrightText text-right" align="right">
            Terms of Service <i>&amp</i> Privacy Policy
          </v-col>
        </v-row>
      </v-container>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data() {
    return {
      title: "MADFest",
      loader: null,
      loading4: false,
    };
  },

  watch: {
    loader() {
      const l = this.loader;
      this[l] = !this[l];

      setTimeout(() => (this[l] = false), 3000);

      this.loader = null;
    },
  },
};
</script>

<style>
.footerTitle {
  font-size: 20px;
  color: #0a142f;
}
.copyrightText {
  font-size: 14px;
  font-weight: 300;
}
</style>
