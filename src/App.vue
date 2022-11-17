<script>
import AppHeader from './components/AppHeader.vue';
export default {
  components: {
    AppHeader
  },
  data() {
    return {

    }
  }
}
</script>

<template>
  <AppHeader/>
  <AppMain/>
</template>

<style lang="scss">
@use "./styles/general.scss" as *; 
@use "./styles/partials/variables.scss" as *;
</style>
