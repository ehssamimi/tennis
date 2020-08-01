<template>
  <b-row class="w-100   ">
         <span class="  Fs0-1 text-white">زمین شماره {{numberField}}</span>
         <span class="mr-auto Fs0-1 ">
                 <img :src="`img/S-img/${types}.png`" alt="green-btn">
         </span>

  </b-row>
</template>

<script>
    export default {
      props:['types','numberField'],
        name: "Header-box-field",
    }
</script>

<style scoped>

</style>
