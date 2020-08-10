<template>
  <b-col cols="6" @click="form=!form" class="pb-2 h-min20em">
    <div class="w-100 position-relative p-3  h-100  d-flex flex-column   br-box-img" :class="bg">
      <HeaderBoxField :types="`white-btn`" :numberField="1"/>
      <div class="mt-3">
        <p class="  text-white Fs-v-1-5  font-w600  mb-0 text-center text-nowrap"   >زمین غیر فعال است</p>
      </div>
    </div>
    <b-img src="img/S-img/bg-light.png" class=" w-100  h-100 d-none" />

  </b-col>
</template>

<script>
    import HeaderBoxField from "../Header-box-field/Header-box-field";
    export default {
      props: {
        bg: {
          type: String,
          default: 'Bg-light',
          description: 'border-bottom line'
        },
        tag: {
          type: String,
          default: 'Bg-light',
          description: 'back-ground color'
        }
        },

        name: "Dashboard-field-manager",
      components: {HeaderBoxField}
    }
</script>

<style scoped>

</style>
