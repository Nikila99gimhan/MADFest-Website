<template>
  <v-row padless no-gutters justify="center" class="my-10">
    <v-card class="mx-auto px-10 py-10" id="myId" max-width="100%" tile elevation="0">
      <v-card-title primary-title class="justify-center" :class="`headline font-weight-bold primary--text`"> Rules and Regulations </v-card-title>
      <v-list-item v-for="(item, i) in items" :key="i">
        <v-list-item-content>
          <v-list-item-title v-text="item.text" :class="` font-weight-medium primary--text`"></v-list-item-title>
        </v-list-item-content>
      </v-list-item>
    </v-card>
  </v-row>
</template>

<script>
export default {
  data: () => ({
    items: [
        { text: "⭕ Only the team leader require to fill out the form with the rest of other member’s details." }, 
        { text: "⭕ Please consider that one team can have maximum 06 members and the minimum 03 members." },
        { text: "⭕ Group members allow to use any programming language and any framework to develop the Mobile Application project." },
        { text: "⭕ Plagiarism will be detected." },
        { text: "⭕ Every participant should accept and respect the final decision made by the judge board." },
        ],
  }),
};
</script>

<style>
#myId {
  background: url("../assets/rules-bg.png") no-repeat center center;
  background-size: 100% 100%;
  
}
</style>