<template>
  <v-app dark>
    <v-main>
      <Nuxt />
    </v-main>
    <v-footer dark padless>
      <v-card class="flex" flat tile>
        <v-card-title class="primary">
          <strong class="subheading"
            >Get connected with us on social networks!</strong
          >

          <v-spacer></v-spacer>

          <v-btn
            class="ml-2 mr-2 mx-4"
            target="_blank"
            href="https://www.facebook.com/ieeecsnsbm"
            icon
          >
            <v-icon large>mdi-facebook</v-icon>
          </v-btn>

          <v-btn
            class="ml-2 mr-2 mx-4"
            target="_blank"
            href="https://github.com/IEEE-Student-Branch-NSBM"
            icon
          >
            <v-icon large>mdi-github</v-icon>
          </v-btn>

          <v-btn
            class="ml-2 mr-2 mx-4"
            target="_blank"
            href="https://www.linkedin.com/company/ieee-student-branch-nsbm/"
            icon
          >
            <v-icon large>mdi-linkedin</v-icon>
          </v-btn>
        </v-card-title>

        <v-card-text class="py-2 white--text text-center">
          <span
            >&copy; {{ new Date().getFullYear() }} IEEE CS Student Chapter of
            NSBM</span
          >
        </v-card-text>
      </v-card>
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
@import url("https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,500;1,600;1,700;1,800;1,900&display=swap");

* {
  font-family: "Poppins", "sans-serif" !important;
  letter-spacing: -0px;
}

::-webkit-scrollbar-track {
  border-radius: 10px;
  opacity: 0.3;
  background-color: #00629b;
}
::-webkit-scrollbar-thumb {
  border-radius: 10px;
  opacity: 1;
  background-color: #ffffff;
}
::-webkit-scrollbar {
  width: 8px;
  opacity: 0.3;
  background-color: #00629b;
}
</style>
