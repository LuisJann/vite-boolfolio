<script>
// import AppMain from './components/AppMain.vue';
import AppHeader from './components/AppHeader.vue';

export default{
  name:'App',
  components: {
    // AppMain,
    AppHeader,
  }
}
</script>

<template>
<AppHeader/>
<router-view></router-view>
<!-- <AppMain></AppMain> -->
</template>

<style lang="scss">
@use "./styles/general.scss" as *;


</style>