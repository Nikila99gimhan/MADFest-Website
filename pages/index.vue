<template>
  <v-container>
    <v-row>
      <CountDownBanner />
    </v-row>
    <v-row class="mt-8" no-gutters justify="center">
      <v-img
        contain
        max-width="45%"
        :src="require('~/assets/logo.png')"
      ></v-img>
    </v-row>

    <v-row class="mt-8" no-gutters justify="center">
      <v-img
        contain
        max-width="50%"
        :src="require('~/assets/logo_line.png')"
      ></v-img>
    </v-row>
    <v-row class="my-16">
      <TimeLine/>
    </v-row>
    <v-row>
      <RulesBanner />
    </v-row>

    <v-row>
      <FaqBanner/>
    </v-row>
    
  </v-container>
</template>


<script>
import CountDownBanner from "../components/CountDownBanner";
import RulesBanner from "../components/RulesBanner";
import FaqBanner from "../components/FaqBanner";
import TimeLine from "../components/TimeLineBanner.vue";

export default {
  components: {
    CountDownBanner,
    RulesBanner,
    FaqBanner,
    TimeLine,
  },
};
</script>

<style>
</style>
