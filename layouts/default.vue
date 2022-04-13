<template>
  <v-app dark>
    <v-app-bar class="NavBarAcrylic" color="transparent" fixed app>
      <v-toolbar-title>
        <v-img width="256" contain :src="require('~/assets/logo_alt.png')"/>
      </v-toolbar-title>
      <v-spacer />

      <v-list dense nav>
        <v-list-item v-for="item in items" :key="item.title" link>
          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-app-bar>
    <v-main class="NavBarAcrylic">
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer absolute app>
      <v-row justify="center" no-gutters>
        <span>&copy; {{ new Date().getFullYear() }} IEEE CS Student Chapter of NSBM</span>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      title: "MADFest",
      loader: null,
      loading4: false,
      items: [
        { title: "Home", route: "/" },
        { title: "Content", route: "/content" },
        { title: "Settings", route: "/settings" },
      ],
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
* {
  font-family: "Poppins";
}
.NavBarAcrylic {
  background-color: transparent;
  backdrop-filter: blur(10px);
}

.context {
  width: 100%;
  position: absolute;
  top:50vh;

}

.context h1{
  text-align: center;
  color: #fff;
  font-size: 50px;
}


.area{
  position: absolute;
  width: 100%;
  height:100vh;
}

@keyframes animate {

  0%{
    transform: translateY(0) rotate(0deg);
    opacity: 1;
    border-radius: 0;
  }

  100%{
    transform: translateY(-1000px) rotate(720deg);
    opacity: 0;
    border-radius: 50%;
  }

}
</style>
