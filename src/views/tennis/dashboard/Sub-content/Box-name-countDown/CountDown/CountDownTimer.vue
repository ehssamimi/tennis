<template>
  <countdown :time="`${number}` * 60 * 60 * 1000">
    <template slot-scope="props" >
      <p class="text-white mb-0 FS1 ">
        {{ props.hours }}:{{ props.minutes }}:{{ props.seconds }}
      </p>


<!--      Time Remaining：{{ props.days }} days, {{ props.hours }} hours, {{ props.minutes }}-->
<!--      minutes, {{ props.seconds }} seconds.-->
    </template>
  </countdown>
</template>

<script>
  import Vue from 'vue';
  import VueCountdown from '@chenfengyuan/vue-countdown';
  Vue.component(VueCountdown.name, VueCountdown);
  export default {
    props:["number"],
    name: "CountDownTimer",
    data() {
      return {
        countDown: 10
      }
    }
  }
</script>

<style scoped>

</style>
