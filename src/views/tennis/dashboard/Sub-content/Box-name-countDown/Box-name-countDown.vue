<template>
  <div class="w-75 d-flex flex-column justify-content-between align-items-center">
    <CountDownTimer :number="number"/>
    <span class="text-white Fs0-1">{{name}}</span>
  </div>
</template>

<script>
    import CountDownTimer from "./CountDown/CountDownTimer";
    export default {
      props:["name","number"],
        name: "Box-name-countDown",
      components: {CountDownTimer}
    }
</script>

<style scoped>

</style>
