<template>
  <v-container>
    <v-row no-gutters justify="center">
      <v-img contain max-width="50%" :src="require('~/assets/logo.png')"></v-img>
    </v-row>

    <v-row class="mt-8" no-gutters justify="center">
      <v-img contain max-width="50%" :src="require('~/assets/logo_line.png')"></v-img>
    </v-row>

    <v-row class="mt-8" no-gutters justify="center">
      <span style="color: #32ad4a;" class="text-h2 font-weight-bold">Coming Soon...</span>
    </v-row>

    <v-row class="mt-8" no-gutters justify="center">

      <v-btn target="_blank" href="https://www.facebook.com/ieeecsnsbm" icon>
        <v-icon large>mdi-facebook</v-icon>
      </v-btn>

      <v-btn class="ml-2 mr-2" target="_blank" href="https://github.com/IEEE-Student-Branch-NSBM" icon>
        <v-icon large>mdi-github</v-icon>
      </v-btn>

      <v-btn target="_blank" href="https://www.linkedin.com/company/ieee-student-branch-nsbm/" icon>
        <v-icon large>mdi-linkedin</v-icon>
      </v-btn>

    </v-row>
  </v-container>
</template>

<style>

</style>
