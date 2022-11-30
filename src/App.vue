<script >
  import SectionCharacters from './components/SectionCharacters.vue';
  import AppHeader from './components/AppHeader.vue';
  export default{
    components:{
      SectionCharacters,
      AppHeader,
    }
  }
</script>

<template>
  <AppHeader/>
  <SectionCharacters/>
</template>

<style lang="scss">
  @import './style/global.scss';
  body{
    background-color: #2e3a46;
  }
</style>
