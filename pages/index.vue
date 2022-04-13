<template>
  <div>
    <v-sheet color="#19589D" class="pt-8 pb-8 text-center">
      <v-container>
        <v-row align="center" no-gutters class="mt-8">
          <v-col class="px-10">
            <v-card-title class="pa-0 pb-2 cardTitle"
              >What is MAD-FEST?</v-card-title
            >
            <v-card-text class="pa-0 pb-2 text-justify cardSubtitle py-8">
              MAD-Fest 2022 is the first- ever Mobile Application Development
              base competition and exhibition organized by Department of
              Software Engineering & Computer Science in Faculty of Computing,
              NSBM with IEEE Computer Society Student Branch Chapter of NSBM.Not
              only that, we organized MAD Awareness and Preparation sessions for
              all MAD enthusiast techies.We welcome all freshers to Mobile
              Application Development as well as who would like to brush up
              their own knowledge to MAD -Fest Awareness & Preparation
              sessions.Do u look right place to give a value for your valuable
              projects? Join with us and give a great value for your priceless
              effort.
            </v-card-text>
          </v-col>
          <v-col>
            <v-img
              quality="100"
              format="webp"
              fit="contain"
              width="450"
              alt="Brand Logo"
              src="Assets/Home/whatis.png"
            />
          </v-col>
        </v-row>
        <v-row class="dateTime mt-7">
          <v-col cols="4"><v-icon>mdi-calender-range</v-icon>25 of May 2022</v-col>
          <v-col cols="4">09.00 AM Onwards</v-col>
          <v-col cols="4">Faculty of Computing</v-col>
        </v-row>
      </v-container>
    </v-sheet>
  </div>
</template>


<script>
export default {};
</script>

<style>
.cardTitle {
  color: white;
  font-size: 45px;
  font-weight: 600;
  letter-spacing: -0px;
}
.cardSubtitle {
  letter-spacing: 0px;
  line-height: 25px;
  color: white;
  font-size: 20px;
  font-weight: 300;
}
.dateTime{
  font-size: 24px;
  font-weight: 500;
  color: white;
}
</style>
