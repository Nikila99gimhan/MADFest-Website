<template>
  <v-app dark>
    <div class="area">
      <ul class="circles">
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
        <li></li>
      </ul>
    </div>

    <v-app-bar class="NavBarAcrylic" color="transparent" fixed app>
      <v-toolbar-title>
        <v-img width="256" contain :src="require('~/assets/logo_alt.png')" />
      </v-toolbar-title>
      <v-spacer />

      <v-btn large target="_blank" href="https://ieeensbm.org" icon>
        <v-icon color="primary" large>mdi-web</v-icon>
      </v-btn>

      <v-btn
        class="ma-2"
        :loading="loading4"
        :disabled="loading4"
        color="primary"
        target="_blank"
        href="https://forms.gle/D44xD9GuXX5YXbvh9"
        @click="loader = 'loading4'"
        large
      >
        <v-icon left> mdi-account-arrow-right </v-icon>
        Register Now!
        <template v-slot:loader>
          <span class="custom-loader">
            <v-icon light large>mdi-cached</v-icon>
          </span>
        </template>
      </v-btn>
    </v-app-bar>
    <v-main class="NavBarAcrylic">
      <v-container>
        <Nuxt />
      </v-container>
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
.NavBarAcrylic {
  background-color: transparent;
  backdrop-filter: blur(10px);
}

body {
  font-family: "Exo", sans-serif;
}

.context {
  width: 100%;
  position: absolute;
  top: 50vh;
}

.context h1 {
  text-align: center;
  color: #fff;
  font-size: 50px;
}

.area {
  position: absolute;
  width: 100%;
  height: 100vh;
}

.circles {
  position: absolute;
  color: #32ad4a;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  overflow: hidden;
}

.circles li {
  position: absolute;
  display: block;
  list-style: none;
  width: 20px;
  height: 20px;
  background: rgb(18, 95, 169);
  animation: animate 25s linear infinite;
  bottom: -150px;
}

.circles li:nth-child(1) {
  left: 25%;
  width: 80px;
  height: 80px;
  animation-delay: 0s;
}

.circles li:nth-child(2) {
  left: 10%;
  width: 20px;
  height: 20px;
  animation-delay: 2s;
  animation-duration: 12s;
}

.circles li:nth-child(3) {
  left: 70%;
  width: 20px;
  height: 20px;
  animation-delay: 4s;
}

.circles li:nth-child(4) {
  left: 40%;
  width: 60px;
  height: 60px;
  animation-delay: 0s;
  animation-duration: 18s;
}

.circles li:nth-child(5) {
  left: 65%;
  width: 20px;
  height: 20px;
  animation-delay: 0s;
}

.circles li:nth-child(6) {
  left: 75%;
  width: 110px;
  height: 110px;
  animation-delay: 3s;
}

.circles li:nth-child(7) {
  left: 35%;
  width: 150px;
  height: 150px;
  animation-delay: 7s;
}

.circles li:nth-child(8) {
  left: 50%;
  width: 25px;
  height: 25px;
  animation-delay: 15s;
  animation-duration: 45s;
}

.circles li:nth-child(9) {
  left: 20%;
  width: 15px;
  height: 15px;
  animation-delay: 2s;
  animation-duration: 35s;
}

.circles li:nth-child(10) {
  left: 85%;
  width: 150px;
  height: 150px;
  animation-delay: 0s;
  animation-duration: 11s;
}

.custom-loader {
  animation: loader 1s infinite;
  display: flex;
}
@-moz-keyframes loader {
  from {
    transform: rotate(0);
  }
  to {
    transform: rotate(360deg);
  }
}
@-webkit-keyframes loader {
  from {
    transform: rotate(0);
  }
  to {
    transform: rotate(360deg);
  }
}
@-o-keyframes loader {
  from {
    transform: rotate(0);
  }
  to {
    transform: rotate(360deg);
  }
}
@keyframes loader {
  from {
    transform: rotate(0);
  }
  to {
    transform: rotate(360deg);
  }
}

@keyframes animate {
  0% {
    transform: translateY(0) rotate(0deg);
    opacity: 1;
    border-radius: 0;
  }

  100% {
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
    border-radius: 50%;
  }
}
</style>
