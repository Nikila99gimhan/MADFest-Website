<template>
  <v-app dark>
    <v-toolbar>
      <v-toolbar-title>
        
        <v-img 
        src="Assets/Navigation/logo_alt.png"
        width="250"
        class="ml-sm-16"
        ></v-img>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-toolbar-items class="hidden-sm-and-down">
        <v-btn v-for="item in menu" :key="item.link" :to="item.link" >{{
          item.title
        }}</v-btn>
      </v-toolbar-items>
      <v-menu class="hidden-md-and-up">
        <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>
        <v-list>
          <v-list-item v-for="item in menu" :key="item.icon">
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-toolbar>

    <!-- main container -->
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
      menu: [
        { icon: "home", title: "Link A" },
        { icon: "info", title: "Link B" },
        { icon: "warning", title: "Link C" },
      ],
    };
  },

  methods: {
    menuItems() {
      return this.menu;
    },
  },

  // watch: {
  //   loader() {
  //     const l = this.loader;
  //     this[l] = !this[l];

  //     setTimeout(() => (this[l] = false), 3000);

  //     this.loader = null;
  //   },
  // },
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
.footerTitle {
  font-size: 20px;
  color: #0a142f;
}
.copyrightText {
  font-size: 14px;
  font-weight: 300;
}
</style>
