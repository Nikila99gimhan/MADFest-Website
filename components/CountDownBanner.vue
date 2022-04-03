<template>
    <v-row no-gutters justify="center">

      <v-col cols="12" class="d-md-none d-lg-none d-xl-none"></v-col>

      <v-col cols="4" sm="3" md="2" lg="2" xl="2">
        <div class="countDownCards" > <span> {{days}} </span> <br/> DAYS</div>
      </v-col>

      <v-col cols="4" sm="3" md="2" lg="2" xl="2">
        <div class="countDownCards xs-6"> <span> {{hours}} </span> <br/> HOURS</div>
      </v-col>

      <v-col cols="12" class="d-md-none d-lg-none d-xl-none"></v-col>

      <v-col cols="4" sm="3" md="2" lg="2" xl="2">
        <div class="countDownCards"> <span> {{minutes}} </span> <br/> MINUTES</div>
      </v-col>

      <v-col cols="4" sm="3" md="2" lg="2" xl="2">
        <div class="countDownCards"> <span> {{seconds}} </span> <br/> SECONDS</div>
      </v-col>
    </v-row>

</template>

<script>

export default {

    mounted(){
      this.countdownTimer(this)
    },
    data: () => {
      return {
        days: 0,
        hours: 0,
        minutes: 0,
        seconds: 0
      }
    },
    methods : {
      countdownTimer(context) {

        setInterval(()=> {
          const difference = +new Date("2022-05-15") - +new Date();

          if (difference > 0) {
            const parts = {
              days: Math.floor(difference / (1000 * 60 * 60 * 24)),
              hours: Math.floor((difference / (1000 * 60 * 60)) % 24),
              minutes: Math.floor((difference / 1000 / 60) % 60),
              seconds: Math.floor((difference / 1000) % 60),
            };

            context.days = parts.days;
            context.hours = parts.hours;
            context.minutes = parts.minutes;
            context.seconds = parts.seconds;

          }
        },500)
      }
    }
  }



</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Orbitron&display=swap');

  .countDownCards span{
    font-size: 30px;
    font-weight: bold;
  }

  .countDownCards{
    box-shadow: 6px 6px 8px lightgrey;
    margin: 15px auto;
    text-align: center;
    padding: 20px 5px;
    width:120px;
    height:120px;
    border-radius:50%;
    background: rgba(18, 85, 150,0.9);
    font-family: 'Orbitron', sans-serif;
    color: #ffffff;
    font-size: 17px;
  }

  @media only screen and (max-width: 600px) {
    div.countDownCards {
      margin-top: 15px;
    }
  }

  @media only screen and (min-width: 600px) and (max-width: 960px){
    div.countDownCards {
      margin-top: 20px;
    }
  }

  /*  div.countDownCards span{*/
  /*    font-size: 25px;*/
  /*  }*/

  /*}*/
</style>
