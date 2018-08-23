<template>
  
<div>
  helloasdasdasdasdasd
</div>

</template>

<script>
import Logo from '~/components/Logo.vue'
import VuetifyLogo from '~/components/VuetifyLogo.vue'

export default {
  components: {
    Logo,
    VuetifyLogo
  },
  mounted(){
    this.$router.push('/portfolio')
  }
}
</script>

<style>

</style>
