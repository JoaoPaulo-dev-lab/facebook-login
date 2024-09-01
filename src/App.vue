<script lang="ts">
import {defineComponent} from 'vue'
import FacebookLogin from './components/login/FacebookLogin.vue'
import FacebookFooter from './components/footer/FacebookFooter.vue';

export default defineComponent({
    components: {FacebookLogin, FacebookFooter}
})

</script>

<template>
  <FacebookLogin/>
  <FacebookFooter/>
</template>

<style scoped>
*{
  background-color: #f0f2f5;
  font-family: SFProDisplay-Regular, Helvetica, Arial, sans-serif;
  
}
</style>
