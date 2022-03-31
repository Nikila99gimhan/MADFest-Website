<template>
  <v-app dark>
    <v-app-bar class="NavBarAcrylic" color="transparent" fixed app>
      <v-toolbar-title>
        <v-img width="256" contain :src="require('~/assets/logo_alt.png')"/>
      </v-toolbar-title>
      <v-spacer />
      <v-btn color="secondary" large>Register NOW!</v-btn>
    </v-app-bar>
    <v-main>
      <v-container>
        <Nuxt />
      </v-container>
    </v-main>
    <v-footer absolute app>
      <span>&copy; {{ new Date().getFullYear() }} IEEE Computer Society Student Chapter of NSBM</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      title: 'MADFest'
    }
  }
}
</script>

<style>
.NavBarAcrylic{
  background-color: transparent;
  backdrop-filter: blur(10px);
}
</style>
