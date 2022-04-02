<template>
  <div>
    <div class="countDownCards">{{days}} Days</div>
    <div class="countDownCards">{{hours}} Hours</div>
    <div class="countDownCards">{{minutes}} Minutes</div>
    <div class="countDownCards">{{seconds}} Seconds</div>
  </div>
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
          const difference = +new Date("2022-05-05") - +new Date();

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

<style>
  .countDownCards{
    display: inline-block;
    margin: 20px;
  }
</style>
